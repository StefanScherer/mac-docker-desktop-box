# Docker Desktop for Mac

This is a Vagrant test environment to run Docker Desktop for Mac in a VMware
Fusion vagrant box. You need an OSX Vagrant box, eg. built with
https://github.com/boxcutter/osx and VMware Fusion 11.0.3 and Vagrant 2.2.x. Or
maybe one of the boxes in the Vagrant Cloud https://app.vagrantup.com/boxes/search?provider=vmware&q=macos&sort=downloads&utf8=%E2%9C%93 may help
you skip the `packer build` step.

```
vagrant up
```

On the desktop the DMG file appears after a while. It is also cached on the
shared folder, so you can easily destroy and rebuild the Vagrant box again and
again.

## Getting started

* https://store.docker.com/editions/community/docker-ce-desktop-mac
