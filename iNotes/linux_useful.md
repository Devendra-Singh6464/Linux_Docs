# linux usefull commands--

By default booting mode
```
systemctl get-default
```

check terminal no.
```
tty
```

if you want to change default booting mode 'test' so
```
systemctl set-default multi-user.target
```

if set garadical mode so 
```
systemctl set-default grafical.taraget
```
  
we are redirecting ">" the o/p to "file3" instead of screen
```
cat file1 file2 > file3
```

"who" display info about each user on separate line & "wc -l" count no. of lines.
```
who |wc -l
```

we want o/p to be display on screen as well as redirected to "file4" use "tee"
```
cat file1 file2 | tee file4
```

### Changing shell as a normal user

display the current shell
```
echo $SHELL
```
show available shells. all the shell are in "/bin/ directory.
```
ls /bin/*sh
```
change the shell as a normal user, it will ask passwd. then enter the shell you want to use
```
chsh 
```

Details file system 
-rw-rw-r-- 1 devendra.singh Wuser      1101 Aug 20 19:20  task
  	
explain--
-rw-rw-r-- : (file permission)
1 :  (no of links)
devenda.singh : user 
Wuser : group 
1101 : size 
Aug 20 19:20 : time last modification 
task : file name



















	
