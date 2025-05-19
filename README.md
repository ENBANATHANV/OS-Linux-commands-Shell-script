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
![Catfile1](https://github.com/user-attachments/assets/db07a5cf-7263-4b16-bb70-a9711211a74b)



cat < file2
## OUTPUT
![catfile2](https://github.com/user-attachments/assets/15cafd0b-62b2-425e-979d-9979723b7386)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![img3](https://github.com/user-attachments/assets/15d8c948-d580-4494-82d1-b5acb0cbdf1e)

comm file1 file2
 ## OUTPUT
![img4](https://github.com/user-attachments/assets/39eefd67-9f5e-4c5a-92d8-4981297b93b2)


 
diff file1 file2
## OUTPUT
![img5](https://github.com/user-attachments/assets/8ae76a50-c442-4d41-8d3a-d3f2fdad5be9)


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
![img6](https://github.com/user-attachments/assets/b99637d5-13b5-4325-9795-311e49a4805d)




cut -d "|" -f 1 file22
## OUTPUT
![img7](https://github.com/user-attachments/assets/3f55b8f4-e800-4617-b74e-9172c027ac25)



cut -d "|" -f 2 file22
## OUTPUT
![img8](https://github.com/user-attachments/assets/b0fa51b7-46ef-4bde-8d0a-d5971ef0daf8)


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
![img9](https://github.com/user-attachments/assets/ed292555-c4cb-4e90-a2e2-9ea01ac6d6c7)



grep hello newfile 
## OUTPUT
![img10](https://github.com/user-attachments/assets/e012630f-4f37-4c9d-b643-81bad077ef09)




grep -v hello newfile 
## OUTPUT
![img11](https://github.com/user-attachments/assets/bb9496d6-584d-4c56-a645-6bb6113563e1)



cat newfile | grep -i "hello"
## OUTPUT
![img12](https://github.com/user-attachments/assets/8b86fac3-b617-4c81-adfe-30fa1b573764)




cat newfile | grep -i -c "hello"
## OUTPUT
![img13](https://github.com/user-attachments/assets/f337fc11-53bc-4d4c-ad1f-573bd9583c16)




grep -R ubuntu /etc
## OUTPUT
![img14](https://github.com/user-attachments/assets/b040c025-3bae-490e-b93f-1529f41ab740)



grep -w -n world newfile   
## OUTPUT
![img15](https://github.com/user-attachments/assets/963c7343-5050-4842-99c6-c21723d89eaf)


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
![img16](https://github.com/user-attachments/assets/8ea8496a-399f-4b59-a146-35596cbfa122)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![img17](https://github.com/user-attachments/assets/8f460d04-1514-43b9-b222-ed2aa91d79d1)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![img18](https://github.com/user-attachments/assets/f6c5a756-7d9c-467a-b89f-bcedea5eca5f)




egrep '(^hello)' newfile 
## OUTPUT
![img19](https://github.com/user-attachments/assets/cb228678-86b9-4eb4-b326-97ebc52c36ee)



egrep '(world$)' newfile 
## OUTPUT
![img20](https://github.com/user-attachments/assets/9554ea22-92a0-4f57-a17a-cba8cb600cb8)



egrep '(World$)' newfile 
## OUTPUT
![img21](https://github.com/user-attachments/assets/5b0b9076-da38-480a-9512-b36d9a85900c)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![img22](https://github.com/user-attachments/assets/6945942d-eb0f-4604-bcb5-46222c58b169)



egrep '[1-9]' newfile 
## OUTPUT
![img23](https://github.com/user-attachments/assets/fce7594b-83cb-44f8-902f-898a4d2da07f)



egrep 'Linux.*world' newfile 
## OUTPUT
![img24](https://github.com/user-attachments/assets/2748f5c3-39a3-4c4b-b019-3431cc532354)


egrep 'Linux.*World' newfile 
## OUTPUT
![img25](https://github.com/user-attachments/assets/0c332810-a1db-4043-a917-1e22cd2281a4)


egrep l{2} newfile
## OUTPUT
![img26](https://github.com/user-attachments/assets/0ba97f6c-bdec-48c3-8088-07e2db126735)



egrep 's{1,2}' newfile
## OUTPUT 
![img27](https://github.com/user-attachments/assets/47ca2064-a3c2-49cf-822d-235b7d7a0603)


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
![img28](https://github.com/user-attachments/assets/c6fc6345-f074-429f-8045-7b1bc3436125)



sed -n -e '$p' file23
## OUTPUT
![img29](https://github.com/user-attachments/assets/71c42494-020c-4f77-b923-ef70d4c06fb7)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![img30](https://github.com/user-attachments/assets/40622a03-f317-4220-8732-d461c5e52a50)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![img31](https://github.com/user-attachments/assets/00063a5d-83a9-4408-b5cb-305bebeeafd6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![img32](https://github.com/user-attachments/assets/1b9eb576-fc49-4f9d-ae82-5e69e72234ce)



sed -n -e '1,5p' file23
## OUTPUT
![img33](https://github.com/user-attachments/assets/b1749d24-6b05-4ed2-a7b6-f0315682b812)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![img34](https://github.com/user-attachments/assets/aeaa4ea8-c679-4741-9e8e-e78550e89d95)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![img35](https://github.com/user-attachments/assets/ac734285-3dac-4bd6-b441-17eb61e3a493)



seq 10 
## OUTPUT
![img36](https://github.com/user-attachments/assets/725d0f96-8c4c-4e35-b381-49847dbcca20)



seq 10 | sed -n '4,6p'
## OUTPUT
![img37](https://github.com/user-attachments/assets/75601a2e-edc1-41a6-a09e-58ac896e986f)



seq 10 | sed -n '2,~4p'
## OUTPUT
![img38](https://github.com/user-attachments/assets/89a6df18-6e01-4b9d-9b20-ebcd7ff257a3)



seq 3 | sed '2a hello'
## OUTPUT
![img39](https://github.com/user-attachments/assets/86b19626-8fbc-4a4d-bad8-4e609b729ed2)




seq 2 | sed '2i hello'
## OUTPUT
![img40](https://github.com/user-attachments/assets/c95e9f2b-f41f-47b5-812f-6b0dd07fc545)


seq 10 | sed '2,9c hello'
## OUTPUT
![img41](https://github.com/user-attachments/assets/1c3d6a50-f777-4b7d-ac45-5c7b7de14b53)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![img42](https://github.com/user-attachments/assets/b997077b-5a8a-40b7-9fab-77e89fde7719)



sed -n '2,4{s/$/*/;p}' file23
![img43](https://github.com/user-attachments/assets/788261d1-70c1-46a3-bd66-0ce92febcac1)


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
![img44](https://github.com/user-attachments/assets/7efc1f61-2830-4dfa-b671-f3afa1c06b62)


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
![img45](https://github.com/user-attachments/assets/615b17fb-ce7f-4f9d-981b-264eb041b80a)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![img46](https://github.com/user-attachments/assets/900d766f-486c-407e-85b9-249329f4feb7)

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
![img47](https://github.com/user-attachments/assets/f48350e6-4f17-4177-8f53-26f93a60bbee)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![img48](https://github.com/user-attachments/assets/424b87b5-67a8-4f4a-a26f-3f6dac1d4f90)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![img49](https://github.com/user-attachments/assets/948af6d6-c3ae-4dda-b7bd-90db5fe86c2e)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![img50](https://github.com/user-attachments/assets/eb9a93c0-3f9a-4dd7-b9cd-1ff7479bc7f9)


tar -xvf backup.tar
## OUTPUT
![img51](https://github.com/user-attachments/assets/7a6ffbbc-73f8-4073-9e65-5220a9fade9f)

gzip backup.tar

ls .gz
## OUTPUT
 ![img52](https://github.com/user-attachments/assets/655df45c-02af-49ef-9e16-8026f4a635b3)

gunzip backup.tar.gz
## OUTPUT
![img53](https://github.com/user-attachments/assets/eb6be429-9b7e-47bc-b010-4458b502e70e)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![img54](https://github.com/user-attachments/assets/b038171a-4eee-4571-b3b4-7589fdebf01f)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![img55](https://github.com/user-attachments/assets/c307c74b-7b07-4bd8-9186-87b188a2018e)


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
![img56](https://github.com/user-attachments/assets/08479870-29d9-427e-9466-fe15c3831617)

 
ls file1
## OUTPUT
![img57](https://github.com/user-attachments/assets/8c39c41a-31e2-41e6-b271-1c91c9b1d33c)

echo $?
## OUTPUT 
![img58](https://github.com/user-attachments/assets/570f61fa-a9c4-405f-a850-89b43168ec14)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![img59](https://github.com/user-attachments/assets/c60be8d2-972a-499c-adcf-804e9d7113f7)

abcd
 
echo $?
 ## OUTPUT
![img59](https://github.com/user-attachments/assets/c09c4b79-cb67-42b7-b348-78465d4e331c)


 
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
![img60](https://github.com/user-attachments/assets/20bf9ee2-292e-4ab7-b6f3-5e0b6c49e72e)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![img61](https://github.com/user-attachments/assets/af41e2dd-5552-41e4-8d54-3d4882c71665)


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
![img62](https://github.com/user-attachments/assets/439237ae-fcea-454e-971f-00c11f74c9de)

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
![img63](https://github.com/user-attachments/assets/cb919f68-96ab-4003-a490-b3fe4fcca3a8)



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
![img64](https://github.com/user-attachments/assets/1114f8e0-a72d-41dc-851e-4a96cc9c9f18)

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
![img65](https://github.com/user-attachments/assets/cd7bb42a-1a43-4932-aad0-2c81114612db)

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
![img66](https://github.com/user-attachments/assets/73ff8ca3-415b-4b78-9183-fec7cea28261)


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
![img67](https://github.com/user-attachments/assets/b4153723-4f02-456a-bfec-25ed27c931dc)

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
![img69](https://github.com/user-attachments/assets/e5c39c11-509d-4eae-9a3c-061f759a6cf6)

 
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
 ![img70](https://github.com/user-attachments/assets/322aadf3-0cd6-4092-a3fa-340f947b1b48)

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
./forin1.sh
![img71](https://github.com/user-attachments/assets/ac89d79b-a52f-429f-abad-ff0f59f8d242)


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
 ![img72](https://github.com/user-attachments/assets/f151626a-21a6-4be3-9735-948f4c6e98e9)

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
 ![img73](https://github.com/user-attachments/assets/d59f5419-2994-4c19-8a34-803cede6aff8)

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
![img74](https://github.com/user-attachments/assets/8a16644d-16df-43d1-b698-3c467ef86125)

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
![img75](https://github.com/user-attachments/assets/b9152006-eec8-4416-a9fc-47fea2e4785e)


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
![img76](https://github.com/user-attachments/assets/d9b9d08e-c73f-4737-bc7a-eb2ecaf7636b)

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
![img77](https://github.com/user-attachments/assets/ac8be574-0fea-4622-8e2c-04d7232558cd)

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
![img78](https://github.com/user-attachments/assets/d098f723-e70f-4911-9a52-639275e5151b)

 
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
![img79](https://github.com/user-attachments/assets/364d94d6-964a-43bf-af61-2cc54e921d0a)


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
 ![img80](https://github.com/user-attachments/assets/924a8b5f-5313-41a1-b9d2-56ca45e40704)

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
![img81](https://github.com/user-attachments/assets/50a5b02a-e87e-478f-97c5-d97f579ec365)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
![img81](https://github.com/user-attachments/assets/fcda7074-7a2c-4261-8b2b-f59e1f82c8ea)





 
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
![img82](https://github.com/user-attachments/assets/04a5e60d-3cc8-4e66-955e-76ec27461880)

 
 ./funcex.sh 1 2
![img83](https://github.com/user-attachments/assets/007a5d36-511a-4449-9e00-fea5f0d087d8)

 
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
 ![img84](https://github.com/user-attachments/assets/ff625016-6af9-4c22-88a1-83febd15143d)

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
 ![img85](https://github.com/user-attachments/assets/9508dd02-4333-4f4c-acc3-6afeb4bf66da)


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
 ![img86](https://github.com/user-attachments/assets/598b83b2-4cc4-41e6-82ad-aca5557822c2)

 
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
 ![img87](https://github.com/user-attachments/assets/f975e55f-3a10-4700-ac14-98897b409918)

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
![img88](https://github.com/user-attachments/assets/58aa066c-d10f-4bdf-ba2b-95d7172a5fe0)


# RESULT:
The Commands are executed successfully.
