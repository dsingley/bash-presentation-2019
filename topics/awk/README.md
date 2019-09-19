
# bash: improve your command line & script productivity

## awk

### start by using more features -- combine line and column selection
```bash
ps -ef | grep pattern | awk '{print $8}'

ps -ef | awk '/pattern/ {print $8}'

# (consider pgrep...)
```

### it's a real programming language! -- reverse a fully qualified host name
```bash
echo www.fortitudetec.com | awk -F . '{for (i=NF;i>1;i--) printf("%s.", $i); print $i}'
```

### read about string functions

- https://www.gnu.org/software/gawk/manual/html_node/String-Functions.html

