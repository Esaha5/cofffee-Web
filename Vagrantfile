# -*- mode: ruby -*- 
# vi: set ft=ruby : 
VAGRANTFILE_API_VERSION = "2" 
Vagrant.configure(VAGRANTFILE_API_VERSION) do|config| 
    config.ssh.insert_key = false 
    config.vm.provider :virtualbox do|vb| 
        vb.customize ["modifyvm", :id, "--memory", "1024"] 
    end 
    
    #Web Server
    config.vm.define "website-server" do|web| 
        web.vm.hostname = "website-server" 
        web.vm.box = "generic/centos7" 
        web.vm.network "private_network", ip: "192.168.56.10" 
    end         

end