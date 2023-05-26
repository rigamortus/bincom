# 1. Setting Up a Mail and Web Server
(i) To set up a mail server, I installed the mailutils package and postfix on a GCP virtual machine with a Linux OS (Ubuntu Distribution):

```
sudo apt update
sudo apt install postfix mailutils -y
```
(ii) Next, the configuration file for postfix was edited and the _inet_interfaces_, _mydestination_, and _myhostname_ fields were modified.

(iii) The Postfix service was restarted:

```
sudo systemctl restart postfix
```

(iv) Mail was sent from the user __davidakalugo__ to the __root__ user.
```
echo "Test email body" | mail -s "Test email subject line" root@google.davidaltschool.me
```
(v) Mail was received
![mail](google.png)

# 2. Web Server

(i) An apache web server was set up using the following commands:

```
sudo apt update
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
```

(ii) Static files were hosted in the /var/www/html directory.
