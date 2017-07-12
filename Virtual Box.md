#Virtual Box

Download virtual box disk image: https://www.virtualbox.org/wiki/Downloads 

Allows you to create a virtual machine, i.e. Windows, Linux, etc.

* Name the machine
* Choose which type (Windows, Linux etc)
* Choose with OS version

Allocate minimum 2gb
VirtualBox hard disk
25GB

Download OS iso image. And locate it through Virtual Box.

Open terminal in emulator, apt-get is the command to do things.

``` apt install git ```

## To get Sublime

```
sudo add-apt-repository ppa:webupd8team/sublime-text-2
sudo apt-get update
sudo apt-get install sublime-text
```

Listing all of the programs available
```
apt list
```

Install git, curl. Curl can be used to make http calls.

```
curl www.google.com
```
This will respond with html.
 
``` echo $PATH ```
 
Showing all system files.
 
``` 
cd /
ls
```
 
Removing files.
 
```
rm -rf
```
There is no warning when deleting things.
 
Install ruby, specify which one
 
```
sudo apt-get install ruby2.3
```
 
Install gems
 
```
sudo gem install bundler
```
 
### To open a secure shell
 
```
sudo apt-get install openssh-server
```
 
In home directory make hidden ssh folder
 
``` mkdir .ssh ```
 
Generate new SSH key and add to ssh agent using https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/
 
Open SSH key in sublime
 
``` subl id_rsa.pub ```
 
Go to git hub, settings, add new SSH key, name it and copy&paste the SSH key into git. The use the following to secure the connection.
 
``` ssh -T git@github.com ```

Command guide: ``` man ls```, ```man ruby ```

To see system processes use ``` ps ```. You can kill process by doing ``` kill <process number> ```.

### Installing postgres

https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04

### Installing rbenv

https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-16-04

### Helpful sources

digital ocean
bash reference manual

##Editing Bash script

In bash file (example.sh)

* Define where the path is
```
#!/bin/bash
```
* To print home location
```
echo $HOME
```

* In terminal to run file

```
chmod +x example.sh

./example.sh 
```


* Functions in bash

```
A=1
B=2
num=$(($A+$B))

echo $num
```

* Can include update and upgrade in bash shell

```
echo $HOME
sudo apt-get update
sudo apt-get upgrade
```

* Getting rid of password prompt

```
sudo nano /etc/sudoers
```

give username same no password permission at end of file.
``` tina ALL(ALL) NOPASSWD: ALL ```
 

