Vagrant.configure("2") do |config|

  config.vm.define "mainsvr" do |mainsvr|
    mainsvr.vm.box = "geerlingguy/centos7"
    mainsvr.vm.hostname = "mainsvr"
    mainsvr.vm.network "private_network", ip: "192.168.10.12"
    mainsvr.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end
  end

  config.vm.define "web01" do |web01|
    web01.vm.box = "geerlingguy/centos7"
    web01.vm.hostname = "web01"
    web01.vm.network "private_network", ip: "192.168.10.13"
  end
  
  config.vm.define "web02" do |web02|
    web02.vm.box = "geerlingguy/centos7"
    web02.vm.hostname = "web02"
    web02.vm.network "private_network", ip: "192.168.10.14"
  end
  
  config.vm.define "web03" do |web03|
    web03.vm.box = "ubuntu/bionic64"
    web03.vm.hostname = "web03"
    web03.vm.network "private_network", ip: "192.168.10.15"
  end
  
end
