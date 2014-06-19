# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.network "public_network", bridge: 'wlan0'
  config.vm.network :private_network, ip: "192.168.1.10"
  config.vm.hostname = "torqueserver"

  config.vm.provision "ansible" do |ansible|
    ansible.limit = 'all'
  	ansible.sudo = true
  	ansible.inventory_path = "provisioning/hosts"
  	ansible.playbook = "provisioning/playbook.yml"
  end
end
