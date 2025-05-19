### Scripting basic syntax

Comments in shells scripting.
1. single line comment `#`.
2. multi-line comments
```
<<comment
code ----
------
comment
```

variable define
```
var_name = value
var_name =$(hostname)
echo $var_name
```

Once you defined a variable and don't wanna change it until end of the script.
```
readonly var_name="Hello"
```

How to define array ?
```
arr =( 1 2 hii "hi man" )
```

how to get length of array
```
echo "${#arr[*]}"
```

how to get all variable of array
```
echo "${arr[*]}"
```

how to get single value of array
```
echo "${arr[3]}"
```

how to get specific values```
```
echo "${arr[*]:1:4}"
```

```
echo "${arr[*]:2}"
```

how to update an array?
```
arr+=( 5 7 8 )
```

#### Array key-values

```
declare  -A  arr
```

```
arr=( [name]=dev [age]=24 )
```

```
echo "${arr[name]}"
```

### String Operations

```
myvar="hello world!"
```

```
length=${#myvar}
```

```
upper=${x^^}
```

```
lower=${y,,}
```

```
replace=${myvar/hello/hey}
```

```
slice=${myvar:6:8}
```

### User Interaction

Tacking input form users
```
read <var_name>
```

```
echo "your name" NAME
```

#### Options
```bash
set -o noclobber  # Avoid overlay files (echo "hi" > foo)
set -o errexit    # command in bash that tells the script to **automatically exit** if any command in the script fails (returns a non-zero exit status).
set -o pipefail   # Unveils hidden failures
set -o nounset    # If variable hasn’t been defined, the script will stop and print an error like:
```

```bash
set +o noclobber  # overlay files (echo "hi" > foo)
set +o errexit    # This will allow the script to continue running even after an error.
set +o pipefail   # continusly runscript 
set +o nounset    # Exposes unset variables
```

What is a Pipeline?
A **pipeline** is when you use the `|` symbol to pass the output of one command to another. For example:

Without pipefail:
By default, bash only checks the last command in the pipeline for success or failure. So, even if one of the earlier commands fails, the pipeline will not return an error unless the last command fails.


