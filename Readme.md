Source OS (with Ansible): 

 - Debian GNU/Linux 10 (buster)


Destination OSes:

 - Ubuntu 18.04.3 LTS (bionic)
 - CentOS Linux release 7.7.1908 (Core)
 - FreeBSD 12.0-RELEASE r341666 GENERIC  amd64


For SSH-key access:

1. ssh-keygen
2. ssh-copy-id username@remote_host



Usage:

1. PING:
    ansible yd77work -m ping

2. NGINX install/enable/restart:
    ansible-playbook nginx.yml -k -K

3. INSTALL zip/unzip/gzip/nano, REMOVE unzip/nano WITH "with_items deprecated warnings"
    ansible-playbook zipponano.yml -k -K

4. INSTALL zip/unzip/gzip/nano, REMOVE unzip/nano WITHOUT "with_items deprecated warnings"
    ansible-playbook zipnano_no_depr.yml -k -K
