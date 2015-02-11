<h2>Mail Server Using <a href="http://www.postfix.org/">Postfix</a>, <a href="http://www.dovecot.org/">Dovecot</a>, <a href="http://www.mysql.com/">MySQL</a>, and <a href="http://spamassassin.apache.org/">SpamAssasin</a></h2><br>

<h3>Requirements</h3><br>
This role requires <a href="http://www.ansibleworks.com/">Ansible</a> version 1.7.2 or higher and the Debian/Ubuntu platform.<br>

<h3>How to use</h3><br>
<p> - Install <a href="http://docs.ansible.com/intro_installation.html#id14">Ansible Via Apt (Ubuntu)</a> on your local machine.</p>
<p> - The remote server should be accessible through ssh by typing:</p>
<code>ssh root@server_ip_address</code><br><br>
<p> - Open the file with root privileges like this:</p>
<code>sudo nano /etc/ansible/hosts</code><br>
<p>The syntax we are going to use though looks something like this:</p>
<code>[group_name]<br>
alias ansible_ssh_host=server_ip_address</code><br>
<p> - You should have something like:</p>
<code>[test]<br>
host1 ansible_ssh_host=192.168.0.100 ansible_ssh_port=22 ansible_ssh_user=root</code><br><br>
<p> - Run it with:</p>
<code><b>ansible-playbook /path/to/file/email.yml</b></code>
<h3>Variables here</h3>

servermail mysql database settings
<code>mail_db_name: servermail</code> 
<code>mail_db_user: usermail</code>
<code>mail_db_password: mypasswordhere</code>

email domains you want to use
<code>domain_com: example.com</code>
<code>hostname_domain_com: hostname.example.com</code>

add email account: user@domain.com with account_password
<code>account_password: firstpassword</code>
<code>useratdomain_com: rambo@example.com</code>
<code>user: rambo</code>

add alias email. all emails from alias will be sent to
user@domain.com
<code>aliasatdomain_com: stallone@example.com</code>
<code>alias: stallone</code>

<code>postfix_dir: /etc/postfix</code>