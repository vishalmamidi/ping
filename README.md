# ping

### Alpine Linux 

```bash
apk update

#delv, dig, host, nslookup...
apk add bind-tools

#telnet
apk add busybox-extras

#curl 
apk add curl
```

### samples to check hostname is accessable 

### nslookup
```bash
nslookup vishalmamidi.com
```
```console
Server:         172.30.48.1
Address:        172.30.48.1#53

Non-authoritative answer:
Name:   vishalmamidi.com
Address: 185.199.108.153
Name:   vishalmamidi.com
Address: 185.199.110.153
Name:   vishalmamidi.com
Address: 185.199.111.153
Name:   vishalmamidi.com
Address: 185.199.109.153
```
### host
```bash
host vishalmamidi.com
```
```console
vishalmamidi.com has address 185.199.108.153
vishalmamidi.com has address 185.199.110.153
vishalmamidi.com has address 185.199.111.153
vishalmamidi.com has address 185.199.109.153
```
```
host -a vishalmamidi.com
```
### dig
```bash
dig vishalmamidi.com
```
```console
; <<>> DiG 9.16.1-Ubuntu <<>> vishalmamidi.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 31932
;; flags: qr rd ad; QUERY: 1, ANSWER: 4, AUTHORITY: 0, ADDITIONAL: 0
;; WARNING: recursion requested but not available

;; QUESTION SECTION:
;vishalmamidi.com.              IN      A

;; ANSWER SECTION:
vishalmamidi.com.       0       IN      A       185.199.108.153
vishalmamidi.com.       0       IN      A       185.199.110.153
vishalmamidi.com.       0       IN      A       185.199.111.153
vishalmamidi.com.       0       IN      A       185.199.109.153

;; Query time: 0 msec
;; SERVER: 172.30.48.1#53(172.30.48.1)
;; WHEN: Thu Feb 16 09:30:14 EST 2023
;; MSG SIZE  rcvd: 114

```

```bash
dig +short vishalmamidi.com
```
```console
185.199.108.153
185.199.110.153
185.199.111.153
185.199.109.153
```

## telnet ( need to give port )
```bash
telnet vishalmamidi.com 80
```
```console
Trying 185.199.108.153...
Connected to vishalmamidi.com.
Escape character is '^]'.
```




