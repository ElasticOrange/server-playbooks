#Mail Server Using <a href="http://www.postfix.org/">Postfix</a>, <a href="http://www.dovecot.org/">Dovecot</a>, <a href="http://www.mysql.com/">MySQL</a>, and <a href="http://spamassassin.apache.org/">SpamAssasin</a>

##Requirements
--------------
This role requires <a href="http://www.ansibleworks.com/">Ansible</a> version 1.7.2 or higher and the Debian/Ubuntu platform.

##How to use
------------
* Install <a href="http://docs.ansible.com/intro_installation.html#id14">Ansible Via Apt (Ubuntu)</a> on your local machine.

* The remote server should be accessible through ssh by typing:
```
ssh root@server_ip_address
```

* Open the file with root privileges like this:
```
sudo nano /etc/ansible/hosts
```

```
The syntax we are going to use though looks something like this:
[group_name]
alias ansible_ssh_host=server_ip_address
```

* You should have something like:
```
[test]
host1 ansible_ssh_host=192.168.0.100 ansible_ssh_port=22 ansible_ssh_user=root
```

* Run it with:
```
ansible-playbook /path/to/file/email.yml
```

##Variables here
----------------

```
* servermail mysql database settings:
mail_db_name: servermail 
mail_db_user: usermail
mail_db_password: mypasswordhere

* email domains you want to use:
domain_com: example.com
hostname_domain_com: hostname.example.com


* add email account: user@domain.com with account_password:
account_password: firstpassword
useratdomain_com: rambo@example.com
user: rambo

* add alias email. all emails from alias will be sent to
user@domain.com
aliasatdomain_com: stallone@example.com
alias: stallone

postfix_dir: /etc/postfix

* ssl self-signed certificates:
Country: RO
State: Bucharest
Locality: Bucharest
Organization: Elasticorange
OrgUnit: IT
FQDN: example.com
```