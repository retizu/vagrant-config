Getting started with vagrant 
=====================

``` bash
vagrant plugin install vagrant-vbox-snapshot
vagrant plugin install vagrant-vbguest
vagrant plugin install vagrant-cachier
```

### Vagrant boxes repositories
* [HasiCorp Atlas](https://atlas.hashicorp.com/boxes/search)
* [Vagrantbox.es](http://www.vagrantbox.es/)
* [Modern.ie Windows boxes](http://dev.modern.ie/tools/vms/windows/)

Get the links from the sites above an add them to your vagrant instalation by issuing the "Vagrant add command". (Beginners tip: you set the title) 

### Vagrant basics

``` bash
vagrant box add [title] [url]   # donwload a new box from url and give it a tile
vagrant box list                # list available boxes, take returned name and put it it your Vagrantfile under config.vm.box
vagrant init                    # generate a default Vagrantfile in the current directory
vagrant up                      # bring up a vm, it boots it up or it provisions it 
vagrant halt                    # stop a machine
vagrant destroy                 # destroy a machine (but doesn't remove the directory)
vagrant reload                  # reload configs from the Vagrant file (accompanied by a halt and up)
vagrant plugin install [plugin-name]    # install a certain plugin 
vagrant plugin list                     # list available plugins 
vagrant ssh-config                      # displays parameters used by vagrant ssh (mostly interesting if you don't know the path to your IdentityFile (that holds the vagrant ssh key)
vagrant ssh                     # under linux or cygwin it connects to the box via ssh using the ssh key (get the path to it from above)
```


### Vbox Snapshots

``` bash 
vagrant snapshot take [vm-name] <SNAPSHOT_NAME>   # take snapshot, labeled by NAME
vagrant snapshot list [vm-name]                   # list snapshots
vagrant snapshot back [vm-name]                   # restore last taken snapshot
vagrant snapshot delete [vm-name] <SNAPSHOT_NAME> # delete specified snapshot
vagrant snapshot go [vm-name] <SNAPSHOT_NAME>     # restore specified snapshot
```


