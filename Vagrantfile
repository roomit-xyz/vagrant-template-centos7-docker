Vagrant.configure("2") do |config|

config.vm.box_check_update = false	
config.vbguest.auto_update = false

config.vm.define "node1" do |node1|
  node1.vm.box = "centos/7"
  node1.vm.hostname = "freeipa.wajtamaka.com"
  node1.vm.network "private_network", ip: "192.168.33.11"
  node1.vm.provider "virtualbox" do |vb|
     vb.name = "node1"
     vb.memory = "2048"
  end
  node1.vm.provision :shell, path: "install-docker.wjt"
end

config.vm.define "node2" do |node2|
  node2.vm.box = "centos/7"
  node2.vm.hostname = "client.wajatmaka.com"
  node2.vm.network "private_network", ip: "192.168.33.12"
  node2.vm.provider "virtualbox" do |vb|
     vb.name = "node2"
     vb.memory = "512"
  end
end

config.vm.define "node3" do |node3|
  node3.vm.box = "centos/7"
  node3.vm.hostname = "client3.wajatmaka.com"
  node3.vm.network "private_network", ip: "192.168.33.13"
  node3.vm.provider "virtualbox" do |vb|
     vb.name = "node3"
     vb.memory = "512"
  end
end
end
