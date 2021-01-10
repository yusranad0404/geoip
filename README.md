mkdir -p /usr/share/xt_geoip/
apt-get install xtables-addons-common xtables-addons-dkms iptables-dev xtables-addons-common libtext-csv-xs-perl pkg-config install libtext-csv-xs-perl libmoosex-types-netaddr-ip-perl -y
iptables-restore iptables.conf


#masukin ip ke whitelist
iptables -I INPUT -s 8.38.148.0/24 -j ACCEPT
	
#check ip
iptables -L

#LANGKAH 
-> CHECK IP DULU
-> BARU MASUKIN IP KE WHITELIST, KALAU UDAH ADA JANGAN DIMASUKIN LAGI!
