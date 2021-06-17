# File-Permissions

1. Set permissions of sensitive files to prevent normal users from obtaining sensitive


information of other users.
chmod 440 /etc/sysctl.conf
chmod 751 /etc/ssh
chmod 644 /etc/passwd
chmod 600 /etc/shadow
chmod 1777 /tmp
chmod 644 /etc/fstab
chmod 640 /etc/login.defs
chmod 640 /etc/logrotate.d/*
chmod 644 /etc/logrotate.d/iscsiuiolog
chmod 600 /etc/pam.d/*
chmod 644 /etc/pam.d/su
chmod 644 /etc/pam.d/su-l
chmod 600 /etc/security/opasswd
chmod 644 /etc/hosts.allow
chmod 644 /etc/hosts.deny
chmod 600 -R /etc/ssl/certs/
chmod 750 /var/run/dbus
chmod -s /lib64/dbus-1/dbus-daemon-launch-helper
chown root:root /etc/passwd
chown root:root /etc/shadow
chown root:root /etc/fstab
chown root:root /etc/ssh/*key
chown root:root /etc/ssh/*key.pub
chown root:messagebus /var/run/dbus
chown polkituser:polkituser /var/run/PolicyKit


2. Set the default umask value to 077 to reduce risks of files being tampered with. To do
this, open the /etc/profile file and search for the umask parameter. If it does not exist,
add the following; if it exists, modify the existing parameter to the following:
umask 077



3. Run the source /etc/profile command to make the modifications take effect
