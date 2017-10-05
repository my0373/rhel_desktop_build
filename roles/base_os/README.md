base_os
=========

This role is designed to allow the initial configuration and setup of a RHEL host.

The steps to be performed include

* Create a new user and group called ansible.
* Allow that user passwordless sudo access.
* Install an SSH public key for the ansible user.
* Look for, and patch any kernel updates.
* Reboot (if required) to allow kernel patches to take effect.
* Update all other packages



Requirements
------------
This role is designed to be run against any RHEL 7.x system that needs to be brought into some level of compliance. At the time of writing, this includes RHEL Server 7.x and RHEL 7.x Desktop.


Role Variables
--------------

The public ssh key we will use to connect to the ansible user.

Example:
    
    SSH_PUBLIC_KEY: "ssh-rsa AAAAB3NzaAADAQABAAABAQCnzhBptmPWnckR97d0Lwlb1nLxGmAOI6wevZhimY37k1n44k+YFPK6oygcwmWHUCwlBm+ZXQoqwR96aSIBAi6ZelNp5l9/U0JD4s0DTR4/M9vKCWSyImgC69ul10f0poLkCsjOG/PPuRe4XUfwzqmKi5YOMjzbceg+ODO8cZYebRH3cUHdgvblnIui+ADSOFMUBIUj9SA1zhg48ApJT4UT/N0kuR1Jik/tcApto35nlmxH99EUeorspjret6KTYNSj5mSaNIf7punowE/HiXTsENkoOe22q/AdkkHmn9oydcXmy3NWDd+tfWk5HRe0GFREfq//Ni4HKLZL+n3n0pBJ"
    
Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
      
    ---
    - name: Configure the desktop hosts to be compliant and secure
      hosts: all
      roles:
         - { role: base_os, username: myork }

License
-------

MIT

Author Information
------------------

myork - my0373 - at; - gmail.com 