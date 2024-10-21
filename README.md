# nrpe-plugin
NRPE berfungsi sebagai jembatan antara server Nagios dan mesin klien yang ingin dipantau. Ketika Nagios mengirim permintaan untuk memeriksa status atau kinerja layanan di server klien, NRPE menerima permintaan tersebut, menjalankan plugin yang sesuai di mesin klien, dan mengembalikan hasilnya ke server Nagios.
## RAM

```bash
cd /usr/local/nagios/libexec/
wget https://raw.githubusercontent.com/ForensicID/nrpe-plugin/refs/heads/main/check_mem
chmod +x check_mem
