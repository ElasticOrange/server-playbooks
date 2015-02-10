<b>Mail Server Using <a href="http://www.postfix.org/">Postfix</a>, <a href="http://www.dovecot.org/">Dovecot</a>, <a href="http://www.mysql.com/">MySQL</a>, and <a href="http://spamassassin.apache.org/">SpamAssasin</a></b><br>

<b>Requirements</b><br>
This role requires <a href="http://www.ansibleworks.com/">Ansible</a> version 1.7.2 or higher and the Debian/Ubuntu platform.<br>

<b>How to use</b>
Install <a href="http://www.ansibleworks.com/">Ansible</a>.<br>
The server should be accessible by typing:<br>
<i>ssh root@server_ip_address</i><br><br>
Open the file with root privileges like this:<br>
<i>sudo nano /etc/ansible/hosts</i><br>
The syntax we are going to use though looks something like this:<br>
<i>[group_name]<br>
alias ansible_ssh_host=server_ip_address</i><br>
You should have something like:<br>
<i>[test]<br>
host1 ansible_ssh_host=192.168.0.100 ansible_ssh_port=22 ansible_ssh_user=root</i><br><br>