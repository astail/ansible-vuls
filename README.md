# ansible-vuls

## vagrant

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
