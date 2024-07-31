
Vagrant.configure("2") do |config|
  config.vm.box = "write-os"
  config.vm.box_url = "https://general-1258399584.cos.ap-shanghai.myqcloud.com/vagrantboxs/write-os.box"
  
  config.vm.define "write_os" do |write_os|
      
    config.vm.provider "virtualbox" do |vb|
      vb.name = "Write OS"
      vb.memory = "4096"
      vb.cpus = "2"
      vb.customize ['modifyvm', :id, '--graphicscontroller', 'vmsvga']
      vb.customize ['modifyvm', :id, '--vram', '256']
      vb.customize ["modifyvm", :id, "--accelerate3d", "on"]
      vb.customize ["modifyvm", :id, "--clipboard-mode", "bidirectional"]
      vb.customize ["modifyvm", :id, "--draganddrop", "bidirectional"]
      #vb.customize ["setextradata", :id, "GUI/ScaleFactor", "2"]
      #vb.customize ["setextradata", :id, "GUI/LastGuestSizeHint", "1920,1080"]
      #vb.customize ["setextradata", :id, "GUI/Fullscreen", "true"]
       
      vb.gui = true
    end
  end
  config.vm.provision "shell", path: "scripts/bochs_install.sh", privileged: false
  
end