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

![Screenshot 2025-03-08 182602](https://github.com/user-attachments/assets/6e41c613-c358-4307-8e35-85348cea760a)


cat < file2
## OUTPUT

![Screenshot 2025-03-08 182616](https://github.com/user-attachments/assets/8eb8dcf7-5f98-4efc-bd7c-c3042249fe25)

# Comparing Files
cmp file1 file2
## OUTPUT

![Screenshot 2025-03-08 182628](https://github.com/user-attachments/assets/5b32c0e7-65d8-48a9-a938-f5570c3e9149)

comm file1 file2
 ## OUTPUT

![Screenshot 2025-03-08 182645](https://github.com/user-attachments/assets/6175ac6b-3a48-43ea-8ff8-4496c5bc4034)

diff file1 file2
## OUTPUT

![Screenshot 2025-03-08 182659](https://github.com/user-attachments/assets/6b578377-8493-424c-b923-5ecdb2df9d30)

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

![Screenshot 2025-03-08 183022](https://github.com/user-attachments/assets/9671d7a2-1d6e-49fe-816c-73476e818658)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot 2025-03-08 183034](https://github.com/user-attachments/assets/27ba82cf-ccf6-4d8e-a628-eb7d4dbacf83)


cut -d "|" -f 2 file22
## OUTPUT
![Screenshot 2025-03-08 183210](https://github.com/user-attachments/assets/eb608c8f-9072-44d5-ae85-4c84e0f35c6d)


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

![Screenshot 2025-03-10 080708](https://github.com/user-attachments/assets/51f57909-b8f0-4757-9f3e-d072250640f5)


grep hello newfile 
## OUTPUT

![Screenshot 2025-03-10 080715](https://github.com/user-attachments/assets/7c9890ee-f2fd-4a94-b93b-262eafe09e09)



grep -v hello newfile 
## OUTPUT

![Screenshot 2025-03-09 110719](https://github.com/user-attachments/assets/e4ff71ed-a8d7-4243-8b50-c6c9efc86ecb)


cat newfile | grep -i "hello"
## OUTPUT

![Screenshot 2025-03-09 110746](https://github.com/user-attachments/assets/f42a2131-e5b2-4453-9b29-85edfc80cfe2)



cat newfile | grep -i -c "hello"
## OUTPUT


![Screenshot 2025-03-09 110757](https://github.com/user-attachments/assets/f48fac3a-6ba4-4c4b-a599-dc355c033f61)


grep -R ubuntu /etc
## OUTPUT

![Screenshot 2025-03-09 110806](https://github.com/user-attachments/assets/77a962ab-e3dd-46f2-b851-032a2ebfaa45)


grep -w -n world newfile   
## OUTPUT
![Screenshot 2025-03-09 110820](https://github.com/user-attachments/assets/dc9f1a66-dd57-4149-b94f-2b82d4632e8e)


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

![Screenshot 2025-03-09 110833](https://github.com/user-attachments/assets/74938553-e8dc-4611-8a35-55f3f77cb94d)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot 2025-03-09 110950](https://github.com/user-attachments/assets/bba99338-c05f-47c4-9266-3f4fac7c0f3c)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![Screenshot 2025-03-09 111000](https://github.com/user-attachments/assets/5b171a40-6689-44c9-b8bd-2d46508f5df0)


egrep '(world$)' newfile 
## OUTPUT

![Screenshot 2025-03-10 081031](https://github.com/user-attachments/assets/fa252fcd-bea2-44a3-99d7-e957c9a0995e)

egrep '((W|w)orld$)' newfile 
## OUTPUT


![Screenshot 2025-03-13 092216](https://github.com/user-attachments/assets/8141aa69-b01f-4df0-a6ce-fdf644d50676)


egrep '[1-9]' newfile 
## OUTPUT



![Screenshot 2025-03-13 092526](https://github.com/user-attachments/assets/216581a0-3c06-435d-8f56-a4003164ceaf)



egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot 2025-03-13 092554](https://github.com/user-attachments/assets/890bcd0e-3a35-485c-86bd-9fcb6340d899)

egrep l{2} newfile
## OUTPUT


![Screenshot 2025-03-13 092651](https://github.com/user-attachments/assets/84c833c6-9fa4-4fff-816d-4ddd2e033e6b)

egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot 2025-03-13 092717](https://github.com/user-attachments/assets/1bbf3162-72ef-4ca5-ba96-a40ebbe84b0d)

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


![Screenshot 2025-03-13 092842](https://github.com/user-attachments/assets/612da89b-e7a6-4cfd-b4fa-d6dad771f889)

sed -n -e '$p' file23
## OUTPUT


![Screenshot 2025-03-13 093107](https://github.com/user-attachments/assets/6e5ff9ef-49dd-4de8-9783-b773da1a8a38)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![Screenshot 2025-03-13 093223](https://github.com/user-attachments/assets/ab55667b-ba21-4873-8d5e-441d5b083f14)


sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot 2025-03-13 093313](https://github.com/user-attachments/assets/3d7015c7-9c1f-42a1-a681-18e80f4320e1)


sed -n -e '1,5p' file23
## OUTPUT

![Screenshot 2025-03-13 093412](https://github.com/user-attachments/assets/6ec356d7-94af-4b60-b59d-5bed8fb080bf)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![Screenshot 2025-03-13 093503](https://github.com/user-attachments/assets/2a6c4f86-8be8-4413-9435-f8d466f2b37c)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![Screenshot 2025-03-13 093600](https://github.com/user-attachments/assets/104dc2d7-320b-460e-bd81-d67de4ab80d7)

seq 10 
## OUTPUT


![Screenshot 2025-03-13 093618](https://github.com/user-attachments/assets/43c20bad-34bd-4148-8b14-1c2a513d8f4d)

seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot 2025-03-13 093727](https://github.com/user-attachments/assets/42b6bdb2-ea69-4054-a705-6c08add7f17f)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot 2025-03-13 093752](https://github.com/user-attachments/assets/d7690ab8-b283-41d4-9cb6-e476c06c8ae3)


seq 3 | sed '2a hello'
## OUTPUT


![Screenshot 2025-03-13 093839](https://github.com/user-attachments/assets/f23d8df5-4ba8-42bd-93c4-a933ee5d1b0f)

seq 2 | sed '2i hello'
## OUTPUT

![Screenshot 2025-03-13 093903](https://github.com/user-attachments/assets/a98eb9a8-764c-4fdc-9c45-8b074f7acda8)

seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2025-03-13 093949](https://github.com/user-attachments/assets/889b8062-7323-438a-92c4-bc09b1bf24ec)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![Screenshot 2025-03-13 094028](https://github.com/user-attachments/assets/00ec909f-2a23-4434-aef3-dbefd107f742)


sed -n '2,4{s/$/*/;p}' file23

![Screenshot 2025-03-13 094133](https://github.com/user-attachments/assets/94d635ae-aa5a-47a4-a9e7-6c3cd3ca326e)

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

![Screenshot 2025-03-13 094211](https://github.com/user-attachments/assets/f63fede8-8ea2-4d08-b3aa-ddfeb5ca5430)

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

![Screenshot 2025-03-13 094341](https://github.com/user-attachments/assets/cf0d47e8-d0f4-4740-ae2e-cb72d7b61ff4)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 
![Screenshot 2025-03-13 094421](https://github.com/user-attachments/assets/9a285ebd-d68a-468a-bf3a-4fdba96107b4)

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


 ![Screenshot 2025-03-13 094622](https://github.com/user-attachments/assets/03abc72d-a8cd-42cd-b61b-504cb622f382)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![Screenshot 2025-03-13 094702](https://github.com/user-attachments/assets/02f75c14-7d44-4cf7-8678-dcd50f217361)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![Screenshot 2025-03-15 185542](https://github.com/user-attachments/assets/fa75a424-5007-43ab-ac1d-0e7667682a03)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2025-03-15 185647](https://github.com/user-attachments/assets/51b4351d-1940-49be-b9ff-8cbf32c3bddc)


tar -xvf backup.tar
## OUTPUT
![Screenshot 2025-03-15 185719](https://github.com/user-attachments/assets/91841117-f9f4-4ab2-81fb-d3df6d762738)

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
```
chmod 755 my-script.sh
./my-script.sh
```
## OUTPUT
![Screenshot 2025-03-15 092303](https://github.com/user-attachments/assets/7d105d73-0d95-450a-a634-b5db0d369c31)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![Screenshot 2025-03-15 092659](https://github.com/user-attachments/assets/f58362e3-2904-498d-92eb-13dbc14cf1d1)

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

 ![Screenshot 2025-03-15 191441](https://github.com/user-attachments/assets/748f67e8-c2af-4e76-acbf-bba6a346fa1f)

ls file1
## OUTPUT
![Screenshot 2025-03-15 094026](https://github.com/user-attachments/assets/e71a0d00-90c3-46c8-b4f7-98eafb331725)

echo $?
## OUTPUT 
![Screenshot 2025-03-15 094032](https://github.com/user-attachments/assets/2da68602-6eeb-49ed-afb0-5d177badc5d7)

./one
bash: ./one: Permission denied
 

 
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

![Screenshot 2025-03-15 193146](https://github.com/user-attachments/assets/2b465baf-ebff-44b2-afdf-fd1389223e39)

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
![Screenshot 2025-03-15 193702](https://github.com/user-attachments/assets/7bea9b90-6c55-403c-a248-1ec5a4032e21)

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


![Screenshot 2025-03-15 193947](https://github.com/user-attachments/assets/6f3340ff-7f41-4378-a485-c9983bd7d621)

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
![Screenshot 2025-03-15 194155](https://github.com/user-attachments/assets/5f755398-84c1-44b4-99a8-74adbf79cc0e)

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
![Screenshot 2025-03-15 193947](https://github.com/user-attachments/assets/e9af050d-a6b9-4c5b-8db2-db8cb33404fb)

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

![Screenshot 2025-03-15 195459](https://github.com/user-attachments/assets/7f378622-a8a9-48c5-bcf8-63d5ff296775)

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
![Screenshot 2025-03-15 195638](https://github.com/user-attachments/assets/bde9281d-73f6-4381-b35c-488cb8d1db4f)

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
 ![Screenshot 2025-03-15 195821](https://github.com/user-attachments/assets/85271ab1-51b9-4431-bb69-4890f5c3dfed)

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
 
 ![Screenshot 2025-03-15 195951](https://github.com/user-attachments/assets/a4ae99e2-aa9e-4f12-a250-806a902f41d2)

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
 
 
 ![Screenshot 2025-03-15 200147](https://github.com/user-attachments/assets/04510f2c-2810-48e5-863c-9bdf6d12f6ba)

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
 
 ![Screenshot 2025-03-15 200329](https://github.com/user-attachments/assets/bce9d444-8cb2-449f-a7f2-502c2ec812d4)


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
 ![Screenshot 2025-03-15 200509](https://github.com/user-attachments/assets/51b72a07-dbd3-465a-b99e-c1d500d93855)

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
 
![Screenshot 2025-03-15 200705](https://github.com/user-attachments/assets/e8f92813-c851-4583-bd06-9b637b5cec54)

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

![Screenshot 2025-03-15 200926](https://github.com/user-attachments/assets/b0408e2f-e7ae-4590-aafe-c891683dc63c)

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
![Screenshot 2025-03-15 201107](https://github.com/user-attachments/assets/6b539ba5-0b1d-4442-922b-6ba97b8d382f)

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
![Screenshot 2025-03-15 201233](https://github.com/user-attachments/assets/06b374dd-9982-4017-b494-cd6cd32c8f96)

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

 ![Screenshot 2025-03-15 201411](https://github.com/user-attachments/assets/930f2fa7-74cc-497c-95e0-5d1e57e44d2d)

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
 ![Screenshot 2025-03-15 204030](https://github.com/user-attachments/assets/e561a833-415f-4573-aac2-77d32d0b06bd)

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
 ![Screenshot 2025-03-15 204505](https://github.com/user-attachments/assets/805f7d2f-a3af-48fd-8bb7-e1b826a060a8)

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

![Screenshot 2025-03-15 204715](https://github.com/user-attachments/assets/0945dd8a-11d5-4623-a584-33a6bed71c39)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![Screenshot 2025-03-15 204937](https://github.com/user-attachments/assets/96e7e65e-6298-4b67-a5ed-f33d85bd3fa3)


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

 ![Screenshot 2025-03-15 205130](https://github.com/user-attachments/assets/f6c0d989-b7a2-4441-8acd-cd3e1df9a6f8)
![Screenshot 2025-03-15 205354](https://github.com/user-attachments/assets/0875f7d3-31d4-43c8-8757-bcdd7b8ad04a)

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
 ![Screenshot 2025-03-15 205317](https://github.com/user-attachments/assets/482d2fbc-f158-4de5-97f1-ea8423dbaaaa)

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
 ![Screenshot 2025-03-15 205624](https://github.com/user-attachments/assets/807df74f-88c9-4fb6-8d8e-8b6bb66fbd83)
 
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
 ![Screenshot 2025-03-15 205903](https://github.com/user-attachments/assets/78b74331-43ab-4da4-a8c9-0bdee6d9c2c8)

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
![Screenshot 2025-03-15 210048](https://github.com/user-attachments/assets/7217ac21-ddbb-4e3e-aaa8-dd0d611b7758)


# RESULT:
The Commands are executed successfully.
