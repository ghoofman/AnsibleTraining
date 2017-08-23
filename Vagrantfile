# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	config.ssh.insert_key = false
	config.vm.provider :virtualbox do |vb|
		vb.customize ["modifyvm", :id, "--memory", "256"]
	end

	# Application server 1.
	config.vm.define "app1" do |app|
		app.vm.hostname = "orc-app1.dev"
		app.vm.box = "geerlingguy/centos7"
		app.vm.network :private_network, ip: "192.168.60.4"
	end

end
