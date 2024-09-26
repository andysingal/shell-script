```
# shell-script

#!/bin/bash
# Author: Ankush Singal
# Date Created: 31/12/2020
# Last Modified: 31/13/2020

# Description:
# Create a backup in ~/bash_course folder of all files in the home directory

# Usage:
#backup_script
```echo "Hello, ${USER^}"```
``` echo "I will now backup your hime directory, $HOME" ```
```currentdir=$(pwd)```
```echo "You are running this script from $currentdir"```
```echo "Therefore, I will save the backup in $currentdir"```
- ```tar -cf $currentdir/my_backup_"$(date +%d-%m-%Y_%H-%M-%S)".tar $HOME/* 2>/dev/null```
```echo "Backup Completed Successfully"```
- exit 0
```

-- Permission Calculator


## Adding scripts to PATH

-- echo "$PATH"


## Add the path as below
--- vi ~/.profile

```export PATH="$PATH:$HOME/bash_course/scripts"```

-- The PATH variable tells the shell where to search for executable files
-- We can make our scripts accessible system-wide by putting them into a folder covered by our PATH

## Parameter Expansion

```numbers=0123456789```
```${parameters:offset:length}^C```
```echo ${numbers:0:7}```

--- ```time=$(date +%H:%m:%S)```

--- ```echo "Hello $USER, the time right now is $time"```

## Arithmetic Expression

x=4
y=2
```echo $(( 4 + 2 )) ```

```echo $(( $x + $y )) ```

## Tilde Expression 

``` echo ~ ```
```echo $PWD ```

## Brace Expression 

```echo month{1..12}```
month1 month2 month3 month4 month5 month6 month7 month


#BAsh processes command lines - Tokenisation, Command Identification, Shell expansions, Quote removal, redirections

```
if [[ 2 -gt 1]]; then 
  echo "hello world"
fi
```

A simple command is just a list of words separated by spaces and terminated by either a new line or one of the other control operators available in bash

## Word splitting
Word splitting can have  some very significant effects on how your command lines are interpreted
