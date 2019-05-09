# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant::Config.run do |config|

 config.vm.box = "ubuntu/xenial64"

 config.vm.provision :shell, :inline => "sudo apt-get update"
 config.vm.provision :shell, :inline => "sudo apt-get install software-properties-common -y"
 config.vm.provision :shell, :inline => "sudo apt-get -y install python-pip -y"
 config.vm.provision :shell, :inline => "pip install pywinrm"
 
 config.vm.provision :shell, :inline => "sudo apt-get install --reinstall ca-certificates -y"
 config.vm.provision :shell, :inline => "sudo apt-add-repository ppa:ansible/ansible -y"
 config.vm.provision :shell, :inline => "sudo apt-get update"
 config.vm.provision :shell, :inline => "sudo apt-get install ansible -y"

 config.vm.provision :shell, :inline => "sudo apt-get install vim -y"

 config.vm.provision :shell, :inline => "ansible --version"
 config.vm.provision :shell, :inline => "echo All done, go vagrant ssh!"

 config.vm.forward_port 8080, 8080

end


Vagrant.configure("2") do |config|

config.vm.provider :virtualbox do |virtualbox|
virtualbox.customize ["modifyvm", :id, "--memory", "1024"]

end

end
