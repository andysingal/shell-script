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
- ```tar -cvf ~/bash_course/my_backup_"$(date +%d-%m-%Y_%H-%M-%S)".tar ~/* 2>/dev/null```
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
