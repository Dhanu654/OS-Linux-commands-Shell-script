
# Operating systems Lab exercise
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
![304675248-87ac0d6a-1446-457d-86a1-988721ea01af](https://github.com/user-attachments/assets/c6aa9fe0-4b20-4d14-8559-1c196636036c)



cat < file2
## OUTPUT
![304675707-8fccc8a1-d8c7-490c-954c-8d12780ad55d](https://github.com/user-attachments/assets/598b0d2d-b25a-42a1-be88-d9e36030a074)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![304675947-faf7be7f-368e-4972-a142-bdb707f5ef60](https://github.com/user-attachments/assets/396b7f4f-6a2c-4716-8b30-355e9cfd5121)

comm file1 file2
 ## OUTPUT
![304676166-a7a105ea-6765-4fd6-b997-014bbd767c2a](https://github.com/user-attachments/assets/4167c2b7-11ea-408a-adeb-6531bc27b1a5)

 
diff file1 file2
## OUTPUT
![304676399-01ad1a86-1512-4ffd-9dd0-33ad1b981581](https://github.com/user-attachments/assets/90a966d4-1c74-49b6-9873-98aa14d76f8e)


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
![304677935-a0cce53d-e73e-455e-9340-72b81f67ad6d](https://github.com/user-attachments/assets/91c235cf-c819-4b36-8020-dd58ac1193cb)




cut -d "|" -f 1 file22
## OUTPUT
![304679935-e7a008d1-3e4c-40d2-a3a5-44ba333b2e4f](https://github.com/user-attachments/assets/4b795354-af50-44e1-b740-398ae0e9dbf9)



cut -d "|" -f 2 file22
## OUTPUT
![304680064-c5735266-0638-486c-a756-e6b0340deb48](https://github.com/user-attachments/assets/56587b9c-295b-46a6-a255-b75ca9de2c2c)


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



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT

![304679551-d193581f-02b6-4555-b088-7b05d7461148](https://github.com/user-attachments/assets/7200d727-2b33-4b8e-9d36-95a16dbb1c64)



cat newfile | grep -i -c "hello"
## OUTPUT
![304680860-65a8474e-cc02-4c2d-9e67-8e76ee6c4584](https://github.com/user-attachments/assets/ca731d50-7d11-45cc-8c9c-fc9769f4a2e4)




grep -R ubuntu /etc
## OUTPUT
![309630290-22fdcf81-932f-4b8d-8525-a64e0ec2f425](https://github.com/user-attachments/assets/40fcc25e-01c0-40b5-b6e2-7142b952df35)



grep -w -n world newfile   
## OUTPUT
![305804614-3e1bda9a-6ea0-4db2-a568-fbc718c37a19](https://github.com/user-attachments/assets/53008cef-a7a3-46d8-980b-e6d0c0635137)


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
![305808474-25d0fec3-0f33-4029-bb7a-8b6dc3d9f165](https://github.com/user-attachments/assets/6f6f2b9e-3d6f-44a7-966e-53415b47897c)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![305809631-949add15-11a4-4fe7-84e8-440126aaa9a4](https://github.com/user-attachments/assets/bc5a7591-ebc1-4c59-bdca-1eddd9d44459)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![305810476-30add5da-a3a2-4363-a53a-130b58db8320](https://github.com/user-attachments/assets/21b01d63-c35c-43f3-8f3e-f582fc22beed)




egrep '(^hello)' newfile 
## OUTPUT
![305811443-55b62521-ae26-4c21-a7ef-76af4069aca8](https://github.com/user-attachments/assets/641cdf64-c3c7-442b-8db0-a2cc4fe34360)



egrep '(world$)' newfile 
## OUTPUT
![305812168-6231c0d4-c8b0-4331-80ab-b50c2c750dfa](https://github.com/user-attachments/assets/ed09dbc1-7339-4b37-af26-6aa3b82b5689)



egrep '(World$)' newfile 
## OUTPUT
![309630312-54bd99ae-8395-4423-a4d5-33985e59bf47](https://github.com/user-attachments/assets/9c24e4ef-7881-4d89-aa6d-969857fdd01f)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![305814671-f34d417b-508e-4569-8d0e-e8a3ad4d6b45](https://github.com/user-attachments/assets/1d0ae0a7-6515-4cdf-934e-301d4099bcb6)



egrep '[1-9]' newfile 
## OUTPUT

![306316795-d39364c0-71da-42bc-844d-be536727a70f](https://github.com/user-attachments/assets/c233f372-4891-40e2-b002-01e6375f8d77)


egrep 'Linux.*world' newfile 
## OUTPUT
![306317421-7149b0f0-5880-435e-8c34-0114f0fa3f94](https://github.com/user-attachments/assets/1a2eecab-994e-44bf-924f-092d64663420)


egrep 'Linux.*World' newfile 
## OUTPUT
![309630686-a1558cfd-123d-4d04-a072-edf7f8e194de](https://github.com/user-attachments/assets/3c263053-15c5-4800-9dde-e4c0a57134cb)


egrep l{2} newfile
## OUTPUT
![306318648-919d40e4-c1ea-42e1-9645-de17925281f8](https://github.com/user-attachments/assets/fcb4ae9f-489d-42ea-a7c2-72481b944d03)



egrep 's{1,2}' newfile
## OUTPUT 
![306319020-cea59baf-267b-419f-aee4-2673da56d2d5](https://github.com/user-attachments/assets/bf1bf20c-ebef-4b70-8316-e643545ac21d)


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
![306320295-98b8fafa-04d2-41ed-ad0a-f1230817d95a](https://github.com/user-attachments/assets/4f96e6e9-0e9b-4df8-8d25-fd6874d3532b)



sed -n -e '$p' file23
## OUTPUT

![306320509-b660c572-1734-40ce-be88-9252a60d9aa3](https://github.com/user-attachments/assets/b80bb1e2-fe3b-4a8b-8c08-34fe756e0a41)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![306320967-dbb7abdd-1f69-4e0f-8433-2953261eb789](https://github.com/user-attachments/assets/3c9f8e87-b028-4484-838b-473389a11bb3)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![306322946-6aa29cfd-6b07-4d27-b36e-1b14d1cb2e7e](https://github.com/user-attachments/assets/da83b7c7-e01c-4a90-b223-2074b94d6eaf)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![309630812-30f5c5a9-9c75-43f0-8ad1-38df5d8c8177](https://github.com/user-attachments/assets/2a612cbd-c634-47a1-aed5-8c4588870a22)


sed -n -e '1,5p' file23
## OUTPUT

![306323531-0257c450-9623-4f9c-a9fa-376e59ea41eb](https://github.com/user-attachments/assets/449dc90b-d456-4acb-b7ab-0123a343b8f8)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![306324580-13bd70de-b1df-4d66-91f4-400ca29f4092](https://github.com/user-attachments/assets/ff1ff4d9-3e2d-4306-8959-258b786bf7f3)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![306324859-f4130ac3-9533-4d96-8f07-cabd48ddeb4b](https://github.com/user-attachments/assets/48f92859-87bb-4c0c-8173-1cc0bfde0213)



seq 10 
## OUTPUT
![306325086-6878d8f6-6916-4079-9662-041241ba0fb7](https://github.com/user-attachments/assets/35f33524-8825-40d5-80a6-17d8f3e64b54)



seq 10 | sed -n '4,6p'
## OUTPUT

![306325371-81bde4e8-4de7-46ae-a6ab-91a67224ad05](https://github.com/user-attachments/assets/40b993dc-503d-46be-8532-de5b6aa7a67e)


seq 10 | sed -n '2,~4p'
## OUTPUT
![306325717-fd8471e6-bc9a-43b1-aa5d-573add27fa89](https://github.com/user-attachments/assets/daac90b3-42fd-4520-bb7c-11727279b2ff)



seq 3 | sed '2a hello'
## OUTPUT

![306327286-444759b0-3989-40f1-add9-59938cbb27f1](https://github.com/user-attachments/assets/4c8f2073-554d-468d-92b4-bcdc4d8e5fdd)


seq 2 | sed '2i hello'
## OUTPUT
![306327545-f725afb5-e8b8-4694-b49c-b8a0c813a692](https://github.com/user-attachments/assets/1d51173a-1d26-418d-a0b5-25cfd0a10d3a)


seq 10 | sed '2,9c hello'
## OUTPUT
![306327729-a00f2a8c-4b7d-4822-99cf-83263a691c6a](https://github.com/user-attachments/assets/3f618c52-3764-4f33-9a4f-b04f1034f9e7)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![306328394-d04ee7c2-46ee-43ac-93b2-0ea156edc231](https://github.com/user-attachments/assets/7c284c1e-cc1e-48d9-a653-c231c769eddc)



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
![306330202-0fa515bd-81b8-4cb3-8d49-4e050065141e](https://github.com/user-attachments/assets/0dfce031-a68c-4c1a-ab93-7c249b84ad83)


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
![306330904-47a9031a-70e8-4290-ab78-aee3b3336700](https://github.com/user-attachments/assets/93ce77b5-cf2f-47cf-bb8d-886572401d03)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![306331301-3a8b94a3-b62c-4e2d-ba61-6b952493ee12](https://github.com/user-attachments/assets/fc7be7ae-2d12-4aba-abda-8b9a68c95b20)

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
![306538649-bfeb1938-f6da-4d70-a305-87724b6f9b66](https://github.com/user-attachments/assets/47dda08b-a0d0-4577-9a95-e95d7172fee6)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![306538982-a0a2671d-6f19-4682-bd0d-36e82d2a7048](https://github.com/user-attachments/assets/91df7353-d803-4f50-807f-500a916047d6)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![309631309-4c9a04e6-dfe5-4928-af8f-b4f35f38d37c](https://github.com/user-attachments/assets/b613719a-5ec6-4d88-a3ef-6e0ea3ddfb65)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![309631412-ccbc4154-17d8-4dc5-bbaf-0896a668b8a5](https://github.com/user-attachments/assets/261d69a2-88d4-42de-a00d-fdccbcf418ab)

tar -xvf backup.tar
## OUTPUT
![309631509-0d5efaa0-863c-4b17-9ed8-3e9dd6f09955](https://github.com/user-attachments/assets/cd5ba1b2-cc39-449b-8913-41f2be126704)

gzip backup.tar

ls .gz

 
gunzip backup.tar.gz



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![309631646-8b571dc0-2f93-4ab2-a314-0055d7559ee3](https://github.com/user-attachments/assets/46aef6ac-0533-4a8f-a237-2248b78bb884)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![306541597-f05197ce-9a61-4432-8677-06f9a3f2074d](https://github.com/user-attachments/assets/b5ec8f0e-29a2-47e8-9fdf-a75a195dcf17)


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
![309631701-66ce463b-a769-4ce7-9701-472a735ec84e](https://github.com/user-attachments/assets/ecc4d0da-87c6-4ec0-b9ef-b7440c6b1145)

 
ls file1
## OUTPUT
![306542056-6d43e64c-5b38-4b4c-953d-15306e4f0962](https://github.com/user-attachments/assets/df501081-210d-43c4-b5c5-71428d9c27fc)

echo $?

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![306542294-e207d92e-1b49-4f24-bf5e-6b509e151ca3](https://github.com/user-attachments/assets/e7983240-6e00-4688-96af-1ced1d928c01)

abcd
 
echo $?
 ## OUTPUT
![309631818-84516bf6-930b-4545-8031-e8922ded7758](https://github.com/user-attachments/assets/0b53e8b1-c1d0-4908-856f-7c6e945bb6bf)


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![307678773-f5691f96-7fb8-405b-aca8-99b245694866](https://github.com/user-attachments/assets/52e75bc1-3b5a-4477-84d4-3df4301231c3)


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
![307679532-9e14508f-e06b-48bd-8335-24ab45869507](https://github.com/user-attachments/assets/4d13463c-da5b-4059-92d3-254cf24500dc)

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
![307680054-a3bbfe31-a584-41fa-bb8e-34f6a8c71c2d](https://github.com/user-attachments/assets/2e0245b4-79e5-4edd-b908-d308f2e77e18)



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
![307680530-f0324dc3-e174-4c13-9e62-2b8e12f0ece8](https://github.com/user-attachments/assets/8af03902-a4a3-4e7c-87c6-d261170cd2bf)

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
![307681129-4d51cbe0-75a7-4c8b-9897-31d80e242b23](https://github.com/user-attachments/assets/f8dfe527-efd9-4814-b793-19cd3f9542f3)

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
![307682021-b23da05d-9057-4155-a3b3-e0d5e1658424](https://github.com/user-attachments/assets/3c32fe4b-315f-429d-ad48-9107bc068153)


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
![307682427-dd2856b3-6746-4001-9bb5-64248d70cbf2](https://github.com/user-attachments/assets/040a92dd-1d9e-42ee-9891-3fc9f6314c2b)

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
 ![307682893-2089b93c-f8f4-4aa2-9a14-7ad18c022649](https://github.com/user-attachments/assets/3cc1a38e-9a98-4b1b-968f-1f3f7b5b2c74)

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
 ![309632182-01d121de-472d-4dbd-b7b9-3b02b5273151](https://github.com/user-attachments/assets/dff278c1-786e-41b8-96cc-c0c1d4cf33f0)

 
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
 ![309632243-37852111-38c2-4d5b-b02e-db081bb55911](https://github.com/user-attachments/assets/c266fbdd-28b9-4189-82ec-2b8e05349015)

 
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
 ![308472685-5db0aa23-2b65-47be-845b-d27e71d1cf0e](https://github.com/user-attachments/assets/142a25ee-b8a5-4485-8586-c3bcb4a7a64c)

 
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
 ## OUTPUT
 ![308473693-e871a57b-eba5-4f24-beaa-b50a1cc05f9d](https://github.com/user-attachments/assets/cf65047f-e5e4-4f42-ad31-9f176475857c)

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
 ![308474292-3e502c00-aa25-42d7-94f4-c1cf42abbeb0](https://github.com/user-attachments/assets/2d37aa7f-033f-4d58-930a-d5ae6ec3f42f)

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
![308474845-57eb9b7e-55ed-4f8a-b04f-299ca7312d54](https://github.com/user-attachments/assets/afe98311-34ff-4764-9ff8-7f8327c46ea9)

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
## OUTPUT
![309632485-a2fc3dd0-6460-481c-93c6-644032cf66bf](https://github.com/user-attachments/assets/d3c0fe4f-355e-401e-ad8d-4982f23860f0)

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![308475810-23e57dee-3012-407b-a599-187a55addb7b](https://github.com/user-attachments/assets/c35c2566-d380-4ff5-8b38-7988db6a4b66)


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
![308478403-2811cf5c-8f23-497a-8175-1e53557b62ab](https://github.com/user-attachments/assets/b9e893bd-29b4-4274-a3e5-964105dfd82e)

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
![309632774-25c8eba9-2ae6-4b0d-aee8-0f5bdc40756f](https://github.com/user-attachments/assets/167ba69e-a673-446a-bcb3-9d3aaf4e0f29)

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
![309632814-7ff92879-790a-4e10-b53d-b3f846385518](https://github.com/user-attachments/assets/7282a7db-2737-4370-9e3e-5edc4c20dac1)

 
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
![308486165-605c7e2c-66cc-4915-b199-f4a7fe1f3dc7](https://github.com/user-attachments/assets/f8f082ae-16ba-4ae0-9ce0-f64bd64807dd)

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
![308486693-85d238ab-8b91-4dd4-a8a6-6b840499c3ba](https://github.com/user-attachments/assets/82d630fb-20f0-44d0-b545-7be09600dcaa)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![368682485-ac5a4a45-d04b-4748-ab7f-c6b5e1d6d381](https://github.com/user-attachments/assets/04a38b20-30bb-4b54-927d-8842e67091d0)


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
![368682576-ad721d8a-b4ae-4eab-81fa-8cef958b6421](https://github.com/user-attachments/assets/f15a86c6-be28-446b-b2d5-7f3821015806)

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
![368682791-24b06404-63f9-4358-8f23-ba80165d2f22](https://github.com/user-attachments/assets/18e60d1f-776a-4a7e-8316-ff69c33da2b6)


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
![368682863-4d226e69-fd6b-4322-8e04-359eccb5b146](https://github.com/user-attachments/assets/7d1cbabd-17ba-4a90-bbd7-b4378f77b2b1)


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
![368682925-0913aaaf-815c-43e5-8a68-67d378785123](https://github.com/user-attachments/assets/e019daf5-3e1e-49d0-aeed-08c4e2b63b9e)

 
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

![368682998-892623f1-936a-4c9a-8fb0-6bdfcf70f9ab](https://github.com/user-attachments/assets/4cd08ae0-2c7d-4281-b7e4-35888616d823)
![368683019-1acacb37-ab32-4a18-85f8-90048c3b8bcd](https://github.com/user-attachments/assets/d0f0d428-0244-4688-8dca-7969324da3a2)

# RESULT:
The Commands are executed successfully.
