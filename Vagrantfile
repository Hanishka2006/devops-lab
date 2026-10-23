Vagrant.configure("2") do |config|
  # --- Operating system (the box) ---
  config.vm.box = "generic/ubuntu2204"
  config.vm.box_check_update = false
  config.vm.hostname = "tradelive-vm"

  # --- Networking ---
  config.vm.network "private_network", type: "dhcp"

  # --- Shared folder between host and VM ---
  config.vm.synced_folder ".", "/vagrant", type: "rsync"

  # --- Provider: who actually builds the machine ---
  config.vm.provider "libvirt" do |lv|
    lv.memory = 2048
    lv.cpus = 2
  end
end
