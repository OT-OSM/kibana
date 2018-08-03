osm_kibana
----------
This repo is configuring kibana which is accessed by nginx for mutil version OS. This repo by default install kibana 6 but can be dynamic by passing extra-vars or changing the values in ```vars/main.yml```

Kibana Directory Structure
--------------------------
```
├── osm_kibana
│   ├── handlers
│   │   └── main.yml
│   ├── meta
│   │   └── main.yml
│   ├── tasks
│   │   ├── Debian.yml
│   │   ├── main.yml
│   │   └── Redhat.yml
│   ├── templates
│   │   ├── default.j2
│   │   ├── kibana.yml.j2
│   │   └── nginx.conf.j2
│   └── vars
│       └── main.yml
├── README.md
└── site.yml
```

Supported OS
------------
```
   This role will work on the following operating systems:

   * Centos 6
   * Centos 7
   * Ubuntu 14/16
   * Debian 14/16
   * Redhat 6/7
```

Role Name
=========

A brief description of the role goes here.

Requirements
------------
The only requirment is python-common-software-properties in Debian based Operating System.

Role Variables
--------------

Available variables are listed below, along with default values [vars](https://github.com/opstree-ansible/osm_kibana/blob/master/vars/main.yml)


Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: "{{ host }}"
      roles:
         - { role: osm_kibana }

License
-------

BSD

Author Information
------------------
###### vishant.sharma@opstree.com

###### 9871665962

###### www.opstree.com

###### blog.opstree.com
