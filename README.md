ANSIBLE-ROLE-VARNISH-VCS
=====================

Ansible role install Varnish Custom Statistics


## Howto use this role?
This role need to be include in a playbook. 

Call this **Galaxy** role  like this:

````bash
ansible-galaxy install -r requirements.yml 
````

Inside requirements.yml
````yaml
# from GitHub, overriding the name and specifying a specific tag
- src: redbeard28.varnish-vcs
````

More info => [Ansible Docs](https://docs.ansible.com/ansible-container/roles/access.html)

## Requirements

 * Ansible 2.9+

```yaml
- src: redbeard28.varnish-repo
```

Role Variables
--------------

**none**

Dependencies
------------

```yaml
- src: redbeard28.varnish-repo
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yaml
- hosts: all
  roles:
     - { role: redbeard28.varnish-repo, tags: varnish-repo }
     - { role: redbeard28.varnish-vcs, tags: vcs }
```

Molecule testing framework
--------------------------

You can use molecule to test this role.
```bash
image=debian tag="buster" molecule converge 
image=debian tag="buster" molecule verify 
```

Author Information
------------------

Jeremie CUADRADO[¹](mailto:info@redbeard-consulting.fr) from redbeard-consulting.fr
