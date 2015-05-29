# vagrant-memex
DARPA MEMEX project Vagrant VM

Notes:
Since the Guest OS is behind a NAT, we set the SPARK_LOCAL_IP using the tun0 interface as the IP address.  This is done in the spark-env.sh file

Please make sure that vbguest is installed (https://github.com/dotless-de/vagrant-vbguest/).  It helps keep the VirtuaalBoxGuestAdditions up to date, install on the cmd line:

vagrant plugin install vagrant-vbguest

When starting this on Linux, do not use your distribution's Vagrant package to install vagrant. Install from Vagrantup.com to ensure you're using the latest version of Vagrant. Using old versions of Vagrant will result in errors.



######PySpark ML Library:
Although numpy is already in your VM, there may be some issues with numpy in the PySpark interpreter. Using the ML Library requires you to make sure numpy is functioning or you will recieve an import error in PySpark ![alt tag](http://s24.postimg.org/juodavkpx/Screen_Shot_2015_05_29_at_10_56_59_AM.png) 

You need to add the export PYTHONPATH=/usr/local/lib/python2.7/site-packages to your the _/.profile files
