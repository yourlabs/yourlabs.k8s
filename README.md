Bare host
---------

Deploy a docker-based k8s:

    bigsudo yourlabs.k8s --become @host

Vagrant/VirtualBox
------------------

You can work in a VM if you have vagrant:

    cd yourlabs.k8s
    vagrant destroy -f && vagrant up
    vagrant ssh-config > ssh
    bigsudo . --ssh-common-args="-F ssh" @default --become -v
