

[Vimdoc](http://vimdoc.sourceforge.net/htmldoc/options.html)


[Vim Help](https://www.cs.swarthmore.edu/oldhelp/vim/home.html)


## Normal Mode

![vim shortcut](/img.png) 

Command      | Description 
------------ | ------------- 
.            | repeat 
A            | $a 
cw           | diw + i 
cc           | dd + i
o            | A<CR>
O            | ko
I            | ^i  
\>            | tab
zz           | scroll to the center
gj           | down one display line
gk           | up one display line
  

## Insert Mode 

Command      | Description 
------------ | ------------- 
\<Ctrl-h>     | backspace 
\<Ctrl-w>     | delete a word
\<Ctrl-u>     | delete to the start of the line
\<Ctrl-r>a    | insert reg a
  
## Replace mode
  

## Visual Mode

  Command      | Description 
------------ | ------------- 
v           | character 
V           | line
\<Ctrl-v>    | block 
gv          | re-select 
  
* <Ctrl-v> + A; + <Esc>
* <Ctrl-v> + r + |

## Command Mode
  
Command      | Description 
------------ | ------------- 
:[range]delete [x]           | copy the range to reg x and delete them
:[range]yank [x]           | copy the range to reg x
:[range]put [x]           | paste reg x
:[range]copy {address}    | copy the range and paste to the address
:[range]join              | merge the range 
:[range]normal command | execute the command 
:[range]s/pattern/string/flag | substitute 
:[range]global/pattern/command | execute the command in the lines pattern matched
  
 
# Copy and Paste (Register)

Command      | Description 
------------ | ------------- 
yy           | copy a line 
"ayy         | copy a line to register a
"add         | delete a line and copy the line to register a
"ap          | paste the line from register a
yiw          | copy a word
diw          | delete a word
ciw          | delete a word and change to edit mode
<Ctrl-r>ap   | paste the line from register a in edit mode
  
  
Register      | Description 
------------ | ------------- 
"%           | current filename 
"#           | previously used filename


copy a line 


n   | repeat forward search
N   |  repeat backward
\*   |  search for word currently under cursor



# * Searching     

    
## Pattern

Command      | Description 
------------ | ------------- 
/pattern     | search forward for pattern
?pattern   | search backward
n   | repeat forward search
N   |  repeat backward
\*   |  search for word currently under cursor

## Case sensitivity

Command      | Description 
------------ | ------------- 
:set ignorecase  | ignore case in search patterns
:set smartcase   | case sensitive if any caps used (ex. Foo)
:set hlsearch   |  highlighting of search matches


## Very magic search

Command      | Description 
------------ | ------------- 
/**pattern** | pattern matching
/\v**pattern** | very magic search - every following character except a-zA-Z0-9 and '\_' have special meaning 
/\V**pattern** | very nomagic search - every following character have no special meaning

Command      | Example  
------------ | ------------- 
/#\x\\{3\\}\\.\x\\{2\\} |  ```#ABC.DE``` 
/\v#\x{3}\\.\x{2} |  ```#ABC.DE``` 
/\V#\x\\{3\\}.\x\\{2\\} |  ```#ABC.DE``` 
/\v"[^"]+" | ```  "quoted words" ```
/\v"\zs[^"]+\ze" | "```quoted words```"
/\v<(\w+)\s+\1> | ```dup dup``` - duplicated words
:%s/\v(%(And\|D)rew) (Neil)/\2 \1/g | Andrew Neil -> Neil Andrew    
:%s/\v([0-9]+)/\=submatch(0)+1/gc | 123 -> 124




