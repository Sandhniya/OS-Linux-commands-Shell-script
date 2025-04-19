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

![image](https://github.com/user-attachments/assets/39ad314f-5d9e-4676-bf21-98fc9bc60a5e)


cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/7772ffcb-094a-436e-8a10-54cd0bdebbe4)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/663e3bac-11df-4370-992d-68b499c2fcf7)
 
comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/8588974b-bcc5-45dc-b882-c2af280b6e0e)

 
diff file1 file2
## OUTPUT

![image](https://github.com/user-attachments/assets/0b8efc5b-7d65-41c9-a549-c9271b849798)

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

![image](https://github.com/user-attachments/assets/10b6451e-eb4f-44b6-a53c-d935791b917f)



cut -d "|" -f 1 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/c1a5ecab-a9a4-4051-be7c-be9e4702a971)


cut -d "|" -f 2 file22
## OUTPUT

![image](https://github.com/user-attachments/assets/bf8f94bf-2ef8-4a2b-9ce1-f1b3a6e27721)

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

![image](https://github.com/user-attachments/assets/2bcc9df9-cdd9-4ca2-98ea-5cb35b06ffbe)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/9ff83404-2f76-414c-9ee0-1f90f4e1af81)



grep -v hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f5f4385e-8475-49a3-bbcf-75307fcce872)


cat newfile | grep -i "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/9526acc7-ee9a-4325-9d61-cd8e00ff5a91)



cat newfile | grep -i -c "hello"
## OUTPUT

![image](https://github.com/user-attachments/assets/b8f8be6a-10dc-4570-b0fd-8257cfdcb49c)



grep -R ubuntu /etc
## OUTPUT

![image](https://github.com/user-attachments/assets/2e92ca4b-3d96-4029-b4b0-83c01149cb7b)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/ec1e40eb-67d5-4401-8a32-c2a14f4d48e1)


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

![image](https://github.com/user-attachments/assets/a52839be-034c-412d-b3eb-8da8bc398bdf)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/0db16c9c-5d6c-4a29-b770-ad010a38ad73)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/56b445a6-ee16-4b61-8662-337bb3d86bc3)



egrep '(^hello)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/53b1e784-126d-4660-8413-60c7581d7e64)


egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/f4342687-3ec6-4c06-a9e8-5bcc99fc000f)


egrep '(World$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/384c5856-6987-467e-8aa0-6bf1b616dc12)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/21371475-5a7e-4a39-b860-11214e3588da)


egrep '[1-9]' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/2ab75d95-149a-4868-aa8e-dad09c349615)


egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d85395a5-09f7-4b31-bdeb-87f7af28ced1)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/059d3d57-66e2-4f03-a01b-e85fd525cbff)


egrep l{2} newfile
## OUTPUT

![image](https://github.com/user-attachments/assets/20127b96-2b29-49ba-bada-c5d37752a9c8)


egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/99de69d9-dcf9-4cfa-b28a-80a8ce739bf4)


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

![image](https://github.com/user-attachments/assets/391c7693-e04c-47aa-ac06-4ca0d8935897)


sed -n -e '$p' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/c29cf8b4-590f-4913-924d-755b138c03f2)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/9eee032a-d12c-43d0-867d-148a33fbf464)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/3e3df33a-ff62-4681-8abd-af38674b176c)


sed  '/tom/s/5000/6000/' file23
## OUTPUT



![image](https://github.com/user-attachments/assets/5a3bfc55-62b1-4a08-a495-50db4b31fe38)


sed -n -e '1,5p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/c1b14608-7d4a-49eb-9855-80f371add5f6)


sed -n -e '2,/Joe/p' file23
## OUTPUT



![image](https://github.com/user-attachments/assets/b2637750-0ef5-4b30-8dd5-93ab0d910e41)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/5b294141-a19d-4aaa-a2ac-3ebf0d903dd3)


seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT


![image](https://github.com/user-attachments/assets/803000e7-c174-46b9-b1dc-225a033cf14e)


seq 10 | sed -n '2,~4p'
## OUTPUT


![image](https://github.com/user-attachments/assets/466d3cf3-551d-4ec0-bd88-f8abcfb291c7)


seq 3 | sed '2a hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/2f8a1452-f488-4773-84f6-aa587948d64c)


seq 2 | sed '2i hello'
## OUTPUT

![image](https://github.com/user-attachments/assets/0d731f42-3240-42f5-a51d-0634da6c9e33)


seq 10 | sed '2,9c hello'
## OUTPUT


![image](https://github.com/user-attachments/assets/330eb5b9-458d-4e03-b5a0-fd50f2a49011)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![image](https://github.com/user-attachments/assets/8707bece-a063-423a-a1a8-3c868d4270d1)


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

![image](https://github.com/user-attachments/assets/cdcb83c3-8ddb-42af-8ec0-1159e7a19596)


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/c2e5fd92-b6a3-4d71-8fd5-5db1747a7fd8)

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


![image](https://github.com/user-attachments/assets/aed46a25-f121-485a-9e6e-954a6cf4ada5)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT


![image](https://github.com/user-attachments/assets/5e785457-05ca-49a9-a197-f44d30d80e54)


#Backup commands
tar -cvf backup.tar *
## OUTPUT


![image](https://github.com/user-attachments/assets/1802b30f-e985-4e91-9df5-a64fb17cebbc)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT


![image](https://github.com/user-attachments/assets/dd195125-fb44-4b18-a53f-818d014843e2)

tar -xvf backup.tar
## OUTPUT

![image](https://github.com/user-attachments/assets/0f125e77-1dac-472f-a7c0-1de417d7b8a0)

gzip backup.tar

ls .gz
## OUTPUT

![image](https://github.com/user-attachments/assets/e5655d40-1a2a-4916-8165-ff9241deddfe)
 
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

![image](https://github.com/user-attachments/assets/7fe546c5-426b-48d1-970f-db13b662a056)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


![image](https://github.com/user-attachments/assets/22cfa042-c0d7-492a-9411-337041f4c7cd)

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


![image](https://github.com/user-attachments/assets/671faae3-d04a-416c-9270-12b22ac2dbe6)
 
ls file1
## OUTPUT

![image](https://github.com/user-attachments/assets/3a6ddd8c-b8b7-49bd-a304-c8927c6d4848)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

 ![image](https://github.com/user-attachments/assets/ccc11dd5-b267-4d79-80f5-4c697f355dd7)

abcd
 
echo $?
 ## OUTPUT


![image](https://github.com/user-attachments/assets/a92425b5-8659-4df3-8de9-f68d73e5858a)

 
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


![image](https://github.com/user-attachments/assets/728ac4b4-4e9d-4b39-ab0b-03f736e54573)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/user-attachments/assets/c2a05d7f-38ee-4982-8167-a82a19955416)


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


![image](https://github.com/user-attachments/assets/a623f6b6-d5cf-4751-9af6-7caff4fe16dc)


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


 ![image](https://github.com/user-attachments/assets/2f127e5e-b1f5-4215-9fd9-bad446b86aa2)

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

![image](https://github.com/user-attachments/assets/ce33bcb4-0951-449d-a2b4-86cd4578862b)

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

 ![image](https://github.com/user-attachments/assets/4b2573e7-94ac-453e-82d9-1801043a5920)

 
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
![Screenshot from 2025-03-05 22-24-09](https://github.com/user-attachments/assets/b186e0ac-8f77-4856-9e93-f3187bdc2f71)
![Screenshot from 2025-03-05 22-33-11](https://github.com/user-attachments/assets/08e2c72f-5c09-43a3-a103-45c4e4b72148)
![Screenshot from 2025-03-05 22-33-39](https://github.com/user-attachments/assets/d6c09abf-b16f-4879-baf9-bc0994894c66)
![Screenshot from 2025-03-05 22-51-43](https://github.com/user-attachments/assets/2a789ca9-deac-47ca-b461-fefb504ff7f2)
![Screenshot from 2025-03-05 22-52-16](https://github.com/user-attachments/assets/4c74f904-04c4-474f-b74f-b81a76f257a6)







# RESULT:
The Commands are executed successfully.
