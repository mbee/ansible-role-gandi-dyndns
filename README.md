ansible-role-gandi-dyndns
=========

Ansible role to install a script which updates a DNS A record with the outbound IP.
The script will be installed in /usr/local/bin/update-dns.sh and will run every 5 mn.

Requirements
------------

- debian
- a gandi account
- a gandi API key
- a subdomain.domain A entry with a TTL of 300s.

Role Variables
--------------

| Variable | Default | Usage |
|----------|---------|-------|
| web_api_key | | The gandi API key |
| web_domain | | domain (ie google.com) |
| web_subdomain | | subdomain (ie www) |

Dependencies
------------

None

Example Playbook
----------------

  - hosts: servers
    roles:
      - role: mbee.ansible-role-gandi-dyndsn
        vars:
          web_api_key: XXXXXXXX
          web_domain: google.com
          web_subdomain: www

License
-------

BSD
