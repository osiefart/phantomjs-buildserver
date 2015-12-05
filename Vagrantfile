# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.box = "debian/jessie64"

  config.vm.network "private_network", ip: "192.168.50.5"

  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
    v.cpus = 3
  end

  config.vm.provision :ansible do |ansible|
    ansible.verbose = "vvv"
    ansible.playbook = "playbook.yml"
  end

end
