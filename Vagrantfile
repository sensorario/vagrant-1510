# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<SCRIPT
    echo "I am the provisioner"
    export GOPATH="/home/vagrant/gopath/"
    export VISUAL=vim
    export EDITOR=vim
    cd $GOPATH; go get github.com/stretchr/testify/assert
    sudo apt-get install -y tree
    sudo apt-get install -y php5
    sudo apt-get install -y bison
    sudo apt-get install -y flex
    sudo apt-get install -y g++
SCRIPT

Vagrant.configure(2) do |config|
  config.vm.box = "ffuenf/ubuntu-15.10-server-amd64"
  config.vm.provision "shell", inline: $script
end
