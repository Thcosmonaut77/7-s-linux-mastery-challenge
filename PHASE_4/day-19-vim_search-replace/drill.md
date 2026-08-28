# Vim Navigation & Search/Replace Drill

In a 50-line config file, jump straight to line 10, search for a keyword, jump between all matches, 
then replace every occurrence of one word with another across the whole file.

## Steps/Commands
- Open terminal
    - launch Ubuntu terminal

- Create sample config file
    - vim sample.config
    - i(insert mode)
    - right click to paste content from AI prompt 
    - esc(normal mode)
    - ZZ (save and exit)

- Jump to line 10
    - vim sample.config
    - :10 + enter

- Search for keyword
    - /server + enter

- Jump between all matches
    - n(to jump to next occurences)

- Replace one word accross the file
    - :%s/server/instance/g



