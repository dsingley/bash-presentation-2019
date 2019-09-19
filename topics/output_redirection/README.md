
# bash: improving your command line and script productivity

## output redirection

|| file descriptor || number ||
| stdin | 0 |
| stdout | 1 |
| stderr | 2 |

```bash
./script.sh 2> err.log > out.log

./script.sh &> outAndErr.log

./script.sh |& tee outAndErr.log # and still shown on the console

./script.sh 2> /dev/null | grep outPattern # stderr is suppressed

./script.sh |& grep outAndErrPattern
```

- https://www.tldp.org/LDP/abs/html/io-redirection.html

