#-*- mode: ruby -*-
#vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
   config.vm.box_url = "http://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
   config.vm.box="Centos65-x86_64"
   config.vm.provision :shell, :path=>"bootstrap.sh"
   
   config.vm.define :web do |web_config|
   config.vm.synced_folder "./web", "/vagrant", create:true
   end

   config.vm.define :db do |db_config|
   config.vm.synced_folder "./db", "/vagrant" , create:true
   end
end
