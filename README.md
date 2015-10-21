## Ein Beispiel-Projelt ##

### Ziel ###

Das Wechselspiel zwischen Docker, Kubernets und Atomic ausprobieren.


## Cloud-init-Imitge genereieren ##
```
genisoimage -output cloud-init-config.iso -volid cidata -joliet -rock user-data meta-data
```

## Externe Dokus ##

* [Workshop-Docker: Container mit Kubernetes managen](http://www.admin-magazin.de/Das-Heft/2015/03/Workshop-Docker-Container-mit-Kubernetes-managen)
* [Kubernetes: services](http://kubernetes.io/v1.0/docs/user-guide/services.html)
* [cloudinit](https://cloudinit.readthedocs.org/en/latest/)
