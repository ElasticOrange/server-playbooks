<h1>Mail Server Using <a href="http://www.postfix.org/">Postfix</a>, <a href="http://www.dovecot.org/">Dovecot</a>, <a href="http://www.mysql.com/">MySQL</a>, and <a href="http://spamassassin.apache.org/">SpamAssasin</a></h1><br>

<h1>Requirements</h1><br>
This role requires <a href="http://www.ansibleworks.com/">Ansible</a> version 1.7.2 or higher and the Debian/Ubuntu platform.<br>

<h1>How to use</h1><br>
<p> - Install <a href="http://www.ansibleworks.com/">Ansible</a>.</p><br>
<p> - The server should be accessible by typing:</p><br>
<i>ssh root@server_ip_address</i><br><br>
<p> - Open the file with root privileges like this:</p><br>
<i>sudo nano /etc/ansible/hosts</i><br>
<p>The syntax we are going to use though looks something like this:</p><br>
<i>[group_name]<br>
alias ansible_ssh_host=server_ip_address</i><br>
<p> - You should have something like:</p><br>
<i>[test]<br>
host1 ansible_ssh_host=192.168.0.100 ansible_ssh_port=22 ansible_ssh_user=root</i><br><br>
<p> - Run it with:</p><br>
<i><b>ansible-playbook /path/to/file/email.yml</b></i>