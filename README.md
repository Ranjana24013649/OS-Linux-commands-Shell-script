# EX1  OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting.

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

<img width="672" height="158" alt="448914043-45f9d6ef-3d1e-4348-be3a-061f38c1dafe" src="https://github.com/user-attachments/assets/0a6d0822-2a6d-4e7e-9623-64681ce26573" />


cat < file2
## OUTPUT
 <img width="610" height="174" alt="448914031-232e347b-b4b6-400d-a05d-ab85b5e5c693" src="https://github.com/user-attachments/assets/56153610-3f6c-4a91-ad71-08340d889765" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="643" height="75" alt="448914003-88c1d3e6-0a43-482c-9ff2-5890767b8652" src="https://github.com/user-attachments/assets/f2510254-1c17-41ba-b63b-f0a3cb11bac8" />
comm file1 file2
 ## OUTPUT

<img width="698" height="223" alt="448913981-35716beb-c8d8-4d75-8d34-60d856d63f3c" src="https://github.com/user-attachments/assets/78348a95-d3e0-4ee4-91b5-98f2c3e494eb" />

diff file1 file2
## OUTPUT
<img width="676" height="283" alt="448913955-9970ea73-fc15-44a8-a969-5c2c031b8793" src="https://github.com/user-attachments/assets/0a4efa8f-a86f-413d-abfe-de8166214d41" />


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


<img width="686" height="104" alt="448913903-abb0126d-ff51-4b8d-b43b-41e34004d641" src="https://github.com/user-attachments/assets/2e6461e1-f746-41c0-adcd-be61631d16ff" />


cut -d "|" -f 1 file22
## OUTPUT
<img width="677" height="127" alt="448913876-5262fe5b-b4ec-4cea-baee-dafcd0704c3c" src="https://github.com/user-attachments/assets/7ab1a40b-4eaf-40c6-934e-c3c6e08baa68" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="718" height="134" alt="448913862-0b740037-c311-457c-81fe-1edd0162d044" src="https://github.com/user-attachments/assets/7943e54a-f308-4cb2-a0b1-e55db5c3d8e0" />


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
<img width="617" height="75" alt="448913837-34cf08a0-7db2-452b-b0ec-1390988ee03a" src="https://github.com/user-attachments/assets/5245f5ab-318d-4424-96cd-1df41be657aa" />



grep hello newfile 
## OUTPUT

<img width="782" height="81" alt="448913811-42acbfd3-c96d-4cda-9487-bf0660c9bc17" src="https://github.com/user-attachments/assets/0d0b2554-f8fa-404c-ab04-b0fa639bf07f" />



grep -v hello newfile 
## OUTPUT

<img width="612" height="74" alt="448913778-dae8694b-3ef2-488b-b1b2-cbe7c1936766" src="https://github.com/user-attachments/assets/64c07727-6a71-4b89-bbb8-15be8a3b2ce0" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="592" height="109" alt="448913759-97a911b6-45e3-4341-922b-2336fe8c0b16" src="https://github.com/user-attachments/assets/5cf0e832-5d48-4851-9384-614bdb506ac9" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="585" height="75" alt="448913737-895a2cbf-245d-4428-a18f-6f126b5e822f" src="https://github.com/user-attachments/assets/fbbcd560-42b2-427d-8347-d3221e0422ad" />



grep -R ubuntu /etc
## OUTPUT

<img width="1348" height="455" alt="448913655-7364d855-2af0-4de7-96bc-4b084822f558" src="https://github.com/user-attachments/assets/784060e5-80f8-4fde-9f6f-64760d9c0084" />


grep -w -n world newfile   
## OUTPUT

<img width="647" height="109" alt="448913634-f6effec6-f633-46f8-b1af-2d89c44c7a6e" src="https://github.com/user-attachments/assets/a944e127-e8a0-4bbb-b25f-91d9ce9d0ca3" />

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

<img width="702" height="106" alt="448913604-82f0feff-b931-465d-9103-fa674471d649" src="https://github.com/user-attachments/assets/02db67aa-499c-4f77-8e8b-cd9590a1075c" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="731" height="103" alt="448913575-c49060ad-2434-4d93-9e2f-a0f44d0c5ba3" src="https://github.com/user-attachments/assets/e55f0a58-fc8c-42cc-ac10-179399a215f5" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="612" height="107" alt="448913556-3db4ccc9-5b43-4421-b589-eeab09b55316" src="https://github.com/user-attachments/assets/07bf6e7f-20b6-4131-824d-232046416670" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="658" height="81" alt="448913518-5abaac36-2cdf-4e09-bdf0-7e1045664178" src="https://github.com/user-attachments/assets/de05226e-3a96-46f8-ba5f-59ce85b08ded" />



egrep '(world$)' newfile 
## OUTPUT
<img width="616" height="104" alt="448913497-c5a72da4-5da9-43c6-a33b-d871c98229d1" src="https://github.com/user-attachments/assets/f39d389f-55b8-44a0-a52a-5d2c9d17c4e5" />



egrep '(World$)' newfile 
## OUTPUT
<img width="616" height="104" alt="448913458-efe0a60f-a693-4bde-9a10-a5217a73aa8a" src="https://github.com/user-attachments/assets/3072d6c9-317e-410c-a6ae-7c5e7fc19226" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="612" height="77" alt="448913395-dc72ec85-f3d6-4484-a729-f3cb793c3f85" src="https://github.com/user-attachments/assets/68b47300-6bf3-4073-b336-04d7b5212538" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="612" height="77" alt="448913395-dc72ec85-f3d6-4484-a729-f3cb793c3f85" src="https://github.com/user-attachments/assets/ca5346f2-0778-4ff6-99df-f453814b89d8" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="617" height="75" alt="448913344-a3f0394b-85f0-4369-8b92-f17ebef2e839" src="https://github.com/user-attachments/assets/5b61d780-748d-445b-bbbc-9f2f360e9e11" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="617" height="75" alt="448913344-a3f0394b-85f0-4369-8b92-f17ebef2e839" src="https://github.com/user-attachments/assets/f1ec5437-bab7-4d6d-848c-09c445f690ba" />

egrep l{2} newfile
## OUTPUT

<img width="614" height="96" alt="448913323-c6742da6-503b-460e-8bb8-a8187338e936" src="https://github.com/user-attachments/assets/e89f28cf-9a71-4385-82dd-f0c3bbe0be8e" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="683" height="134" alt="448913312-6d8efd65-fe73-439a-9ef7-8db01b598303" src="https://github.com/user-attachments/assets/20688eab-d375-461c-a4ee-f2f0a9b5146f" />


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

<img width="640" height="81" alt="448913269-82b2f494-67a0-4c06-9a44-36be83fd88ca" src="https://github.com/user-attachments/assets/169037ce-208f-4ed5-a7ee-6e7883e26934" />


sed -n -e '$p' file23
## OUTPUT

<img width="646" height="71" alt="448913229-1b521880-6181-45ea-b386-07ddf3d094ec" src="https://github.com/user-attachments/assets/58cd8c83-dd5b-4146-a07b-500a4dc1ce68" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="620" height="243" alt="448913194-70cb6541-6d05-49f3-aa23-4349a0d74a35" src="https://github.com/user-attachments/assets/3acbe15d-004e-4076-925a-1e2dc518b774" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="682" height="244" alt="448913165-3d5cc653-8bb2-44bb-acbd-9f03d8dbd26f" src="https://github.com/user-attachments/assets/433808be-803b-4842-b684-ff6187cf5100" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT



sed -n -e '1,5p' file23
## OUTPUT

<img width="638" height="253" alt="448913127-7ec97fa3-94ab-4d8c-95dc-0c84a614555c" src="https://github.com/user-attachments/assets/0c940412-8d6c-4f11-a9a7-da9f15287dc9" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="657" height="130" alt="448913041-489aecf1-c7c8-42cc-9789-88b0725bfa33" src="https://github.com/user-attachments/assets/132b31d1-7c76-46d0-be05-29363dad388d" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="622" height="97" alt="448913015-bb1e1abc-cb3c-4bda-b9e3-ba476109a603" src="https://github.com/user-attachments/assets/391fade4-8a7c-4725-9b91-2412d44ddd25" />



seq 10 
## OUTPUT

<img width="762" height="300" alt="448912979-716076b0-624c-4280-aae5-fc7e7eba6516" src="https://github.com/user-attachments/assets/badd5928-fdd5-4dca-9020-53d1d7c83afd" />


seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="625" height="128" alt="448912942-7e64642c-f2b7-4d25-ba95-1fc9afb1d005" src="https://github.com/user-attachments/assets/5af6b066-8e0d-420d-8270-05504aa2168d" />


seq 3 | sed '2a hello'
## OUTPUT


<img width="627" height="151" alt="448912856-841325fe-5a3e-475e-b467-116be20ca3ef" src="https://github.com/user-attachments/assets/aaac4260-8b91-4d37-9215-39265a8ad1d1" />

seq 2 | sed '2i hello'
## OUTPUT

<img width="703" height="141" alt="448912811-7b3e6d82-e59f-49eb-9ef5-40eb79c991bf" src="https://github.com/user-attachments/assets/200a9af2-4274-4038-baad-e3cd6f923c21" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="641" height="130" alt="448912779-3db7a343-e554-44f6-a852-19448535d5e1" src="https://github.com/user-attachments/assets/6d7d002e-7d79-4813-8514-23517cce892b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="642" height="124" alt="448912731-4b741865-61b0-41fd-adef-c0c629c4719b" src="https://github.com/user-attachments/assets/8a8f6202-bb75-4a95-97f5-32a8e730bab5" />


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

<img width="701" height="174" alt="448912686-d6d3d497-329c-4e4f-b614-a2df1eaed832" src="https://github.com/user-attachments/assets/ba20f306-ff3b-4898-af34-4935db20d882" />

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

<img width="730" height="178" alt="448912655-302fe84a-9ea6-4c33-b8d1-ed3257963d63" src="https://github.com/user-attachments/assets/77466f77-bbb7-4823-ae4c-0872530407fb" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="697" height="255" alt="448912627-0d836af6-dda2-40f0-8f2d-1fa4186efe95" src="https://github.com/user-attachments/assets/73e99650-6c3a-489f-b844-24954fe3459d" />

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

<img width="636" height="129" alt="448912591-adbb939c-3dbe-4b8a-ab87-56821d64c5bc" src="https://github.com/user-attachments/assets/c1f5939e-39d5-436e-ac45-6d42a0cedc6e" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="661" height="116" alt="448912542-91827cc4-179b-4c99-a647-2dec382268cc" src="https://github.com/user-attachments/assets/7fb22fd5-81d3-42b1-8867-c958205b560b" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="869" height="509" alt="448912507-be92064c-be65-457e-97b4-f5cff5420cd7" src="https://github.com/user-attachments/assets/f94e9675-10e5-4b5d-b743-f29f322c6f24" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="869" height="509" alt="448912507-be92064c-be65-457e-97b4-f5cff5420cd7" src="https://github.com/user-attachments/assets/d251a706-b570-4458-aa6c-f111d626235c" />

tar -xvf backup.tar
## OUTPUT
<img width="751" height="496" alt="448912440-cb74dff7-2dd9-4046-8eae-bbd33b1368bb" src="https://github.com/user-attachments/assets/eeccd926-d85d-4646-a4cd-6be5cb860971" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="702" height="84" alt="448912412-31401447-2616-4c35-93ea-5105f7ae6e8d" src="https://github.com/user-attachments/assets/c9f8bc47-3f34-4433-b489-fba66e16daa5" />

gunzip backup.tar.gz
## OUTPUT
<img width="782" height="334" alt="448912380-e2068e35-52e4-48ae-937a-785b9646077a" src="https://github.com/user-attachments/assets/240eea96-0701-4445-a831-de7cb90d235f" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="681" height="156" alt="448912329-232a9582-c956-4fb1-886d-a4138e2f0c60" src="https://github.com/user-attachments/assets/8de5d33b-be3a-4eb7-b930-920d8fc2ad7f" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="681" height="156" alt="448912329-232a9582-c956-4fb1-886d-a4138e2f0c60" src="https://github.com/user-attachments/assets/8119859e-4753-4e38-9c98-3809088dab4a" />


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

 <img width="815" height="375" alt="448912285-f54387be-ae91-4091-85db-c8823549896c" src="https://github.com/user-attachments/assets/0fe20d93-0a0a-4ab9-bc98-47cf8b30ae00" />

ls file1
## OUTPUT
<img width="656" height="158" alt="448912243-346dd54e-8972-42fc-903f-8646c26c8d45" src="https://github.com/user-attachments/assets/7d1453c7-d006-46b8-bf92-46084f3a355d" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="701" height="86" alt="448912202-75a066f4-1ea8-4e42-a505-13e43a3f4342" src="https://github.com/user-attachments/assets/ccd0b533-a045-43ba-a2a7-4ff2460fa3bb" />

abcd
 
echo $?
 ## OUTPUT

<img width="762" height="82" alt="448912064-8ae83e0b-14bd-498d-8db0-307d0cce1989" src="https://github.com/user-attachments/assets/c555fab1-a219-42ff-a3ec-27f8a9cc29ed" />

 
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
## OUTPUT
<img width="800" height="277" alt="448912001-aa8e9c4d-d1cb-42c8-bbff-056290512781" src="https://github.com/user-attachments/assets/7810a850-f619-40b1-8e44-31af5956a49b" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="719" height="108" alt="448911946-451f4430-8670-4976-91bb-b536a332cdf5" src="https://github.com/user-attachments/assets/673e6617-ea15-471e-993a-71e78605a950" />


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
<img width="717" height="83" alt="448911893-f923be78-4a05-41c9-bc8f-6229c1b28552" src="https://github.com/user-attachments/assets/06e41133-8d36-4e05-b949-bd13f7525744" />

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
## OUTPUT
<img width="676" height="147" alt="448911761-3a67de23-9c27-4b6d-867e-0fd98ce5c560" src="https://github.com/user-attachments/assets/cc3d1e31-074e-43cf-8ec2-9edd02219ccc" />

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
<img width="740" height="204" alt="448911648-5b9123f1-0189-4b4c-9bd7-82033fcbd6bd" src="https://github.com/user-attachments/assets/36abfee6-3d17-4df5-800a-4268c1f48a2c" />

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

<img width="767" height="104" alt="448911414-f16ff5e6-99ec-4018-8fe5-8ce166819d22" src="https://github.com/user-attachments/assets/3edc30a5-8f6b-4a9f-ac02-532cf68c0736" />

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
<img width="707" height="94" alt="448910586-575749e2-ee0d-4f3a-a56e-bdd6c25ad47e" src="https://github.com/user-attachments/assets/66b7723a-846f-4d05-a121-b87d3e6e0f7b" />

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
<img width="707" height="94" alt="448910586-575749e2-ee0d-4f3a-a56e-bdd6c25ad47e" src="https://github.com/user-attachments/assets/eace442f-0c4e-46d5-b21a-83867c03a725" />

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
 <img width="766" height="178" alt="448909679-83030502-0f28-4513-957c-9d3303e08a6b" src="https://github.com/user-attachments/assets/5e85470d-17ae-455f-8264-3fa8c9f4227b" />

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

<img width="697" height="111" alt="448909584-a55c5e85-5f8d-41b3-adfb-a5ccd637633b" src="https://github.com/user-attachments/assets/701b1cd0-563f-4489-a515-e473753adc90" />


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
<img width="727" height="81" alt="448909529-f99fc5f1-dfcd-4eef-9881-c2cc9a4801ea" src="https://github.com/user-attachments/assets/3766ee8f-0f22-4f74-be9f-ff45f682e9a9" />

 
 ./funcex.sh 1 2
<img width="722" height="85" alt="448909546-37a05eaa-1a84-4170-a8c9-5eb9266bcf98" src="https://github.com/user-attachments/assets/b318983b-fea9-44b0-8ef9-57e9a236c880" />

 
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
<img width="809" height="132" alt="448909444-b56470ec-b074-4c9d-a105-38f83b3ff2b1" src="https://github.com/user-attachments/assets/b4529ffb-12d6-4c4b-9906-cf22b84630ca" />


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

<img width="756" height="404" alt="448909393-7923915e-ba4b-48a4-90b1-c8e1abc72972" src="https://github.com/user-attachments/assets/56bfecd0-d38e-41e9-8576-eca46414feb2" />

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
 <img width="707" height="380" alt="448909276-1ffeb4cf-82c1-48f8-bb67-65740754c4c7" src="https://github.com/user-attachments/assets/8e2ce67d-b3c0-4ce4-a561-7092bd20e560" />

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
<img width="730" height="135" alt="448909199-61385812-8e6a-4a75-ac7c-166963bd056a" src="https://github.com/user-attachments/assets/2fb84077-32ef-4da9-82f8-dc47c4eb1d3d" />


# RESULT:
The Commands are executed successfully.
