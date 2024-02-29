Unlock the full potential of PICO-8 game development with this comprehensive cheat sheet, your essential guide to mastering the intricacies of this unique fantasy console. From sprite creation to code optimization, this cheat sheet puts a wealth of tips, tricks, and shortcuts at your fingertips, simplifying your creative process. Whether you're a seasoned developer or a hobbyist, this resource is your stepping stone to crafting engaging 8-bit classics.

## Basics
### Specifications

- **Display**: 128x128, 16 colors
- **Input**: 6-Button controllers
- **Carts**: 32K data enc. PNG files
- **Sound**: 4-channel, 64 chip blerps
- **Code**: [Lua](/tech/lua) subset (Max 8192 code tokens)
- **CPU**: 8MHz, 4M Lua vm insts/sec
- **Sprite**: 1 bank of 128 8x8 SPR's (+ 128 shared)
- **Map**: 128x32 Tilemap (+ 128x32 shared)

⬇️[Downloadable PICO-8 Cheat Sheet (pdf format)](/www/assets/img/pico-8/pico-8-cheat-sheet-downloadable-pdf-format.pdf)

### Controls

| Button | P1          | P2             | Pause    |
|--------|-------------|----------------|----------|
| 0      | Left Arrow  | S              |          |
| 1      | Right Arrow | F              |          |
| 2      | Up Arrow    | E              |          |
| 3      | Down Arrow  | D              |          |
| 4      | Z           | LShift / A     |          |
| 5      | X           | C / V / N / M  | P / Enter|

- **API**: `BTN(i)`, `BTN(p)`
- **Player**: `BTN(i,p)`

### Command Line

- **HELP**
- **SAVE** `<FILENAME>.P8` / `.PNG`
- **LOAD** `<FILENAME>.P8`
- **RUN** `[PARAM]`
- **IMPORT** `S.PNG`
- **EXPORT** `X.BIN` / `X.HTML`
- **SPLORE**
- **FOLDER**
- **MKDIR** `<DIR_NAME>`
- **LS** `[DIR]`
- **CD**
- **CLS** 
- **INFO**
- **SHUTDOWN**
- **REBOOT**
- **SAVE/LOAD** `("@CLIP")`
- **SAVE** `("@URL")` -- P8 EDU URL
- **EXTCMD** `(CMD_STR,[P1],[P2])`

## Coding
### Functions
`FUNCTION SUM(A,B)`  -- DECLARE

  `RETURN A+B`      -- RETURN VALUE

`END`


### Program Structure

- `INIT()` -- 1X ON STARTUP
- `UPDATE()` -- UPDATE @ 30FPS
- `UPDATE60()` -- UPDATE @ 60FPS
- `_DRAW()` -- 1X/VISIBLE FRAME

- `#INCLUDE <FILE_NAME>.LUA`
- `#INCLUDE ONETAB.P8:1`
- `#INCLUDE ALLTABS.P8`


### COMMENTS & TYPES

-- THIS IS A COMMENT

--[[ THIS IS A MULTI-
LINE COMMENT ]]

`O=NIL N=23` -- GLOBAL SCOPE

`LOCAL S="TEXT"` -- LOCAL SCOPE


### TABLES

* `T={1,2,3,4}`     
* `T={A="X", B=1}`
* `ADD(T,VAL,[I])`    
* `DEL(T,VAL)`
* `DEL(T,[I])`
* `PRINT(T[1])` -- 1-BASED
* `#T/COUNT(T,VAL)`
* `ALL(T)`
* `PAIRS(T)`
* `T=PACK(...)`
* `A,B,C=UNPACK(T,[I],[J])`
* `FOREACH(T,F)`
* `IPAIRS(T)`

### FLOW CONTROL1
#### Goto
`::LABEL::` -- LABEL

`GOTO LABEL` -- JUMP

#### If Then Else
`IF (TRUE) CLS()` -- INLINE IF

`IF <CONDITION> THEN`

  -- IF BLOCK
	
`ELSEIF <CONDITION> THEN`

  -- ELSEIF BLOCK
	
`ELSE`

  -- ELSE BLOCK
	
`END`

#### While
`WHILE <CONDITION> DO`

  -- WHILE BLOCK
	
`BREAK` -- EXIT LOOP EARLY

`END`


### FLOW CONTROL2
#### Repeat
`REPEAT`

  -- REPEAT BLOCK
	
`UNTIL <CONDITION>`

#### For
`FOR I=1,10 DO`

  -- COUNT UP
	
  -- (DOWN:FOR I=10,0,-1 DO)
	
`END`

`FOR V IN ALL(T) DO`

  -- TABLE/ARRAY
	
`END`

`FOR K,V IN PAIRS(T) DO`

  -- TABLE: T[K]=V
	
`END`

### OPERATORS
```
+ - * / ^ %
+= -= *= /= ^= %=
< > <= >= == ~=
#LIST "A" .. "B"
AND OR NOT
```

### COLOR PALETTES
![PICO-8 Color Palette](/www/assets/img/pico-8/pico-8-color-palettes-min.png)

- `PAL(C0, C1, [P])` --P: 0=DRAW
- `PAL(TABLE, [P])` --P: 1=DISP
--P: 2=2ND PAL
- `PALT(COL, T)` -- TRANS(BOOL)

### SCREEN
![PICO-8 Screen Size](/www/assets/img/pico-8/pico-8-screen-min.png)

- `CAMERA(X, Y)`
- `CLS([COL])`
- `COLOR([COL])`
- `PGET(X, Y)`
- `PSET(X, Y, [COL])`
- `FLIP()`
- `CLIP([X, Y, W, H, CLIP_PREV])`

### SHAPES

- `CIRC(X, Y, R, [COL])`
- `CIRCFILL(X, Y, R, [COL])`
- `LINE(X0, Y0, X1, Y1, [COL])`
- `OVAL(X0, Y0, X1, Y1, [COL])`
- `OVALFILL(X0, Y0, X1, Y1, [COL])`
- `RECT(X0, Y0, X1, Y1, [COL])`
- `RECTFILL(X0, Y0, X1, Y1, [COL])`
- `FILLP([MASK])`

![PICO-8 Shapes](/www/assets/img/pico-8/pico-8-shapes-min.png)

### SPRITES

- `SPR(N, X, Y, [W, H, FLIP_X, FLIP_Y])`
- `SSPR(SX, SY, SW, SH, DX, DY, [DW, DH, FLIP_X, FLIP_Y])`
- `SGET(X, Y)`
- `SSET(X, Y, [COL])`
- `FGET(N, [F])`
- `FSET(N, [F], V)`

### MAP

- `MAP(TILE_X, TILE_Y, [SX, SY], [TILE_W, TILE_H], [LAYERS])`
- `MGET(X, Y)`
- `MSET(X, Y, VAL)`
- `TLINE(X0, Y0, X1, Y1, MX, MY, MDX, [MDY], [LAYERS])`



### AUDIO + Tracker
#### Audio
- `SFX(N, [CH], [OFFSET], [LEN])`
- `MUSIC([N, [FADE, [MASK]]])`

#### TRACKER
![PICO-8 Tracker](/www/assets/img/pico-8/pico-8-tracker-min.png)

```
--INSTRUMENT      --EFFECT
0 Triangle        0 None
1 Tilt.Saw        1 Slide
2 Saw             2 Vibrato
3 Square          3 Drop
4 Pulse           4 Fade In
5 Organ           5 Fade Out
6 Noise           6 Arp Fast
7 Phaser          7 Arp Slow
```

### Math

- Numeric range: `-32768.0` to `32767.99`
- `MAX(X, Y)`
- `MIN(X, Y)`
- `MID(X, Y, Z)`
- `FLR(X)`
- `CEIL(X)`
- `COS(X)`
- `SIN(X)`
- `ATAN2(DX, DY)`
- `SQRT(X)`
- `ABS(X)`
- `RND(X)` -- 0 <= N < X
- `SRAND(X)` -- SET RND SEED
- `SGN(X)` -- -1 OR 1
#### FUNC - OPERATOR
- `BAND(X, Y)` -- `&`
- `BOR(X, Y)` -- `|`
- `BXOR(X, Y)` -- `^^`
- `BNOT(X)` -- `~`
- `SHL(X, N)` -- `<<`
- `SHR(X, N)` -- `>>`
- `LSHR(X, N)` -- `>>>`
- `ROTL(X, N)` -- `<<`
- `ROTR(X, N)` -- `>>`

### Strings

```plaintext
S="HELLO"
S=[[HELLO
MULTILINE]]
```

- `PRINT(S, [X, Y, COL])`
- `?S, [X, Y, COL]` -- SHORTHAND
- `#S` -- LENGTH
- `"STR="..S` -- CONCAT

```plaintext
CHR(VAL0, VAL1, ...)
ORD(STR, [POS], [LEN])
SPLIT(STR, [SEP], [TO_NUM])
SUB(STR, POS0, [POS1])
TOSTR(VAL, [FLAGS])
TONUM(VAL, [FLAGS])
TYPE(VAL)
```

### Glyphs 1
![PICO-8 Glyphs 1](/www/assets/img/pico-8/pico-8-glyphs1-min.png)

### Glyphs 2
![PICO-8 Glyphs 2](/www/assets/img/pico-8/pico-8-glyphs2-min.png)


## SYSTEM
### COROUTINES
- `C=COCREATE(FUNC)`
- `CORESUME(C, [...])`
- `COSTATUS(C)`
- `YIELD()`


### CARTRIDGE DATA

- `-- GAME SAVES`
- `CARTDATA("ID")`
- `DGET(I)` -- 0..63
- `DSET(I, VAL)`

### SYSTEM FLAGS

- `POKE(0x5F2D,FLAGS)`
  - `-- DEVKIT MODE FLAGS:`
    - `0x1 Enable`
    - `0x2 Mouse buttons>btn()`
    - `0x4 Pointer Lock`
- `POKE(0x5F5C, D)` -- BTNP 1X DELAY
- `POKE(0x5F5D, D)` -- REPEAT DELAY
- `POKE(0x5F34,1)` -- INT.FILLP
- `POKE(0x5F36, 0x8)` -- DRAW SPR 0


### RAM MEMORY LAYOUT
- `0x0` GFX
- `0x1000` GFX2/Map2 (Shared)
- `0x2000` Map
- `0x3000` GFX Flags
- `0x3100` Song
- `0x3200` SFX
- `0x4300` User Data
- `0x5600` Custom Font (If def.)
- `0x5E00` Persistent Cart Data
- `0x5F00` Draw State
- `0x5F40` Hardware State
- `0x5F80` GPIO Pins (128 Bytes)
- `0x6000` Screen Data (8K)
- `0x8000` User Data

### MEMORY FUNCTIONS
- `CSTORE(DEST, SRC, LEN, [FILENAME])`
- `MEMCPY(DEST_ADDR, SRC_ADDR, LEN)`
- `MEMSET(DEST_ADDR, VAL, LEN)`
- `RELOAD(DEST, SRC, LEN, [FILENAME])`
- `POKE(ADDR, VAL1 [, VAL2, ...])`
- `PEEK(ADDR, [N])` -- @ADDR
- `PEEK2(ADDR)` -- %ADDR
- `POKE2(ADDR, VAL)`
- `PEEK4(ADDR)` -- $ADDR
- `POKE4(ADDR, VAL)`
- `SERIAL(CH, ADDR, LEN)`


### SYSTEM & DEBUG
- `TIME()/T()`
- `ASSERT(CONDITION, [MESSAGE])`
- `PRINTH(STR, [FILE], [O/W], [DESK])`
- `STOP([MESSAGE])`
- `RESUME()` -- `"."=Frame-by-Frame`
- `TRACE([C], [MESSAGE], [SKIP])`
- `STAT(X)` -- Status of X:

|  |  |
| -------- | -------- | 
 | `0` Mem Usage |  `1` CPU Used |
 | `4` Clipboard | `6` Param str |
 | `7` Curr fps |  `30` Keypressed |
 | `31` Key char | `32, 33` Mouse X,Y |
 | `34` Mouse btns | `36` Mouse Wheel |
 | `38, 39` Rel.X,Y move (Req. 0x4) | `46..49` Curr SFX (CH 0..3) |
 | `50..53` Curr Note (CH 0..3) | `54` Patt.Idx |
 | `55` Patt.Played | `56` Patt.Ticks |
 | `57` Music Playing | `80..85` UTC Time (Y,M,D,H,M,S) |
 | `90..95` Local Time | `100` Breadcrumb Label |
 | `110` Frame-by-Frame Mode | |


## SHORTCUTS
### COMMON
- `ALT+ENTER`: Fullscreen
- `CTRL+R`: Reload/Run
- `CTRL+S`: Quick-Save
- `CTRL+M`: Mute/Unmute
- `ENTER/P`: Pause Menu
- `ESC`: Console/Editor
- `CTRL+6`: Save Screenshot
- `CTRL+7`: Save Label Image
- `CTRL+8`: Start GIF/Video
- `CTRL+9`: Save GIF/Video
- `CTRL+P`: Toggle CPU Meter

### CODE EDITOR
- `CTRL+X,C,V`: Cut, Copy, Paste
- `CTRL+Z,Y`: Undo, Redo
- `CTRL+F`: Search
- `CTRL+G`: Next Result
- `CTRL+H`: Next Res(all tabs)
- `CTRL+L`: Jump to Line No.
- `CTRL+A,V`: Jump Start, End
- `ALT+A,V`: Prev, Next Func()
- `CTRL+<,>`: Jump Word
- `CTRL+W,E`: Start, End Line
- `CTRL+D`: Duplicate Line
- `TAB`: Indent Selection
- `SHIFT+TAB`: Un-indent Sel.
- `CTRL+B`: Un/Comment Block
- `CTRL+U`: HELP for keyword
- `SHIFT+▲,▼,◄,►,O,X`

### SPRITE/MAP EDITOR
- `SPACE`: Pan view
- `TAB`: Fullscreen
- `Mousewheel`: Zoom
- `SHIFT+,/.`: Zoom In/Out
- `F,V`: Flip Y,X
- `R`: Rotate
- `▲,▼,◄,►`: Move
- `S`: Select

### DRAW TOOL
- `CTRL+LMB`: Replace Col
- `RMB`: Grab Col
- `CTRL+G`: Toggle Gridlines

### SFX/MUSIC EDITOR
- `SPACE`: Play/Pause
- `SHIFT+LMB`: Set all notes
- `◄,►`: Modify speed
- `+, -`: Prev/Next Pattern
- `a`: Release Loop

## Useful Tips + Links
### Top 5 PICO-8 Coding Tips

1. **Keep It Simple**: Start with a small project to get familiar with the PICO-8 environment and Lua syntax.
2. **Optimize Your Tokens**: Use short variable names and consider token-saving techniques like using bitwise operations for simple math.
3. **Use Tables Wisely**: Tables are powerful. Use them for everything from data storage to object management.
4. **Take Advantage of PICO-8 APIs**: PICO-8 offers a variety of built-in functions. Learn them well to save time and tokens.
5. **Iterate and Test**: Make small changes and test often to avoid introducing hard-to-track bugs.

### Top 5 PICO-8 Game Design Tips

1. **Design Around Limitations**: The constraints of PICO-8 are part of its charm. Embrace them in your game design.
2. **Focus on Gameplay**: Graphics and sound are limited, so prioritize solid gameplay mechanics.
3. **Prototype Quickly**: Get a playable version up as soon as possible and iterate on your design.
4. **Engage the Community**: Share your game with the PICO-8 community for feedback and suggestions.
5. **Polish**: Small details can make a big difference. Polish your game with screen shake, particle effects, and juicy feedback.

### Top 5 PICO-8 Links
1. [PICO-8 Official Website](https://www.lexaloffle.com/pico-8.php)
2. [PICO-8 Zine](https://sectordub.itch.io/pico-8-fanzine-1) - A community-created magazine full of tips and tricks.
3. [PICO-8 BBS](https://www.lexaloffle.com/bbs/) - The official forums for sharing games, tools, and discussions.
4. [PICO-8 Wiki](https://pico-8.fandom.com/wiki/Pico-8_Wikia) - A comprehensive resource for all things PICO-8.
5. [Awesome PICO-8](https://github.com/pico-8/awesome-PICO-8) - A curated list of awesome PICO-8 resources, carts, and tools.
