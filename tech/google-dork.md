Unlock the full potential of Google search with our ultimate Google Dork Cheat Sheet! From mastering basic search filters to exploring special content and unreliable filters, our guide simplifies complex searches into actionable insights. Perfect for cybersecurity professionals, researchers, and anyone inquisitive about digging deeper into the web. Elevate your search game and discover a treasure trove of information hidden in plain sight.

## Filters

 ### Basic Search filters
 | Search filter | What it does | Example |
|-----------------|--------------|---------|
| `site:` | Search for results from a particular website. | [site:apple.com](https://www.google.com/search?q=site%3Aapple.com) |
| `related:` | Search for sites related to a given domain. | [related:apple.com](https://www.google.com/search?q=related%3Aapple.com) |
| `intitle:` | Search for pages with a particular word in the title tag. | [intitle:apple](https://www.google.com/search?q=intitle%3Aapple) |
| `allintitle:` | Search for pages with multiple words in the title tag. | [allintitle:apple iphone](https://www.google.com/search?q=allintitle%3Aapple+iphone) |
| `inurl:` | Search for pages with a particular word in the URL. | [inurl:apple](https://www.google.com/search?q=inurl%3Aapple) |
| `allinurl:` | Search for pages with multiple words in the URL. | [allinurl:apple iphone](https://www.google.com/search?q=allinurl%3Aapple+iphone) |
| `intext:` | Search for pages with a particular word in their content. | [intext:apple iphone](https://www.google.com/search?q=intext%3Aapple) |
| `allintext:` | Search for pages with multiple words in their content. | [allintext:apple iphone](https://www.google.com/search?q=allintext%3Aapple+iphone) |
| `source:` | Search for results from a particular source in Google News. | [apple source:the_verge](https://www.google.com/search?q=apple+source%3Athe_verge&tbm=nws) |
| `before:` | Search for results from before a particular date.
 
 
 
 


### Special Content Filters
 | Search filter | What it does | Example |
|-----------------|--------------|---------|
| `filetype:` | Search for particular types of files (e.g., PDF). | [apple filetype:pdf](https://www.google.com/search?q=apple+filetype%3Apdf) |
| `ext: ` | Same as `filetype:` | [apple ext:pdf](https://www.google.com/search?q=apple+ext%3Apdf) |
| `weather:` | Search for the weather in a location. | [weather:san francisco](https://www.google.com/search?q=weather%3Asan+francisco) |
| `stocks:` | Search for stock information for a ticker. | [stocks:aapl](https://www.google.com/search?q=stocks%3Aaapl) |
| `map:` | Force Google to show map results. | [map:silicon valley](https://www.google.com/search?q=map%3Asilicon+valley) |
| `movie:` | Search for information about a movie. | [movie:steve jobs](https://www.google.com/search?q=movie%3Asteve+jobs) |
| `in` | Convert one unit to another. | [$329 in GBP](https://www.google.com/search?q=$329+in+GBP) |

### Unreliable Filters
| Search filter | What it does | Example |
|-----------------|--------------|---------|
| `#..#` | Search within a range of numbers. | [iphone case $50..$60](https://www.google.com/search?q=iphone+case+%2450..%2460) |
| `inanchor:` | Search for pages with backlinks containing specific anchor text. | [inanchor:apple](https://www.google.com/search?q=inanchor%3Aapple) |
| `allinanchor:` | Search for pages with backlinks containing multiple words in their anchor text. | [allinanchor:apple iphone](https://www.google.com/search?q=allinanchor%3Aapple+iphone) |
| `AROUND(X)` | Search for pages with two words or phrases within X words of one another. | [apple AROUND(4) iphone](https://www.google.com/search?q=apple+AROUND(4)+iphone) |
| `loc:` | Find results from a given area. | loc:”san francisco” apple |
| `location:` | Find news from a certain location in Google News. | [location:”san francisco” apple](https://www.google.com/search?q=loc:%22san+francisco%22+apple) |
| `daterange:` | Search for results from a particular date range. | [daterange:11278-13278](https://www.google.com/search?q=steve+jobs+daterange%3A11278-13278) |




## Operators

### Search Term

This operator searches for the exact phrase within speech marks only.  This is ideal when the phrase you are using to search is ambiguous and  could be easily confused with something else, or when you’re not quite  getting relevant enough results back. For example:

```
"Tinned Sandwiches"
```

### OR
This self explanatory operator searches for a given search term OR an equivalent term.

```
site:facebook.com | site:twitter.com
```

### AND

```
site:facebook.com & site:twitter.com
```

#### Operators combinaison

```
(site:facebook.com | site:twitter.com) & intext:"login"
(site:facebook.com | site:twitter.com) (intext:"login")
```

### Include results

This will order results by the number of occurrence of the keyword.

```
-site:facebook.com +site:facebook.*
```

### Exclude results

```
site:facebook.* -site:facebook.com
```

### Synonyms

Adding a tilde to a search word tells Google that you want it to bring back synonyms for the term as well. For example, entering “~set” will bring back results that include words like “configure”, “collection” and “change” which are all synonyms of “set”. Fun fact: “set” has the most definitions of any word in the dictionary.

```
~set
```

### Glob pattern (*)

Putting an asterisk in a search tells Google ‘I don’t know what goes  here’. Basically, it’s really good for finding half remembered song  lyrics or names of things.

```
site:*.com
```

## Useful Tips
### Tips for Google Dorking

1. **Use Quotes for Exact Matches**: When searching for an exact phrase or specific sequence of words, enclose the phrase in quotation marks. This tells Google to search for the exact phrase within the quotes, which can help filter out irrelevant results. `"exact phrase here"`
2. **Combine Operators for Powerful Searches**: You can combine various operators to create more specific and powerful search queries. For example, using `site:` with `-inurl:` can help you find pages on a specific website while excluding certain URLs. `site:example.com -inurl:login`
3. **Wildcard Searches with** *: The asterisk acts as a wildcard symbol that can replace any word or phrase. This is particularly useful when you're trying to find something but don't remember the exact phrasing. `"president * speech"`
4. **Search Within a Specific Date Range**: Use the `before:` and `after:` operators to narrow down search results to a specific timeframe. This is especially useful for finding content published within certain dates. `related:example.com`
5. By incorporating these tips into your searches, you can leverage Google's capabilities to find exactly what you're looking for more efficiently.


### Useful Links
* [Google Search Operators: The Complete List](https://ahrefs.com/blog/google-advanced-search-operators/)
* [GoogleDorking](https://gist.github.com/sundowndev/283efaddbcf896ab405488330d1bbc06)
* [Refine Google searches](https://support.google.com/websearch/answer/2466433?hl=en)
