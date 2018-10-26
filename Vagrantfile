Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 4000, host: 4000
  # config.vm.network "public_network"
  # config.vm.provider "virtualbox" do |vb|
  #   vb.memory = "1024"
  # end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update && apt full-upgrade -y
    apt-get install -y build-essential zlib1g-dev ruby ruby-dev ruby-bundler
    su -c 'mkdir -p /home/vagrant/test' vagrant
  SHELL
  config.vm.provision "shell", run: "always", inline: <<-SHELL
    su -c 'cp -Rf /vagrant/* /home/vagrant/test' vagrant
    su -c 'cd /home/vagrant/test ; bundle install' vagrant
    su -c 'cd /home/vagrant/test ; bundle exec jekyll serve -H 0.0.0.0' vagrant
  SHELL
end
