Role Name  Incron 
========

A brief description of the role goes here.

Incron works similar way as the regular cron. The difference is that the inotify cron handles filesystem events rather than time periods.

Requirements
------------

There are no any special requirments in Debian Family and in RedHat Family [libselinux-pyhton](ftp://195.220.108.108/linux/fedora-secondary/updates/testing/27/aarch64/l/libselinux-python-2.7-2.fc27.aarch64.rpm) package should be installed.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in [defaults](https://github.com/opstree-ansible/osm_incron/blob/master/defaults/main.yml), [vars](https://github.com/opstree-ansible/osm_incron/blob/master/vars/main.yml), and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------
There are no any futher dependecies for this role.

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: "{{ hosts }}"
      roles:
         - osm_incron
         
    - hosts: incron_server
 -hosts: '{{ hosts }}
  roles:
   - role: osm_incron
     incron_system_tables:
       - name: incron_test
         path: /home/vagrant/incron_test1 // this is a variable which needs to be change as per our requirement.
         mask: IN_MODIFY  // this can be anything like IN_CREATE ,IN_ACCESS etc
         command: touch /home/newfile     // this is a variable where we mention what command has to be run if the given speified condition  is met

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed) .
