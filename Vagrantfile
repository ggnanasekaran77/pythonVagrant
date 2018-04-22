Vagrant.configure("2") do |config|
 config.vm.box = "ubuntu/trusty64"
  config.vm.network "private_network", ip: "10.10.10.20"
  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
  end
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "setup.yml"
  end
end
