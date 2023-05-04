## Description
Download the packet capture file and use packet analysis software to find the flag.

-   [Download packet capture](https://artifacts.picoctf.net/c/194/network-dump.flag.pcap)

## Hints
Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.

## Solution
Solo use cat porque me parecio raro que tuviera dos puntos y salio hehe

```bash
┌──(ulrich㉿DasMausoleum)-[~/…/Forensic/Examen-2/Forensic2022/Packets]
└─$ cat network-dump.flag.pcap 
�ò�k&Nar�J'��'�9E<P�@@��

�n#('�Զ���A�
���dk&Na�J'�9'��E<@@"�

#(�n�&��'�Է���*O�
h��Í��dk&Na`�B'��'�9E4P�@@��

�n#('�Է�&����9
���eh���k&Na;�~'��'�9EpP�@@ѳ

�n#('�Է�&����u
���eh���p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ c e c c a a 7 f }
k&Naa�B'�9'��E4g�@@��

#(�n�&��'����Ui
h��č��ep&Na(
            <'�9''��s

p&NaX
     *'��''�9�
'��s
p&Na28*'��''�9�

p&Na�;<'�9''��s
'�9�
```

## Flag
picoCTF{p4ck37_5h4rk_ceccaa7f}

## Aditional Notes

## References
