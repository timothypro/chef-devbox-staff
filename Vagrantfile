Vagrant.configure("2") do |config|
    config.vm.box = "chef/ubuntu-14.04"
    config.vm.network :private_network, ip: "192.168.33.10"
    config.vm.provider "virtualbox" do |v|
        v.name = "unibox-1"
        v.customize ["modifyvm", :id, "--memory", "2048"]
        # v.customize ["modifyvm", :id, "--cpuexecutioncap","90"]
        # v.customize ["modifyvm", :id, "--cpus",4]
        # v.customize ["modifyvm", :id, "--nictype1", "virtio"]
        # v.customize ["modifyvm", :id, "--nictype2", "virtio"]
        # v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
        # v.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
        # v.auto_nat_dns_proxy = false
    end
    config.vm.provision "shell", path: "https://raw.githubusercontent.com/AOEpeople/chef-devbox/master/setup.sh"
end
