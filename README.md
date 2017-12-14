# Docker for Mac Beta

This is a Vagrant test environment to run the Docker for Mac Beta in a VMware
Fusion vagrant box. You need an OSX Vagrant box, eg. built with
https://github.com/boxcutter/osx and VMware Fusion 10 and Vagrant 2.0.1. Or
maybe one of the boxes at Altas
https://atlas.hashicorp.com/boxes/search?utf8=✓&sort=&provider=&q=osx may help
you skip the `packer build` step.

```
vagrant up
```

On the desktop the DMG file appears after a while. It is also cached on the
shared folder, so you can easily destroy and rebuild the Vagrant box again and
again.

## Getting started

* https://beta.docker.com
* https://docs.docker.com/docker-for-mac/kubernetes/
