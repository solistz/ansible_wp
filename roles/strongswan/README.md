https://www.vitaliy.org/post/7243

GITHUB

IPTABLES rules for strongswan
strongswan/testing/tests/ha/both-active/hosts/alice/etc/iptables.rules
https://github.com/strongswan/strongswan/blob/master/testing/tests/ha/both-active/hosts/alice/etc/iptables.rules

config strongswan + iptables
https://www.digitalocean.com/community/tutorials/how-to-set-up-an-ikev2-vpn-server-with-strongswan-on-ubuntu-16-04


/etc/sysctl.conf

net.ipv4.ip_forward = 1
net.ipv4.conf.all.accept_redirects = 0
net.ipv4.conf.all.send_redirects = 0
net.ipv4.conf.default.rp_filter = 0
net.ipv4.conf.default.accept_source_route = 0
net.ipv4.conf.default.send_redirects = 0
net.ipv4.icmp_ignore_bogus_error_responses = 1


Create Dir
- name: сreate directory
  file:
    path=/src/www
    mode=0755
    owner=root
    group=root
    state=directory

ansible-playbook -i test-project/inventory.txt playbook.yml

Copy directory(recurs)
scp -r username@example.com:/remote/path/to/directory  /local/path
scp -r /local/directory/path username@example:/remote/directory/path
scp -i /path/to/key username@example.com:/remote/path/to/file /local/path

Erorr
TPM 2.0 - could not load
apt install libtss2-tcti-tabrmd0