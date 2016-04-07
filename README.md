Zookeeper
=========

[![Build Status](https://travis-ci.org/abelboldu/ansible-zookeeper.svg?branch=master)](https://travis-ci.org/abelboldu/ansible-zookeeper)

Zookeeper cluster role for MidoNet deployments.

Requirements
------------

Ubuntu or RedHat/CentOS

Role Variables
--------------

`zookeeper_hosts` should be a dictionary or group in hosts inventory. 
`myid` variable will be assigned dynamically across hosts in the group.

Example:

```
[zookeeper]
zk1.midoexample.net
zk2.midoexample.net
zk3.midoexample.net
```
```
zookeeper_hosts: '{{ groups["zookeper"] }}'
```


Dependencies
------------

Java ( geerlingguy.java )
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
