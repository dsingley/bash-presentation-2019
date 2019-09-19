
# bash: improve your command line & script productivity

## commands worth trying

### column

```bash
printf "hello, world\t42\na\tbb\nccc\tdddd\neeeee\tffffff\n" | column -t -s $'\t'
```

### jq

```bash
jq '.' ./example.json

# find the objects in the `"array"` field that have even `"id"` values
jq '.array[] | select(.id % 2 == 0)' ./example.json

# transform output...
# to CSV
jq -r '.array[] | select(.id % 2 == 0) | [.id, .color] | @csv' ./example.json

# into new objects
jq '.array[] | select(.id % 2 == 0) | {concatinated: (.color + "-" + (.id | tostring))}' ./example.json
```

- https://stedolan.github.io/jq/manual/

