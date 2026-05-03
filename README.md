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

<img width="270" height="159" alt="image" src="https://github.com/user-attachments/assets/61bb7cd3-3e79-47dc-985d-67877dfe18f7" />


cat < file2
## OUTPUT

<img width="233" height="179" alt="image" src="https://github.com/user-attachments/assets/52b69164-426d-4246-bf3b-2e2095f8c849" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="342" height="80" alt="image" src="https://github.com/user-attachments/assets/0d8e44b5-26fc-4ee8-923f-42f029a88bd3" />

 
comm file1 file2
 ## OUTPUT

<img width="295" height="221" alt="image" src="https://github.com/user-attachments/assets/87cffc17-6d04-4fd6-a53a-a50730b435db" />

 
diff file1 file2
## OUTPUT

<img width="279" height="285" alt="image" src="https://github.com/user-attachments/assets/7f9f6324-eefe-4f68-9f8e-987e44e742c6" />


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

<img width="278" height="94" alt="image" src="https://github.com/user-attachments/assets/0f07cbd8-39ea-45f5-8208-933146c5f736" />

cut -d "|" -f 1 file22
## OUTPUT

<img width="289" height="118" alt="image" src="https://github.com/user-attachments/assets/bf906b21-8c3f-408d-b54b-ab0ff14965fa" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="313" height="124" alt="image" src="https://github.com/user-attachments/assets/190e8270-a4d5-4150-ac6a-5bd66fa1e55c" />


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

<img width="250" height="76" alt="image" src="https://github.com/user-attachments/assets/56c02c51-fb04-4ef5-9ea7-efbdf7442106" />


grep hello newfile 
## OUTPUT

<img width="250" height="75" alt="image" src="https://github.com/user-attachments/assets/cf8fe62c-2f9b-4bfe-9d64-2c791570cb4a" />


grep -v hello newfile 
## OUTPUT

<img width="279" height="81" alt="image" src="https://github.com/user-attachments/assets/c2000322-9cf5-476e-b489-77f1b7210492" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="363" height="100" alt="image" src="https://github.com/user-attachments/assets/777e7e2f-18ae-4b69-bdf6-1264f113bba4" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="390" height="71" alt="image" src="https://github.com/user-attachments/assets/2b31b0a2-382e-4b48-b53e-9123b96de689" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

<img width="315" height="98" alt="image" src="https://github.com/user-attachments/assets/38e81347-84ec-4c66-a2f9-40927d12077f" />


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

<img width="378" height="103" alt="image" src="https://github.com/user-attachments/assets/95b1b5f2-5305-4500-b1a9-e24977ad0bbb" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="364" height="106" alt="image" src="https://github.com/user-attachments/assets/dd9fa05e-b60d-4770-acbc-12c06a4500f8" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="393" height="99" alt="image" src="https://github.com/user-attachments/assets/b69e3176-8891-470f-9060-0ebf1bedff5e" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="325" height="77" alt="image" src="https://github.com/user-attachments/assets/4144cc8d-12c3-4c66-9f12-8743596e970a" />


egrep '(world$)' newfile 
## OUTPUT

<img width="324" height="101" alt="image" src="https://github.com/user-attachments/assets/2342168b-5b5e-4a7b-b0dd-a52b46d24040" />


egrep '(World$)' newfile 
## OUTPUT

<img width="332" height="76" alt="image" src="https://github.com/user-attachments/assets/10169a55-f377-4077-a95d-f0258569c368" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="357" height="104" alt="image" src="https://github.com/user-attachments/assets/5ffbbf1a-a7db-40bc-b3a3-b6dc1ff75113" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="303" height="78" alt="image" src="https://github.com/user-attachments/assets/00d63e85-2f54-421d-a00e-a2a1d4062562" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="344" height="76" alt="image" src="https://github.com/user-attachments/assets/16f84e56-8310-4417-a0f6-0ce970bf2f45" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="357" height="80" alt="image" src="https://github.com/user-attachments/assets/fe914e90-d972-4cc9-a031-a7c32c696193" />


egrep l{2} newfile
## OUTPUT

<img width="255" height="95" alt="image" src="https://github.com/user-attachments/assets/7a67c74a-2b0a-400f-a7ce-434f0ee983c8" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="290" height="126" alt="image" src="https://github.com/user-attachments/assets/7f4e0da5-9080-43d0-b14c-95f0e9d2f821" />


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

<img width="297" height="81" alt="image" src="https://github.com/user-attachments/assets/a5c5ba7c-703d-4a16-9fba-6d6c5ad4b7ec" />


sed -n -e '$p' file23
## OUTPUT

<img width="292" height="72" alt="image" src="https://github.com/user-attachments/assets/211d657c-47a9-49ac-8e46-7efeec817d50" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="351" height="248" alt="image" src="https://github.com/user-attachments/assets/7ce38836-46c4-4a5e-86a8-b499c9c8a2ea" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="373" height="250" alt="image" src="https://github.com/user-attachments/assets/e01944b5-69cc-442a-9d81-91037f839d22" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="388" height="260" alt="image" src="https://github.com/user-attachments/assets/acf7c27e-cdde-49c8-bb7a-6e9f312805d3" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="329" height="187" alt="image" src="https://github.com/user-attachments/assets/149c68e2-35f2-4088-9566-7d6d087f5e19" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="376" height="138" alt="image" src="https://github.com/user-attachments/assets/79efd096-6a0c-48d5-ae1a-9d39f21be0b0" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="401" height="116" alt="image" src="https://github.com/user-attachments/assets/275e624e-816f-4601-ac16-dd6229564732" />


seq 10 
## OUTPUT

<img width="318" height="293" alt="image" src="https://github.com/user-attachments/assets/3868973d-28db-4be5-a7f1-852cc6983b3a" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="282" height="121" alt="image" src="https://github.com/user-attachments/assets/7a67a7f4-bdae-4090-b02d-c4964f347d48" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="306" height="125" alt="image" src="https://github.com/user-attachments/assets/1eed51ba-0003-46ee-8177-882583dcb86c" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="308" height="149" alt="image" src="https://github.com/user-attachments/assets/bf5cbb93-51c7-4864-8523-69cef46a6486" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="301" height="120" alt="image" src="https://github.com/user-attachments/assets/008359e8-0723-4888-b18a-772efb1f42c7" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="339" height="125" alt="image" src="https://github.com/user-attachments/assets/bb27a260-c929-4053-9d90-d871a6fdd801" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="360" height="132" alt="image" src="https://github.com/user-attachments/assets/17ed4c28-6656-486e-8554-e1f732768e53" />


sed -n '2,4{s/$/*/;p}' file23


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

<img width="314" height="182" alt="image" src="https://github.com/user-attachments/assets/7d00c123-d43c-43ed-a4d1-1034557ed296" />


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

<img width="318" height="178" alt="image" src="https://github.com/user-attachments/assets/ea2c9962-5db7-4d89-8d39-68ba47d40120" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="430" height="261" alt="image" src="https://github.com/user-attachments/assets/fa9233f5-f7f7-4129-8a5e-5a6aa44d49a9" />

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

<img width="359" height="137" alt="image" src="https://github.com/user-attachments/assets/49712bb2-dbc1-4432-b9ab-597389f431f8" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="474" height="121" alt="image" src="https://github.com/user-attachments/assets/99169c0b-cd21-4b39-ad48-3ab0906afe84" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="378" height="586" alt="image" src="https://github.com/user-attachments/assets/8cd8bcae-1631-4871-92e2-e7989d8735b4" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar


## OUTPUT
<img width="619" height="589" alt="image" src="https://github.com/user-attachments/assets/db1a887e-a39f-4f72-8070-73967836b6be" />


tar -xvf backup.tar
## OUTPUT
<img width="327" height="585" alt="image" src="https://github.com/user-attachments/assets/9ea1b170-0068-45a9-9426-de44614b4452" />

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

<img width="491" height="253" alt="image" src="https://github.com/user-attachments/assets/4a66cef0-b1a8-42d2-9ba3-b876dedcfe3a" />
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="362" height="135" alt="image" src="https://github.com/user-attachments/assets/34d6a809-e040-49da-a1bb-4ebd3fb46be2" />

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

 <img width="621" height="453" alt="image" src="https://github.com/user-attachments/assets/90fbe6fa-3db5-4274-a531-7e2cc2606e23" />

ls file1
## OUTPUT
<img width="352" height="77" alt="image" src="https://github.com/user-attachments/assets/a66d3db2-b047-4adc-a0e6-58dbc6b30a3c" />

echo $?
## OUTPUT 
<img width="367" height="69" alt="image" src="https://github.com/user-attachments/assets/da09bcd1-f546-4671-a420-ae181674b9e5" />

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

<img width="381" height="278" alt="image" src="https://github.com/user-attachments/assets/f0c4a1ed-b805-4d2c-b956-2eb62679adab" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="612" height="152" alt="image" src="https://github.com/user-attachments/assets/50b79123-9df4-4ca8-9e51-f06754540da9" />


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
<img width="418" height="71" alt="image" src="https://github.com/user-attachments/assets/1148a0ce-725b-4e28-827f-d5c3bd27ef5e" />

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

<img width="422" height="80" alt="image" src="https://github.com/user-attachments/assets/8f0901bf-89b9-4438-af66-1a7b2ed73056" />


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
<img width="593" height="177" alt="image" src="https://github.com/user-attachments/assets/9829f4d1-2ebd-435e-ae06-c56478a83cf8" />

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
<img width="624" height="199" alt="image" src="https://github.com/user-attachments/assets/0a8a0a02-986d-4a73-86a6-b74aeb87f992" />

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
<img width="628" height="162" alt="image" src="https://github.com/user-attachments/assets/ba8326b1-84a5-4c6e-917d-75d60170de7f" />


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

<img width="646" height="157" alt="image" src="https://github.com/user-attachments/assets/93e3f833-4160-4b3b-915b-73df58d75913" />

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
 <img width="452" height="166" alt="image" src="https://github.com/user-attachments/assets/9c08bc7f-14dc-4ee2-b935-ba1691ce6969" />

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
 <img width="632" height="416" alt="image" src="https://github.com/user-attachments/assets/9ac52305-0556-4c1f-a5b4-5522bf7cdac3" />

 
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
 
 <img width="530" height="224" alt="image" src="https://github.com/user-attachments/assets/1b1d199d-3e72-47c7-b3cb-bf28cf913c5f" />

 
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
 
 <img width="610" height="243" alt="image" src="https://github.com/user-attachments/assets/ccbb2edc-2115-4fa8-89ca-43885a80ade0" />

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
 <img width="610" height="227" alt="image" src="https://github.com/user-attachments/assets/1bf9e85e-9d61-4173-bfe5-0ba0b378b61f" />

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
<img width="624" height="301" alt="image" src="https://github.com/user-attachments/assets/f68d8d9d-387f-4409-b253-91f5c63271bc" />

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
<img width="444" height="234" alt="image" src="https://github.com/user-attachments/assets/b7df6d3a-217d-4580-83a7-c2de45cdf412" />

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
<img width="390" height="216" alt="image" src="https://github.com/user-attachments/assets/1595c6e6-b787-47a8-b2a5-cfbd02cae535" />

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

 <img width="407" height="404" alt="image" src="https://github.com/user-attachments/assets/6ab646d0-399e-46a4-9d09-7b76fd112517" />


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
<img width="634" height="190" alt="image" src="https://github.com/user-attachments/assets/b6a0d95b-b8c5-42c5-b230-1535cb593fa3" />

 
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
 <img width="440" height="333" alt="image" src="https://github.com/user-attachments/assets/e38cb7eb-5852-45a6-837e-3a7fd791c050" />

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
<img width="456" height="165" alt="image" src="https://github.com/user-attachments/assets/abccd32f-9ed8-40c3-93c8-7c2ec8edc13e" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="676" height="140" alt="image" src="https://github.com/user-attachments/assets/505acfdb-7b5e-4db1-a9d5-7a2deecd34d7" />


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
<img width="373" height="75" alt="image" src="https://github.com/user-attachments/assets/4253c6b9-4c22-42a0-8f58-cb992c92b29d" />

 
 ./funcex.sh 1 2
<img width="352" height="75" alt="image" src="https://github.com/user-attachments/assets/12e6bb14-53a0-4c49-af23-048342690366" />

 
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
<img width="432" height="170" alt="image" src="https://github.com/user-attachments/assets/7bc7ae98-743b-47da-ae98-737cab0dc01b" />

 
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
<img width="483" height="169" alt="image" src="https://github.com/user-attachments/assets/6c000650-3312-46ec-99e0-944c74186ee9" />

 
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
 <img width="406" height="448" alt="image" src="https://github.com/user-attachments/assets/74765cd2-673c-4c26-b126-e0fd6f235045" />

 
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
 <img width="458" height="405" alt="image" src="https://github.com/user-attachments/assets/ec7a3e41-5449-4300-afba-ae777890e038" />

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
<img width="408" height="182" alt="image" src="https://github.com/user-attachments/assets/5d4c0a5c-b70a-4fc9-9df0-faad0e0e69e8" />

<img width="432" height="133" alt="image" src="https://github.com/user-attachments/assets/a4832965-67a0-4df1-9a10-00f2ef1ffa04" />

# RESULT:
The Commands are executed successfully.
