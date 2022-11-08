nfs_client
=========

A role to mount multiple NFS shares to a host.

Requirements
------------

None.

Role Variables
--------------

    nfs_server: The IP/FQDN of the NFS server you are connecting to. Example: mynas.somedomain.com

    nfs_volume: Volume on the remote server to connect to. Example: volume1

    mount_options: NFS Mount options to be used. Example: "rw,async,soft"
    
    mount_path: Where to mount the NFS share on the local server. Default is /mnt/share

    fstype: Filesystem of the remote server. Default is nfs

    nfs_mounts: List of shared folders on the remote to mount. This should be defined at either the host or group level.

Dependencies
------------

None.

Example Playbook
----------------

    - name: Mount NFS shares
      hosts: all
      become: yes
      roles:
        - nfs_client
      tags:
        - nfs_client

         ---


License
-------

GPLv3
