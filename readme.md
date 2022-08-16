## JSON structure change tolerant Windoes git repository

### Installation
Replace with `git-files` folder files in your project `.git` folder. Script `pre-commit` should be placed in `./.git/hooks`.

### Usage
Command `git diff` will not show any changes if you swap some object keys.
In case of `git commit` command, using `pre-commit` git hook script, should automatically prettify *.json files, sort objects keys and stage changes. 

### Under the hood 
Under the hood used `./bin/jq.exe` console application for JSON processing and keys sorting. For using on Linux systems `jq` can be installed from repository https://stedolan.github.io/jq/ and `git-files` need to changed to run just `jq` globally.    
