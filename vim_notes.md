## vim key bindings 

### Basic stuff 

    1. :wq --> Save and Quit 
    2. :q --> quit vim (q! override quit if quit doesn't work or if its only a read file)
    3. a --> append mode 
    4. I --> insert begging of a line  
    5. A --> insert end of a line 

### Moving around vim 

1. hjkl 

        h --> Left  
        j --> Down  
        k --> Up  
        l --> Right  

2. Standard movement 

        1> w --> move from word to word  
        2> b --> jump to previous word
        3> W --> passes through every string literal
        4> W --> passes through every word
        5> 0 --> Move to first part of the line 
        6> $ --> Move to last part of the line 
    
    Advanced movement 

        1> Move 15 lines above --> 15 and up arrow 
        2> Move 15 lines below --> 15 and down arrow
        3> gg -- move to first line of the file 
        4> G -- move to the end of the file  

3. Replacing 

        r --> replace 
        R --> Replace entire word 

4. Changing a word  

        1> cw
        --> change word
            doing this say in between a word would replace everything after that letter   
            \-- 3w --> move 3 words 
            \-- c7w --> change 7 words
        2> ciw --> Change inner word
        3> diw --> Delete inner word

5. Deletion 

        1> C - Delete the rest of Line
        \-- D- Delete the rest of Line
        2> dw - Delete the word only
        3> d4w - Delete Fours words  
        4> dd - Delete that entire line 
        5> cc - Change an entire line
     
6. Undo something 

        1> u - Undo 

7. Redo something 
    
        ctrl+R - Redo 

8. Change inner 

        1> ci -- change inside something 
        \ -- () -- change something inside a function 
        \ -- ciw -- change the word itself     

        2> % -- helps us traverse through a bracket 
        \ -- c% -- Change until a bracket  (removes a bracket)

9. Goto line number 

        1> Go to line number - :linenumber eg :19
        2> Go to begging of a line 0 
        3> Go to end of a line $
    
10. Entering Visual mode (copy and pasting)

        v - Enter visual mode
        d - delete something 
        c - change the text 
        y - yanking (copy)
        yy - yank an entire line  
        y5w - copy 5 words 
        p - paste before 
        P - paste after

        1> Enter visual line -- Shift + v
        2> Enter Visual block -- ctrl + v

11. copy inside bracket 

        1> yi) - Yank stuff inside a bracket 
        2> yiw - Yank inner word

12 . Centre screen 

    1. zz - centre screen

13. Indentation 
    
        1. ' > ' - shift to right (use >> for doing it in one shot)

        2. ' < ' - shift to left  (use << for doing it in one shot) 

        3. = - indent (== indent a line)

        4. full indentation --> gg=G

Command line mode in vim 

    1> / -- search something in vim 
    2> n -- go to next word 
    3> N -- go to previous word 
    4> :s/old/new/g - replace stuff in that one line only 
    5> :%s/old/new/g - Replace everything 

commenting code 

1> Enter visual mode 

    Give V to entire visual line mode 

    Then give : you would get something like this 
    
    :'<,'>
    
    Then add this s/^/#/ 

2> Entering multi-line mode 

    1. enter visual block mode 
    2. to insert give shift + I to insert 
    3. add stuff 
    4. quit

### Macros 

A macro is a way to repeat something  

How to record a macro in vim ? 

    1. to being recording press q followed by the register to want to store the macro say 'a' 

    2. do your stuff 

    3. every key gets stored in the register 

    4. To excute the macro do @a 
