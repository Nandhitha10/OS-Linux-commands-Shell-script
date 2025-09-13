# OS-Linux-commands-Shell-scripting
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
cat < file1
## OUTPUT

<img width="854" height="124" alt="image" src="https://github.com/user-attachments/assets/78a7422e-e6be-4276-8b9a-9ad14f4e93af" />


cat < file2
## OUTPUT
<img width="863" height="152" alt="image" src="https://github.com/user-attachments/assets/4c5e89a3-87d4-4d60-b5ab-1198657195a4" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="774" height="54" alt="image" src="https://github.com/user-attachments/assets/41b610fe-0186-44f0-865e-590fec99e7a8" />

comm file1 file2
 ## OUTPUT
<img width="744" height="273" alt="image" src="https://github.com/user-attachments/assets/2d4a5602-94b0-46ec-aa1f-a949e9a7af8f" />

 
diff file1 file2
## OUTPUT

<img width="744" height="273" alt="image" src="https://github.com/user-attachments/assets/a31c78fb-e7c8-41c2-90be-dfbee75dc8f0" />

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


<img width="709" height="85" alt="image" src="https://github.com/user-attachments/assets/511d6eb7-1e5d-4be8-884b-5c992128255c" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="707" height="95" alt="image" src="https://github.com/user-attachments/assets/a53ffe17-56d3-48a2-9f9c-043d7b1b40d6" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="707" height="95" alt="image" src="https://github.com/user-attachments/assets/5c28c5f5-f132-478c-8fa8-cef9f89cfdcc" />

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="711" height="60" alt="image" src="https://github.com/user-attachments/assets/5dc4f1bb-2e1e-490b-b486-bd0f626db4cd" />


grep hello newfile 
## OUTPUT

<img width="711" height="60" alt="image" src="https://github.com/user-attachments/assets/579624fa-fdca-4b27-9d73-22c2d981e766" />



grep -v hello newfile 
## OUTPUT

<img width="711" height="60" alt="image" src="https://github.com/user-attachments/assets/96fd4f71-d3ea-42e9-8e23-44844d8b848c" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="722" height="77" alt="image" src="https://github.com/user-attachments/assets/044fe341-ffa7-487e-8ed9-32ad88a4bcc3" />



cat newfile | grep -i -c "hello"
## OUTPUT


<img width="664" height="57" alt="image" src="https://github.com/user-attachments/assets/432d31e6-cf27-48bf-af81-a675085b9131" />


grep -R ubuntu /etc
## OUTPUT


<img width="1245" height="1108" alt="image" src="https://github.com/user-attachments/assets/d8844be1-bae0-4db2-afaf-74e289d4dffa" />

grep -w -n world newfile   
## OUTPUT

<img width="668" height="73" alt="image" src="https://github.com/user-attachments/assets/0f0cd086-471a-4e4c-af30-bb5f9b4b0ebf" />

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

<img width="668" height="73" alt="image" src="https://github.com/user-attachments/assets/7d3b1ff5-334a-40ee-8855-fcf21d4e6fbc" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="668" height="73" alt="image" src="https://github.com/user-attachments/assets/67061da1-e711-4669-b21a-ea02ed411c31" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="668" height="73" alt="image" src="https://github.com/user-attachments/assets/cf619088-1873-42f7-99a0-963ad9d2d071" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="671" height="59" alt="image" src="https://github.com/user-attachments/assets/49656164-8b7f-41c1-ba29-c7e7d7f88c15" />

egrep '(world$)' newfile 
## OUTPUT

<img width="675" height="75" alt="image" src="https://github.com/user-attachments/assets/63f83751-f1d3-47dc-9698-994a2a5493ef" />


egrep '(World$)' newfile 
## OUTPUT
<img width="685" height="53" alt="image" src="https://github.com/user-attachments/assets/014c4ebb-e68e-4213-9bf6-52423ab3cdfb" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="699" height="120" alt="image" src="https://github.com/user-attachments/assets/4ad8ed7a-e5de-46be-a5eb-ad4118027cf6" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="720" height="56" alt="image" src="https://github.com/user-attachments/assets/b911a509-7221-4bcb-9484-13408faface0" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="720" height="56" alt="image" src="https://github.com/user-attachments/assets/72f5ff4e-b71e-4f2c-8418-d42870e52f17" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="720" height="56" alt="image" src="https://github.com/user-attachments/assets/9935d8e8-0a63-4b61-835f-8e1821d346c9" />


egrep l{2} newfile
## OUTPUT

<img width="720" height="78" alt="image" src="https://github.com/user-attachments/assets/0de3d47e-a359-42e0-9c59-8500f3691b10" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="732" height="95" alt="image" src="https://github.com/user-attachments/assets/04c5dbed-1d16-4086-9853-c4c86d674694" />

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

<img width="725" height="58" alt="image" src="https://github.com/user-attachments/assets/a7a252f9-9a63-4872-a265-c267aabdfdf4" />


sed -n -e '$p' file23

## OUTPUT

<img width="725" height="58" alt="image" src="https://github.com/user-attachments/assets/ce944450-2a4c-4212-a319-1ce0cfe64b10" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="731" height="206" alt="image" src="https://github.com/user-attachments/assets/c8fbf7af-ad17-4001-bcfc-334f3637c7e5" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="731" height="206" alt="image" src="https://github.com/user-attachments/assets/852cbbe1-349d-45f9-a7ec-101793f9bca2" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="731" height="206" alt="image" src="https://github.com/user-attachments/assets/bb8842e1-57ac-4787-a145-c9e870450119" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="747" height="135" alt="image" src="https://github.com/user-attachments/assets/1a57c47a-ffac-48fe-afd5-9233a0ff7f90" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="754" height="272" alt="image" src="https://github.com/user-attachments/assets/066cab18-085f-4bb8-8233-106557529359" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="706" height="253" alt="image" src="https://github.com/user-attachments/assets/e52d1a79-ceb0-4f74-aeaa-40aab0e68aab" />


seq 10 
## OUTPUT

<img width="706" height="253" alt="image" src="https://github.com/user-attachments/assets/37ff1dc0-9f41-4e40-9e1c-4dc45a84d196" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="699" height="106" alt="image" src="https://github.com/user-attachments/assets/61c95406-0697-495c-967e-ebc9f423f51c" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="694" height="107" alt="image" src="https://github.com/user-attachments/assets/1197e0c7-28c6-482e-8c6a-cc1091ffc318" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="694" height="107" alt="image" src="https://github.com/user-attachments/assets/95839fb4-7747-4ea9-8fec-5be8267cfe81" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="694" height="107" alt="image" src="https://github.com/user-attachments/assets/4c59212c-6809-4b94-b3c4-b9260ce953cb" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="694" height="107" alt="image" src="https://github.com/user-attachments/assets/106215fa-543f-4c69-81be-44e27367b069" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="694" height="107" alt="image" src="https://github.com/user-attachments/assets/f8dcfe1b-7dff-4dd0-9307-ef7309f15965" />


sed -n '2,4{s/$/*/;p}' file23
<img width="693" height="99" alt="image" src="https://github.com/user-attachments/assets/73076aee-d2d3-486c-8b23-0b4bb26843ff" />


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

<img width="690" height="142" alt="image" src="https://github.com/user-attachments/assets/6ed41c80-ba7a-496d-be01-7a9bfed25e17" />


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

<img width="690" height="142" alt="image" src="https://github.com/user-attachments/assets/138a327a-5a04-43ba-8e0c-eb8932191515" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="703" height="206" alt="image" src="https://github.com/user-attachments/assets/b87cfaa5-9342-4d04-a1ca-d0dbe67ed04b" />

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

<img width="706" height="102" alt="image" src="https://github.com/user-attachments/assets/3b6722f5-d6f6-45d0-9ddd-8e6d633098a8" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="706" height="102" alt="image" src="https://github.com/user-attachments/assets/fbaa2550-86eb-4c0f-9a29-b2015a312eaf" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
