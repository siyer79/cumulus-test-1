#Vagrant.configure(2) do |config|
#  config.vm.box = "cumulus-vx-3.0.0" end

Vagrant.configure(2) do |config|

   config.vm.box = "cumulus-vx-3.0.0"

   
##### DEFINE VM for server01 #####
   config.vm.define "server01" do |device|
     device.vm.hostname = "server01"
     device.vm.network "private_network", ip: "10.0.0.10/24"
     
     device.vm.provider "virtualbox" do |v|
       v.name = "server01"
       v.memory = 512
     end

   end

##### DEFINE VM for server02 #####
   config.vm.define "server02" do |device|
     device.vm.hostname = "server02"
     device.vm.network "private_network", ip: "10.0.0.11/24"
    
     device.vm.provider "virtualbox" do |v|
       v.name = "server02"
       v.memory = 512
     end

   end

##### DEFINE VM for switch01 #####
   config.vm.define "switch01" do |device|
     device.vm.hostname = "switch01"
     device.vm.network "private_network", ip: "10.0.0.1/24"

     device.vm.provider "virtualbox" do |v|
       v.name = "switch01"
       v.memory = 512
     end

   end

##### DEFINE VM for switch02 #####
   config.vm.define "switch02" do |device|
     device.vm.hostname = "switch02"
     device.vm.network "private_network", ip: "10.0.0.2/24"

     device.vm.provider "virtualbox" do |v|
       v.name = "switch02"
       v.memory = 512
     end

   end
   

   config.vm.provision "ansible" do |ansible|
     ansible.verbose = "vvv"
     ansible.playbook = "./playbook/wd-playbook.yml"
   end


end



