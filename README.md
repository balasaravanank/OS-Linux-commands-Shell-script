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
<img width="600" height="183" alt="Screenshot from 2025-08-18 20-55-24" src="https://github.com/user-attachments/assets/4ddb8af6-43a6-45bb-ae5d-8f48c392bf0a" />




cat < file2
## OUTPUT
<img width="615" height="220" alt="Screenshot from 2025-08-18 20-55-33" src="https://github.com/user-attachments/assets/85bf8d0b-3b66-4a0d-8999-2036c5ac79a2" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="663" height="75" alt="Screenshot from 2025-08-18 20-55-49" src="https://github.com/user-attachments/assets/43aaa056-a333-4ed8-846f-8202fa84d099" />


 
comm file1 file2
 ## OUTPUT
 <img width="726" height="380" alt="Screenshot from 2025-08-18 20-58-34" src="https://github.com/user-attachments/assets/f23bc09a-cf49-47a9-8c63-5ba2ac7b25ca" />


 
diff file1 file2
## OUTPUT
<img width="723" height="371" alt="Screenshot from 2025-08-18 20-56-06" src="https://github.com/user-attachments/assets/63c5c00d-8224-43ef-8d71-024b517b7d07" />


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
<img width="692" height="88" alt="Screenshot from 2025-08-18 21-01-41" src="https://github.com/user-attachments/assets/440fc0e2-74ee-4978-8d7c-b5a3861c5c5f" />





cut -d "|" -f 1 file22
## OUTPUT
<img width="702" height="113" alt="Screenshot from 2025-08-18 21-01-50" src="https://github.com/user-attachments/assets/85a256d8-c24e-448b-a7d2-06d4ef3c0e2e" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="690" height="118" alt="Screenshot from 2025-08-18 21-02-01" src="https://github.com/user-attachments/assets/4850722b-1331-4bb0-a52b-5b5d9b1bcd8f" />


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
<img width="685" height="58" alt="Screenshot from 2025-08-18 21-05-25" src="https://github.com/user-attachments/assets/6143a1a1-ffcf-4b65-8b2a-d6a088c75324" />




grep hello newfile 
## OUTPUT
<img width="683" height="65" alt="Screenshot from 2025-08-18 21-05-35" src="https://github.com/user-attachments/assets/e2d3b3ed-fc96-4431-a960-e6d373d6e7a5" />





grep -v hello newfile 
## OUTPUT
<img width="686" height="53" alt="Screenshot from 2025-08-18 21-05-44" src="https://github.com/user-attachments/assets/5d3677ca-e930-4686-baed-7dcbeb7aec6a" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="767" height="86" alt="Screenshot from 2025-08-18 21-05-55" src="https://github.com/user-attachments/assets/e20686cf-f6e8-4724-888b-1ceb193305b6" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="833" height="66" alt="Screenshot from 2025-08-18 21-06-02" src="https://github.com/user-attachments/assets/19edacea-9936-421f-8c52-bc5efdca9e8b" />


grep -w -n world newfile   
## OUTPUT
<img width="712" height="90" alt="Screenshot from 2025-08-18 21-06-13" src="https://github.com/user-attachments/assets/9ebf4246-e3f8-47b5-b99d-d76108f91156" />



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
<img width="791" height="80" alt="Screenshot from 2025-08-18 21-10-19" src="https://github.com/user-attachments/assets/4bb863c8-a93d-4efe-8bf0-fd59463da53b" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="781" height="125" alt="Screenshot from 2025-08-18 21-10-32" src="https://github.com/user-attachments/assets/df5413dc-28e6-4bd9-96b3-6817c8bdeeb8" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="818" height="86" alt="Screenshot from 2025-08-18 21-10-38" src="https://github.com/user-attachments/assets/5dd216ab-5663-454a-bd32-af1c1fad9d12" />


egrep '(world$)' newfile 
## OUTPUT
<img width="808" height="87" alt="Screenshot from 2025-08-18 21-10-57" src="https://github.com/user-attachments/assets/b104e492-210e-42cf-b520-99e9f65bb640" />




egrep '(World$)' newfile 
## OUTPUT
<img width="808" height="67" alt="Screenshot from 2025-08-18 21-11-03" src="https://github.com/user-attachments/assets/11a7d81a-079e-4ae2-a5f3-58df89a0aa08" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="780" height="88" alt="Screenshot from 2025-08-18 21-11-11" src="https://github.com/user-attachments/assets/512cf17d-daa8-4533-977d-d9d134bc7c6d" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="780" height="67" alt="Screenshot from 2025-08-18 21-11-18" src="https://github.com/user-attachments/assets/3194c96d-fd9a-4c82-8f6b-b67120dcf815" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="780" height="62" alt="Screenshot from 2025-08-18 21-11-27" src="https://github.com/user-attachments/assets/fad6d99a-9182-423d-9e4d-2bbc66b2529d" />




egrep 'Linux.*World' newfile 
## OUTPUT
<img width="780" height="62" alt="Screenshot from 2025-08-18 21-11-33" src="https://github.com/user-attachments/assets/262ebec0-5718-43dc-8a1b-28bf82f1c18a" />


egrep l{2} newfile
## OUTPUT
<img width="780" height="91" alt="Screenshot from 2025-08-18 21-11-39" src="https://github.com/user-attachments/assets/e876b849-a56a-4ffa-b0f5-0d1e6b7c339a" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="780" height="143" alt="Screenshot from 2025-08-18 21-11-46" src="https://github.com/user-attachments/assets/3de5b7b6-07f3-4120-9881-dec43b27bbce" />



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
<img width="793" height="246" alt="Screenshot from 2025-08-18 21-17-12" src="https://github.com/user-attachments/assets/9fba19a7-5e11-40e7-b7c9-0d5ae42cbc2a" />




sed -n -e '$p' file23
## OUTPUT
<img width="742" height="66" alt="Screenshot from 2025-08-18 21-17-19" src="https://github.com/user-attachments/assets/e701f94d-c778-4e53-9bc6-6cf75c814846" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="753" height="47" alt="Screenshot from 2025-08-18 21-17-24" src="https://github.com/user-attachments/assets/a3a1adcb-97ac-4257-939d-aa21343f5ff5" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="745" height="248" alt="Screenshot from 2025-08-18 21-17-30" src="https://github.com/user-attachments/assets/cce054eb-272b-48b7-b1e2-fdaff1429692" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="776" height="255" alt="Screenshot from 2025-08-18 21-17-36" src="https://github.com/user-attachments/assets/132b5235-fad4-4b9a-a182-2f4c60bda928" />




sed -n -e '1,5p' file23
## OUTPUT
<img width="783" height="255" alt="Screenshot from 2025-08-18 21-17-52" src="https://github.com/user-attachments/assets/25b8a226-86ee-446b-afce-1da6ccea82f0" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="735" height="166" alt="Screenshot from 2025-08-18 21-18-01" src="https://github.com/user-attachments/assets/36604027-2d6e-43b5-9768-ca8bb28a334a" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="768" height="120" alt="Screenshot from 2025-08-18 21-18-08" src="https://github.com/user-attachments/assets/0bb615cc-6b69-42f3-be5a-9140fdf6ab81" />




seq 10 
## OUTPUT
<img width="817" height="297" alt="Screenshot from 2025-08-18 21-18-34" src="https://github.com/user-attachments/assets/94c8c1a5-0475-40d6-ba10-a6446c201be8" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="675" height="120" alt="Screenshot from 2025-08-18 21-18-44" src="https://github.com/user-attachments/assets/9b7be62c-5b57-4b2f-bbff-42dcd2ea6615" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="675" height="120" alt="Screenshot from 2025-08-18 21-18-49" src="https://github.com/user-attachments/assets/82dd2d0c-cc20-4d0c-9684-b176ccc74ce3" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="681" height="153" alt="Screenshot from 2025-08-18 21-19-00" src="https://github.com/user-attachments/assets/e109220f-4e4c-4ce2-a29a-2bfd28ec44db" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="686" height="116" alt="Screenshot from 2025-08-18 21-19-05" src="https://github.com/user-attachments/assets/b9dac495-e100-4c74-9360-3f6a55924d43" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="745" height="120" alt="Screenshot from 2025-08-18 21-19-13" src="https://github.com/user-attachments/assets/64fecded-4e8e-4e5a-8b1b-ac857edba356" />




sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="790" height="140" alt="Screenshot from 2025-08-18 21-19-21" src="https://github.com/user-attachments/assets/dbee3681-19f0-424c-9b5d-0506a8cd6c28" />





sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="797" height="118" alt="Screenshot from 2025-08-18 21-19-29" src="https://github.com/user-attachments/assets/5821c4fb-ec44-45cd-ba1f-88f923f98833" />


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
<img width="547" height="163" alt="Screenshot from 2025-08-18 22-18-58" src="https://github.com/user-attachments/assets/b7db1ec2-6924-4f93-b503-fdf28cdcd4a2" />




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
<img width="566" height="177" alt="Screenshot from 2025-08-18 22-19-12" src="https://github.com/user-attachments/assets/0ed1ec17-67d7-4171-bb1e-fb50665031b4" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
<img width="872" height="216" alt="Screenshot from 2025-08-18 22-19-27" src="https://github.com/user-attachments/assets/7037c263-d544-4ba9-a3f2-2b917eec61f8" />


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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


# RESULT:
The Commands are executed successfully.
