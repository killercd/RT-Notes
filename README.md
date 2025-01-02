# RT-Notes
Red teaming notes


## Seclist/Wordlist repo
https://github.com/danielmiessler/SecLists
git clone https://github.com/danielmiessler/SecLists


## Wordlist SecList raft medium files
$SECLIST_FOLDER/Discovery/Web-Content/raft-medium-files.txt

## Set batch environment vars
```batch
## Set batch variables (current session)
set SECLIST_FOLDER="c:\data\seclist"
echo %SECLIST_FOLDER%

## Set batch variables (persistent current-user)
setx SECLIST_FOLDER "c:\data\seclist"
echo %SECLIST_FOLDER%


## Set batch variables (persistent system)
setx SECLIST_FOLDER "c:\data\seclist" /M
echo %SECLIST_FOLDER%
```

## read text file line by line in python
```python
file = open(args.wordlist, "r", encoding="utf-8")
while True:
	content=file.readline()
	if not content:
		break
	print(content.strip())
file.close()
```

## display open ports and pid in windows
```batch
netstat -nao
```

## Radagast: fuzz web application
```bash
python radagast.py --url http://localhost:8000/vulnerabilities/FUZZ --wordlist wordlist.txt --ic 200 --timeout 1
```
