# Vagrant
### Tutorial and Notes for Vagrant


I knocked against this thing called Vagrant in Janurary 2023 and started a bit of research ever since. Firstly I would advice you to download and install Vagrant and Virtual Box on your system 

* [Vagrant](https://www.vagrantup.com/)
* [VirtualBox](https://www.virtualbox.org/)

Do download the extension pack for VB as well

Now if you do not know what Vagrant is , it is nothing but portable virtual development environments , if you are familiar with docker this is something very similar , except we use vms instead of containers.

I have a Linux System (Arch Based) so all I needed to do was 

``` sudo pacman -Syu```

```sudo pacman -S virtualbox```

```sudo pacman -S vagrant```

Also I downloaded and installed the vb extension pack

Now we are good to go to get our hands dirty.

We start by checking out if vagrant installation was successsful

``` vagrant -v```

Create a directory and open a text editor (I used VSCode)

```mkdir vagrant-test```

``` cd vagrant-test```

``` code . ```

This is where our vagrant file and our project files will go

The vagrant file is the core of vagrant it is where all the setting goes 

It has 5 main parts : 

* config.vm.box - OS
* config.vm.provider - VM provider (VB in our case)
* config.vm.network - Network Configuration for the box 
* config.vm.shared_folder - how we can access files from our system
* config.vm.provision - what we want to setup in the box 


We can head over to Vagrant Boxes to see what boxes we can start with here I am goinig with CentOS

All kinds of Varant Boxes are available [here](https://app.vagrantup.com/boxes/search)

In your terminal run vagrant init <box name>

```vagrant init centos/7 ```

You can check my vagrant file 

  
``` vagrant up ```
  
  
  Now if you really don't like what we did so far and you are having second thoughts....
  
  ```vagrant destroy```

  If you want to suspend the vm 
  
  ``` vagrant suspend ```
  
  and to resume 
  
  ``` vagrant resume ```

  There are few changes that I want to do on the base Centos file before I get started
  
  First I want to change amount of memory and cores allocated to the box 
  
 In config.vm.box we make the following changes
  
  ```
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "2048"
    vb.cpus = 2
  end
  ```
  
Keep your vb up so you can check wheather the specs have changed or not and reload the box once to make the changes

``` vagrant reload ```
  
Now we ssh into our box 
  
``` vagrant ssh ```
