Vagrant.configure(2) do |config|
  config.vm.box = "bento/ubuntu-18.04" # 18.04 LTS
  config.vm.hostname = "ansible"
  config.vm.network "private_network", type: "dhcp"

  # Increase memory for Virtualbox
  config.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
  end
  # Increase memory for VMware
  ["vmware_fusion", "vmware_workstation"].each do |p|
    config.vm.provider p do |v|
      v.vmx["memsize"] = "1024"
    end
  end
end