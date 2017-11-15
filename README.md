# ansible-vuls

## vagrant

### vuls

1. install vagrant
2. ` MacBook-Pro % brew install git ansible`
3. ` MacBook-Pro % git clone git@github.com:astail/ansible-vuls.git`
4. ` MacBook-Pro % cd ansible-vuls`
5. ` MacBook-Pro % vagrant plugin install vagrant-hostmanager`
6. ` MacBook-Pro % vagrant up`
7. ` MacBook-Pro % ssh vuls@vuls.vagrant.com -i roles/vuls/files/id_rsa_vuls`
8. `[vuls@vuls ~]$ vuls configtest`
9. `[vuls@vuls ~]$ vuls scan`
10. `[vuls@vuls ~]$ vuls report -format-short-text | less`

### vuls-repo

1. ` MacBook-Pro % ssh vuls@vuls.vagrant.com -i roles/vuls/files/id_rsa_vuls`
2. `[vuls@vuls ~]$ cd /home/vuls/vulsrepo/server`
3. `[vuls@vuls ~]$ ./vulsrepo-server`
4. http://vuls.vagrant.com:5111/

## mac

1. ` MacBook-Pro % brew install git ansible`
2. ` MacBook-Pro % git clone git@github.com:astail/ansible-vuls.git`
3. ` MacBook-Pro % cd ansible-vuls`
4. ` MacBook-Pro % ansible-playbook -i inventory/hosts site.yml -lmac`
5. ` MacBook-Pro % cd ~/vuls`
6. ` MacBook-Pro % cp config.toml.sample config.toml`
7. fix config.toml
8. ` MacBook-Pro % vuls configtest`
9. ` MacBook-Pro % vuls scan`
10. ` MacBook-Pro % vuls report -format-short-text | less`

## my_server

1. `MacBook-Pro % vim inventory/hosts`
2. 111.111.111.111  => your server ip address
3. ssh_user_name    => your server ssh user
4. ansible_ssh_port => your server ssh port
5. ~/.ssh/id_rsa    => your server ssh key
6. `MacBook-Pro % ansible-playbook -i inventory/hosts site.yml -l my_server`
