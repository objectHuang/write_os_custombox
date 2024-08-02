
Vagrant.configure("2") do |config|
  config.vm.box = "write-os-allin"
  config.vm.box_url = "https://general-1258399584.cos.ap-shanghai.myqcloud.com/vagrantboxs/write-os-allin.box"
  
  config.vm.define "ubuntu_write_os" do |write_os|
      
    config.vm.provider "virtualbox" do |vb|
      vb.name = "Ubuntu Write OS"
      vb.memory = "4096"
      vb.cpus = "2"    
      vb.customize ["modifyvm", :id, "--clipboard-mode", "bidirectional"]
      vb.customize ["modifyvm", :id, "--draganddrop", "bidirectional"]    
      vb.gui = true
    end
  end
end