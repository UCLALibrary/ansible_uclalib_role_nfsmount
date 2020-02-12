UCLA Library NFS Mount Role [![Build Status](https://travis-ci.com/UCLALibrary/uclalib_role_nfsmount.svg?branch=master)](https://travis-ci.com/UCLALibrary/uclalib_role_nfsmount)
=========

Ansible role to configure nfs mount(s).

Requirements
------------

This role will install the prerequisite packages needed to mount an NFS volume on RHEL and CentOS 7 servers.

Role Variables
--------------

A dictionary with mountpoint information defined under the following schema:

     nfs_mounts:
        avalon:
          type: nfs
          opt: "vers=3,ro"
          src: netapp:/avalonmedia
          mountpoint: /streaming/avalon
        lanews:
          type: nfs
          opt: "vers=3,ro"
          src: netapp:/lanews
          mountpoint: /streaming/lanews
          
Dependencies
------------

No external dependencies, you will likely want to configure a firewall from an external role.

Example Playbook
----------------

This role can be ran with the defaults, but should be customized according to your requirements.

    - hosts: servers
      roles:
         - { role: uclalib_role_nfsmount }

License
-------
Please see [LICENSE](LICENSE)

Author Information
------------------

GitHub [issues](https://github.com/UCLALibrary/uclalib_role_nfsmount/issues) is open in case you'd like to file a ticket or make a suggestion. You can also contact Anthony Vuong at <a href="mailto:avuong@cachemeoutside.io">avuong@cachemeoutside.io</a> if you have a question about the project.
