Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  
  config.vm.define "docker-machine" do |node|
    node.vm.hostname = "docker-machine"
    config.vm.box_check_update = false
    config.vm.network "public_network"
    config.vm.provider "virtualbox" do |vb|
      vb.name = "docker-machine"
      vb.memory = "4096"
      vb.cpus = "2"
    end

    node.vm.provision "install-docker", type: "shell", :path => "provision/install-docker-2.sh"
  end
  
end

