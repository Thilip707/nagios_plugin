# nagios_plugin

check_website examples
$ ./check_website www.google.com
HTTP OK: 174ms - http://www.google.com/|time=174ms;500;2000;0;

$ ./check_website -f www.amazon.com
HTTP WARNING: 740ms - http://www.amazon.com/|time=740ms;500;2000;0;

$ ./check_website -p 8080 -u /index.html -s -P 192.168.27.111:3128 -c 4000 -w 1500 www.myweb.com
HTTPS OK: 274ms - https://www.myweb.com:8080/index.html|time=274ms;1500;4000;0;



check_ddos example
./check_ddos.py -c 300 -w 200

check_nginx 
./check_nginx.sh -H localhost -P 80 -p /var/run -n nginx.pid -s nginx_status -o /tmp -w 15000 -c 20000
