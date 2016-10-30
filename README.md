# Docker for Mac Beta

This is a Vagrant test environment to run the Docker for Mac Beta in a VMware Fusion vagrant box. You need an OSX Vagrant box, eg. built with https://github.com/boxcutter/macos and VMware Fusion 8 and Vagrant 1.8.x. Or maybe one of the boxes at Atlas https://atlas.hashicorp.com/boxes/search?utf8=✓&sort=&provider=&q=osx may help you skip the `packer build` step.

```
vagrant up
```

On the desktop the DMG file appears after a while. It is also cached on the shared folder, so you can easily destroy and rebuild the Vagrant box again and again.

When you start the app for the first time, you'll be asked to enter your invitation code (token). Your private invitation code is:

```
pass docker-mac-beta | pbcopy
```

Please note that these apps are under active development! We do expect things to break and with your feedback we'll be working hard to fix bugs, implement new features, and make design improvements.

## Getting started

https://docs.docker.com/docker-for-mac/

## Download the app
https://download.docker.com/mac/beta/Docker.dmg
