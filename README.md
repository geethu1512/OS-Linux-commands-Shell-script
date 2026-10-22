<img width="137" height="132" alt="image" src="https://github.com/user-attachments/assets/ec8de525-983c-41d8-b39a-7839de7aff8c" /># OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
<img width="220" height="110" alt="image" src="https://github.com/user-attachments/assets/580d1584-3e8e-4a4a-92e7-e58874245fc5" />

cat < file1
## OUTPUT
<img width="197" height="106" alt="image" src="https://github.com/user-attachments/assets/c9bde325-6404-41ad-9c89-84c55ea7a15e" />



cat < file2
## OUTPUT


# Comparing Files
<img width="327" height="66" alt="image" src="https://github.com/user-attachments/assets/d071bed5-3780-4d01-83d6-e89421af9c71" />

cmp file1 file2
## OUTPUT
 <img width="277" height="140" alt="image" src="https://github.com/user-attachments/assets/b8dcfbbf-1995-4281-bbc0-0ab220f662b0" />

comm file1 file2
 ## OUTPUT
<img width="232" height="212" alt="image" src="https://github.com/user-attachments/assets/80b10f35-1a5c-418b-8102-ace0f07f0a2d" />

 
diff file1 file2
## OUTPUT


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT




cut -d "|" -f 1 file22
## OUTPUT
<img width="231" height="92" alt="image" src="https://github.com/user-attachments/assets/13eca3d7-7073-4efc-91c9-a03d51320932" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="230" height="87" alt="image" src="https://github.com/user-attachments/assets/d2b35801-80f2-431d-a4bd-b793306fc157" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 <img width="216" height="67" alt="image" src="https://github.com/user-attachments/assets/9df4da77-eed3-4399-8157-b2f449ce633e" />

grep Hello newfile 
## OUTPUT


<img width="218" height="53" alt="image" src="https://github.com/user-attachments/assets/2cae3e3d-1164-417c-af17-538c4be7956c" />


grep hello newfile 
## OUTPUT
<img width="235" height="61" alt="image" src="https://github.com/user-attachments/assets/47fa2eb5-9670-484f-b8e0-61057a250961" />




grep -v hello newfile 
## OUTPUT
<img width="336" height="56" alt="image" src="https://github.com/user-attachments/assets/ad9ca0af-d0c5-4848-ab61-d0dbcab1506a" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="235" height="61" alt="image" src="https://github.com/user-attachments/assets/c5a1ea1d-dee6-4e0d-8a24-0b335de4fd23" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="336" height="56" alt="image" src="https://github.com/user-attachments/assets/cff0cc1b-8ce4-45da-9d07-4d8f25e0b778" />




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="272" height="56" alt="image" src="https://github.com/user-attachments/assets/02db7f39-21ae-4ed1-87b4-03691138a59d" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="423" height="80" alt="image" src="https://github.com/user-attachments/assets/a81ea954-6cc4-475c-9803-cb67091ad515" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="338" height="73" alt="image" src="https://github.com/user-attachments/assets/0e9af89e-e1d5-4a0c-a6c4-0ba74f80045f" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="338" height="71" alt="image" src="https://github.com/user-attachments/assets/2c045fb4-2661-4b46-b237-6c32977983f4" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="310" height="60" alt="image" src="https://github.com/user-attachments/assets/e804c08c-bdbd-4b65-83ba-948b84484ba7" />


egrep '(world$)' newfile 
## OUTPUT

<img width="243" height="98" alt="image" src="https://github.com/user-attachments/assets/38da3e5d-16d5-466e-a4bc-696b6c89b19e" />


egrep '(World$)' newfile 
## OUTPUT
<img width="251" height="52" alt="image" src="https://github.com/user-attachments/assets/7880ebfd-c975-4894-ab51-3281e16cc62a" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="285" height="97" alt="image" src="https://github.com/user-attachments/assets/ecd73a18-de24-4e7f-8e58-4e7e95281ec7" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="262" height="60" alt="image" src="https://github.com/user-attachments/assets/b150ea7b-1dae-4d33-b844-320cd0922635" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="296" height="72" alt="image" src="https://github.com/user-attachments/assets/8f27cfbf-2f0c-4623-a45a-bebab9043640" />


egrep 'Linux.*World' newfile 
## OUTPUT


egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
<img width="271" height="91" alt="image" src="https://github.com/user-attachments/assets/4e45e1fe-3bc1-4f30-9dab-b442ea8194bf" />


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="317" height="70" alt="image" src="https://github.com/user-attachments/assets/c2687844-1719-418b-9a5a-47767650d82c" />



sed -n -e '$p' file23
## OUTPUT
<img width="227" height="60" alt="image" src="https://github.com/user-attachments/assets/5ef195f4-6143-4c46-9dd1-385c7c5e4d14" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="295" height="173" alt="image" src="https://github.com/user-attachments/assets/d77fb34d-57b3-49e0-8f4b-87812d31cfa9" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="350" height="170" alt="image" src="https://github.com/user-attachments/assets/ce6644ac-059e-46aa-a115-ed685abce84b" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="301" height="170" alt="image" src="https://github.com/user-attachments/assets/8f6ed6ac-2afc-4c76-958b-d4507870e9d6" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="272" height="122" alt="image" src="https://github.com/user-attachments/assets/2cdce36b-8e61-464f-b01e-a6b9a02c9329" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="290" height="101" alt="image" src="https://github.com/user-attachments/assets/344cd740-6d01-4d87-921d-3ad6be5e6be4" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="307" height="90" alt="image" src="https://github.com/user-attachments/assets/0fd902bb-f676-468b-9950-9cbef56cf5df" />



seq 10 
## OUTPUT
<img width="237" height="210" alt="image" src="https://github.com/user-attachments/assets/51725df7-16f6-4b28-88c5-03f856ef36e9" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="237" height="92" alt="image" src="https://github.com/user-attachments/assets/5d97c03a-2480-4771-a7b2-5e2c9b9545fa" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="256" height="87" alt="image" src="https://github.com/user-attachments/assets/69ea6a29-a368-4ac2-9d9d-b2b270fe2f8d" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="277" height="112" alt="image" src="https://github.com/user-attachments/assets/2695db4d-75f2-456d-8afb-1e454058e6b8" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="286" height="91" alt="image" src="https://github.com/user-attachments/assets/fc62693a-7994-451a-8a1a-f20094f5d9b6" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="315" height="92" alt="image" src="https://github.com/user-attachments/assets/9c3953d7-c638-45df-8abe-49c085ac9191" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="307" height="105" alt="image" src="https://github.com/user-attachments/assets/88bf37d7-c5ad-4898-b9a8-ef4419d28a76" />


sed -n '2,4{s/$/*/;p}' file23
<img width="351" height="101" alt="image" src="https://github.com/user-attachments/assets/429960e9-e410-4f8d-9d96-c08b9a0c493e" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="262" height="126" alt="image" src="https://github.com/user-attachments/assets/18427684-55b9-4006-9ff8-a84b78348404" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
<img width="267" height="121" alt="image" src="https://github.com/user-attachments/assets/9f125c52-de8f-4c2d-95fc-0ecc47b4083c" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="338" height="176" alt="image" src="https://github.com/user-attachments/assets/e5cbe7c1-cdef-4700-a31c-d683d7694232" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="301" height="101" alt="image" src="https://github.com/user-attachments/assets/eda5dc77-a1f0-4653-bc83-9169a706e8e6" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="367" height="98" alt="image" src="https://github.com/user-attachments/assets/6aeb15df-36e7-4db4-85a9-6a6f05ac3f41" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="305" height="551" alt="image" src="https://github.com/user-attachments/assets/b525bc3a-458f-4502-b5d4-687fed3cedab" />
<img width="137" height="132" alt="image" src="https://github.com/user-attachments/assets/fde11bca-5eda-4510-86d9-6b78ab09cb2a" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="552" height="703" alt="image" src="https://github.com/user-attachments/assets/800bf8ea-ec35-4de5-ba5e-6a27706c4f83" />
<img width="508" height="125" alt="image" src="https://github.com/user-attachments/assets/218543de-a3c1-4eba-8986-69fce278beee" />


tar -xvf backup.tar
## OUTPUT
<img width="408" height="552" alt="image" src="https://github.com/user-attachments/assets/d366d4b0-1891-4baa-a8f5-e5031e556422" />
<img width="146" height="137" alt="image" src="https://github.com/user-attachments/assets/a0ab9077-be80-4b41-9961-564ac60bc2b2" />

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="352" height="215" alt="image" src="https://github.com/user-attachments/assets/e92fae5a-4344-476c-9ad9-ec6cbf16ee5a" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="357" height="103" alt="image" src="https://github.com/user-attachments/assets/dd74b888-69d0-41d5-a701-3c46d4c10b15" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="422" height="323" alt="image" src="https://github.com/user-attachments/assets/fcbe9c13-15e0-4bb7-bed3-fdb411c4cd83" />

 
ls file1
## OUTPUT
<img width="353" height="55" alt="image" src="https://github.com/user-attachments/assets/cf0dc271-4a09-4fb9-81bd-e657c9f54d31" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="372" height="247" alt="image" src="https://github.com/user-attachments/assets/c0ab95d1-1a81-4fcd-b982-ebe3adfeabd2" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="351" height="207" alt="image" src="https://github.com/user-attachments/assets/5c4fbe88-25e3-4547-b409-8717f63a63fa" />


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
<img width="398" height="202" alt="image" src="https://github.com/user-attachments/assets/d0576d58-c427-4747-ab86-71e7f967fc44" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="325" height="113" alt="image" src="https://github.com/user-attachments/assets/f1fb5f2a-8fb2-49f6-90d4-796885ef67db" />


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="580" height="168" alt="image" src="https://github.com/user-attachments/assets/7324b4d4-0479-4913-99a5-f141dfd89606" />

# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="427" height="385" alt="image" src="https://github.com/user-attachments/assets/052971e3-6ff3-48a7-9da9-f8be21fb028a" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="377" height="243" alt="image" src="https://github.com/user-attachments/assets/fe5379ff-ec00-4c8b-8b2f-85219aa38926" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 
 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 


# RESULT:
The Commands are executed successfully.
