ENV['VAGRANT_DEFAULT_PROVIDER'] = 'libvirt'

Vagrant.configure("2") do |config|
  config.vm.define "bab" do |config|
    config.vm.hostname = "bab"
    config.vm.box = "generic/ubuntu1804"
    config.vm.box_check_update = false
    config.vm.network "public_network", dev: "endless_swap", mode: "bridge", type: "bridge"
    config.vm.provider :libvirt do |v|
      v.driver = "kvm"
      v.memory = 400
      v.cpus = 1
      v.storage :file, :size => '2G', :type => 'qcow2'
    end
  end
end
