Memcached Ansible Role
=========

![HE:Labs](https://raw.githubusercontent.com/Helabs/helabs.github.com/master/images/logo.png "HE:Labs")

This is a simple role, based on [bennojoy/memcached](https://github.com/bennojoy/memcached)
that installs and configures Memcached.

Requirements
------------

This role only requires Ansible version 1.4+

Role Variables
--------------

All variables should be overwritten at the playbook level. Those are:

`memcached_port` - Memcached default port to bind on:

    11211

`memcached_listen_address` - Memached listen address to bind on:

    0.0.0.0

`memcached_max_conn` - Memcached maximum number of connections to accept:

    1024

`memcached_cache_size` - Memcached cache size:

    64

`memcached_fs_file_max` - System-wide File Descriptors (FD) Limits:

    756024

Dependencies
------------

This role has no dependecies

Using this role
----------------

Using this roles as as simples as:

    - hosts: servers
      gather_facts: true
      vars:
        memcached_max_conn: 2048
        memcached_cache_size: 128
        memcached_fs_file_max: 1512048
      roles:
         - helabs.memcached

License
-------

BSD

Author Information
------------------

Lucas do Amaral Saboya Works as DevOps/SysOps @ [HE:Labs](https://www.helabs.com)
