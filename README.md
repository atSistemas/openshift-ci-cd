# openshift-ci-cd
CI/CD Demo based on Openshift

## Objective
Due to minishift/oc cluster up limitations to support *logging and metrics* we use Vagrant to provision openshift in a single vm.
This setup allows us to have fully-functional *logging and monitoring* within the platform.

## Requirements
- [Vagrant](https://www.vagrantup.com/downloads.html) 2.0+
- 16GB RAM

## Run
```
vagrant up
```
## Add local DNS lookup

```
#append the following to your /etc/hosts file
192.168.77.21 console.openshift hawkular-metrics.apps.openshift gogs-cicd.apps.openshift jenkins-cicd.apps.openshift nexus-cicd.apps.openshift sonarqube-cicd.apps.openshift kibana.apps.openshift
```
## Access openshift
```
#username: developer
#password: any
https://console.openshift:443
```

## Deploy CI-CD demo to openshift *WIP*
```
#ssh into vagrant vm
[locahost] vagrant ssh
[vagrant@origin ~]$  sudo su -
[root@origin ~]$  cd /vagrant/demo-ci-cd/
[vagrant@origin ~]$  chmod +x demo-*
[vagrant@origin ~]$  ./demo-bootstrap
```