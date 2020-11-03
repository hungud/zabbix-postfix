# Monitoring Exim in Zabbix — CentOS 7 (ISPManager)

- Install
```
yum -y install curl zabbix-sender logcheck
```

- Create or download zbx-exim-stats.sh into /usr/local/sbin/

```
chmod +x /usr/local/sbin/zbx-exim-stats.sh
```

- Create cron
```
*/5 * * * *  /usr/local/sbin/zbx-exim-stats.sh >/dev/null 2>&1
```

- restart service
```
 service zabbix-agent restart
```
