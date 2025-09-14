<img width="1383" height="385" alt="image" src="https://github.com/user-attachments/assets/b1e9d307-ca8e-4cc8-9705-307d7c649e0e" /># OS-Linux-commands-Shell-scripting
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
<img width="1436" height="978" alt="image" src="https://github.com/user-attachments/assets/12219faa-6f65-407b-86ca-63d705c65d0f" />
<img width="1452" height="858" alt="image" src="https://github.com/user-attachments/assets/c57608e7-7253-4bfc-ba47-d4344309906a" />

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
<img width="837" height="247" alt="image" src="https://github.com/user-attachments/assets/ce913f46-7c84-4118-bd7a-262679821330" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="837" height="247" alt="image" src="https://github.com/user-attachments/assets/838cc6d7-d030-4edc-9ebc-f16af4a66680" />

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

<img width="832" height="141" alt="image" src="https://github.com/user-attachments/assets/b63a34bc-860e-48fe-a073-1307edfa5263" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1051" height="216" alt="image" src="https://github.com/user-attachments/assets/26a14867-bb80-43df-aa20-18e314a8f0c0" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="703" height="311" alt="image" src="https://github.com/user-attachments/assets/7c933021-d434-4d69-b561-561251435e66" />


tar -xvf backup.tar
## OUTPUT
<img width="716" height="213" alt="image" src="https://github.com/user-attachments/assets/bcd9e574-9bf2-42dd-8db9-609edac43452" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="965" height="86" alt="image" src="https://github.com/user-attachments/assets/2c616cb4-a071-4ddc-bc31-ec992a4971e1" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="1612" height="170" alt="image" src="https://github.com/user-attachments/assets/57eaabc7-fcb2-4063-b091-58452ee92239" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1612" height="170" alt="image" src="https://github.com/user-attachments/assets/d875d9bd-120a-427f-a446-e3f8d869cb68" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1612" height="234" alt="image" src="https://github.com/user-attachments/assets/f43cb1fb-8809-400c-893e-0492b420a6c9" />


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
## OUTPUT
<img width="1612" height="306" alt="image" src="https://github.com/user-attachments/assets/d48dc494-7617-4298-a888-9631ba301be5" />

chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="1612" height="363" alt="image" src="https://github.com/user-attachments/assets/e5238fbe-1022-4bda-9dc9-54c5f5cac88c" />

 
ls file1
## OUTPUT
<img width="1612" height="123" alt="image" src="https://github.com/user-attachments/assets/d8d9bc59-951a-47eb-bc57-72d6024eba0f" />

echo $?
## OUTPUT 
<img width="1612" height="123" alt="image" src="https://github.com/user-attachments/assets/cc00274c-ed2a-476d-b3dc-d6f9d2ca0634" />

./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="1612" height="123" alt="image" src="https://github.com/user-attachments/assets/8ec26265-dfda-4111-b48d-72e5141e85b6" />

abcd
 
echo $?
 ## OUTPUT

<img width="1612" height="57" alt="image" src="https://github.com/user-attachments/assets/1498cbf7-5cc5-49ad-8910-32698c483f42" />

 
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
<img width="1613" height="715" alt="image" src="https://github.com/user-attachments/assets/2afca7ff-10d5-4e48-b87f-5809f2ebc4cc" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1606" height="99" alt="image" src="https://github.com/user-attachments/assets/0689dfa7-fa9f-4460-a273-ad67855bcadc" />


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
<img width="1606" height="185" alt="image" src="https://github.com/user-attachments/assets/93e475fa-d1f8-4f8b-a54c-7b3e07a4bc7e" />

./psswdperm.sh
## OUTPUT
<img width="1606" height="236" alt="image" src="https://github.com/user-attachments/assets/8e8a6296-3402-456f-b2ae-52afb6cc54bc" />

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
<img width="696" height="402" alt="image" src="https://github.com/user-attachments/assets/42a63f53-3fc2-4cf4-a7db-fea52954ab24" />

./ifnested.sh 
## OUTPUT

<img width="699" height="51" alt="image" src="https://github.com/user-attachments/assets/1e52d762-b7c2-46cf-aabc-8ab9bf7b5e0b" />


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
## OUTPUT
<img width="699" height="316" alt="image" src="https://github.com/user-attachments/assets/c1ed1c98-9dc7-4f4c-a486-20ecac6821cc" />


$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="682" height="120" alt="image" src="https://github.com/user-attachments/assets/ee000509-def5-4e01-8362-db236192253e" />

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
## OUTPUT
<img width="735" height="404" alt="image" src="https://github.com/user-attachments/assets/0412683b-773e-4725-a492-d0f1adb022f4" />


$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="642" height="168" alt="image" src="https://github.com/user-attachments/assets/6339d6ac-8873-42ce-9e27-c68b8f4bf55b" />

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

chmod 755 elifcheck.sh
 
 ./elifcheck.sh 
## OUTPUT
<img width="676" height="122" alt="image" src="https://github.com/user-attachments/assets/be0dcccb-6bd5-473b-98ba-8358c95ca14a" />


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
<img width="676" height="122" alt="image" src="https://github.com/user-attachments/assets/0c6c25f4-d8d9-42f5-9d9e-9a904f77873b" />

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
## OUTPUT 
<img width="670" height="91" alt="image" src="https://github.com/user-attachments/assets/454dda3a-dd15-4001-8064-e1f875466974" />

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
 
## OUTPUT
<img width="744" height="283" alt="image" src="https://github.com/user-attachments/assets/e6a27fb7-6c2d-4d08-8100-8af80f34a712" />

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
 ./untiltest.sh
 ## OUTPUT
 <img width="755" height="153" alt="image" src="https://github.com/user-attachments/assets/afc7d358-3d50-40b0-959e-4f7d7e456028" />

 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
chmod 755 forin1.sh
./forin1.sh 
 <img width="755" height="199" alt="image" src="https://github.com/user-attachments/assets/c4dbe17b-3b10-43aa-a967-9dc16243bc62" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
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

 <img width="755" height="138" alt="image" src="https://github.com/user-attachments/assets/5a5dabbe-d469-4f1f-98fe-4aa6ad8043f2" />

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
<img width="755" height="324" alt="image" src="https://github.com/user-attachments/assets/f47face7-b667-4510-b1a0-809e8bbd9990" />
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in 'cat $file'
do
echo Visit beautiful $file
done
```
$ chmod 777 forinfile.sh
$ cat cities Hyderabad Alampur Basara Warangal Adilabad Bhadrachalam Khammam

## OUTPUT

<img width="1383" height="196" alt="image" src="https://github.com/user-attachments/assets/87bfefdc-7056-4051-9637-eaba506cc134" />

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
<img width="1383" height="295" alt="image" src="https://github.com/user-attachments/assets/91048b5f-f794-4f01-81d6-ac4c38b8e3f1" />

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
<img width="1314" height="282" alt="image" src="https://github.com/user-attachments/assets/ab1f780a-dd16-4612-b268-f961c54cc19a" />

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
<img width="1386" height="317" alt="image" src="https://github.com/user-attachments/assets/8e06d957-8c9b-48c9-88af-4805117413c7" />

 
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
echo "The for loop is completed"
```
## OUTPUT

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
<img width="1383" height="365" alt="image" src="https://github.com/user-attachments/assets/45ed877a-ba9e-4ed0-a3fb-cc6b391cc4dd" />

cat forcontinue.sh 
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
 <img width="1383" height="385" alt="image" src="https://github.com/user-attachments/assets/4b2ab116-e6ac-4f94-9b01-d8a2ceef1ad2" />

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
<img width="1383" height="212" alt="image" src="https://github.com/user-attachments/assets/6aac84fb-0c51-43dd-9132-88e1529a5865" />


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
 <img width="1383" height="186" alt="image" src="https://github.com/user-attachments/assets/cc67b82f-66e7-4435-95e7-e667d28aeb4d" />

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

 <img width="1383" height="350" alt="image" src="https://github.com/user-attachments/assets/20fefca3-6e80-4ce7-9590-9bfb397f3507" />

 ./funcex.sh 1 2
<img width="1383" height="406" alt="image" src="https://github.com/user-attachments/assets/b6b55c3a-0b97-4996-9178-84f83cd0e53a" />

 
cat >argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh


$ ./argshift.sh 1 2 3
 ## OUTPUT
 <img width="1383" height="253" alt="image" src="https://github.com/user-attachments/assets/9a34524d-96fb-4514-8158-7da0b7e923dc" />

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
## OUTPUT
$ chmod 777 argshift.sh

$ ./argshift.sh 1 2 3
 <img width="1383" height="350" alt="image" src="https://github.com/user-attachments/assets/101154b9-d383-434f-9394-2596af2ade26" />

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
 
 <img width="1383" height="479" alt="image" src="https://github.com/user-attachments/assets/f1afa222-0828-4f6a-8ba8-6c7bafaa11fb" />

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
 <img width="1383" height="351" alt="image" src="https://github.com/user-attachments/assets/ed1ffa23-9ae7-417e-875f-4b3e8f0d3b7d" />

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
<img width="1383" height="245" alt="image" src="https://github.com/user-attachments/assets/36652a9e-66fd-457f-8519-d9651f354ce0" />


# RESULT:
The Commands are executed successfully.
