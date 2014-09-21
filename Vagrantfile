# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"
  config.vm.hostname = "default"
  
  # config.vm.network :private_network, ip: "192.168.33.13"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:3000" will access port 3000 on the guest machine.
  # config.vm.network "forwarded_port", guest: 3000, host: 8000

  config.vm.provider "virtualbox" do |v|
      v.name = "default"
      v.customize ["modifyvm", :id, "--memory", 4096]
  end

  config.vm.synced_folder "./src", "/vagrant/src"

  config.vm.provision "ansible" do |ansible|
    ansible.groups = {
      "dev" => ["default"]
    }
    ansible.inventory_path = "provisioning/hosts"
    ansible.playbook = "provisioning/vagrant.yml"
  end
end
