# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<SCRIPT
dnf copr enable msehnout/sozu -y
dnf install sozu -y
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.box = "fedora/26-cloud-base"
  config.vm.synced_folder ".", "/vagrant", type: "rsync", rsync__exclude: ".git/", rsync__auto: true
  config.vm.provision "shell", inline: $script
end
