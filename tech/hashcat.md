The Hashcat Cheatsheet offers an extensive guide to using Hashcat for password cracking, covering miscellaneous tricks, automating commands with Wrapcat, various attack modes, character sets, and command options. It includes practical examples to benchmark, create sessions, and crack different hash types using specific strategies, alongside a scenario for cracking large files like NTDS.dit, detailing initial setup, dictionary attacks, and advanced strategies. A valuable resource for both beginners and experienced users seeking to optimize their password cracking workflows with Hashcat.

## The Basics

### MISC and tricks
- [One Rule to Rule Them All](#https://www.notsosecure.com/one-rule-to-rule-them-all/)
- MAX POWER: Force the CUDA GPU interface, optimize for <32 char passwords and set the workload to insane (-w 4). It is supposed to make the computer unusable during the cracking process. Finally, use both the GPU and CPU to handle the cracking.
  ```
  --force -O -w 4 --opencl-device-types 1,2
  ```

### Wrapcat - Automating hashcat commands
- Links to resources:
- [https://twitter.com/Haax9_/status/1340354639464722434?s=20](https://twitter.com/Haax9_/status/1340354639464722434?s=20)
- [https://github.com/Haax9/Wrapcat](https://github.com/Haax9/Wrapcat)
  ```
- Command:
  ```
  $ python wrapcat.py -m 1000 -f HASH_FILE.txt -p POT_FILE.txt --full --save
  ```

### Attack modes
- Straight : hash dict
  ```
  -a 0
  ```
- Combination : hash dict dict
  ```
  -a 1
  ```
- Bruteforce : hash mask
  ```
  -a 3
  ```
- Hybrid wordlist + mask : hash dict mask
  ```
  -a 6
  ```
- Hybrid mask + wordlist : hash mask dict
  ```
  -a 7
  ```

### Charsets
- Lowercase a-z
  ```
  ?l
  ```
- Uppercase A-Z
  ```
  ?u
  ```
- Decimals
  ```
  ?d
  ```
- Hex using lowercase chars
  ```
  ?h
  ```
- Hex using uppercase chars
  ```
  ?H
  ```
- Special chars
  ```
  ?s
  ```
- All (l,u,d,s)
  ```
  ?a
  ```
- Binary
  ```
  ?b
  ```

### Options
  ```
  -m # Hash type
  -a # Attack mode
  -r # Rules file
  -V # Version
  --status # Keep screen updated
  -b # Benchmark
  --runtime # Abort after X seconds
  --session [text] # Set session name
  --restore # Restore/Resume session
  -o filename # Output to filename
  --username # Ignore username field in a hash
  --potfile-disable # Ignore potfile and do not write
  --potfile-path # Set a potfile path
  -d # Specify an OpenCL Device
  -D # Specify an OpenCL Device Type
  -l # List OpenCL Devices & Types
  -O # Optimized Kernel, Passwords <32 chars
  -i # Increment (bruteforce)
  --increment-min # Start increment at X chars
  --increment-max # Stop increment at X chars
  ```

## Examples + Cracking Large Files
### Examples
- Benchmark MD4 hashes
  ```
  hashcat -b -m 900
  ```

- Create a hashcat session to hash Kerberos 5 tickets using wordlist
  ```
  hashcat -m 13100 -a 0 --session crackin1 hashes.txt wordlist.txt -o output.pot
  ```

- Crack MD5 hashes using all char in 7 char passwords
  ```
  hashcat -m 0 -a 3 -i hashes.txt ?a?a?a?a?a?a?a -o output.pot
  ```

- Crack SHA1 by using wordlist with 2 char at the end
  ```
  hashcat -m 100 -a 6 hashes.txt wordlist.txt ?a?a -o output.pot
  ```

- Crack WinZip hash using mask (Summer2018!)
  ```
  hashcat -m 13600 -a 3 hashes.txt ?u?l?l?l?l?l?l?d?d?d?d! -o output.pot
  ```

- Crack MD5 hashes using dictionary and rules
  ```
  hashcat -a 0 -m 0 example0.hash example.dict -r rules/best64.rules
  ```

- Crack MD5 using combinator function with 2 dictionaries
  ```
  hashcat -a 1 -m 0 example0.hash example.dict example.dict
  ```

- Cracking NTLM hashes
  ```
  hashcat64 -m 1000 -a 0 -w 4 --force --opencl-device-types 1,2 -O d:\hashsample.hash "d:\WORDLISTS\realuniq.lst" -r OneRuleToRuleThemAll.rule
  ```

- Cracking hashes from kerberoasting
  ```
  hashcat64 -m 13100 -a 0 -w 4 --force --opencl-device-types 1,2 -O d:\krb5tgs.hash d:\WORDLISTS\realhuman_phill.txt -r OneRuleToRuleThemAll.rule
  ```

- You can use hashcat to perform combined attacks, for example by using wordlist + mask + rules
  ```
  hashcat -a 6 -m 0 prenoms.txt ?d?d?d?d -r rules/yourule.rule
  ```

- Single rule used to uppercase first letter --> Marie2018
  ```
  hashcat -a 6 -m 0 prenoms.txt ?d?d?d?d -j 'c'
  ```


### Scenario - Cracking large files (eg NTDS.dit)
- Start by making a specific potfile and cracked files (clean environment) - domain_ntds.dit - domain_ntds_potfile.pot
- Goal is to run many different instances with different settings, so each one has to be quite quick.
- You can generate a wordlist using CeWL. It usually works pretty well.
  ```
  cewl -d 5 -m 4 -w OUTFILE -v URL
  cewl -d 5 -m 4 -w OUTFILE -o -v URL
  ```

- With some basic dictionary cracking (use known wordlists) like rockyou, hibp, crackstation, richelieu, kaonashi, french and english.
  ```
  .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot -a 0 rockyou.txt --force -O
  ```

- Then start to use wordlists + masks + simple rule. For special chars, you can use a custom charset: "?!%$&amp;#-_@+=* ".
  Multiple tests, multiple masks, and multiple wordlists (including generated ones).
  ```
  .\hashcat64.exe -m 1000 hashs.txt -a 6 .\french\* '?d?d?d?d' -j c --increment --force -O
  .\hashcat64.exe -m 1000 hashs.txt -a 6 .\french\* -1 .\charsets\custom.chr '?1' -j c --force -O
  ```

- Then, wordlists + complex rules. Once again, run against multiple wordlists (including generated ones). Kaonashi and OneRuleToRuleThemAll can produce massive cracking time.
  ```
  .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot -a 0 french.txt -r .rules\best64.rule --force -O
  .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot -a 0 french.txt -r .rules\OneRuleToRuleThemAll.rule --force -O
  ```

- Then smart bruteforce using masks (custom charset can be useful too). Can be quite long, depending on the mask. Many little tests with different masks.
  Knowing for example that password is min 8 char long, only 8+ masks. Play by incrementing or decrementing char vs decimal (you can also use a specific charset to reduce time).
  ```
  .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot -a 3 '?u?l?l?l?d?d?d?d' --force -O
  ```

- Then increment mask size and play again. Can be longer for 9 char and above. Up to you to decide which masks and how long you want to wait.

- If you have few hashes and a small/medium wordlist, you can use random rules and make several loops.
  ```
  .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot -a 0 wl.txt -g 1000000 --force -O -w 3
  ```

- You can use combination attacks. For example, combine different names, or combine names with dates. Then apply masks directly using hashcat or in memory feeding, it allows you to use rules but not masks.
  ```
  .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot -a 1 wordlist1.txt wordlist2.txt --force -O
  .\combinator.exe wordlist1.txt wordlist2.txt | .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot -a 0 -rules .\rules\best64.rule --force -O
  ```

- Finally, use your already cracked passwords to build a new wordlist. Then try reuse or apply rules on them.
  ```
  .\hashcat64.exe -m 1000 hashs.txt --potfile-path potfile.pot --show | %{$_}.split(':')[1]} > cracked.txt
  .\hashcat64.exe -m 1000 hashs.txt -a 6 cracked.txt '?d?d?d?d' -j c --increment --force -O
  ```

This section provides a comprehensive guide for tackling large file cracking scenarios, outlining a progression from initial setup and basic dictionary attacks through to advanced strategies incorporating  custom charsets, complex rules, and smart bruteforce techniques.
