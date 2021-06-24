# vim

```
:set ignorecase
:set smartcase
```
# * Searching

## Pattern

Command      | Description 
------------ | ------------- 
/pattern     | search forward for pattern
?pattern   | search backward
n   | repeat forward search
N   |  repeat backward
*   |  search for word currently under cursor



## Case sensitivity

Command      | Description 
------------ | ------------- 
:set ignorecase  | ignore case in search patterns
:set smartcase   | case sensitive if any caps used (ex. Foo)
:set hlsearch   |  highlighting of search matches


## Very magic search

Command      | Description 
------------ | ------------- 
/**pattern** | /\v\x\{6\}
/\v**pattern** | very magic search - every following character except a-zA-Z0-9 and '\_' have special meaning /\v\x{6}
/\V**pattern** | very nomagic search - every following character have no special meaning /Va.k.a



