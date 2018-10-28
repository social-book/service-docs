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

# primeri sporočil
## pridobi seznam uporabnikov
### endpoint
GET	{URL}/user/
### Response
	[
	  {
	    "userId": 1,
	    "name": "Miha",
	    "surname": "Stele",
	    "imgref": "https://yt3.ggpht.com/a-/AN66SAzNhh8W59TE7Sr71gmJxt8r44FmtXlokJJkfQ=s900-mo-c-c0xffffffff-rj-k-no",
	    "username": "mihastele",
	    "password": "e1e91f36d2440c01ca7a97fefb416980"
	  },
	  {
	    "userId": 2,
	    "name": "Nejc",
	    "surname": "Ribic",
	    "username": "user_nrbibic",
	    "password": "fcb65e884890ef14cf50b8c427f63b1e"
	  },
	  {
	    "userId": 3,
	    "name": "User",
	    "surname": "Gpor",
	    "username": "user_gpor",
	    "password": "f711eca236eba5b6dea0ae20c991cd0d"
	  },
	  {
	    "userId": 4,
	    "name": "Ok",
	    "surname": "Afk",
	    "username": "ok",
	    "password": "2497862a6844efa42a1d1f483426af73"
	  }
	]

## pridobi podatke albumih
### endpoint

GET	{URL}/statistics/albums

#### pokliče

GET	{URL}/user/   -> pridobi vse uporabnike

GET	{URL}/album   -> pridobi vs albume

### Response

{JSON objekt z obdelano statistiko}

# Diagrami

## Diagram povezav med servisi
![alt text](https://raw.githubusercontent.com/social-book/service-docs/master/services.png)

## Diagram entitet (v0.1)
![alt text](https://raw.githubusercontent.com/social-book/service-docs/master/Social%20Book.png)

# Docker

## Run commands
	docker run -d -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=nejc -p 5432:5432 postgres:10.5
	docker pull 40850473/service-catalog:0.0.3
	docker run 40850473/service-catalog:0.0.3

