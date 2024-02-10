Vagrant.configure(2) do |config|
  # образ системы Ubuntu 18/04 LTS (Bionic Beaver)
  config.vm.box = "ubuntu/focal64"
  # не проверять репозиторий на наличие обновлений
  config.vm.box_check_update = false

  config.vm.provider "virtualbox" do |vb|
    # имя виртуальной машины
    vb.name = "testserver"
    # объем оперативной памяти
    vb.memory = 512
    # количество ядер процессора
    vb.cpus = 1
  end
  
  # hostname виртуальной машины
  config.vm.hostname = "testserver"
  config.vm.network "forwarded_port", guest: 80, host: 8080, id: "web1"
  config.vm.network "forwarded_port", guest: 443, host: 8443, id: "web1"
end
