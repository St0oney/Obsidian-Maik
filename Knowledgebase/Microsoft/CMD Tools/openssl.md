# Openssl - Windows

**aufsplitten einer pfx Datei in privaten Schlüssel und cer File**

-> *in den openssl Pfad navigieren*

-> *privaten Schlüssel abspeichern*
```
openssl.exe pkcs12 -in C:\Pfad\der\pfx.pfx -nocerts -out C:\Pfad\des\priv.key -nodes
```

-> *Zertifikat abspeichern*
```
openssl.exe pkcs12 -in C:\Pfad\der\pfx.pfx -clcerts -nokeys -out C:\Pfad\des\priv.key -nodes
```

