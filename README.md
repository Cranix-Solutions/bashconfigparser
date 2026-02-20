# bashconfigparser
This python for reading and writing variables in bash files.
This script can parse any arbitary bash files and find all variables with following syntax:
```
VAR=value
export VAR=value
declare -x VAR=value
setenv VAR value
```
The variable names must conform the bash conventions expect of the first case. In this case '.' is also allowed to be able to parse java property files.
## Documentation

Usage:
```
from bashconfigparser import BashConfigParser

config = BashConfigParser(config_file="/opt/cranix-java/conf/cranix-api.properties")
passwd = config.get('de.cranix.dao.User.Register.Password')
```

Functions:
```
config.get('EXAMPLE_NAME') -> returns value from configuration
config.set('EXAMPLE_NAME') -> sets value in configuration
```

Examples:
```
config = BashConfigParser(config_file="EXAMPLE_FILE")
passwd = config.get('PATH_TO_THE_PASSWORD')
name = config.get('PATH_TO_THE_NAME')
age = config.get('PATH_TO_THE_AGE')
```

## Status
The module is tested and works fine.
