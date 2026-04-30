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
<img width="206" height="150" alt="Screenshot 2026-04-29 224455" src="https://github.com/user-attachments/assets/4ee5aab1-7ea0-4d71-8b30-920c991f5f26" />
cat < file2
## OUTPUT
<img width="366" height="173" alt="Screenshot 2026-04-29 224832" src="https://github.com/user-attachments/assets/fc9ab946-23e5-4fe7-9949-42686ff5d418" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="342" height="82" alt="Screenshot 2026-04-25 145028" src="https://github.com/user-attachments/assets/1008051b-ec96-4bef-b054-d5244ea44517" />
comm file1 file2
 ## OUTPUT
<img width="259" height="165" alt="Screenshot 2026-04-26 224734" src="https://github.com/user-attachments/assets/0414277e-e471-4e02-b08e-256722e6e1a6" /> 
diff file1 file2
## OUTPUT
<img width="263" height="213" alt="Screenshot 2026-04-26 224745" src="https://github.com/user-attachments/assets/e06e1011-21c2-4e9d-998b-88246cd1e275" />
#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="187" height="86" alt="Screenshot 2026-04-26 224807" src="https://github.com/user-attachments/assets/ab60b332-4807-48f0-9b22-3d41f82e36a0" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="260" height="103" alt="Screenshot 2026-04-26 224813" src="https://github.com/user-attachments/assets/af835063-302b-41f6-94e4-c754707b2013" />


cut -c1-3 file11
## OUTPUT
<img width="233" height="79" alt="Screenshot 2026-04-26 224819" src="https://github.com/user-attachments/assets/59694506-6091-46c2-90a0-501eae6154f2" />

cut -d "|" -f 1 file22
## OUTPUT


cut -d "|" -f 2 file22
## OUTPUT
<img width="240" height="95" alt="Screenshot 2026-04-26 224823" src="https://github.com/user-attachments/assets/9998c870-4bd3-4c0a-8bca-4e79efc6d1ae" />

cat < newfile 
```
Hello world
hello world
^d
````
<img width="239" height="96" alt="Screenshot 2026-04-29 222735" src="https://github.com/user-attachments/assets/c44bb410-0446-4bf8-93d5-53d3a4c1ed4c" />

cat > newfile 
Hello world
hello world
 <img width="370" height="117" alt="Screenshot 2026-04-26 224902" src="https://github.com/user-attachments/assets/0088895d-d608-495d-8e2d-6fd91a6867e5" />

grep Hello newfile 
## OUTPUT



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT
<img width="342" height="77" alt="Screenshot 2026-04-29 222754" src="https://github.com/user-attachments/assets/77069d9c-3cc9-40f4-b635-47a6004aac9d" />

cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
<img width="283" height="73" alt="Screenshot 2026-04-26 224840" src="https://github.com/user-attachments/assets/becc395e-ca08-4f28-98b7-6b770fcf456e" />

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
<img width="307" height="58" alt="Screenshot 2026-04-26 224909" src="https://github.com/user-attachments/assets/e7de2f6c-c231-4a18-9922-32af75384cf9" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="326" height="84" alt="Screenshot 2026-04-26 224913" src="https://github.com/user-attachments/assets/04d0cb5d-19bb-4a4a-9a6a-f40319a5fdd3" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="326" height="84" alt="Screenshot 2026-04-26 224913" src="https://github.com/user-attachments/assets/36f8aae5-be55-4c2d-91cd-63f6bd4219cc" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="295" height="57" alt="Screenshot 2026-04-26 224919" src="https://github.com/user-attachments/assets/45f68ea8-f91c-48ce-9104-00ad4c35208e" />

egrep '(world$)' newfile 
## OUTPUT
<img width="307" height="94" alt="Screenshot 2026-04-26 224926" src="https://github.com/user-attachments/assets/d2eee10a-c359-48b6-b0bc-1ddef9185d01" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="265" height="72" alt="Screenshot 2026-04-28 222744" src="https://github.com/user-attachments/assets/47223edc-6a8e-4835-a795-ab9f9a4e790f" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="902" height="168" alt="Screenshot 2026-04-29 222710" src="https://github.com/user-attachments/assets/8fdb0780-bde7-4ca0-b8a1-466fff72b9fd" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="873" height="218" alt="Screenshot 2026-04-29 222716" src="https://github.com/user-attachments/assets/b22b5f79-a71d-457a-af42-403a89542ee0" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="873" height="218" alt="Screenshot 2026-04-29 222716" src="https://github.com/user-attachments/assets/4e733847-c419-4dc2-9272-5f4956ffd07f" />

egrep l{2} newfile
## OUTPUT
<img width="278" height="118" alt="Screenshot 2026-04-29 222815" src="https://github.com/user-attachments/assets/05a75bb9-9bd0-4fa8-9401-d45e12b01faa" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="469" height="109" alt="Screenshot 2026-04-29 222820" src="https://github.com/user-attachments/assets/2d5798f2-7d28-4f17-b71d-7b5289859acd" />

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
<img width="358" height="70" alt="Screenshot 2026-04-29 222836" src="https://github.com/user-attachments/assets/10ba4ad3-fef5-49a4-b051-2d5c1f67d0b2" />

sed -n -e '$p' file23
## OUTPUT



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="463" height="249" alt="Screenshot 2026-04-26 224105" src="https://github.com/user-attachments/assets/b2ac0051-a2c1-41c9-accd-0a016d43cd41" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="414" height="241" alt="Screenshot 2026-04-26 224201" src="https://github.com/user-attachments/assets/2c34c525-d03c-40bd-94e3-bd61b0fcec70" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="439" height="248" alt="Screenshot 2026-04-26 224249" src="https://github.com/user-attachments/assets/bf5ae526-0d6e-4c2a-8bb0-dcfb6add9805" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="369" height="174" alt="Screenshot 2026-04-26 224424" src="https://github.com/user-attachments/assets/fdca12ea-04e4-4856-b9a2-8774daee8263" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="373" height="124" alt="Screenshot 2026-04-26 224434" src="https://github.com/user-attachments/assets/551e6b05-f467-4934-850d-d28808e97c0c" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="426" height="102" alt="Screenshot 2026-04-26 224520" src="https://github.com/user-attachments/assets/6e82a310-ea7f-48d5-a5e3-ee933a51255b" />

seq 10 
## OUTPUT
<img width="359" height="305" alt="Screenshot 2026-04-26 225005" src="https://github.com/user-attachments/assets/07c3a998-3a22-4e17-a39e-1100839bc8aa" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="346" height="121" alt="Screenshot 2026-04-26 225140" src="https://github.com/user-attachments/assets/92c4752f-8cb6-4365-a794-80cf13b494c7" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="341" height="129" alt="Screenshot 2026-04-26 225154" src="https://github.com/user-attachments/assets/ff7eb601-7399-4225-8bb8-839063214993" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="324" height="151" alt="Screenshot 2026-04-26 225159" src="https://github.com/user-attachments/assets/b3594763-8c74-45fd-bb00-b568e82e49a2" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="319" height="128" alt="Screenshot 2026-04-26 225337" src="https://github.com/user-attachments/assets/beaeb664-ba61-4014-b830-9dddcfe2d680" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="413" height="128" alt="Screenshot 2026-04-26 225344" src="https://github.com/user-attachments/assets/e96e6a9b-8ff3-4fa5-aba2-9a3379eb5d38" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="391" height="129" alt="Screenshot 2026-04-26 225412" src="https://github.com/user-attachments/assets/735c0ecf-8ce7-4d61-8172-acd166f31393" />
sed -n '2,4{s/$/*/;p}' file23
<img width="382" height="129" alt="Screenshot 2026-04-26 225417" src="https://github.com/user-attachments/assets/1ae06c24-0b9c-47e3-8533-c44d6aacc067" />

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
<img width="325" height="174" alt="Screenshot 2026-04-26 225753" src="https://github.com/user-attachments/assets/2cdfa012-dd69-4fbf-a23e-cbfdadcc405e" />
cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="329" height="211" alt="Screenshot 2026-04-26 230203" src="https://github.com/user-attachments/assets/da3464e9-bd4b-44cc-8f2f-1a95e884b987" />
 
uniq file22
## OUTPUT



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="509" height="261" alt="Screenshot 2026-04-26 230210" src="https://github.com/user-attachments/assets/7795284b-26a4-4c5f-8ea9-19f76b73a1ce" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
<img width="279" height="127" alt="Screenshot 2026-04-26 230447" src="https://github.com/user-attachments/assets/66f80263-b85d-4543-86f3-857f2bdd7fdf" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
<img width="374" height="137" alt="Screenshot 2026-04-26 230452" src="https://github.com/user-attachments/assets/f3560b92-a971-4c2d-8f38-652f3cbf1088" />

cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="448" height="127" alt="Screenshot 2026-04-26 230537" src="https://github.com/user-attachments/assets/4e13cdb6-1ff9-4e05-aadf-902a063db84a" />
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="448" height="127" alt="Screenshot 2026-04-26 230537" src="https://github.com/user-attachments/assets/daf7d8d9-06af-41e4-bab3-928ad07d943e" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="595" height="599" alt="Screenshot 2026-04-30 204407" src="https://github.com/user-attachments/assets/49e472f3-3e66-4f32-a3d3-892153d6de71" />
mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="642" height="556" alt="Screenshot 2026-04-30 204351" src="https://github.com/user-attachments/assets/e246e2fe-4db4-40f3-a613-e8df1c4c66e8" />

tar -xvf backup.tar
## OUTPUT
<img width="365" height="505" alt="Screenshot 2026-04-30 204455" src="https://github.com/user-attachments/assets/e1c3d80c-a319-49fe-a533-a1b91d826471" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="405" height="77" alt="Screenshot 2026-04-30 204610" src="https://github.com/user-attachments/assets/74b1f435-39f7-4b98-a477-112374a7e4d1" />

gunzip backup.tar.gz
## OUTPUT
<img width="394" height="46" alt="Screenshot 2026-04-30 204619" src="https://github.com/user-attachments/assets/ff5ab818-b6fd-4724-ad54-02ad42962117" />
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="482" height="178" alt="Screenshot 2026-04-30 205051" src="https://github.com/user-attachments/assets/a6e7727c-71b5-444b-a5ad-7f396b4baba4" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="391" height="277" alt="Screenshot 2026-04-28 221315" src="https://github.com/user-attachments/assets/073a47e2-b4be-4ec0-b65f-01f5a3f295e9" />

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
<img width="361" height="353" alt="Screenshot 2026-04-28 222436" src="https://github.com/user-attachments/assets/d75237f7-6fef-4695-aa92-8f7dd1d2f00d" />

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
<img width="628" height="202" alt="Screenshot 2026-04-28 222658" src="https://github.com/user-attachments/assets/e6ca37cf-fbb7-454f-8a38-e8ccd7f7b301" />

 
ls file1
## OUTPUT
<img width="482" height="149" alt="Screenshot 2026-04-28 222851" src="https://github.com/user-attachments/assets/3601988c-44cb-4457-9846-33c9a1eb997d" />

echo $?
## OUTPUT 
<img width="252" height="78" alt="Screenshot 2026-04-26 230609" src="https://github.com/user-attachments/assets/7c7e2ff7-99ef-4958-b664-c1e08b42af33" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="265" height="72" alt="Screenshot 2026-04-28 222744" src="https://github.com/user-attachments/assets/6b01b394-9ed9-4056-91b8-f520d22a6595" />

abcd
 
echo $?
 ## OUTPUT
<img width="252" height="78" alt="Screenshot 2026-04-26 230609" src="https://github.com/user-attachments/assets/fa211861-2f61-46b5-9a04-2451a6ed233e" />

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
<img width="396" height="273" alt="Screenshot 2026-04-28 221306" src="https://github.com/user-attachments/assets/df7a4c1d-69e4-4557-ba1d-56cf844800cf" />

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

<img width="396" height="273" alt="Screenshot 2026-04-28 221306" src="https://github.com/user-attachments/assets/59fdf17d-73e2-4ff9-be73-e0a26689f923" />
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="653" height="146" alt="Screenshot 2026-04-28 223155" src="https://github.com/user-attachments/assets/0d352025-ca0b-4900-aebd-f5170d921cb0" />

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
<img width="614" height="197" alt="Screenshot 2026-04-28 223447" src="https://github.com/user-attachments/assets/7186f765-8b0a-4006-a418-7ad868a2d00f" />

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
<img width="440" height="82" alt="Screenshot 2026-04-28 223455" src="https://github.com/user-attachments/assets/64750dd4-2214-4939-b86d-e45896afe29c" />

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
<img width="464" height="448" alt="Screenshot 2026-04-28 223921" src="https://github.com/user-attachments/assets/a9d4585a-9fa0-4fc0-841a-aa10eee6d3f2" />

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
<img width="514" height="81" alt="Screenshot 2026-04-28 224013" src="https://github.com/user-attachments/assets/0ac577b3-ec4c-42f2-8a66-b8ab167ed22b" />

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

<img width="495" height="368" alt="Screenshot 2026-04-28 224258" src="https://github.com/user-attachments/assets/02f63866-dc4f-447b-a062-07151f900523" />

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

<img width="600" height="125" alt="image" src="https://github.com/user-attachments/assets/a5c32dbf-8ed0-4186-bc96-335df90b2f0f" />

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

<img width="464" height="448" alt="Screenshot 2026-04-28 223921" src="https://github.com/user-attachments/assets/70a52de9-dc2a-42d2-9972-90db8a53219c" />

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT

<img width="495" height="368" alt="Screenshot 2026-04-28 224258" src="https://github.com/user-attachments/assets/8e0e23ce-1ead-4c1f-b8ce-dbba1b7d1036" />

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

<img width="584" height="528" alt="Screenshot 2026-04-30 211724" src="https://github.com/user-attachments/assets/0f3b6b35-f8af-4d55-b5f5-7e27f4960ed0" />

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

<img width="501" height="76" alt="image" src="https://github.com/user-attachments/assets/5574f8ab-1f24-4f67-b3b0-5db180d5867f" />

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

<img width="498" height="224" alt="image" src="https://github.com/user-attachments/assets/2a60bfc7-5387-4c34-b9dd-10b7fd668a70" />

$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT

<img width="452" height="78" alt="image" src="https://github.com/user-attachments/assets/22688a8c-7604-4703-b1a4-7cfcd555b6fc" />

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

<img width="400" height="212" alt="image" src="https://github.com/user-attachments/assets/27eb9ecb-25c9-43d0-b3ea-f8440b79fb46" />

$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 

 <img width="516" height="89" alt="image" src="https://github.com/user-attachments/assets/b58bf9a3-bca0-48da-b869-2a58003f099b" />

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
<img width="452" height="473" alt="Screenshot 2026-04-29 225400" src="https://github.com/user-attachments/assets/57e3c1c9-ad85-4f28-a1f6-c6cdeb741062" />

# RESULT:
The Commands are executed successfully.
