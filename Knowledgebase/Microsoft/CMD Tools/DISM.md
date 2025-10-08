# DISM
**Tool zur Imagebearbeitung**

---

*Image Mounten und bearbeiten*
 -> *Mount Verzeichnis erstellen bsp.:*  *"C:\Temp\Mount"*

*in CMD eingeben und die Pfade anpassen*
```
	dism /Mount-Image /ImageFile:E:\Test\test1\sources\install.wim /index:1 /MountDir:C:\Temp\Mount
```
*Nun kann das Image nach belieben unter dem Mountpfad bearbeitet werden*

*nach Abschluss Image unmounten*
```
dism /Unmount-Image /MountDir:C:\Temp\Mount /Commit
```

---

*Treiber hinzufügen (PE)*
```
dism /Image:C:\Temp\Mount /Add-Driver /Driver:C:\Pfad\zu den\Treibern /recurse
```
