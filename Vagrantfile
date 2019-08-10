Vagrant.configure("2") do |config|
  config.vm.define "ewb" do |ewb|
    ewb.vm.box = "generic/ubuntu1804"
    ewb.vm.hostname = 'Manager'
    ewb.vm.box_url = "generic/ubuntu1804"

    ewb.vm.network :private_network, ip: "192.168.56.201"

    ewb.vm.provider :virtuablox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "ewb"]
    end
  end

  config.vm.define "bd" do |bd|
    bd.vm.box = "generic/ubuntu1804"
    bd.vm.hostname = 'Worker1'
    bd.vm.box_url = "generic/ubuntu1804"

    bd.vm.network :private_network, ip: "192.168.56.202"

    bd.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "bd"]
    end
  end

  config.vm.define "bl" do |bl|
    bl.vm.box = "generic/ubuntu1804"
    bl.vm.hostname = 'Worker2'
    bl.vm.box_url = "generic/ubuntu1804"

    bl.vm.network :private_network, ip: "192.168.56.203"

    bl.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "bl"]
    end
  end

end
