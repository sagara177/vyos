Create VyOS minimum image
=========================

Originaly created by Radovan Brezula ( http://brezular.com/2014/07/12/vyos-x64-installation-on-qemu/ )

Setup
-----

    yum install -y telnet
    yum install -y expect

Image Create
------------

    chmod a+x deploy_vyos
    chmod a+x install_vyos
    ./deploy_vyos


Optional: Convert QCOW2 to VMDK
-------------------------------

    qemu-img convert vyos-1.1.0.x86_64.qcow2 -O vmdk vyos-1.1.0-`date '+%Y%m%d'`.0.x86_64.vmdk
