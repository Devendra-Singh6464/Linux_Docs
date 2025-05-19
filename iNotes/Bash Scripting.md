#### Creating Functions

Reference: https://devhints.io/bash
https://linuxconfig.org/bash-scripting-tutorial
https://www.freecodecamp.org/news/bash-scripting-tutorial-linux-shell-script-and-command-line-for-beginners/
https://www.youtube.com/watch?v=TtGM9GfBuok&list=PL0tP8lerTbX3MeIyMxGW2sLhWnPdn_xhd&ab_channel=MPrashant


** Always user variable in curly brackets {}'.

- Tack input With Prompt Message
```bash
read <variable>
```
example:-
```bash
read -p "Please enty your name" name 
```
- -p : print
1.  The two techniques to create and access a function
```bash 
#!/bin/bash

# Method 1
seyhlo() {
	echo "hey men" 
}

# Method 1
function seyhlo {
	echo "hey men"
}

seyhlo 
seyhlo
```

Consider modifying the sayhlo() function as shown below.
```bash

seyhlo() { echo "hey" }

seyhlo
```
`syntax error: unexpected end of file error. This is because the command for `sayHello1` is on the same line as the function name.`

#### Working with Function Arguments

 -- you access the value using `$1` because `$0` contains the function name. Two special symbols merit mention when working with functions.The first, `$#`, provides the number of parameters sent to the function. The second, `$@`, provides access to the parameters as a list.
```bash
#!/bin/bash

sayhlo() {
   echo "Hello $1"
}

sayhlo "deepak"
```

#### Tack Input form the user
```bash
echo "Enter your name"
read name 
echo "your name si $name"
```
- If you tack input lint in same line so 
```bash
read -p 'enter your name: ' name
```
- If you tack password in input with security so.
-  -s : silent input from the user.
-  -p : input in same line
```bash
read -sp 'enter the password: ' password 
```
-  If you not declare a variable  so value automatically store in built in variable.
```bash
echo "enter your name: "
read 
echo "your name is $REPLY"
```

`SED` command :-
-  It allows you to manipulate text in files or streams by performing actions like searching, replacing, and deleting text.
Syntax : ` sed [options] 'command' file` 
- **`[options]`**: Optional flags that modify how `sed` works.
- **`'command'`**: The text operation or command you want to perform.
```bash
sed -i 's|<Directory /var/www/>|<Directory /home/users/devendra.singh/www/>|'
```
- this command change the `/var/www/` to `directory to /home/users/devendra.singh/www`
- -i : taking input
-  -n : last modification
- & : last line
- p : print the line
- '3p' : print the line no. 3
- -e : multiple expressions.

`awk` command :-
syntax:
```bash
awk options 'pattern {action}' file_name
```
and 
```bash
echo "hello" | awk options 'pattern {action}'
```
options:
-  -F field separator
-  -v var=value
-  -f=file

* Terms used in AWK *
- NR : No. of record/row
- NF :  No. of fields
- $0 : print everything
- $1,$2 : Filed no.

- If you want to read special row or column in file .
- demo.txt - file name
- $2 - column 2 read
```shell
awk '{print $2}' demo.txt
```

```shell
 	FILED      
   F1  F2  F3  F4	
| ---------------- |
| THIS IS LINE ONE | ROW 1
| THIS IS LINE TWO | ROW 2
```
 - If your print last column.
```
awk '{print $NF}' demo.txt
```
- If search a word in column so.
```
awk '/deepak/{print $name}' demo.txt
```
- If you print line no. on all rows.
- &0 : print all data
```
awk '{print  NR, $0}' demo.txt
```
- Ignore case sensitive.
```
awk 'BEGIN{IGNORECASE=1} /dev/ {print $0}' demo.txt
```
- working with CSV files.
```
awk -F, '{print $name}' demo.csv
```
- filter (print anyone who has a salary up to 50000).
```
awk -F, '&NF>50000 {print $0}' demo.csv
```
- AWK scripting concept.
```
awk 'BEGIN{print "------------START DETAILS----------"}' {print $0} END{print "----------END-----------"}' demo.txt
```



#### Array
- how to define array
```bash
arr=(4 6 55 4.6 hey "hlo bro")
```
- print values of arrays
```bash
echo "values are ${arr[*]}"
```
- print 3rd index of value
```bash
echo "value of  3rd ${arr[3]}"
```
- find length of arrays.
```bash
echo "${#myarr[*]}"
```
- value from index 2-3
```bash
echo "value of index 2-3 ${#arr[*]:2:3}"
```
- Get length of array
```
echo "${#arr[*]}"
```
- get specific values
```bash
echo "${arr[*]:1}"
echo "${arr[*]:1:4}"
```
- update an array
```bash
arr+=(add 4 6)
```
arrays key-value
```bash
declare -A arr
arr=([name]=Deepak [age]=34)
echo "my name is ${arr[name]}"
echo "my age is ${arr[age]}"
```

#### String Operations
```bash
myvar="Hello wolrd"
length=${#myvar}
upper=${x^^} # all charectors
lower=${y,,} # all charectors
replace=${myvar/world/buddy} 
slice=${myvar:6:11}
```

#### User Interaction
- taking input from the user....
`read <var_name>`
```bash
read -p "your name" name
echo "What is your Name" $name 
```

#### Arithmetic Operations
- Use Expressions
```bash
a=5
b=10
let mult++ 
let mult=$a*$b
echo"$mult"
```
example 2.
```bash
let sum++
let sum=5+10
echo"$sum"
```
- Another option for to perform arithmetic operation
```bash
a=5
b=10
echo"Substraction is $(($a-$b))"
```

#### IF-ELSE
- Note: `[[]] : Inhanstd version of Gshell More Functionality of compare to []`
example-
```bash
read -p "pelase enter the marks: " marks
if [[ $marks -gt 33 ]]
then
	echo"You are pass"
else
	echo"You are fail"
fi
```
symbols-
```bash
|     Description        |    Symbol     |
| ---------------------- | --------------|
| Greaterthanorequalto   |      -ge      |
| Lessthanorequalto      |      -le      | 
| Not Equal              |      -ne/!=   |
| Greater Than           |      -gt      |
| Less Than              |      -lt      |
| Equal                  |      -eq/==   |
```
- ELIF -
```bash
read -p "Please enter the marks: " marks
if [ $marks -ge 60 ]
then
	echo "First Division"
elif [ $marks -ge 45 ]
then
	echo "Second Division"
elif [ $marks -ge 33 ]
then
	echo "Thred division"
else
	echo"Faild"
fi
```

#### CASE
- It works like a simplified `if-elif-else` structure, but it is often easier to read and write when you have multiple conditions to check.
```bash

echo "Provide an option"
echo "a for print date"
echo "b for current directory"
echo "c for list of script"

read choice

case $choice in
	a)date;;
	b)pwd;;
	c)ls;;
	*)echo "Please chose valid value"
esac
```

#### FOR LOOP
- Counting number 
```bash
for i in {1..10}
do
	echo "Number is $i"
done
``` 
-  Iterate values form the file.
```bash
items="/home/users/devendra.singh/myscript/file.txt

for items in $(cat $items)
do
	echo $items
done
```

#### Redirect the file output
- users '> and >>'
- '>' : this overwrite the data in file.
- '>>' : add the data in file.
```bash
ls >> redirect.txt
```

#### Debugging Script:
- If we can enable the debugging of the script using below the script
```bash
set -x
```
- Run script into the background.
```shell
nohup ./<script_name>
```

- For scheduling only one time, use AT
syntax:
```shell
at 12:09 PM <your_command> ctrl+D
```
- to check scheduled job 
```
arq
```
- to remove the schedule
```
atrm <id>
```
- Example
```shell
at 03:17 PM
```

```shell
at> bash /home/users/devendra.singh/myscript/32_redirect.sh
```

```shell
ctrl+d
```







