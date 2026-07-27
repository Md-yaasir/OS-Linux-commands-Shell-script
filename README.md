<img width="610" height="226" alt="image" src="https://github.com/user-attachments/assets/4847dc78-11c4-4b18-ba9e-4c1b07cd7ac5" /># OS-Linux-commands-Shell-scripting
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
<img width="508" height="152" alt="image" src="https://github.com/user-attachments/assets/56d8698c-6e1d-40b3-8122-906c32f3ce74" />



cat < file2
## OUTPUT
<img width="607" height="177" alt="image" src="https://github.com/user-attachments/assets/0bb3ca60-900f-441c-bfca-c13d8f56d102" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="562" height="72" alt="image" src="https://github.com/user-attachments/assets/600090eb-cf30-4a0a-b917-1eb6f729bbe1" />

comm file1 file2
 ## OUTPUT
<img width="602" height="222" alt="image" src="https://github.com/user-attachments/assets/1e2e4370-3c7c-419f-afa4-4f40a36edbff" />

 
diff file1 file2
## OUTPUT
<img width="705" height="275" alt="image" src="https://github.com/user-attachments/assets/37b397f3-ec0d-476a-b9c1-39e7fc9e2bad" />


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
<img width="690" height="97" alt="image" src="https://github.com/user-attachments/assets/93e93b70-bb52-482f-a5c6-18a1cee231f4" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="587" height="122" alt="image" src="https://github.com/user-attachments/assets/46db65a3-f56c-47b8-bf18-8c5e8d6b8c9a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="597" height="127" alt="image" src="https://github.com/user-attachments/assets/b8cf1f3a-31e9-4226-b806-ad57f34ae5c9" />


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
<img width="600" height="77" alt="image" src="https://github.com/user-attachments/assets/9e011e4d-6bbf-4b2a-a968-f87acafb20af" />



grep hello newfile 
## OUTPUT

<img width="562" height="72" alt="image" src="https://github.com/user-attachments/assets/c80f19ef-5e0d-44ad-a3a4-5d5786eccca5" />



grep -v hello newfile 
## OUTPUT
<img width="532" height="76" alt="image" src="https://github.com/user-attachments/assets/bf57d2e5-7593-4f65-bc1f-3523f1c38feb" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="615" height="97" alt="image" src="https://github.com/user-attachments/assets/557c6978-c635-4ad6-a8b1-1e7841e8efa7" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="581" height="72" alt="image" src="https://github.com/user-attachments/assets/a154c680-0e7b-4929-983c-a66f04f1caf8" />



grep -R ubuntu /etc
## OUTPUT

<img width="1802" height="917" alt="image" src="https://github.com/user-attachments/assets/d1193406-00c8-49e7-8243-c95a0f3d66ec" />


grep -w -n world newfile   
## OUTPUT
<img width="616" height="102" alt="image" src="https://github.com/user-attachments/assets/ca733093-6a27-45ec-97fc-d7d14cd3950d" />


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
<img width="557" height="102" alt="image" src="https://github.com/user-attachments/assets/c4d53532-7371-4d90-952d-3160d64550a0" />



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="640" height="101" alt="image" src="https://github.com/user-attachments/assets/d21433d8-d223-4309-83c4-96d5079b3a9f" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="617" height="101" alt="image" src="https://github.com/user-attachments/assets/0707380a-90d6-4741-ae75-c869cf79b559" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="616" height="75" alt="image" src="https://github.com/user-attachments/assets/26ae6cbe-aaf8-42b3-ac42-2adb09413a95" />



egrep '(World$)' newfile 
## OUTPUT
<img width="617" height="125" alt="image" src="https://github.com/user-attachments/assets/cf454288-454a-4d68-bd1e-35218115416d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="552" height="125" alt="image" src="https://github.com/user-attachments/assets/cf5a944e-6a9f-489a-9e5b-a9a390107e2f" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="576" height="77" alt="image" src="https://github.com/user-attachments/assets/ecfaa500-6bf9-439f-b72e-a8efbc97c7b3" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="617" height="102" alt="image" src="https://github.com/user-attachments/assets/8eb19462-8c44-4f2f-8c43-6c8d2586ccbc" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="595" height="52" alt="image" src="https://github.com/user-attachments/assets/a1c9a14b-13cf-4feb-ab44-33a8caaa2ac6" />


egrep l{2} newfile
## OUTPUT
<img width="605" height="102" alt="image" src="https://github.com/user-attachments/assets/4a42ea3f-1f42-4d83-aee3-7ac4ca7fb34d" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="750" height="117" alt="image" src="https://github.com/user-attachments/assets/9f071fa3-d837-4415-8ddd-0a1a3af9c82a" />


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
<img width="567" height="77" alt="image" src="https://github.com/user-attachments/assets/f6d8c501-58f1-4106-81bc-49386bd87c46" />



sed -n -e '$p' file23
## OUTPUT
<img width="502" height="75" alt="image" src="https://github.com/user-attachments/assets/bfa03655-da02-4b0d-a74a-0424c3ef00f8" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="587" height="275" alt="image" src="https://github.com/user-attachments/assets/f2cd7fc1-cc8f-473e-be97-120b4e8b90a7" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="687" height="275" alt="image" src="https://github.com/user-attachments/assets/c6b05837-53ff-4ea6-b5d2-7b9792a5c230" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="647" height="281" alt="image" src="https://github.com/user-attachments/assets/94c8026e-21c8-46f0-ade8-51f7dc21bd40" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="547" height="180" alt="image" src="https://github.com/user-attachments/assets/0e957af2-80cc-4a50-99bc-848d19dc3e16" />



sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="485" height="150" alt="image" src="https://github.com/user-attachments/assets/16419c04-1c61-4fb8-8612-2ed0a80f4bbd" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="577" height="127" alt="image" src="https://github.com/user-attachments/assets/96e962cc-a3f6-4c4c-b839-139672303a94" />


seq 10 
## OUTPUT
<img width="472" height="307" alt="image" src="https://github.com/user-attachments/assets/d4bc174f-4c04-42dc-b240-63ca20a95357" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="510" height="131" alt="image" src="https://github.com/user-attachments/assets/d6a05b32-a104-4a5b-b783-90c6e812021c" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="502" height="126" alt="image" src="https://github.com/user-attachments/assets/dc918932-14f8-48d3-85ba-632b8909b060" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="432" height="152" alt="image" src="https://github.com/user-attachments/assets/12454e5e-7f7e-4435-bb77-6abfe6b9417f" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="492" height="120" alt="image" src="https://github.com/user-attachments/assets/0c467e9b-88df-4471-9152-51b35d1b358f" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="557" height="122" alt="image" src="https://github.com/user-attachments/assets/df8d4ac5-c1b6-4e04-836b-1d4299920ac5" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="511" height="126" alt="image" src="https://github.com/user-attachments/assets/02f50998-91fa-41a8-9b86-580208084a78" />


sed -n '2,4{s/$/*/;p}' file23

## OUTPUT
<img width="562" height="121" alt="image" src="https://github.com/user-attachments/assets/80759cbf-9dfd-42b7-94c5-4c3d918e1890" />



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


<img width="485" height="172" alt="image" src="https://github.com/user-attachments/assets/8e4b01a3-4356-45bc-b48b-d123b236353b" />

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

<img width="502" height="172" alt="image" src="https://github.com/user-attachments/assets/d57c7222-ced0-4c39-819a-9f89887de3c7" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="621" height="272" alt="image" src="https://github.com/user-attachments/assets/e61854ad-548b-4afd-a1dc-2b187e736a29" />

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
<img width="660" height="120" alt="image" src="https://github.com/user-attachments/assets/126a6671-bdba-40f8-b7a1-b6e5155082c9" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="652" height="127" alt="image" src="https://github.com/user-attachments/assets/dc91851f-5737-4771-b89e-946c9d9be134" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1667" height="921" alt="image" src="https://github.com/user-attachments/assets/3abcc162-66eb-47b9-9de8-f71e6ce60b84" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1807" height="922" alt="image" src="https://github.com/user-attachments/assets/cc4b47c4-781f-45d0-9380-56fdbf4cea12" />


tar -xvf backup.tar
## OUTPUT
<img width="1702" height="922" alt="image" src="https://github.com/user-attachments/assets/6b95a680-ca1a-4956-9b9f-6ba59f9583a3" />

gzip backup.tar

ls *.gz
## OUTPUT
 <img width="567" height="75" alt="image" src="https://github.com/user-attachments/assets/8ccb1a7b-6b73-42ac-ae15-396266c60e9f" />

gunzip backup.tar.gz
## OUTPUT
<img width="1901" height="132" alt="image" src="https://github.com/user-attachments/assets/59c845e8-db91-4d5b-864f-da5792d99e73" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="775" height="276" alt="image" src="https://github.com/user-attachments/assets/3bc676a4-888b-447e-9273-d036c06286c7" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="556" height="122" alt="image" src="https://github.com/user-attachments/assets/d588e84f-d21f-48f0-8ceb-b9591f34e671" />


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
<img width="1246" height="847" alt="image" src="https://github.com/user-attachments/assets/3dcd9fad-aed5-4f31-a089-77efe5df96f2" />

 
ls file1
## OUTPUT
<img width="630" height="82" alt="image" src="https://github.com/user-attachments/assets/a2a3aa62-bb90-4c2b-81fa-cbf0d4914005" />

echo $?
## OUTPUT 
<img width="602" height="80" alt="image" src="https://github.com/user-attachments/assets/2e5d1081-9fca-461a-bdcf-d85f4dc98521" />
 
 
abcd
 
echo $?
 ## OUTPUT
<img width="607" height="147" alt="image" src="https://github.com/user-attachments/assets/6879b9d5-14dc-4191-a3c2-6434e53e25c6" />


 
# mis-using string comparisons

cat > strcomp.sh 
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
## OUTPUT
<img width="771" height="282" alt="image" src="https://github.com/user-attachments/assets/2faee552-e396-49a8-86e2-25d0e829ecfe" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="767" height="150" alt="image" src="https://github.com/user-attachments/assets/329f0efb-87b9-414e-a98b-41e56b7f74a0" />


# check file ownership
cat > psswdperm.sh 
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
<img width="817" height="301" alt="image" src="https://github.com/user-attachments/assets/db569b96-a639-4e51-92f4-7dc6863ebfd8" />

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

<img width="685" height="82" alt="image" src="https://github.com/user-attachments/assets/9065fec9-9307-4022-981c-ea2e9bfdd736" />


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
## OUTPUT


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
## OUTPUT
<img width="802" height="200" alt="image" src="https://github.com/user-attachments/assets/bc808167-af58-4d5e-b2da-3c49d2381dde" />

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
<img width="667" height="152" alt="image" src="https://github.com/user-attachments/assets/8b8e7974-093f-4bc9-bc31-260410b3ca5d" />


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
<img width="871" height="151" alt="image" src="https://github.com/user-attachments/assets/caf63214-b719-4f0e-a65a-6bddde511cb3" />

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

 <img width="692" height="447" alt="image" src="https://github.com/user-attachments/assets/3a848362-795b-4288-a391-5b52545fcab9" />

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
 <img width="652" height="355" alt="image" src="https://github.com/user-attachments/assets/52332925-8065-44b1-af56-0d5fd72b2fc4" />


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
 ## OUTPUT 
 <img width="677" height="221" alt="image" src="https://github.com/user-attachments/assets/08234b79-8a7a-4bfd-9bbf-a56ed005f0b3" />

 
 
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
 ## OUTPUT
<img width="712" height="302" alt="image" src="https://github.com/user-attachments/assets/96209f70-8b10-4171-be35-8769d6826f43" />

 
 
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
 ## OUTPUT
<img width="771" height="227" alt="image" src="https://github.com/user-attachments/assets/987be83b-d0f1-4b74-a6a3-e0a17786fe0c" />


 
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
 ## OUTPUT

<img width="732" height="300" alt="image" src="https://github.com/user-attachments/assets/bbf9348e-8999-492f-9ace-bb788f38cbd7" />

 

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
<img width="662" height="347" alt="image" src="https://github.com/user-attachments/assets/46390442-8f5f-4619-92a9-11c7d7efd11d" />


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
<img width="610" height="226" alt="image" src="https://github.com/user-attachments/assets/2a56b83c-6a00-4ccb-a02d-9ef5ccca5d5f" />


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
$ ./forctype.sh 
## OUTPUT
<img width="612" height="177" alt="image" src="https://github.com/user-attachments/assets/040b9a85-4c66-4f0a-a55b-0528d6fa4391" />

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
<img width="721" height="350" alt="image" src="https://github.com/user-attachments/assets/bd793d15-3819-41ac-9c2c-022c7267937b" />

 
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


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ## OUTPUT

 <img width="736" height="170" alt="image" src="https://github.com/user-attachments/assets/6a69d241-67c2-4f7a-bc73-3fc3824b8a21" />

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

 
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

 
 
 
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
<img width="772" height="102" alt="image" src="https://github.com/user-attachments/assets/31856dc4-28ae-49e7-952c-155310f6c876" />







 
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

chmod 755 funcex.sh
## OUTPUT
<img width="512" height="127" alt="image" src="https://github.com/user-attachments/assets/9fe90fd1-cc58-401e-bd92-37eb71b596ab" />

 
cat argshift.sh
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
<img width="437" height="222" alt="image" src="https://github.com/user-attachments/assets/027368f4-f353-4bcf-91eb-b552503579a2" />


 
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
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="501" height="180" alt="image" src="https://github.com/user-attachments/assets/6c041a4c-1edc-4bfe-b676-19c2613df477" />


 

 
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
 <img width="605" height="377" alt="image" src="https://github.com/user-attachments/assets/c6cc8065-f725-4e31-9d9c-cbc49d83044e" />

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
<img width="971" height="782" alt="image" src="https://github.com/user-attachments/assets/ab1f6ffb-5a7c-42d2-9c5f-fe1cdc73e0a9" />


# RESULT:
The Commands are executed successfully.
