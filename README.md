# what is devenv and benefits
Development environment is a set of tools for developing the source code of software. It normally utilises virtual machines in order to not break anything on the developers localhost and to make sure the software works on all machines despite hardware and operating system inconcistencies. It also helps improve collaboration between cross functional teams of the development process.

![image](https://user-images.githubusercontent.com/110176257/184311163-1934ee36-368d-4025-96bf-4e43c2652bb4.png)


## vagrant and virtual box
Vagrant is a solution for creating a Virtual Machine with minimalistic configuration and with extreme ease, which can be used across different Virtual machine environments. Vagrant automates the work of setting up development environments for your projects.

### virtualisation


- how can we find out the name of the OS `nuname` or `uname -a`
- how to create a file in liux `touch tfilename` or `nano filename`
- how to check exitsting files/ folders `ls` `ls -a`
- how to create a folder `mkdir foldername`
- how to navigate inside the folder `cd foldername`
- how to move one step back `cd ..`
- how can we check our current location `pwd`
- whoami
- how to copy file `cp filename destination`
- to copy without being in the current location you can do `cp filename_with_path destination`
- how to remove file `rm -rf file/folder_name`
- how to cut paste the file `mv filname destination_path`
- `top` tasks running or `ps aux`
- `sudo su` for admin tasks super user
- how to use pipe 
- kill terminates processes based on Process ID number (PID), while the killall and pkill commands terminate running processes based on their names
- how to check permission with `ll`
- change file permission `chmod permission filename`
  - `r` or `w` or `rw` or `all` also numbers `400` or `600` or `700`
- update our ubuntu OS `apt-get isntall update`
- upgrade our ubuntu `apt-get upgrade`
- hopw to create automated tasks with provisioning spcripts
- automate update and upgrade
- `cat filename` for check inside
- 

## This inside the vagrantfile will make a virtualmachine. Using init will do a lot more that we do not need yet.
```ruby
#vagrant

Vagrant.configure("2") do |config|



 config.vm.box = "ubuntu/xenial64" # Linux - ubuntu 16.04

# creating a virtual machine ubuntu 



 




end
```
