# Vagrant
Tutorial and Notes for Vagrant


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

``` cd vagrant-test````

``` code . ```
