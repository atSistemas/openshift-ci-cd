Vagrant.configure("2") do |config|

  config.vm.box = 'centos/7'

  config.vm.hostname = "origin"
  config.vm.network "private_network", ip: "192.168.77.21"
  config.vm.box_check_update = false
  config.vm.synced_folder ".idea/", disabled: true
  config.vm.provider "virtualbox" do |v|
    #play with this value
    v.memory = 12000
    v.cpus = 4
  end

  config.vm.provision "shell", path: "openshift-bootstrap"

end