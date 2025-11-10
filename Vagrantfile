# Box / OS
#VAGRANT_BOX = 'generic/rhel8'
VAGRANT_BOX = 'almalinux/9'
# Memorable name for your VM
VM_NAME = 'node1'
# Domain name
VM_DOMAIN = '.example.com'
# VM User — 'vagrant' by default
VM_USER = 'vagrant'
# VM IP address
VM_IP = '192.168.56.21'
# Username on your PC
WIN_USER = 'Elitebook'
# Host folder to sync
HOST_PATH = 'C:/Users/Elitebook/' + WIN_USER + '/' + VM_NAME
# Where to sync to on Guest — 'vagrant' is the default user name
GUEST_PATH = '/home/' + VM_USER + '/' + VM_NAME
# # VM Port — uncomment this to use NAT instead of DHCP
# VM_PORT = 8080


Vagrant.configure(2) do |config|
  # Vagrant box from Hashicorp
  config.vm.box = VAGRANT_BOX
  # VM name in vagrant
  config.vm.define VM_NAME
  # Actual machine name
  config.vm.hostname = VM_NAME+VM_DOMAIN
  # Config network
  config.vm.network :private_network, ip: VM_IP
  # Set VM name in Virtualbox
  config.vm.provider "virtualbox" do |v|
    v.name = VM_NAME
    v.memory = 2048
	v.cpus = "1"
  end
end

