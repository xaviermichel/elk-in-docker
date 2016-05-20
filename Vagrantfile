Vagrant.require_version ">= 1.6.0"
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	config.vm.provider "virtualbox" do |v|
		v.memory = 4096
		v.cpus = 2
	end

	config.vm.box = "williamyeh/ubuntu-trusty64-docker"

	config.vm.provision :shell, path: "init.sh", privileged: true
	config.vm.provision :docker
	
	config.vm.network "forwarded_port", guest: 5000, host: 5090
	config.vm.network "forwarded_port", guest: 9200, host: 9290
	config.vm.network "forwarded_port", guest: 9300, host: 9390
	config.vm.network "forwarded_port", guest: 5601, host: 5691
end
