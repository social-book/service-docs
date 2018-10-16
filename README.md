# Social book

## Abstract Mikroservisi

### uporabnik
* registriraj_uporabnika() - uporabnik se bo preko vmesnika lahko registriral
* prijava_uporabnika() - avtentikacija prijave uporabnika

### Objave
* objavi() - registriran uporabnik bo lahko objavil poljubne stvari
* zbrisiObjavo() - objavo bo zmožen tudi izbrisati

### Upravljanje komentarjev
* komentirajObjavo() - objavo lahko katerikoli uporabnik komentira
* izbrišiKomentar() - uporabnik lahko zbriše svoj komentar
* vseckaj() - uporabnik lahko všečka neko objavo

### Sporočilni sistem
* poslji_sporocilo() - uporabiki si lahko med seboj pošiljajo sporočila
* pridobi_sporočila() - klic za prejem sporočil določenega pogovora

## Podatkovne entitete

### Users
Podatki uporabnika

### Messages
Podatki sporočil

### Posts
Podatki objav

### Comments
Podatki komentarjev



# Actual services 
## Upravljanje uporabniških profilov
### Entitete
* User
?
### Endpoints


## Katalog slik
### Entitete
* Album
* Slika
* (User) -> Retrieve from users service?
* Kategorija
			
			entitea album, album inma več slik
				podatki o sliki
					kdo jo uploada 
						kategorije itd,...


# upravljanjanje s komentarji
### Entitete
* Komentar

# sporočilni sistem
### Entitete
* Sporočilo
* (User) -> Kdo pošilja sporočilo / Komu je namenjeno sporočilo

# urejanje slik?
### Entitete
* Kdo ureja
* Katero sliko ureja
* Pošlji sporočilo o urejanju
* ?
