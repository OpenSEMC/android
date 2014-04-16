OpenSEMC
===========


Getting Started
---------------

To get started with TeamEOS, you'll need to get
familiar with [Git and Repo](http://source.android.com/source/using-repo.html).

Init core trees without any device/kernel/vendor :

    $ repo init -u git://github.com/OpenSEMC/android.git -b kk4.4

Init repo with all devices, kernels and vendors supported by TeamEOS :

    $ repo init -u git://github.com/OpenSEMC/android.git -b kk4.4 -g all,kernel,device,vendor

Init repo only for a particular device :

    $ repo init -u git://github.com/OpenSEMC/android.git -b kk4.4 -g all,-notdefault,<devicename>,<vendorname>

For example, to init only trees needed to build nozomi :

    $ repo init -u git://github.com/OpenSEMC/android.git -b kk4.4 -g all,-notdefault,nozomi,sony


Then to sync up:

    repo sync
