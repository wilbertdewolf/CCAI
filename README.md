![cimsolutions - LinkedIn persoonlijke profiel banner](https://user-images.githubusercontent.com/63059377/143780859-b786a79a-fe4d-4aa4-aab0-67fbdda546f9.jpg)

# CCAI
CIMSOLUTIONS Conversational Artificial Intelligence repository

# Opzetten van een SSH-Authentication: SSH-secured connectiviteit Archi - Github

1. Installeer CoArchi - plugin
- Eerst downloaden op https://www.archimatetool.com/plugins/
￼
- Open Archi en navigeer naar 
![Pasted Graphic 22](https://user-images.githubusercontent.com/63059377/143779893-44a43124-e352-4040-964a-25d9fa0b6197.png)
- Installeer hier het *.archiplugin bestand

2. (Enkel voor de eigenaar van het github-account) Maak een ssh-keypair aan:
￼
- open de terminal.
- type het volgende commando: ssh-keygen -t rsa -b 4096 -m PEM -C “wilbertdewolf@yahoo.com”
- filename := id_rsa
- de passphrase := opvragen bij de github-eigenaar
- Als je een mac hebt: dan moet je in folder ~/.ssh/config het volgende toevoegen:
![Pasted Graphic 9](https://user-images.githubusercontent.com/63059377/143779953-c5942ee6-c4cb-4f5d-a1d2-e9838066d9ee.png)
3. Voeg de ssh-private-key id_rsa toe aan je mac-ssh-process. 
- Kijk of die ook draait:
￼
![Pasted Graphic 10](https://user-images.githubusercontent.com/63059377/143779974-3ded6b68-fbeb-4246-bf0c-e6d1eab4ab6e.png)
- bij mij draait hij onder pid 1932 
- Nu toevoegen:
![Pasted Graphic 11](https://user-images.githubusercontent.com/63059377/143779979-98e431cd-1f94-47fb-8a09-7327430587f5.png)
 ￼
4. kopieer de ssh-public-key id_rsa.pub naar clipboard:
![Pasted Graphic 12](https://user-images.githubusercontent.com/63059377/143780027-7fcbc903-3156-40d7-b8ea-14327e168ba4.png)

5. Maak in Github een nieuwe ssh-key aan en “paste” clipboard
- Ga naar Settings
![Pasted Graphic 13](https://user-images.githubusercontent.com/63059377/143780052-a34ce9a8-db96-47c3-a0bd-44a41896f2b6.png)
- Klik op
![Pasted Graphic 14](https://user-images.githubusercontent.com/63059377/143780063-2806e13e-59f4-4a05-bfa4-ed107326c288.png)
- Klik op
![Pasted Graphic 15](https://user-images.githubusercontent.com/63059377/143780082-979cf789-e4ae-41e4-854d-a777aacd8b27.png)
- Geef de key een naam: id_rsa_pub en “paste” je clipboard
- Geef akkoord met je Github-wachtwoord om de SSH-configuratie door te voeren.
6. Open Archi en klik op preferences
![Pasted Graphic 16](https://user-images.githubusercontent.com/63059377/143780113-492409b6-002a-455b-90a6-74cbea76a43b.png)
- selecteer Collaboration
![Pasted Graphic 17](https://user-images.githubusercontent.com/63059377/143780129-5cb1f7d1-4236-4682-a3ae-d9ffd0df2d91.png)
7. Configureer SSH als volgt (n.b. vul je eigen username in ipv “wilbertwolf”):
![Pasted Graphic 18](https://user-images.githubusercontent.com/63059377/143780147-c09f903c-3a4d-4b8f-8031-1c51d54ddd94.png)
- Identity password = de passphrase
- Klik op ￼
![Pasted Graphic 19](https://user-images.githubusercontent.com/63059377/143780170-c416386c-42cb-4719-a508-08d37eac6922.png)

# Koppelen van een Github-repository in Archi
1. Open Archi en klik op menu: 
![Pasted Graphic 20](https://user-images.githubusercontent.com/63059377/143780285-6f5f8dda-da22-49e5-8996-88d8f99cb1a6.png)
2. Vul in (n.b. Geen username en password omdat we authenticeren via SSH):
![Pasted Graphic 21](https://user-images.githubusercontent.com/63059377/143780302-f24eae0f-9c7b-4b01-8ff7-bad5b3d8537a.png)
