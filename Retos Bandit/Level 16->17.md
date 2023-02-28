# Retos Bandit

## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Datos de acceso al nivel
***Usuario: bandit16
Contraseña: JQttfApK4SeyHwDlI9SXGR50qclOAil1

## Solucion
```bash
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-28 14:54 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.000097s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

Nmap done: 1 IP address (1 host up) scanned in 0.07 seconds
bandit16@bandit:~$ openssl s_client -conect localhost:31790
s_client: Unknown option: -conect
s_client: Use -help for summary.
bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 24 22:59:05 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 24 22:59:05 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 24 22:58:05 2023 GMT; NotAfter: Feb 24 22:59:05 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEXaCVVzANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjI0MjI1ODA1WhcNMjMwMjI0MjI1OTA1WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDP
cZ+PR+x7nAI6TVhZvc6x5//nXHJUZnIv2kf6x8SOY5al5BV8I5njUSVQef9fQNE2
JlBdoYNJ65jgzYWrVqPCObCqrPsHZHf8pMD/iElYUcD5u/qtNReuVPfeYefxCvBg
Cy0MltMiLGskDn3rDSwCRWNB2jr9+jQYa7rIGDyWCAq4WH/IsWtF6tan25Bqe6tp
LIMJhuAH56EjZ0biNJ3aOgsWHwqS1bBdMzURABvR+PZc0mikWaNjb2R0d8v0gJTf
qz0qkea6IstFSfwEu2FdslmDZ8PWlIwexw3erL+Ae0L2mFhdf3g1nkUARl8R0Bbe
L9/rtYsV7dF3KG7CFJbbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBH
HpXhIirw6+X3VNmrtXw7HjpriGDA1UTjP2yfeu2YuLIm83iUpz3HuiiwsfJJX9HY
VeDQnJjgMekib2qbq99OHkz+4jFKpw0zR7wTa9K8fifkrQHW/KJOVg1fmJCyFl+j
LF06QYp5f8yA+I2ICGKuNSXd3NvYEVh0tWVXemx/oXqQLHUFBjWNcyBDfCnfZIfe
jhHPhGj/9DuJJWx1lBEOIFHrfOj2uge0R5YZvU0kEm3IQ6iabWM2JF8MHOWWYX8s
wXL4aeNo+K4lnz3wjqnRfSClTwTo9zvaaq+Ym8UxPx3w7SmAU3CXbLh/ukYR6xYp
YEsSAXuYvKkxrTvey2Ik
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 33F8E37ABC16A9B40CFE90C741F4C22115E1ACAE3EA3A881A48BDD05E9A5050A
    Session-ID-ctx: 
    Resumption PSK: E2FFD65593E393CCA495E6768264D27611D112DE3B8A6D153CCE7C9FB495EB79EDE8F3E36A9BF84D5683DBBA0CB844E4
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 70 f2 f5 0a f4 da 59 2b-66 40 bc 3c 8d 67 67 76   p.....Y+f@.<.ggv
    0010 - 87 bc 50 6c c9 ff c1 3a-da 46 10 d0 16 4e 01 96   ..Pl...:.F...N..
    0020 - 1a 3d 0d 24 83 90 ec cb-8d 80 b5 3a 3b 91 33 8b   .=.$.......:;.3.
    0030 - 8a f2 80 d3 c1 52 1e 4d-1a 5d 42 d7 ab 87 54 cb   .....R.M.]B...T.
    0040 - 40 ac e0 a9 db fe bb 68-c9 08 69 00 8c 15 af 0e   @......h..i.....
    0050 - 63 d1 ff a0 73 57 f9 cf-96 fe 1c 1f 78 f2 71 48   c...sW......x.qH
    0060 - bd e4 5f 73 e9 3e 58 cb-ec 54 6f 7b a9 cb 9f 1d   .._s.>X..To{....
    0070 - 5f 1f 02 ee da 9d e4 33-55 b3 17 c0 fb 8c 92 f1   _......3U.......
    0080 - 2e 4c ef b3 52 e5 71 b6-5d 7a 60 27 67 b7 67 f4   .L..R.q.]z`'g.g.
    0090 - 53 e9 d6 af ac 48 ea 42-c6 4f 60 12 ce 90 85 8f   S....H.B.O`.....
    00a0 - 4e a5 ca f4 ea 50 21 2e-6b 83 66 9e e4 23 85 a6   N....P!.k.f..#..
    00b0 - 86 50 86 72 c8 0a 91 b1-84 bd 67 60 74 0e cf 2c   .P.r......g`t..,
    00c0 - ac 0e 9e 04 e7 37 af 16-03 0f 2d 7e f5 e8 cf 86   .....7....-~....

    Start Time: 1677596168
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: E0B98072826EE5D4F784B8EBBE77279C2A380E77C173FC69A8EBF91B85BD861D
    Session-ID-ctx: 
    Resumption PSK: E6D4EA9BF398311200F87B41765DE8AE72E45D432FA998B20B802574A92DB2E4C92F6A2D073404F6A4F90A8BD89E88CE
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - 70 f2 f5 0a f4 da 59 2b-66 40 bc 3c 8d 67 67 76   p.....Y+f@.<.ggv
    0010 - e6 03 a8 f3 ab 85 d4 c2-de 2e f4 ac 8d 4f 9c 80   .............O..
    0020 - 66 e6 c0 c8 5f c7 52 53-3e d0 61 31 69 7a e6 ab   f..._.RS>.a1iz..
    0030 - 84 03 5d d8 13 5a fd ff-9b c8 15 e1 80 65 0f c7   ..]..Z.......e..
    0040 - 31 39 e9 ba 70 2a 1a 61-4d a5 0a fd fb 0a 65 5b   19..p*.aM.....e[
    0050 - 24 f2 93 5e 70 01 31 e7-56 ab f7 c6 bd e0 8e eb   $..^p.1.V.......
    0060 - b5 e4 56 59 70 55 42 ec-82 22 4e 8c 56 3c 80 24   ..VYpUB.."N.V<.$
    0070 - 8a f4 d5 0a 2c 79 1c 1a-f8 17 4c e7 97 43 95 86   ....,y....L..C..
    0080 - 42 b3 d3 97 aa 2c 74 6f-41 0d e1 ed ac cf ef 2e   B....,toA.......
    0090 - 75 91 69 62 ad 17 6d 79-de b2 48 60 63 b2 a5 09   u.ib..my..H`c...
    00a0 - d1 5c b5 eb e3 fa 83 35-8a 6e 5e be 73 20 7f 19   .\.....5.n^.s ..
    00b0 - 59 cc 85 64 32 6e 2f e8-19 76 eb de 09 40 95 d4   Y..d2n/..v...@..
    00c0 - 33 b6 ed de fe 65 be 0d-23 71 d9 59 d9 a7 94 37   3....e..#q.Y...7

    Start Time: 1677596168
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----


```

## Notas adicionales
Se probo cada puerto abierto, cuando se encontro el que daria las cedenciales nos dio una clave privada rsa, con esta clave entraremos desde ahi a la 17!
## Referencias

