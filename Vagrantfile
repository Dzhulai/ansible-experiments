# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "CentOS"
  config.vm.hostname = "php"
  config.vm.network :private_network, ip: "192.168.100.10"
  config.vm.network :forwarded_port, guest: 80, host: 8080
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.sudo = true
  end
end
