VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise32"

  config.vm.provision :shell, inline: "sudo apt-get -y update"
  config.vm.provision :shell, inline: "sudo apt-get -y install vim"
  config.vm.provision :shell, inline: "sudo apt-get -y install openjdk-7-jdk"
  config.vm.provision :shell, inline: "wget http://ftp.unicamp.br/pub/apache/spark/spark-1.5.2/spark-1.5.2-bin-hadoop2.6.tgz"
  config.vm.provision :shell, inline: "tar -zxf spark-1.5.2-bin-hadoop2.6.tgz"  
  
  config.vm.synced_folder "./data", "/vagrant_data"
end
