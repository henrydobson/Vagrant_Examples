Vagrant.configure(2) do |config|
  config.vm.box = "YOUROSXBOX"
  config.vm.hostname = "HOSTNAME"
  config.vm.synced_folder "/path/to/source", "/path/to/destination", create: true
  config.vm.provision "file", source: "/path/to/source/enrolpkg", destination: "/path/to/destination/enrolpkg"
config.vm.provision "shell", inline: "sudo installer -pkg /path/to/destination/enrolpkg -target / && sudo reboot"
config.ssh.insert_key = false
  config.vm.provider "vmware_fusion" do |v|
        v.gui = true
        v.vmx["memsize"] = "4096"
        v.vmx["numvcpus"] = "2"
        v.vmx["serialNumber"] = "SERIALNUMBER"
  end
end
