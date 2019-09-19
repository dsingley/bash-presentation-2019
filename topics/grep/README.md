
# bash:  improve your command line & script productivity

# grep

```bash
ps -ef | grep patter[n] # no "grep --color=auto pattern" in the results

ps -ef | grep -E 'one thing|or another' # extended grep

# show context with -C, -B, and/or -A
grep -A1 diverged ./the-road-not-taken.txt

# inverse match -- exclude blank lines
grep -v '^\s*$' ./the-road-not-taken.txt
```

