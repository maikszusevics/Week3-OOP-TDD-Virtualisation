# Week 3: OOP, TDD, and Virtualisation

## OOP
Object Oriented Programming is a model of programming which organises software development around objects instead of 
ectensive blocks of code with functions and logic. It contains 4 pillars:

#### Abstraction:

Abstraction in OOP is the practise of hiding the unnecesary information from the user and only showing the essential information.
Here is a block of unabstracted code which creates a simple calculator:

![image](https://user-images.githubusercontent.com/110176257/184597491-be9f610b-f207-46f2-a7ef-2c2680a8e576.png)

And by creating a class with this code, we can abstract most of it and use it by only typing the following into a different file:

![image](https://user-images.githubusercontent.com/110176257/184597608-f6394df4-e802-4811-890d-c84949faff7d.png)

#### Encapsulation

The above calculator also incoroporates encapsulation. Encapsulation is the practise of bundling data storage, functions and methods into one place, often called a class. In the above code there is functions for different operators all encapsulated within the calculator class.

#### Inhretitance

![image](https://user-images.githubusercontent.com/110176257/184598801-d6929029-5b18-4126-bff9-c72a0d552c5e.png)

Inheritance allows us to incroporate the attributes and functions of a parent or super class into a subclass or child class.
in this example the reptile class is a subclass of the animal class yet it still has attributes of the animal class despite not having to program them into the class directly.

```python
# create an animal class
# syntax class Name:
# good practise to name class with capital letter

class Animal:
    # need to initialise a class every time
    # __init__ to declare class attributes
    def __init__(self): #refers to current class
        self.alive = True
        self.spine = True

    def sleep(self):
        return "all animals sleep"

    def eat(self):
        return "eating is vital"

# create an object of the class before using it
cat = Animal()

# print(cat.eat()) # abstracted how eat was created or what info is available
```
```python
# inherit everything from Animal class into reptile
from animal import Animal

# create reptile class
class Reptile(Animal): # write the name of the class in () to inherit
    # parent class / base class / superclass
    def __del__(self):
        # let it know to inherit everything from parent class
        super().__init__() # super() is used to inherit everything from parent class
        self.cold_blooded = True
        self.heart_chamber = [3, 4]

    def seek_heat(self):
        return "looking for direct sunlight"

    def hunt(self):
        return "they do be hunting for food"

# create object of reptile class

reptile_object = Reptile()

print(reptile_object.eat())
print(reptile_object.hunt())

```


#### Polymorphism
Polymorphism is being able to take morph inherited attributes such that they are relevant to the class which is inheriting them.
In the following code, the attribute "facial_hair" is inherited from the Male class by the Boy class. But it is morphed to be False by default instead of True by default as children dont tend to have facial hair.

![image](https://user-images.githubusercontent.com/110176257/184599210-f8e91b3d-20cd-4730-873b-939e53a658d7.png)

![image](https://user-images.githubusercontent.com/110176257/184599223-a2832519-b0be-4b73-a72a-b8ee3722399a.png)


## TDD
#### Test Driven Development

TDD is a framework of software development which revolves around testing before any development. This means you have to write more code overall because you have to make tests for every function before you even start to code the features, but it saves a lot of time that is normally spent on debugging code later on. It relies on an iterative approach which includes creation of tests first, development after, and finally refratoring

![image](https://user-images.githubusercontent.com/110176257/184599965-d852081c-8b8a-4681-b854-4558d6d2c011.png)

Steps of TDD:
- Create tests
- Test tests to check if they are testing what we are looking to test
- Code what you need to be able to pass the test, and pass the test.
- Refractor what is necessary
- Repeat
- Benefits of TDD
- Efficient
- Cohesive
- Results in error-free code
- Results in readable code


Benefits of TDD
- Efficient
- Cohesive
- Results in error-free code
- Results in readable code



## Development Evnironment



The dev environment is a comprehensive set of tools for software development. The purpose is to have a place for developers to work 
without worrying about writing code which only works on their localhost and takes time to share with the rest of the development team.

Benefits of DevEnv
- Streamlined workflows
- Reduced chance of localhost differences breaking the software
- Valuable infrastructure for integrating different parts of the development process

### vagrant and virtual box
Vagrant is a solution for creating a Virtual Machine with minimalistic configuration and with extreme ease, which can be used across different Virtual machine environments. Vagrant automates the work of setting up development environments for your projects.

VirtualBox is open-source and industry standard software for virtualizing the x86 operating systems within an operating system.

### virtualisation

Virtualisation creates a simulated computing environment within your operating system. Virtualisation utilises a specified fraction of your physical hardware resources to create a new environment with your choice of operating system. This allows partitions of a single physical computer or server into several machines. Each virtual machine can interact independently and run different systems and applications while sharing the resources of a single host machine.

### Setting up virtual environment:

![image](https://user-images.githubusercontent.com/110176257/184600589-78c80dcf-3286-4f95-9122-98d292bbb535.png)

The way we've been using virtualisation is utilising the vagrant and virtualbox tools to create an ubuntu based basic virtual machine.

First steps are to install Ruby, Virtualbox, and Vagrant.

Next we have to create a location and file for setting up vagrant, which will set up our virtualmachine using virtualbox:

- Make a directory

    - mkdir new_folder

- Move in the directory

    - cd new_folder

- Create a Vagrant file nano Vagrantfile

    - Paste the block of code and save it

```ruby
#vagrant

Vagrant.configure("2") do |config|



 config.vm.box = "ubuntu/xenial64" # Linux - ubuntu 16.04

# creating a virtual machine ubuntu 



 




end
```


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
- install nginx `sudo apt get install nginx -y`
- how to check if its installed `sudo systemctl status nginx`
- how ro restart a process - in the case its an NGINX
- restart or start `sudo systemctl restart nginx`
- enable the process `sudo systemctl enable nginx`


### Adding private network functionality to the VM:

```ruby
#vagrant

Vagrant.configure("2") do |config|



 config.vm.box = "ubuntu/xenial64" # Linux - ubuntu 16.04

# creating a virtual machine ubuntu 
config.vm.network "private_network", ip:"192.168.10.100"
#once you added private network, need to reboot vm



 
end
```

