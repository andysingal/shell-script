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


## Globbing: It is also known as filename expansion, is used to generate an alphabetically-sorted list of file names that match a certain pattern exactly. Any word on the command line that contains an unquoted *,? or [ will be interpreted as a pattern

```ls * ```
```ls file[ab].txt ```

```ls file[abc][abc][abc].txt```

```ls file[a-g].txt```

```rm ~/Downloads/*.jpg```

## Types of Quotes
1. Backslashes: \
2. Single Quotes: ``
3. Double Quotes " "



## EXAMPLES 

echo $name > "~/$out"
echo $name > "$HOME/$out"

## Advanced

echo "$(ls *.txt)"


## Requesting User input 

```
#!/bin/bash
echo "My name is $1"
echo "My home directory is $2"
echo "My favourite color is $3"
echo "The 10th argument is ${10}
```

- Command line arguments are information you give to your script from your command line. Each argument is separated by a spac
- Positional parameters are parameters set by the shell to store the value of each of these command line arguments

#!/bin/bash 

echo $(( {2:-0} $1 ${3:-0} $1 ${4:-0} $1 ${5:-0}  $1 ${6:-0} $1 ${7:-0} $1 ${8:-0} $1 ${9:-0} $1 ${10:-0}  ))

chmod 744 calculator.sh

./calculator.sh + 5 5 5 5 
${parameter:-word}

## Special Parameters

#!/bin/bash
echo "My name is $1"
echo "My home directory is $2"
echo "My favourite color is $3"
echo "The 10th argument is ${10}
echo $#

$@: $1 $2 $3 ... $N..... Where N is the number of command line arguments provided

$*: $1 $2 $3... $N.. Where N is the number of command line arguments provided... All positional parameters as separate words.... Its exactly the same as $@

- That $@ and $* allow you to access all the positional parameters that are provided to your bash script
- The $@ expands to all the positional parameters provided to the script, but provides them as unquoted separate words , that are subject to word splitting
- "$@" stops subsequent word splitting and ensures the value of the positional parameters is exactly how they were provided by the user 
