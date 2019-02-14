# check_shelly
A php-based Nagios compliant check for the popular Shelly IoT devices.
This check should work with any nagios compliant monitoring system such as Icinga, Neamon, check_mk, Zabbix and others ...

Note: Currently only Shelly1 and Shelly2 are supported.

The check reads uptime, ram and file system usage and reports warning, if the defined threshold is reached. 

### system requirements
php with php-curl module

###Example:
a check command example:
```./check_shelly -h=<shelly-ip> -u=shellyuser -p=shellypassword -w=90 -c=95```

###Parameters:
-h (host) is mandatory
-u (username) and -p (password) are optional, if the Shelly is protected via username / password
-w and -c are optional warning /critical thresholds .. (default is 90 for warning, 95 for critical)

###Output:
OK: shelly1-1D9ABA - Type: SHSW-1 (Uptime: 0 days, 16 hours, 5 minutes and 50 seconds) is healthy.

###Todo: 
  - add support for other Shelly devices 
  - generate perfdata output
  - add monitoring for relay states (warn or critical, if relay state is off)
  
