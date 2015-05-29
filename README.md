Zookeeper
=========

[![Build Status](https://travis-ci.org/abelboldu/ansible-zookeeper.svg?branch=master)](https://travis-ci.org/abelboldu/ansible-zookeeper)

Zookeeper cluster role for MidoNet deployments.

Requirements
------------

Ubuntu or RedHat/CentOS

Role Variables
--------------

`zookeeper` dictionary or group in hosts inventory, each host with it's myid value. See example:

```
[zookeeper]
zk1.midoexample.net myid=1
zk2.midoexample.net myid=2
zk3.midoexample.net myid=3
```

Dependencies
------------

Midonet repositories ( abelboldu.midonet-repos )

Example Playbook
----------------

```
hosts: zookeeper
  roles:
    - role: abelboldu.zookeeper
      zookeeper_hosts: '{{ groups["zookeeper"] }}'
```



License
-------

Apache 2.0

Author Information
------------------

Abel Boldú < abel.boldu@gmx.com >
