#Adding comments and using it to print

I added some comments to the cupsFilePrintf() function, which was located in the scheduler's log.c file. Then saved the modified log.c file. Enter the make and make install commands once again:
```
make
make install
```

Then stop the CUPS service using Ctrl+C and start again using the following command:
```
sudo /usr/sbin/cupsd -f
```

Then i gave the print job and checked the access.log file:

#Modified Access Log
```
localhost - - [04/Jan/2022:18:17:13 +0530] "POST /admin/ HTTP/1.1" 401 242 CUPS-Add-Modify-Printer successful-ok
localhost - rishabh [04/Jan/2022:18:17:13 +0530] "POST /admin/ HTTP/1.1" 200 242 CUPS-Add-Modify-Printer successful-ok
localhost - - [04/Jan/2022:18:19:08 +0530] "POST /printers/nowhere HTTP/1.1" 200 328 Create-Job successful-ok
localhost - - [04/Jan/2022:18:19:08 +0530] "POST /printers/nowhere HTTP/1.1" 200 8069 Send-Document successful-ok
localhost - - [04/Jan/2022:18:24:52 +0530] "POST /printers/nowhere HTTP/1.1" 200 328 Create-Job successful-ok
localhost - - [04/Jan/2022:18:24:52 +0530] "POST /printers/nowhere HTTP/1.1" 200 8140 Send-Document successful-ok
localhost - - [04/Jan/2022:18:26:21 +0530] "POST /admin/ HTTP/1.1" 401 155 CUPS-Delete-Printer successful-ok
localhost - rishabh [04/Jan/2022:18:26:21 +0530] "POST /admin/ HTTP/1.1" 200 155 CUPS-Delete-Printer successful-ok
localhost - - [04/Jan/2022:18:27:05 +0530] "POST /admin/ HTTP/1.1" 401 239 CUPS-Add-Modify-Printer successful-ok
localhost - rishabh [04/Jan/2022:18:27:05 +0530] "POST /admin/ HTTP/1.1" 200 239 CUPS-Add-Modify-Printer successful-ok
localhost - - [04/Jan/2022:18:27:32 +0530] "POST /printers/test HTTP/1.1" 200 325 Create-Job successful-ok
localhost - - [04/Jan/2022:18:27:32 +0530] "POST /printers/test HTTP/1.1" 200 8137 Send-Document successful-ok
rishabh contributed here  
 localhost - - [04/Jan/2022:18:28:49 +0530] "POST /printers/test HTTP/1.1" 200 325 Create-Job successful-ok
rishabh contributed here  
 localhost - - [04/Jan/2022:18:28:49 +0530] "POST /printers/test HTTP/1.1" 200 8137 Send-Document successful-ok
```