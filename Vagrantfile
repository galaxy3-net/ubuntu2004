# -*- mode: ruby -*-
# vi: set ft=ruby

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	#config.vm.provider
	config.vm.box = "generic/ubuntu2004"

	config.vm.define "ubuntu20.04" do |ubuntu|
		ubuntu.vm.hostname = "ubuntu20.04"
	end

	config.vm.provision "file", source: "./mysql_secure_install.sh", destination: "$HOME/mysql_secure_install.sh"

	config.vm.provision:shell, path: "./bootstrap.sh"
end
