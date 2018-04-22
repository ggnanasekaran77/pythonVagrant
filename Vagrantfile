
Vagrant.configure("2") do |config|
 config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.network "private_network", ip: "10.10.10.20"
  config.vm.provision :ansible do |ansible|
    ansible.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    ansible.playbook = "setup.yml"
  end
end