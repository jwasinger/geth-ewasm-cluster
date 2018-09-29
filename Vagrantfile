Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

   config.vm.network "forwarded_port", guest: 8545, host: 8545
   config.vm.network "forwarded_port", guest: 3000, host: 3000
   config.disksize.size = '50GB'
   config.vm.provision "file", source: "ansible", destination: "/home/vagrant/geth-ewasm-cluster"
   config.vm.provider "virtualbox" do |v|
    v.memory = 6096
    v.cpus = 2
  end
end

