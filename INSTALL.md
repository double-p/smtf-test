Groundworks
=======
packer
------
- adapt ./Packer/OpenBSD-config.json if need be
- cd Packer && packer build -var-file=OpenBSD-config.json OpenBSD-60.json && cd ..

vagrant
-----
- vagrant box add obsd60 Packer/packer_vbox-obsd60-amd64_virtualbox.box
- Vagrantfile as provided
- vagrant up #takes <3 min on my MBP
- vagrant ssh-config > sshconf
  enables us to scp easily (e.g. scp -F sshconf INSTALL.md tenant1.21:.)
