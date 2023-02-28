# Retos Bandit

## Objetivo

## Datos de acceso al nivel
***Usuario: bandit10
Contraseña: jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
## Solucion
```bash
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 24 22:59:04 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 24 22:59:04 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 24 22:58:04 2023 GMT; NotAfter: Feb 24 22:59:04 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEdtHsNjANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjI0MjI1ODA0WhcNMjMwMjI0MjI1OTA0WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCx
mrCINhzIGCIeMR5GsleGkWUZWNcLl1D3FFa0OwDgYG0lj4VP3fC2jf7SJ8DbMdGT
jqyOhsM+LZhKWPJ+NH60lzWTeYq6/pe2OMFhZ6bbd84coT7Fo7Evjk4bye2+qYsH
J6MR7Gk+bhL9U4KpCVOpZwHitiC4ZbX+s7n8PHQsfMeQfhSS7J+Xa0vTw3KQoVCg
3BhKTD9bt3gXVfGNaIvECku2sCECDkFyCR5+AqswPHCT7QK8Q3sb9gbA0/zhWbXb
h4RVpbwm+NqmDivMxPVSH+J6NzgmBpLTpeFsN05rlN9CdzRP9l+tLCJnf1irtKMI
0KkVzlGMg/vwLKYA0G5pAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBx
vsPCAfYKiOZH0RDDB18SoiFpjkw3A9lSM14tvFlYsEdx31DvJNwc6QT/E8uOV2sB
Kl4wGwJQPJ7VT93CClFN3je9drqlNryCm+P4VO1Fhay8JIb6PyW0z4WCIlJqCRKT
68SPozIEfx/lwquR+MPyopny7tIlA1IZN4aF5yA+Gi570zC7UtdRBVyfGrdANeS8
5pmwA2NzxauCh3QJc2jWYVk4qmmTsLJBgElaFN1QrZHk60rxaUjS4rFnsSYZ/d4n
kmj3TPpRidAxlDM5qnXqD7fcBNy3s7XXk40ygWS/GsJJx38sHr0yFmMV7l0QKVBC
rsP6Hy0UaGAkUNBjj/Fi
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
    Session-ID: F24AB09CF033F5E4D1C36FF809A653EC8485C2D066A025D8B3A32C98B922A275
    Session-ID-ctx: 
    Resumption PSK: 06EA0CDEF7D550AF771F0F974BD1B8CF8CAA559454CE954F3A795F31C4F57864F5564BFD03B56CD035D2D8565B7C9F86
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - cb 00 ae d3 fc cf 12 aa-e1 f0 d3 ef 6c 0e a6 aa   ............l...
    0010 - 25 3b d8 c7 aa 34 e9 85-f8 48 88 99 05 dd 2e 55   %;...4...H.....U
    0020 - f6 31 38 0f e3 4a f3 7c-04 33 db 38 f2 eb 7a 67   .18..J.|.3.8..zg
    0030 - b9 6f 4f ac 12 c4 79 f3-85 a5 df 34 b8 a1 29 e6   .oO...y....4..).
    0040 - 2f 7d ee 19 b4 70 f1 d5-9a 02 0b 8a d9 64 d2 09   /}...p.......d..
    0050 - b4 9f bc b2 13 4c 41 c3-2a fb cb 92 41 74 bb 1a   .....LA.*...At..
    0060 - 0e 21 f2 40 3f 64 ed b0-27 63 0c 8f 41 6e 1a 8a   .!.@?d..'c..An..
    0070 - 35 b7 a7 91 2e 2c 5d 15-5c d6 17 0d 40 b4 f4 25   5....,].\...@..%
    0080 - 5e 82 0d 81 67 15 10 95-7a c0 f7 d6 36 25 85 63   ^...g...z...6%.c
    0090 - fd cc ba 7e 31 33 41 d2-eb 49 1f c5 0d b1 cf 61   ...~13A..I.....a
    00a0 - 9a 82 e7 c5 bc f8 7d 38-e9 0d d9 c4 68 6c 94 d6   ......}8....hl..
    00b0 - 39 6b 55 ad 2a 9d b3 1e-ae 42 c3 e8 3f 70 00 d3   9kU.*....B..?p..
    00c0 - 3f da bc a1 fb ef 88 9c-3b e0 de 94 38 f3 73 e7   ?.......;...8.s.

    Start Time: 1677595563
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
    Session-ID: EF342FC33B05DB9A7F9F7D15E83D8022ED8C4422196D000B9967BAACF4297D73
    Session-ID-ctx: 
    Resumption PSK: BA75F8423906C7B6640547E5289A028C6F09D02E44D3E9D8CEC0D77B3D2FD3A1E9AB3B191815FAD4896AB9F2715C0599
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - cb 00 ae d3 fc cf 12 aa-e1 f0 d3 ef 6c 0e a6 aa   ............l...
    0010 - c2 d3 84 3d 24 b7 92 15-61 bf f0 b8 b1 f5 36 6c   ...=$...a.....6l
    0020 - b3 e2 21 ec 36 cf f2 21-b9 4f bf 9a 3f 96 19 71   ..!.6..!.O..?..q
    0030 - 2e fa 82 aa c8 09 3f 1d-9f 54 3b c8 8d 73 a2 9a   ......?..T;..s..
    0040 - 51 1d 24 01 1b 97 4e 44-9e 05 7d 83 37 3a 49 76   Q.$...ND..}.7:Iv
    0050 - f6 18 16 8b 1f 72 81 c1-bf 46 1e 89 df d6 6f ee   .....r...F....o.
    0060 - 8c 6c 41 cb e5 e3 08 d6-8b 26 92 33 49 eb 8d 2d   .lA......&.3I..-
    0070 - 10 d1 ef a0 07 9b 28 51-d7 c1 f9 3e 43 eb 46 36   ......(Q...>C.F6
    0080 - 8d 36 d0 66 62 83 6b d5-f4 18 9c 1f 4b fe e4 19   .6.fb.k.....K...
    0090 - 54 09 ee 20 e6 18 ee f8-99 1f 28 b6 78 03 67 24   T.. ......(.x.g$
    00a0 - 95 06 d5 a1 19 a6 ba ef-d7 7c ca fc 68 1a af 34   .........|..h..4
    00b0 - 42 f5 eb 54 ef 8c a2 ba-9f 09 97 7c 43 5a f8 5c   B..T.......|CZ.\
    00c0 - 04 67 f6 b1 fe e0 77 f4-34 f2 4b fc 64 c0 a8 a9   .g....w.4.K.d...

    Start Time: 1677595563
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed


```

## Notas adicionales
## Referencias

