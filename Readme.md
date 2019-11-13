Source OS (with Ansible):
=========================

Debian GNU/Linux 10 (buster)



Destination OSes (Oracle VM VirtualBox v6.0.14 r133895 (Qt5.11.3)):
===================================================================

Ubuntu 18.04.3 LTS (bionic)

CentOS Linux release 7.7.1908 (Core)

FreeBSD 12.0-RELEASE r341666 GENERIC amd64



For SSH-key access:
===================

ssh-keygen

ssh-copy-id username@remote_host



HOMEWORK #1
===========

Usage:

PING:

ansible yd77work -m ping


NGINX install/enable/restart:

ansible-playbook nginx.yml -K


INSTALL zip/unzip/gzip/nano, UNINSTALL unzip/nano WITH "with_items deprecated warnings":

ansible-playbook zipponano.yml -K


INSTALL zip/unzip/gzip/nano, UNINSTALL unzip/nano WITHOUT "with_items deprecated warnings":

ansible-playbook zipnano_no_depr.yml -K



HOMEWORK #2
===========

Usage:

INSTALL nginx:

ansible-playbook nginx_tags.yml --tags "install_centos" -K

ansible-playbook nginx_tags.yml --tags "install_debian" -K

ansible-playbook nginx_tags.yml --tags "install_freebsd" -K


START nginx:

ansible-playbook nginx_tags.yml --tags "start_nginx_centos" -K

ansible-playbook nginx_tags.yml --tags "start_nginx_debian" -K

ansible-playbook nginx_tags.yml --tags "start_nginx_freebsd" -K


RESTART nginx:

ansible-playbook nginx_tags.yml --tags "restart_nginx_centos" -K

ansible-playbook nginx_tags.yml --tags "restart_nginx_debian" -K

ansible-playbook nginx_tags.yml --tags "restart_nginx_freebsd" -K


STOP nginx:

ansible-playbook nginx_tags.yml --tags "stop_nginx_centos" -K

ansible-playbook nginx_tags.yml --tags "stop_nginx_debian" -K

ansible-playbook nginx_tags.yml --tags "stop_nginx_freebsd" -K


INSTALL zip/unzip/gzip/nano:

ansible-playbook zipnano_tags.yml --tags "install_centos" -K

ansible-playbook zipnano_tags.yml --tags "install_debian" -K

ansible-playbook zipnano_tags.yml --tags "install_freebsd" -K


UNINSTALL unzip/nano:

ansible-playbook zipnano_tags.yml --tags "uninstall_centos" -K

ansible-playbook zipnano_tags.yml --tags "uninstall_debian" -K

ansible-playbook zipnano_tags.yml --tags "uninstall_freebsd" -K
