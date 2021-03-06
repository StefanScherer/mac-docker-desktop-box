# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

$script = <<SCRIPT
link="https://download.docker.com/mac/edge/Docker.dmg"
version="2.0.4.1"
dmg="/vagrant/Docker-${version}.dmg"
desktop="/Users/vagrant/Desktop/Docker-${version}.dmg"
if [ ! -f "$dmg" ]; then
  echo "Downloading DMG to shared folder."
  curl -Lo "$dmg" "$link"
fi
echo "Copying DMG to desktop."
mkdir -p /Users/vagrant/Desktop
cp "$dmg" "$desktop"
echo "Now double-click the DMG file."
# Enable HiDPI display modes (requires restart)
sudo defaults write /Library/Preferences/com.apple.windowserver DisplayResolutionEnabled -bool true
SCRIPT

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "osx1013-desktop"

  config.vm.provision "shell", inline: $script, privileged: false

  ["vmware_fusion", "vmware_workstation"].each do |provider|
    config.vm.provider provider do |v, override|
      v.linked_clone = true
      v.gui = true
      v.vmx["memsize"] = "6144"
      v.vmx["numvcpus"] = "2"
      v.vmx["vhv.enable"] = "TRUE"
    end
  end

  config.vm.provider "vmware_fusion" do |v|
    v.vmx["gui.fitguestusingnativedisplayresolution"] = "TRUE"
    v.vmx["mks.enable3d"] = "TRUE"
    v.vmx["mks.forceDiscreteGPU"] = "TRUE"
    v.vmx["gui.fullscreenatpoweron"] = "TRUE"
    v.vmx["gui.viewmodeatpoweron"] = "fullscreen"
    v.vmx["gui.lastPoweredViewMode"] = "fullscreen"
    v.vmx["virtualHW.version"] = "14"
    v.enable_vmrun_ip_lookup = false
  end
end
