# supersearch
The purpose of this script is to make it easy to search every file in a directory for a given string (case insensitive). I use `grep -rnwi` multiple times a day, almost every day, so this simplifies it so I can run that with a single command.

## Parameters
This script supports two parameters: A directory, and a search string. If no directory is specified, it will use the current directory.

### Example Command
The following command will search every file in the current directory and all subdirectories for the text `endpoint`.
```
supersearch . "endpoint"
```

### Example Output
```
Found in (./main.py)
Line 20: def get_status_code(endpoint)

Found in (./main.py)
Line 21:        url = base_url + endpoint

Found in (./main.py)
Line 25: def get_all(endpoint, is_active=None, updated_since=None)

Found in (./main.py)
Line 26:        url = base_url + endpoint

Found in (./main.py)
Line 40: def delete_by_id(endpoint, id)
```

### Installation
1. Execute `git clone https://github.com/somnolentPumpkin/supersearch.git`.
2. Execute `cd supersearch`.
3. Execute `sudo chmod +x supersearch`.
4. Execute `./supersearch <DIRECTORY> <TEXT>`

Optionally, if you want to be able to run the script from anywhere, you can put the `supersearch` script in your `/bin` folder. To do that, execute `sudo mv supersearch /bin/supersearch` on Linux, or `sudo mv supersearch /usr/local/bin/supersearch` on OS X.
