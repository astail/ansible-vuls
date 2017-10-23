# ansible-vuls

1. install vagrant and ansible
2. ` MacBook-Pro % vagrant plugin install vagrant-hostmanager`
3. ` MacBook-Pro % vagrant up`
4. ` MacBook-Pro % ssh vuls@vuls.vagrant.com -i roles/vuls/files/id_rsa_vuls`
5. `[vuls@vuls ~]$ vuls configtest`
6. `[vuls@vuls ~]$ vuls scan`
7. `[vuls@vuls ~]$ vuls report -format-short-text | less`
