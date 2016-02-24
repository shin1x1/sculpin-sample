# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/centos-7.1"
  config.vm.network "private_network", ip: "192.168.34.99"

  config.vm.provision "shell", inline: <<-SHELL
    yum install -y epel-release
    yum install -y http://rpms.famillecollet.com/enterprise/remi-release-7.rpm
    yum install -y git vim php php-xml --enablerepo=remi-php56
    cd /vagrant
    curl -o /usr/local/bin/sculpin https://download.sculpin.io/sculpin.phar -o sculpin
    chmod a+x /usr/local/bin/sculpin
  SHELL
end
