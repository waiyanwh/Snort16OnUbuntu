### Check snort configuration is right or not
```
sudo snort -T -c /etc/snort/snort.conf -i eth1
```
### Watch the laert
```
sudo /usr/local/bin/snort -A console -q -u snort -g snort -c /etc/snort/snort.conf -i eth1
```
| Flag | Description |
| --- | --- |
| `-A console` | The ‘console’ option prints fast mode alerts to stdout |
| `-q` | Quiet mode. Don’t show banner and status report. |
| `-u snort` | Run Snort as the following user after startup |
| `-g snort` | Run Snort as the following group after startup |
| `-c /etc/snort/snort.conf` | The path to our `snort.conf` file |
| `-i enp0s3` | The interface to listen on (change to your interface if different) |
### Run snort in alert mode
```
sudo /usr/local/bin/snort -q -u snort -g snort -c /etc/snort/snort.conf -i eth1
```
### Run Barnyard2
```
sudo barnyard2 -c /etc/snort/barnyard2.conf -d /var/log/snort -f snort.u2 -w /var/log/snort/barnyard2.waldo -g snort -u snort
```
### Default login information for snorby WEB-GUI
```
E-mail: snorby@example.com
Password: snorby
```
