Getting started with vagrant 
=====================

``` bash
vagrant plugin install vagrant-vbox-snapshot
vagrant plugin install vagrant-vbguest
vagrant plugin install vagrant-cachier
```
### Vagrant basics

``` bash
vagrant init
vagrant up
vagrant halt
vagrant destroy
vagrant reload
```


### Vbox Snapshots

``` bash 
vagrant snapshot take [vm-name] <SNAPSHOT_NAME>   # take snapshot, labeled by NAME
vagrant snapshot list [vm-name]                   # list snapshots
vagrant snapshot back [vm-name]                   # restore last taken snapshot
vagrant snapshot delete [vm-name] <SNAPSHOT_NAME> # delete specified snapshot
vagrant snapshot go [vm-name] <SNAPSHOT_NAME>     # restore specified snapshot
```


