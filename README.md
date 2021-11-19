# EU-DigitalCovidCertificateViewer


## Français :


###### Cet utilisataire permet de visualiser le contenu du passe sanitaire européen sans vérifier qu'il est authentique (signé) 
###### Exécutable pour windows 64 bits : Télécharger le fichier EU-DigitalCovidCertificateViewer-1.0_fr.exe (md5sum : 702aaa783903b8686555c60c84d721f7)
###### Ouvrir une console MSDOS (dans la zone de recherche de windows, il suffit de tapper : cmd)
###### Exécuter le programme et lui passant l'argument -i et le nom du fichier contenant l'image du passe sanitaire.
###### ex : C:\Users\Dev\Documents>EU-DigitalCovidCertificateViewer-1.0_fr.exe -i passSan.jpg


## English :


###### This tools allow data visualisation of th european covid certificate without checking it's authenticity (signed) 
###### Binary for windows 64 bits : Download file EU-DigitalCovidCertificateViewer-1.0_en.exe (md5sum : 886626c0a6f7c0a2ef8753fc52782d6e)
###### Open a MSDOS console (in the windows search area, you just have to write : cmd)
###### Execute the tool with -i argument and the name of the file containing the QR Code.
###### ex : C:\Users\Dev\Documents>EU-DigitalCovidCertificateViewer-1.0_fr.exe -i passSan.jpg

----------------------------------------------------------------

###### Le QR Code est localisé par la librairie pyzbar tel que :
###### QR Code is found by pyzbar library like that :
----------------------------------------------------------------

###### decodedObjects = pyzbar.decode(Image.open(imFile))
###### myObject=None
###### for obj in decodedObjects:
###### if obj.data.decode("utf-8") != scannedCode: 
######   scannedCode = obj.data.decode("utf-8")
######   if obj.type == "QRCODE":
######         myObject = obj
###### if myObject != None:
######  try:  
######   passSan=str(myObject.data) 
######   payload = passSan[6:][:-1]
######   decodePassSan(payload)
![Screenshot](https://github.com/go-mcf/EU-DigitalCovidCertificateViewer/blob/main/Screenshot.JPG)
