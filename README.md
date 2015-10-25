## Ein Beispiel-Projelt ##

### Ziel ###

Das Wechselspiel zwischen Ansible, Docker, Kubernets und Atomic ausprobieren.


## Die Playbooks ##

### Erstellung des Clusters ###

```
ansible-playbook -vvvv  -i ./hosts ./init-cluster.ymlansible-playbook -vvvv  -i ./hosts ./init-cluster.ymlansible-playbook -vvvv  -i ./hosts ./init-cluster.yml
```

### Verwaltung der Cluster VMs ###
(Aus Virtualiesierungssicht)
```
ansible-playbook -vvvv  -i ./hosts ./config-cluster-kvm
```

### Verwaltung des Kubernetes Cluster ###
```
ansible-playbook -vvvv  -i ./config-cluster-hosts
```

## Login ##

ssh-key erstellen
```
ssh-keygen -f atomic_rsa
```

default user: *fedora* (mit Fedora-Images) bzw. *centos* (mit CentOS-Images)
Passwort: *atomic* (wenn der ssk-key nicht greift)

Zusatz-User: *ansible*
Kein Passwort

## IP-Adressen herausfinden ##

```
[root@prag ansible]# cat /var/lib/libvirt/dnsmasq/*
##WARNING:  THIS IS AN AUTO-GENERATED FILE. CHANGES TO IT ARE LIKELY TO BE
##OVERWRITTEN AND LOST.  Changes to this configuration should be made using:
##    virsh net-edit default
## or other application using the libvirt API.
##
## dnsmasq conf file created by libvirt
strict-order
pid-file=/var/run/libvirt/network/default.pid
except-interface=lo
bind-dynamic
interface=virbr0
dhcp-range=192.168.122.2,192.168.122.254
dhcp-no-override
dhcp-lease-max=253
dhcp-hostsfile=/var/lib/libvirt/dnsmasq/default.hostsfile
addn-hosts=/var/lib/libvirt/dnsmasq/default.addnhosts
[
    {
        "ip-address": "192.168.122.230",
        "mac-address": "52:54:00:13:09:8e",
        "expiry-time": 1445504272
    }
]
```

## Externe Dokus ##

* [Workshop-Docker: Container mit Kubernetes managen](http://www.admin-magazin.de/Das-Heft/2015/03/Workshop-Docker-Container-mit-Kubernetes-managen)
* [Kubernetes: services](http://kubernetes.io/v1.0/docs/user-guide/services.html)
* [cloudinit](https://cloudinit.readthedocs.org/en/latest/)
* [atomic quickstart](http://www.projectatomic.io/docs/quickstart/)
