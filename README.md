jb-mr2 local_manifest
======================

Local Manifest for building AOKP on our supported Devices

Getting Started
---------------

To get started with Android, you'll need to get
familiar with [Git and Repo](http://source.android.com/download/using-repo).

Make a build directory:

	mkdir Andoid (or whatever name you choose)
	cd Android (or the name  you chose)
	mkdir .repo/local_manifests

Init repo only for official devices first:

    repo init -u https://github.com/AOKP/platform_manifest.git -b jb-mr2 -g all,-notdefault,flo,grouper,toro,jfltevzw,xt1060,asus,samsung,motorola

Then download additional repo's for unofficial devices:

    curl -L -o .repo/local_manifests/droidfx.xml -O -L https://raw.github.com/droidfx/local_manifest/jb-mr2/droidfx.xml
 
    	( or Download: https://github.com/droidfx/local_manifest/blob/jb-mr2/droidfx.xml
		and place it in your ~/Android/.repo/local_manifest.xml (or ~/'name you choose'/.repo)

Then sync up:

    repo sync
