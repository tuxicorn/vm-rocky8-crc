Vagrant.configure("2") do |config|
config.vm.define "vm2" do |vm2|
vm2.vm.box = "rockylinux/8"
vm2.vm.hostname = "vm2"
vm2.vm.network "public_network", ip: "192.168.0.17", auto_config: false

end
config.vm.provider "virtualbox" do |v|
  v.memory = 20000
  v.cpus = 4
  v.customize ["modifyvm", :id, "--nested-hw-virt", "on"]
end
end
