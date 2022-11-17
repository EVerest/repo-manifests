# repo-manifests

Repo manifests for Phytec boards.

Get the phyLinux tool:

```
wget https://download.phytec.de/Software/Linux/Yocto/Tools/phyLinux
chmod +x phyLinux
```

Setup the yocto build environment:

```
./phyLinux init -u https://github.com/EVerest/repo-manifests
echo 'ACCEPT_FSL_EULA = "1"' >> build/conf/local.conf
. ./sources/poky/oe-init-build-env
```

Now you can use bitbake. To build a basic headless image with EVerest SIL support type:

```
bitbake phytec-headless-everest-sil-image
```


