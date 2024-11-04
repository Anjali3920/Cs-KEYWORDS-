# CLOUD COMPUTING 

# How to make a vm( virtual machine)=
1.make an account on aws.

2.select ec2 service.

3.inside ec2 make an instance,

For an instance select an os( operating system),
5.make an key pair ( the key pair will automatically be downloaded).

6 while making key pair select ppk type ,

7.an public ip will be generated,

8.launch the instance

Install an putty ( search on google how to download putty for (the operating system you have chosen) and download it.

After that open the putty and on ssh option paste the public ip from the instance,

11.in the aut option select credentials and browse the key pair you have created in instance,

Now to download a web server open putty and type :-sudo apt update, after that type :-sudo apt Install apache2,
13:- to remove the dollar sign type:- sudo su,

14:- after that the next step is to type :-/var/www/html/

15.enter the above and on the next line type index.html

16.after that type :-rm index.html

17.enter the above and type :-vi index.html ( by writing this a new page will appear in which you have to either type html code aur copy paste it from GitHub),

18.to run the code type :- control+c ,shift+ ,wq and enter


# using EC2 in aws
First open aws search EC2 then Launch Instance and there select keypair in putty then download it.

after that Launch it and run putty and paste public id on HOST NAME and open that downloaded key pair for putty in SSH then Auth then Credentials and open there.

after that run it and write username as ubuntu as selected os and then type following commands.

```bash
sudo apt update
```
``` bash
sudo apt install apache2
```
to install a web server on ip then
```
sudo su
```
for convert $ into # for getting admin role then
```
cd /var/www/html/
```
then
```
ls
```
for list of html file in it
then copy that html file name and write

```
rm index.html
```
rm means remove command

```
vi index.html
```
this will open a notepad like and write html code there like (vi is editor) 

 then press ctrl+c then shift+colon then write wq and enter

12. now copy your public ip and paste it on browser you will see the texts written by you (by using html above).

# Hosting a Website on AWS with Apache2 Using PowerShell
(These are the steps after launching instance and downloading .pem passkey)





Step 1: Connect to EC2 Instance Using PowerShell
Open PowerShell in Windows.
Navigate to your PEM file: First, ensure you’re in the directory where your .pem file is located. Use cd to change directories:
cd path\to\your-pem-file
Use the ssh command to connect to your EC2 instance:
ssh -i "path_to_your_key.pem" ec2-user@your_instance_public_IP
Replace path_to_your_key.pem with the location of your private key. Replace your_instance_public_IP with the public IP of your EC2 instance.

Step 2: Update the Package List on Your EC2 Instance
Run the following command after logging in to update your packages:

sudo apt update
Step 3: Install Apache2
To install the Apache2 web server:

sudo apt install apache2 -y
Step 4: Delete the Default index.html and Create Your Own
Navigate to the Apache web directory:

cd /var/www/html
Delete the default index.html file:
sudo rm index.html
Create a new index.html file:
sudo vi index.html
Add your website's HTML content and save the file.
YAY! Your link or IP adress of your instance will now work.









