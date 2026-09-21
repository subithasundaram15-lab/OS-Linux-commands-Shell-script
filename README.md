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

<img width="422" height="181" alt="image" src="https://github.com/user-attachments/assets/e1e2c245-e1e8-42e3-a503-9057beb77236" />

cat < file2
## OUTPUT

<img width="382" height="197" alt="image" src="https://github.com/user-attachments/assets/84741db9-b60b-454b-bd46-dbc8d8741de2" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="426" height="95" alt="image" src="https://github.com/user-attachments/assets/16d714c4-6d64-4457-b056-7b2813a10efc" />
 
comm file1 file2
 ## OUTPUT

<img width="550" height="292" alt="image" src="https://github.com/user-attachments/assets/e05c11c7-7acd-4469-abe1-a4e4d7463f51" />

 
diff file1 file2
## OUTPUT


<img width="455" height="317" alt="image" src="https://github.com/user-attachments/assets/cd85fb9a-7f13-4a83-9365-0e15eb60c4a3" />

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


<img width="415" height="92" alt="image" src="https://github.com/user-attachments/assets/c0dfc7ef-f4d9-4606-9a5c-4f74eb7e1d98" />


cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT


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

<img width="437" height="112" alt="image" src="https://github.com/user-attachments/assets/46956b82-e2c3-4a58-b49f-23f1f791fe5a" />


grep hello newfile 
## OUTPUT


<img width="277" height="137" alt="image" src="https://github.com/user-attachments/assets/ba998876-6cbf-4f84-8c93-b72153968fe0" />


grep -v hello newfile 
## OUTPUT

<img width="362" height="77" alt="image" src="https://github.com/user-attachments/assets/4262a347-af77-4164-9df8-07135ca46dab" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="502" height="171" alt="image" src="https://github.com/user-attachments/assets/b17cc5a4-deb7-43e2-8bea-afa1d88123f5" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="476" height="81" alt="image" src="https://github.com/user-attachments/assets/b6a07385-8f89-46f8-842d-f2c02b54cc11" />



grep -R ubuntu /etc
## OUTPUT

<img width="801" height="557" alt="image" src="https://github.com/user-attachments/assets/79da9f47-1e0c-4eda-b715-1e20bb9ff7a6" />



grep -w -n world newfile   
## OUTPUT
<img width="422" height="132" alt="image" src="https://github.com/user-attachments/assets/ee248e41-fec1-4e8a-bd1b-2dbd4ce396d0" />


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

<img width="502" height="347" alt="image" src="https://github.com/user-attachments/assets/8272718d-b922-4b7e-8a7e-c129ad02e5d9" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="451" height="131" alt="image" src="https://github.com/user-attachments/assets/1a649ea6-ad75-4236-b1cf-de6d1d1ff79d" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="616" height="152" alt="image" src="https://github.com/user-attachments/assets/84723266-8622-47df-aaa0-2f0675fa57fb" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="446" height="81" alt="image" src="https://github.com/user-attachments/assets/1dbdfbe8-0ade-4135-a54d-6794a4223ad6" />


egrep '(world$)' newfile 
## OUTPUT

<img width="452" height="110" alt="image" src="https://github.com/user-attachments/assets/9997d02a-9fc4-4b1e-91f7-60ed99006249" />


egrep '(World$)' newfile 
## OUTPUT

<img width="481" height="80" alt="image" src="https://github.com/user-attachments/assets/8f9155ba-113a-46b5-80a9-bb1a16ccf298" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="502" height="137" alt="image" src="https://github.com/user-attachments/assets/937ceeb2-1b52-4db1-a55b-8fa2e617ad8c" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="511" height="82" alt="image" src="https://github.com/user-attachments/assets/e9b6295a-6fba-44be-be8e-4d8837861bee" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="502" height="76" alt="image" src="https://github.com/user-attachments/assets/7612e4c6-8669-4c39-8c8f-b8271331ba2a" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="477" height="106" alt="image" src="https://github.com/user-attachments/assets/2a4ce2fa-b8b3-484b-8c90-ff530237bb8a" />

egrep l{2} newfile
## OUTPUT

<img width="477" height="106" alt="image" src="https://github.com/user-attachments/assets/54cc42ac-8216-4b3f-9759-b89d1dd5520a" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="455" height="122" alt="image" src="https://github.com/user-attachments/assets/46d57bf9-035b-481b-b5f8-399bbab20613" />

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

<img width="447" height="86" alt="image" src="https://github.com/user-attachments/assets/64729683-ed6c-4119-8722-7645d8fb3c90" />


sed -n -e '$p' file23
## OUTPUT

<img width="505" height="82" alt="image" src="https://github.com/user-attachments/assets/89f8d73f-9942-4e27-ac58-cccda2e975a4" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="505" height="82" alt="image" src="https://github.com/user-attachments/assets/0a61d9f8-4d19-4a60-a72f-0aecceec312e" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="527" height="252" alt="image" src="https://github.com/user-attachments/assets/883da5a7-d63a-4565-b246-eec73d35af22" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="602" height="257" alt="image" src="https://github.com/user-attachments/assets/37c402e1-f924-4c10-856b-6429f50b03b4" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="476" height="185" alt="image" src="https://github.com/user-attachments/assets/0690bf93-541c-4df9-9e7e-3bf77b148bdd" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="500" height="132" alt="image" src="https://github.com/user-attachments/assets/203a6af0-6cdf-443a-a6ca-ac9f81fe5509" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="486" height="107" alt="image" src="https://github.com/user-attachments/assets/3a2ff15a-136a-490b-bfa2-4985c7e9e6df" />


seq 10 
## OUTPUT

<img width="467" height="302" alt="image" src="https://github.com/user-attachments/assets/298772f2-5649-40a1-876a-e55f7097bb83" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="422" height="127" alt="image" src="https://github.com/user-attachments/assets/9dbb12d9-fb6d-4557-80ab-506648211abc" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="425" height="125" alt="image" src="https://github.com/user-attachments/assets/869a0602-0b28-4cf0-9ee1-3dab667ed270" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="517" height="155" alt="image" src="https://github.com/user-attachments/assets/334a150a-9014-4449-8231-674c663b3899" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="452" height="125" alt="image" src="https://github.com/user-attachments/assets/5c6c6250-f06e-4755-b0f7-0c45eda2a8dd" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="472" height="127" alt="image" src="https://github.com/user-attachments/assets/ef132e26-c980-43db-8656-571cffda12a1" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="505" height="136" alt="image" src="https://github.com/user-attachments/assets/f8bf79c6-e663-4281-a236-ef197f576451" />


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

<img width="542" height="357" alt="image" src="https://github.com/user-attachments/assets/e2ab6427-f5d9-4f38-974b-fb0c8bb0cd28" />


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

<img width="677" height="375" alt="image" src="https://github.com/user-attachments/assets/88ca1815-ac70-4701-9a06-5d804e88eb33" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="532" height="252" alt="image" src="https://github.com/user-attachments/assets/29b6fba9-62ef-4768-a441-5fa427e848be" />

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

<img width="477" height="256" alt="image" src="https://github.com/user-attachments/assets/1cabb92e-f5f1-464c-869e-550cdcfdd730" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="491" height="130" alt="image" src="https://github.com/user-attachments/assets/8d95f6b4-1794-4663-870a-f3b887685258" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="491" height="130" alt="image" src="https://github.com/user-attachments/assets/7f014dec-4ef0-4ffe-936d-8beba22831c0" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="670" height="702" alt="image" src="https://github.com/user-attachments/assets/f35fa7e7-fd72-45d9-925f-d338fea8dd6a" />


tar -xvf backup.tar
## OUTPUT

<img width="807" height="702" alt="image" src="https://github.com/user-attachments/assets/daf516ff-d24c-4f45-8e41-59baf18eca10" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="547" height="122" alt="image" src="https://github.com/user-attachments/assets/8bcf7323-0f45-465f-a003-ca46139b0abf" />


gunzip backup.tar.gz
## OUTPUT

 <img width="547" height="122" alt="image" src="https://github.com/user-attachments/assets/0aec7a13-a135-4bad-8c65-42eb27947dc2" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="516" height="227" alt="image" src="https://github.com/user-attachments/assets/37ba1438-7896-4942-8b70-843582619969" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="452" height="272" alt="image" src="https://github.com/user-attachments/assets/7dd04f74-4130-4650-8cbd-cabaae2be40d" />


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

 <img width="707" height="347" alt="image" src="https://github.com/user-attachments/assets/e7f2e022-0e07-43e2-a2e6-84712f174d41" />

ls file1
## OUTPUT

<img width="293" height="74" alt="image" src="https://github.com/user-attachments/assets/89ac4e1a-f783-47df-825e-be52c9930f13" />

echo $?
## OUTPUT 

<img width="377" height="75" alt="image" src="https://github.com/user-attachments/assets/ccf41494-fb96-45db-af3c-f1d8194769e8" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 <img width="367" height="80" alt="image" src="https://github.com/user-attachments/assets/4c1f1fb2-9cb0-4273-9773-5a7479ca7b9d" />

abcd
 
echo $?
 ## OUTPUT

<img width="367" height="80" alt="image" src="https://github.com/user-attachments/assets/96960f73-ffa4-41c8-843d-9bb992585308" />

 
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

<img width="827" height="281" alt="image" src="https://github.com/user-attachments/assets/0c635497-3c0f-46f6-a86a-f216dda84fc5" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="677" height="156" alt="image" src="https://github.com/user-attachments/assets/55ad124f-3cfd-41de-91a3-0a7e55ab128d" />


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

<img width="750" height="237" alt="image" src="https://github.com/user-attachments/assets/254f5a2d-c967-47c3-9d44-da3121cd2435" />


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

<img width="657" height="475" alt="image" src="https://github.com/user-attachments/assets/9d004456-4fa8-4e62-93e6-114a686f10e9" />


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

<img width="613" height="166" alt="image" src="https://github.com/user-attachments/assets/d0002f1a-9b55-48b8-9c51-ce47221f263f" />

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

<img width="791" height="200" alt="image" src="https://github.com/user-attachments/assets/a2c26a01-c1db-4204-b4ec-c1138d129851" />

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

<img width="782" height="167" alt="image" src="https://github.com/user-attachments/assets/96fb362d-c02b-404f-982b-e838abfa3d65" />

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

<img width="587" height="137" alt="image" src="https://github.com/user-attachments/assets/a0eb6222-fc06-4fca-8089-0eba30e3b1d0" />

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

<img width="517" height="257" alt="image" src="https://github.com/user-attachments/assets/9a8657f4-310f-44f1-a2e3-5c3e9f34fd54" />

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

<img width="600" height="230" alt="image" src="https://github.com/user-attachments/assets/dc80fb9f-5268-48cd-a39b-67a0e4cef6df" />

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

 <img width="441" height="230" alt="image" src="https://github.com/user-attachments/assets/ca60a09b-e7fe-484a-85c1-f56331148120" />

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

<img width="517" height="402" alt="image" src="https://github.com/user-attachments/assets/df88afc3-5f1f-4555-b663-89bb4484f264" />

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

<img width="532" height="197" alt="image" src="https://github.com/user-attachments/assets/73589110-fa8d-4ea9-8408-5338f46a0457" />
 
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

<img width="600" height="155" alt="image" src="https://github.com/user-attachments/assets/82f01480-7fe2-4527-a89f-4cad19dd693a" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="407" height="127" alt="image" src="https://github.com/user-attachments/assets/7a40e0b9-9454-42b3-95b8-2af0599ed394" />


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

<img width="502" height="210" alt="image" src="https://github.com/user-attachments/assets/bb9f7492-ee58-4629-99b7-aa26ba3a63b9" />

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

<img width="309" height="127" alt="image" src="https://github.com/user-attachments/assets/8b99ba39-2afd-4c89-8531-1525a7f2e3d6" />

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

<img width="309" height="127" alt="image" src="https://github.com/user-attachments/assets/33ff9458-675c-4a52-be4c-f3be33c16471" />

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

<img width="665" height="462" alt="image" src="https://github.com/user-attachments/assets/26324649-63da-469c-a659-0b02db783ca0" />

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

<img width="472" height="381" alt="image" src="https://github.com/user-attachments/assets/ace23bdc-90e6-4a75-8909-4cdc6c515589" />
 
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

<img width="590" height="185" alt="image" src="https://github.com/user-attachments/assets/2b2485cb-87cd-4444-bf30-42b94e954758" />

# RESULT:
The Commands are executed successfully.
