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

<img width="414" height="120" alt="image" src="https://github.com/user-attachments/assets/eb8af2bb-c94d-4c8b-b5fd-51f165b64c45" />


cat < file2
## OUTPUT

<img width="421" height="134" alt="Screenshot from 2025-09-14 17-35-10" src="https://github.com/user-attachments/assets/0b87178e-a4fa-4661-9eea-9b69e7558e98" />

# Comparing Files
cmp file1 file2
## OUTPUT

 <img width="397" height="70" alt="Screenshot from 2025-09-14 17-37-32" src="https://github.com/user-attachments/assets/4b9e8ee7-e569-494c-89e1-0c961f3142a2" />

comm file1 file2
 ## OUTPUT

<img width="400" height="179" alt="Screenshot from 2025-09-14 17-39-15" src="https://github.com/user-attachments/assets/ef25d147-1126-4140-adcd-9a89559805b3" />

 
diff file1 file2
## OUTPUT

<img width="401" height="209" alt="Screenshot from 2025-09-14 17-40-35" src="https://github.com/user-attachments/assets/db1de250-2f21-4da9-94c3-d859858a05c5" />


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

<img width="362" height="101" alt="Screenshot from 2025-09-14 17-46-22" src="https://github.com/user-attachments/assets/1e4882a2-0fce-47a1-a071-df20114bc6bb" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="407" height="98" alt="Screenshot from 2025-09-14 17-53-01" src="https://github.com/user-attachments/assets/e9baea97-6fcd-409d-8c85-a5fe02e0cef4" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="433" height="117" alt="Screenshot from 2025-09-14 17-54-34" src="https://github.com/user-attachments/assets/593caf84-eb6f-4651-b114-6afa88d689e9" />


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

<img width="424" height="68" alt="Screenshot from 2025-09-14 17-59-48" src="https://github.com/user-attachments/assets/1584e1db-a175-427b-a9d6-9744c60b9e3c" />



<img width="424" height="68" alt="Screenshot from 2025-09-14 17-59-48" src="https://github.com/user-attachments/assets/5cc5b062-b486-4b75-85a6-63b1339f10d0" />

## OUTPUT

<img width="424" height="68" alt="Screenshot from 2025-09-14 18-00-51" src="https://github.com/user-attachments/assets/8f376229-dca4-4bd6-9d0b-ff0fd2bb2fd4" />



grep -v hello newfile 
## OUTPUT

<img width="424" height="68" alt="Screenshot from 2025-09-14 18-01-53" src="https://github.com/user-attachments/assets/b6c4c052-bc82-439d-98c4-ae3d51147a38" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="482" height="78" alt="Screenshot from 2025-09-14 18-03-00" src="https://github.com/user-attachments/assets/f819cac3-2078-49d6-9efc-e8dd5cb6ab45" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="507" height="80" alt="Screenshot from 2025-09-14 18-03-41" src="https://github.com/user-attachments/assets/2fb04eba-53e0-40f7-be74-fee4e5aa86d6" />



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

<img width="507" height="80" alt="Screenshot from 2025-09-14 18-06-30" src="https://github.com/user-attachments/assets/f92409e6-b49a-48bd-aef3-a4234e2ed633" />


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

<img width="515" height="68" alt="Screenshot from 2025-09-14 18-10-31" src="https://github.com/user-attachments/assets/3c9a0d90-aa67-47de-ae97-f4c56998d0f7" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="516" height="79" alt="Screenshot from 2025-09-14 18-11-11" src="https://github.com/user-attachments/assets/f6c30c3c-6354-493c-8e0c-c468dd1adab6" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="585" height="84" alt="Screenshot from 2025-09-14 18-12-08" src="https://github.com/user-attachments/assets/79bdbc9e-6645-406d-af17-749ec9f6d683" />



egrep '(^hello)' newfile 
## OUTPUT



egrep '(world$)' newfile 
## OUTPUT

<img width="583" height="46" alt="Screenshot from 2025-09-14 18-12-51" src="https://github.com/user-attachments/assets/2b66996e-a51f-481e-b981-ef5271407c53" />


egrep '(World$)' newfile 
## OUTPUT

<img width="595" height="65" alt="Screenshot from 2025-09-14 18-13-59" src="https://github.com/user-attachments/assets/331df05e-5bcd-402d-90da-237eca598124" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="602" height="98" alt="Screenshot from 2025-09-14 18-14-55" src="https://github.com/user-attachments/assets/08ccb819-5ae7-4e0c-a761-664e04b8b0ea" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="604" height="64" alt="Screenshot from 2025-09-14 18-15-34" src="https://github.com/user-attachments/assets/61283b69-85af-4e96-afc0-b2b9fedd278a" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="604" height="64" alt="Screenshot from 2025-09-14 18-16-06" src="https://github.com/user-attachments/assets/46b9829d-7701-404b-b7d3-c741cd3426e1" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="604" height="64" alt="Screenshot from 2025-09-14 18-17-00" src="https://github.com/user-attachments/assets/e063829a-5e22-4fa6-8274-7c553afa88ae" />


egrep l{2} newfile
## OUTPUT

<img width="604" height="78" alt="Screenshot from 2025-09-14 18-17-36" src="https://github.com/user-attachments/assets/4933ebe1-b82c-40c1-8435-e2d049fbaa48" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="615" height="103" alt="Screenshot from 2025-09-14 18-18-25" src="https://github.com/user-attachments/assets/bed213a0-c185-4a52-a309-5c1a5846e374" />


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

<img width="622" height="61" alt="Screenshot from 2025-09-14 18-19-38" src="https://github.com/user-attachments/assets/4693e3a6-06f9-4cc8-bf64-77e94027a018" />


sed -n -e '$p' file23
## OUTPUT

<img width="622" height="61" alt="Screenshot from 2025-09-14 18-20-12" src="https://github.com/user-attachments/assets/130a5336-445a-4e88-95b3-63f5905037e7" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="620" height="186" alt="Screenshot from 2025-09-14 18-20-41" src="https://github.com/user-attachments/assets/94e2fae3-9bfc-45d8-89eb-bc0b186c09e4" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="620" height="186" alt="Screenshot from 2025-09-14 18-21-27" src="https://github.com/user-attachments/assets/d9d23265-94e9-4b07-93b7-6e4ad0718d50" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="620" height="186" alt="Screenshot from 2025-09-14 18-25-49" src="https://github.com/user-attachments/assets/cb7a649c-8c43-46ad-ac2d-79d9bee9a98b" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="630" height="135" alt="Screenshot from 2025-09-14 18-26-20" src="https://github.com/user-attachments/assets/38767d56-141e-4e54-b326-a00c87c0ff91" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="634" height="101" alt="Screenshot from 2025-09-14 18-26-53" src="https://github.com/user-attachments/assets/46963d9f-1f95-4b5e-b115-b10dc9933c87" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="507" height="82" alt="Screenshot from 2025-09-14 18-27-26" src="https://github.com/user-attachments/assets/0564b8de-af90-48d1-b6f4-60b543f570d3" />


seq 10

## OUTPUT

<img width="510" height="223" alt="Screenshot from 2025-09-14 18-27-57" src="https://github.com/user-attachments/assets/a965cc13-2f3a-46b5-bde6-a901a588dcee" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="543" height="101" alt="Screenshot from 2025-09-14 18-28-43" src="https://github.com/user-attachments/assets/43518ce0-3df2-4923-bde6-8ab9c9d8513f" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="543" height="101" alt="Screenshot from 2025-09-14 18-29-17" src="https://github.com/user-attachments/assets/b3a1fa69-a800-483c-b671-909daf00d82e" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="548" height="117" alt="Screenshot from 2025-09-14 18-29-51" src="https://github.com/user-attachments/assets/bf7b6559-90f7-4968-a0a7-2bfc71aa92fd" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="547" height="101" alt="Screenshot from 2025-09-14 18-30-18" src="https://github.com/user-attachments/assets/bc807319-687f-4667-b173-1f0da83e5365" />


seq 10 | sed '2,9c hello'

## OUTPUT

<img width="547" height="101" alt="Screenshot from 2025-09-14 18-30-46" src="https://github.com/user-attachments/assets/6cabc45a-e407-4f02-bda1-dd23305eb7d0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="547" height="101" alt="Screenshot from 2025-09-14 18-31-40" src="https://github.com/user-attachments/assets/d8de691b-42b0-4c1c-88db-0419509c2de3" />


sed -n '2,4{s/$/*/;p}' file23

<img width="547" height="101" alt="Screenshot from 2025-09-14 18-32-19" src="https://github.com/user-attachments/assets/629ff931-505a-4724-9eb1-dc19a144b3b7" />


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

<img width="549" height="131" alt="Screenshot from 2025-09-14 18-33-14" src="https://github.com/user-attachments/assets/84cf90f3-d554-4e7d-919b-3d0b5626697f" />


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

<img width="549" height="131" alt="Screenshot from 2025-09-14 18-34-11" src="https://github.com/user-attachments/assets/ab51f290-d9b8-49e1-aa6b-0424c948661d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="562" height="191" alt="Screenshot from 2025-09-14 18-34-51" src="https://github.com/user-attachments/assets/ccae0008-daf4-4823-9775-d424c5ccd795" />


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

<img width="568" height="98" alt="Screenshot from 2025-09-14 18-36-44" src="https://github.com/user-attachments/assets/4f6a644b-6baa-4938-ba53-02eefe4b6761" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="568" height="98" alt="Screenshot from 2025-09-14 18-37-24" src="https://github.com/user-attachments/assets/43d7b9e4-d25e-4533-8a17-5f25454fcefe" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="579" height="1086" alt="Screenshot from 2025-09-14 18-40-28" src="https://github.com/user-attachments/assets/bb6df3b8-23b3-4571-b475-78cae89d1ab8" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1003" height="1083" alt="Screenshot from 2025-09-14 18-43-31" src="https://github.com/user-attachments/assets/2b7d0946-07d1-488b-872d-8cc73fe90eab" />


tar -xvf backup.tar
## OUTPUT

<img width="1003" height="1083" alt="Screenshot from 2025-09-14 18-44-29" src="https://github.com/user-attachments/assets/b05d9d8d-9bf2-4d06-9353-509d7f654d6b" />

gzip backup.tar

ls .gz
## OUTPUT

<img width="376" height="81" alt="Screenshot from 2025-09-14 18-50-12" src="https://github.com/user-attachments/assets/3e7edbef-f4e4-4f5d-a283-c72720eddf71" />

 
gunzip backup.tar.gz
## OUTPUT

<img width="1675" height="183" alt="Screenshot from 2025-09-14 18-51-25" src="https://github.com/user-attachments/assets/f618dbab-9d72-4d40-80b2-82fb8de92994" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="464" height="147" alt="Screenshot from 2025-09-14 18-59-14" src="https://github.com/user-attachments/assets/16369228-5545-45fe-9f33-f3ae5c233327" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="509" height="201" alt="Screenshot from 2025-09-14 19-00-42" src="https://github.com/user-attachments/assets/faffb69d-0d87-4d7b-92c2-e8d848200c4a" />


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

<img width="569" height="525" alt="Screenshot from 2025-09-14 19-03-00" src="https://github.com/user-attachments/assets/21079288-2d8b-493b-89b7-39c6b62b70c4" />

 
ls file1
## OUTPUT

<img width="637" height="57" alt="Screenshot from 2025-09-14 19-03-36" src="https://github.com/user-attachments/assets/f1200ba2-cc72-4a2b-bed8-6228e9240f69" />


echo $?
## OUTPUT 
./onebash: ./one: Permission denied

<img width="637" height="57" alt="Screenshot from 2025-09-14 19-04-05" src="https://github.com/user-attachments/assets/ac0c8eb6-e78b-4817-bad8-52401111192a" />

 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

<img width="622" height="167" alt="Screenshot from 2025-09-14 19-06-10" src="https://github.com/user-attachments/assets/36347540-b729-44e3-ada6-4ef80b38a7cd" />


 
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

<img width="401" height="378" alt="Screenshot from 2025-09-14 19-08-42" src="https://github.com/user-attachments/assets/fe5827d5-edd9-4c06-8317-ed3e03ead4a1" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="558" height="87" alt="Screenshot from 2025-09-14 19-09-43" src="https://github.com/user-attachments/assets/69c3f692-9319-41b3-bc4f-2cad77968b6b" />


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

<img width="619" height="345" alt="Screenshot from 2025-09-14 19-15-14" src="https://github.com/user-attachments/assets/5aae3597-2417-48f1-be75-b081a7bbbb47" />


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

<img width="574" height="755" alt="Screenshot from 2025-09-14 20-20-42" src="https://github.com/user-attachments/assets/8e911d95-fb79-4e48-94a7-b728649d2360" />


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

<img width="545" height="615" alt="Screenshot from 2025-09-14 20-40-04" src="https://github.com/user-attachments/assets/9983ad70-2239-4fc8-8da7-a2aa29c9f4f3" />


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

<img width="574" height="755" alt="Screenshot from 2025-09-14 20-20-42" src="https://github.com/user-attachments/assets/4d673f4b-1c9a-4dab-935f-2131f1056e55" />


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

<img width="640" height="436" alt="Screenshot from 2025-09-14 20-29-50" src="https://github.com/user-attachments/assets/bf6a015b-50fc-4bba-9867-ac8d295cc00b" />


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

<img width="686" height="237" alt="Screenshot from 2025-09-14 20-31-05" src="https://github.com/user-attachments/assets/8a944391-33bf-4f6c-b558-08f2dfad01a0" />


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
##OUTPUT

<img width="686" height="286" alt="Screenshot from 2025-09-14 20-32-09" src="https://github.com/user-attachments/assets/c38d3c56-959b-4bf8-adeb-95f7289aef67" />


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
 ##OUTPUT

<img width="615" height="633" alt="Screenshot from 2025-09-14 20-44-26" src="https://github.com/user-attachments/assets/55c7d7eb-2a6c-4c42-89a3-1283c7ee8bf2" />
 
 
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
##OUTPUT

<img width="528" height="332" alt="Screenshot from 2025-09-14 20-46-33" src="https://github.com/user-attachments/assets/2e366c09-15c2-40ac-a83c-a428d88cc9d0" />
 
 
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
##OUTPUT

<img width="592" height="401" alt="Screenshot from 2025-09-14 20-48-28" src="https://github.com/user-attachments/assets/907503dc-679d-42f5-ac94-79f82e71a511" />

 
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
##OUTPUT

<img width="600" height="273" alt="Screenshot from 2025-09-14 20-50-50" src="https://github.com/user-attachments/assets/02f5def3-14bc-4cea-bc5e-8474e05cd9c3" />

 
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
##OUTPUT

<img width="645" height="271" alt="Screenshot from 2025-09-14 20-52-19" src="https://github.com/user-attachments/assets/9b1b33b4-e666-4241-88a1-42e13d5e2b08" />

 
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
##OUTPUT

<img width="663" height="364" alt="Screenshot from 2025-09-14 20-53-34" src="https://github.com/user-attachments/assets/9a240e75-2582-48f3-89ac-c5297178113d" />

 
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

<img width="663" height="291" alt="Screenshot from 2025-09-14 20-57-30" src="https://github.com/user-attachments/assets/50df415b-f5bd-4096-8b3a-7db0f8c24800" />


cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in 'cat $file'
do
echo "Visit beautiful $file"
done
```
$ chmod 777 forinfile.sh
##OUTPUT

<img width="655" height="220" alt="Screenshot from 2025-09-14 21-00-37" src="https://github.com/user-attachments/assets/ad15f960-1362-4d6f-95be-b1d310b4382f" />


$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT

<img width="645" height="362" alt="Screenshot from 2025-09-14 21-02-10" src="https://github.com/user-attachments/assets/c8bde26c-9000-42c2-a225-34946ea1e536" />


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

<img width="626" height="270" alt="Screenshot from 2025-09-14 21-03-03" src="https://github.com/user-attachments/assets/88e1c326-4f29-4f42-b4e4-c0adbd662a61" />


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

<img width="626" height="270" alt="Screenshot from 2025-09-14 21-04-12" src="https://github.com/user-attachments/assets/d81c8d8c-342a-45b8-97ea-d448c2b9c39b" />


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

<img width="444" height="469" alt="Screenshot from 2025-09-14 21-05-44" src="https://github.com/user-attachments/assets/e4d47126-e0d2-4131-8126-e510732e1b21" />

 
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
echo "The for loop is completed
```
$ chmod 755 forbreak.sh
$ ./forbreak.sh 
## OUTPUT


<img width="444" height="326" alt="Screenshot from 2025-09-14 21-08-18" src="https://github.com/user-attachments/assets/c6b115d3-c525-459c-851e-a5cb6d0f02c4" />

 
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

<img width="612" height="403" alt="Screenshot from 2025-09-14 21-11-06" src="https://github.com/user-attachments/assets/d360bf44-5fa4-4e60-90d8-32c392d0141b" />

 
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

<img width="609" height="206" alt="Screenshot from 2025-09-14 21-12-35" src="https://github.com/user-attachments/assets/e91dc024-162d-4512-a0b6-781c6de62a78" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="609" height="206" alt="Screenshot from 2025-09-14 21-15-30" src="https://github.com/user-attachments/assets/5b11e40d-88f0-4eb2-9f1f-b413e0dc27d4" />


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

<img width="607" height="312" alt="Screenshot from 2025-09-14 21-16-59" src="https://github.com/user-attachments/assets/db2414c7-ffdd-4395-aeb3-59342b42252f" />

 
 ./funcex.sh 1 2
## OUTPUT

<img width="612" height="70" alt="Screenshot from 2025-09-14 21-17-27" src="https://github.com/user-attachments/assets/d4b7b96c-9244-47cf-b434-5d0aded473bd" />

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

$ ./arghift.sh
 
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

 ./argshift.sh 1 2 3
 ## OUTPUT

<img width="604" height="597" alt="Screenshot from 2025-09-14 21-22-58" src="https://github.com/user-attachments/assets/ab62a2c2-57d9-4325-85a9-4efb0eafb23a" />

 
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

<img width="493" height="437" alt="Screenshot from 2025-09-14 21-33-26" src="https://github.com/user-attachments/assets/70393de7-4778-4919-8cb9-d144a3ad62c2" />

 
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

<img width="785" height="597" alt="Screenshot from 2025-09-14 21-32-17" src="https://github.com/user-attachments/assets/d6b07ca9-3953-4947-891e-408d3c606f51" />



# RESULT:
The Commands are executed successfully.
