OSM_KIBANA
==========
This repo is configuring kibana. This repo by default install kibana 7 but can be dynamic by passing extra-vars or changing the values in ```vars/main.yml```

Version History
---------------

|**Date**| **Version**| **Description**| **Changed By** |
|----------|---------|---------------|-----------------|
|**April '03** | v.1.0 | Initial Draft | Vishant Sharma |

Supported OS
------------
```
   This role will work on the following operating systems:

    * ubutnu 14
    * ubuntu 16
    * RHEL/CENTOS 6
    * RHEL/CENTOS 7
    * Amazon AMI
```

Requirements
------------
```
The only requirment is root access of the server and python-common-software-properties in Debian based Operating System.
```

Role Variables
--------------

|**Variable**|**Default Value**|**Description**|
|------------|-----------------|---------------|
| kibana_version_series | 7 | Kibana series version series |
| kibana_version | 7.5.1 | Kibana specific version |
| kibana_version_rpm | 7.5.1 | Kibana specific version |
| es_username | elastic | Username of Elastic search |
| es_password | elastic@pass | Password for Elastic search |
| kibana_server_ip | 0.0.0.0 | Server IP for Kibana |
| kibana_port | 5601 | Port on which kibana runs |
| elasticsearch_port | Value of Elastic Search port |
| elasticsearch_ip | 192.168.1.2 | Ip address of Elastic search |

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
│   │   ├── kibana.yml.j2
│   └── vars
│       └── main.yml
├── README.md
└── site.yml
```
Inventory
---------
An example inventory could be like this:-

```ini
[kibana]
kibana_server ansible_user=ubuntu
```

Example Playbook
----------------

Here is an example of playbook to execute this role:-

```yaml
---
- hosts: kibana
  roles:
    - role: osm_kibana
```

Futuristic Scopes
-----------------
```
Integrating kibana dashboards in ansible role.
```
License
-------

BSD

Author Information
------------------
**[vishant.sharma](vishant.sharma@opstree.com)**

###### www.opstree.com
###### blog.opstree.com
