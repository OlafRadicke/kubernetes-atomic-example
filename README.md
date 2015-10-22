## Ein Beispiel-Projelt ##

### Ziel ###

Das Wechselspiel zwischen Ansible, Docker, Kubernets und Atomic ausprobieren.


## Die Playbooks ##

### Erstellung des Clusters ###

```
ansible-playbook -vvvv  -i ./hosts ./init-cluster.ymlansible-playbook -vvvv  -i ./hosts ./init-cluster.ymlansible-playbook -vvvv  -i ./hosts ./init-cluster.yml
```

### Verwaltung der des Clusters ###
```
ansible-playbook -vvvv  -i ./hosts ./config-cluster.yml
```

## Login ##

default user: *fedora* (mit Fedora-Images) bzw. *centos* (mit CentOS-Images)
Passwort: *atomic* (wenn der ssk-key nicht greift)

Zusatz-User: *ansible*
Kein Passwort

## Externe Dokus ##

* [Workshop-Docker: Container mit Kubernetes managen](http://www.admin-magazin.de/Das-Heft/2015/03/Workshop-Docker-Container-mit-Kubernetes-managen)
* [Kubernetes: services](http://kubernetes.io/v1.0/docs/user-guide/services.html)
* [cloudinit](https://cloudinit.readthedocs.org/en/latest/)
