Vagrant.configure(2) do |config|

  config.vm.define "vm1" do |vm1|
      vm1.vm.box = "ubuntu/xenial64"
      vm1.vm.hostname = "vm1"
      vm1.vm.network :private_network, ip: "192.168.27.100"
      vm1.vm.provider :virtualbox do |vb|
          vb.memory = 1024
          vb.cpus = 2
      end
      vm1.vm.provision :shell, :inline => "apt-get update && apt-get install -y nginx"
      vm1.vm.provision :shell, :inline => "ln -s /vagrant /var/www/html/demo"      
  end

  config.vm.define "vm2" do |vm2|
      vm2.vm.box = "ubuntu/xenial64"
      vm2.vm.hostname = "vm2"
      vm2.vm.network :private_network, ip: "192.168.27.101"
      vm2.vm.provider :virtualbox do |vb|
          vb.memory = 1024
          vb.cpus = 2
      end
  end

  
end