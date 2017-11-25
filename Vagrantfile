Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.synced_folder ".", "/home/ubuntu/Krypto-trading-bot"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install build-essential software-properties-common -y
    add-apt-repository ppa:ubuntu-toolchain-r/test -y
    apt-get update
    apt-get install gcc-snapshot -y
    apt-get update
    apt-get install gcc-6 g++-6 -y
    update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-6 60 --slave /usr/bin/g++ g++ /usr/bin/g++-6
    SHELL
end
