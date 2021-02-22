# How to run multi machine set up in Vagrant

You can define multiple machines in a single vagrant file.

To perform an action on a specifc machine, the commands look like: `vagrant [action] [machineName]`

```VagrantFile
Vagrant.configure(2) do | config |
  config.vm.box = "jasonc/centos7"

  config.vm.define "server1" do | server1 |
    server1.vm.hostname = "server1"
    server1.vm.network "private_network", ip: "10.2.3.4"
  end

  config.vm.define "server2" do | server2 |
    server2.vm.hostname = "server2"
    server2.vm.network "private_network", ip: "10.2.3.5"
  end
end
```
