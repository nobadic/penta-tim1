Kategorije gledatelja imate poseban json.

Ispod su sve vrijednosti za PlaceStatus
Id          Naziv         
----------- --------------
1           Zauzet        
2           Slobodan      
3           Rezerviran    
5           Blokiran      
7           Pretplatnik   

prostorCijene je glavni json file ali ga nisam ogao spremiti kao cjelinu nego sam ga podijelio u više komada.
To su sva sjedala sa cijenama, i statusom zauzetosti i koja kategorija gledatelja može sjesti na neko mjesto. 
File je pun LastUser,LastUpdate polja; to ignorirajte. To su podaci tko je posljednji i kada mijenao podatak.
Ako je sjedalo zauzeto prodajom papirnate karte onda ima status Zauzet i SellingPrice je namještena na neku vrijednost.
Ako je sjedalo zauzeto pretplatom onda ima status Pretplatnik ali SellingPrice nije namješten.

Za početak bi mogle:
- za sjedalo zauzeto papirnatom kartom prikazati cijenu
- za sjedalo zauzeto pretplatom prikazati samo pretplata i koja kategorija gledatelja je na tom mjestu
- za ostale statuse prikazati samo status
- ako neko sjedalo ima status Active=0 ili to preskačite i ne prikazujte ništa (nisam siguran ako ima neko sjedalo takvo)

Ako stignete mogu vam dati tabelu pretplatnika pa da pored sjedala sa pretplatnikom prikažete i njegovo ime/prezime

Negdje stavite statistiku po sektorima gdje će biti:
- T totalni broj mjesta na sektoru
- A broj prodanih karata 
- B broj pretplata
- C broj slobodnih mjesta (ne mora biti T=A+B+C jer neko sjedalo može i biti neaktivno i kao takvo ne zbraja se ni u A ni u B ni u C)



