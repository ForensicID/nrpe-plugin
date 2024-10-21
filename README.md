# nrpe-plugin
NRPE berfungsi sebagai jembatan antara server Nagios dan mesin klien yang ingin dipantau. Ketika Nagios mengirim permintaan untuk memeriksa status atau kinerja layanan di server klien, NRPE menerima permintaan tersebut, menjalankan plugin yang sesuai di mesin klien, dan mengembalikan hasilnya ke server Nagios.
## RAM

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_mem
chmod +x check_mem
```

## CPU

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_cpusage.sh
chmod +x check_cpusage.sh
```

## NETWORK

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_bandwidth
chmod +x check_bandwidth
```

## DATABASE

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_mysql_query.pl
chmod +x check_mysql_query.pl
```

## Command and Parameter

```bash
command[check_mem]=/usr/local/nagios/libexec/check_mem -f -w 20 -c 10
command[check_netstat]=/usr/local/nagios/libexec/check_bandwidth 100 500 100 500
command[check_cpusage]=/usr/local/nagios/libexec/check_cpusage.sh -w 80 -c 90
command[check_database]=/usr/local/nagios/libexec/check_mysql_query.pl -H 127.0.0.1 -u username -p password
```
