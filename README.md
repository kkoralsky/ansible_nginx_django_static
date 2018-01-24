Nginx Django staticfiles server
===============================

Nginx as staticfiles server for Django app

Role Variables
--------------

- `http_port` - defaults to: 80
- `domains` - list of domains on which server will run (required)
- `ssl` - if set, provides SSL server
- `cert` - path to SSL cert public key
- `cert_key` - path to SSL private key
- `static_root` - path to static files to serve
- `media_root` - path to media files to serve
- `media_base_path` - defaults to `/media`
- `static_base_path` - defaults to `/static`

Dependencies
------------

- [nginx_base](https://github.com/kkoralsky/ansible_nginx_base)

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: nginx_django_static
           domains: [ static.example.com, www.static.example.com ]
           static_root: /home/django/app/static
           media_root: /home/django/app/media

License
-------

BSD
