# Install OpenKinect in Beagle board

First, install every software and library related to OpenKinect as follows:
```bash
FREENECT_PKGS=$(apt-cache --names-only search freenect | awk '{ print $1 }' | grep -v bad-pkg)
sudo apt-get -y install $FREENECT_PKGS
```

After installing, you need to add permisions for accessing the kinnect:
```bash
sudo curl -O "/etc/udev/rules.d" 
```
