# what is devenv and benefits
## vagrant and virtual box
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
