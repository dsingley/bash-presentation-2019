
# bash: improve your command line & script productivity

## scipting best practices

### fail on errors including undefined variables!
```bash
#!/bin/bash -eu

set -e
set -u

# temporarily accept failure with:
set +x
# or:
./bad-program || true
```

### log tracing to a file (other than stderr)
```bash
exec 42>log.xtrace
BASH_XTRACEFD=42
set -x
```

### log to a file (from within a script)
```bash
exec &> >(tee script.log)
```

