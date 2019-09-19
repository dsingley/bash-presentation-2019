
# bash: improve your command line & script productivity

## sed

### that edit you're making with `vi`? try using `sed`
```bash
sed -e 's|find|replace|' ./filename.txt # changed file to stdout

sed -e 's|David Bowman:|Dave:|' \
    -e 's|HAL 9000:|HAL:|' \
    -i ./pod-bay-doors.txt              # no output shown,
                                        # file is modified in place
                                        # use -i.bak to save a backup
```

### inserting content
```bash
sed -e '/This mission/a **new line here***' ./pod-bay-doors.txt

sed -e '/This mission/r ./two-lines.txt' ./pod-bay-doors.txt
```

