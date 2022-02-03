# DomainEnum

DomainEnum is a tool to enumerate various records of a domain and output to a linux terminal.

DomainEnum allows you to specify your own nameserver or use the default of 1.1.1.1.

## Requirements

Linux

## Install

1. Clone the main file

    ```bash
    git clone https://github.com/pntha/DomainEnum.git
    ```

2. Make the script executable

    ```bash
    chmod +x DomainEnum/domainenum
    ```

3. [Optional] Copy `domainenum` executable to `/usr/bin/` for usage without the full path

    ```bash
    sudo cp /path/to/domainenum /usr/bin/
    ```

## Usage

### Without custom nameserver

```bash
domainenum example.com
```

### With custom nameserver

```bash
domainenum example.com -n 1.0.0.1
```

or

```bash
domainenum example.com --nameserver 1.0.0.1
```

## Example output

```bash
$ domainenum google.com.au
DomainEnum: v1.0
Using nameserver: 1.1.1.1

-------------------------------- WHOIS INFORMATION -------------------------------
Domain Name: GOOGLE.COM.AU
Registry Domain ID: D407400000001774763-AU
Registrar WHOIS Server: whois.auda.org.au
Registrar URL:
Last Modified: 2021-08-05T15:18:41Z
Registrar Name: MarkMonitor Corporate Services Inc
Registrar Abuse Contact Email:
Registrar Abuse Contact Phone:
Reseller Name:
Status: clientDeleteProhibited https://afilias.com.au/get-au/whois-status-codes#clientDeleteProhibited
Status: clientUpdateProhibited https://afilias.com.au/get-au/whois-status-codes#clientUpdateProhibited
Status: serverDeleteProhibited https://afilias.com.au/get-au/whois-status-codes#serverDeleteProhibited
Status Reason: Registry Lock
Status: serverRenewProhibited https://afilias.com.au/get-au/whois-status-codes#serverRenewProhibited
Status Reason: Not Currently Eligible For Renewal
Status: serverTransferProhibited https://afilias.com.au/get-au/whois-status-codes#serverTransferProhibited
Status Reason: Registry Lock
Status: serverUpdateProhibited https://afilias.com.au/get-au/whois-status-codes#serverUpdateProhibited
Status Reason: Registry Lock
Registrant Contact ID: MMR-174095
Registrant Contact Name: Domain Admin
Tech Contact ID: MMR-171195
Tech Contact Name: Domain Administrator
Name Server: NS1.GOOGLE.COM
Name Server: NS2.GOOGLE.COM
Name Server: NS3.GOOGLE.COM
Name Server: NS4.GOOGLE.COM
DNSSEC: unsigned
Registrant: Google LLC
Eligibility Type: Trademark Owner
Eligibility Name: GOOGLE
Eligibility ID: TM 788234
>>> Last update of WHOIS database: 2021-09-07T07:12:36Z <<<

----------------------------------- SOA RECORD -----------------------------------
MNAME: ns1.google.com
RNAME: dns-admin@google.com
Serial: 395058775
Refresh: 900
Retry: 900
Expire: 1800
TTL: 60

--------------------------------- A/AAAA RECORDS ---------------------------------
142.250.66.227 >> syd15s15-in-f3.1e100.net.
2404:6800:4006:810::2003 >> syd15s15-in-x03.1e100.net.

----------------------------------- WWW RECORD -----------------------------------
www.google.com.au >> 142.250.71.67

---------------------------------- HTTP HEADERS ----------------------------------
HTTP/1.1 301 Moved Permanently
Location: http://www.google.com.au/
Content-Type: text/html; charset=UTF-8
Date: Tue, 07 Sep 2021 07:12:49 GMT
Expires: Thu, 07 Oct 2021 07:12:49 GMT
Cache-Control: public, max-age=2592000
Server: gws
Content-Length: 222
X-XSS-Protection: 0
X-Frame-Options: SAMEORIGIN

--------------------------------- SSL CERTIFICATE --------------------------------
Issuer:
  Google Trust Services LLC
Subject DN:
  CN = *.google.com.au
Issuer DN:
  C = US, O = Google Trust Services LLC, CN = GTS CA 1C3
SKI:
  12:DE:C3:11:DA:8B:3C:EC:70:A4:8C:4E:2E:20:34:E9:DD:6D:59:FD
AKI:
  keyid:8A:74:7F:AF:85:CD:EE:95:CD:3D:9C:D0:E2:46:14:F3:71:35:1D:27
Serial:
  50:5b:4c:33:47:51:a1:c5:0a:00:00:00:00:fa:6a:a4
SAN:
  *.google.com.au
  google.com.au
Usage:
  Digital Signature
Valid From:
  Aug 16 04:47:26 2021 GMT
Valid Until:
  Nov  8 04:47:25 2021 GMT

----------------------------------- MX RECORDS -----------------------------------
smtp.google.com >> 142.251.10.27 >> sd-in-f27.1e100.net
smtp.google.com >> 172.217.194.26 >> si-in-f26.1e100.net
smtp.google.com >> 172.217.194.27 >> si-in-f27.1e100.net
smtp.google.com >> 2404:6800:4003:c03::1a >> sf-in-f26.1e100.net
smtp.google.com >> 2404:6800:4003:c03::1b >> sf-in-f27.1e100.net
smtp.google.com >> 2404:6800:4003:c04::1b >> si-in-f27.1e100.net
smtp.google.com >> 2404:6800:4003:c0f::1a >> sd-in-f26.1e100.net
smtp.google.com >> 74.125.24.26 >> sf-in-f26.1e100.net
smtp.google.com >> 74.125.24.27 >> sf-in-f27.1e100.net

----------------------------------- TXT RECORDS ----------------------------------
"v=spf1 -all"
```
