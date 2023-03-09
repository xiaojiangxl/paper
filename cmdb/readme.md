# CMDB  command injection

## Description

Because the installation program does not filter the parameters, it directly concatenates them to the system commands, resulting in the execution of malicious commands.

## Addr

https://github.com/open-cmdb/cmdb

## Vulnerability Location

./cmdb\tools\install_cmdb.py

## Detailed
<img src=./img/cmdb1.png>

The specific position is line 79. The function run_cmd_container() is called. Since variables such as site_url, email_host, and email_port are controllable, they can be concatenated into the base() function.
<img src=./img/cmdb2.png>
<img src=./img/cmdb3.png>
