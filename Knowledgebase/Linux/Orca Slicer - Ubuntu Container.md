**Voraussetzung**
-> Docker muss installiert sein

*Orcaslicer Docker Image ziehen und installieren*
``` 
docker pull linuxserver/orcaslicer
```

*Docker Container erstellen*
```
docker run -d \
  --name=orcaslicer \
  -p 3000:3000 \
  -v <host_path>:/config \
  linuxserver/orcaslicer
```

-> Docker kann nun über die <ipadresse>:3000 in einem Browser aufgerufen werden.

