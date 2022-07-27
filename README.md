# dbfuzzhash
Fuzzy hash search project using databases. 

## Installation
fysa: im using Python 3.8.2
You might want to make a virtual environment first.....

```cmd
python -m venv .venv
```

Next, activate the virtual environment 
```
 .\.venv\Scripts\Activate.ps1
```

install dependencies
```cmd
python -m pip install -r requirements.txt
```

## Use
create the database from schema 
```
python .\tools\db_create.py -c .\test_files\db_new_v4.sql
```

upload files to database
```
python .\tools\hash_and_upload.py -p .\hash_testing\samples\
```

search for ssdeep hashes
```
py .\tools\db_query.py -s 192:97YqBqyeE+dLRpWL61P8ZOTXb5PA5iDxrP0srSwfExZ:jK+DkTA
```

search for cryptographic hashes for matching 
```
py .\tools\db_query.py -i 1 
```

## Deactivation 

```cmd
deactivate
```

# references
https://www.intezer.com/blog/malware-analysis/intezer-community-tip-ssdeep-comparisons-with-elasticsearch/
https://github.com/intezer/ssdeep-elastic
https://www.virusbulletin.com/virusbulletin/2015/11/optimizing-ssdeep-use-scale
https://github.com/bwall/ssdc/blob/master/ssdc


# TODO
possible dataset available at 
https://www.nist.gov/itl/ssd/software-quality-group/ssdeep-datasets

