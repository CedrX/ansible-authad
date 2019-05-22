Role Name
=========

Join Linux workstation to active directory 

Requirements
------------

Redhat family workstation or Debian family workstation

Role Variables
--------------

  * *authad_workgroup* : WORKGROUP
  * *authad_realm* : EXAMPLE.COM
  * *authad_pdc* : fqdn of primary domain controller
  * *authad_sdc* : fqdn of secondary domain controller
  * *authad_ldap_base* : LDAP search base
  * *authad_username* : User that has privileges to join workstations
  * *authad_password*: Password of this user
  * *authad_server_ou* : Organizational Unit where computers objects will be stored
  * *authad_access_filter* : LDAP search query to limit who can login to the server


Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: authad, tags: [ 'authad','active-directory' ] }

License
-------

MIT

Author Information
------------------

Cédric TINTANET (Senior IT Architect)
# ansible-authad
