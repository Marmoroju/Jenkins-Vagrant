Vagrant.configure("2") do |config|
 
    config.vm.box = "centos/7"
    config.vm.hostname = "Jenkins"
    config.vm.network "private_network", ip: "192.168.56.4" 
    config.vm.network "forwarded_port", guest: 8080, host: 8080, host_ip: "127.0.0.1" 
    config.vm.provision "shell", path: "provision.sh"
    config.vm.provider "virtualbox" do |v|
        v.memory = 1024
        v.cpus = 2
    end
end