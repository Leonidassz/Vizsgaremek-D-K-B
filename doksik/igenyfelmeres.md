# Igényfelmérés

Felkeresett minket a Gandiegyszálse, amely egy technikus segítséget nyújtó cég. A kérés után elmentünk a céggel diskurálni a feltételekről, igényekről, hogy képzelték el és hogy mi hogy tudnánk megvalósítani.

## A cégnél

Amint a cégnél leültünk beszélgetni az igazgatóval. 
Közölte, hogy négy eltérő helységben működnének, ebből kettő irodai közeg, egy pedig bolti közeg, illetve a rendszergazdájuk nem minden nap jár be dolgozni, ezért egy home office-os környezet is lenne.
A feladatunk ezeknek a helyeknek a teljes konfigurálása, megvalósítása.

A plusz feltételekért, egyéni kérésekért leültünk beszélni a vezérigazgatóval, hogy megtudjuk, milyen extra szolgáltatásokra van szükségük.

### Kérdések:
- A vezetőség és a dolgozók hogy oszlanak el?
- Lesz egy iroda, ahol a vezetőség és a dolgozók egy helyen vannak, a másikban csak a dolgozók lennének.

A vezetőséges irodában több vlan-t fogunk alkalmazni, hogy ne egy szálon fussanak a pornép adataival, illetve, ami a másik irodai közegben is meg lesz valósítva, hogy külön vlan-okat hozunk létre a telefonhoz és a rendszergazdának is (mivel neki mindkét irodában biztosíttunk helyet) azt itt is alkalmazni fogjuk.

- A rendszergazdák akkor otthontól is dolgoznának?
- Igen, a hétnek négy napján járnának csak be.

Ahhoz, hogy ez megvalósítható legyen, lehetőve kell tennünk számukra a távolról való elérést is, amit SSH-val tervezünk megvalósítani. Minden router-re és switch-re feltelepítetnénk, ezáltal otthonról is be tudnak lépni az eszközökbe.

- Éjjel-nappali szolgáltatás lenne?
- Igen, szeretnénk, ha folyamatos segítséget tudnánk nyújtani.

Ennek érdekében az összes hálózatot redundánssá alakítunk, hogy fizikai kapcsolatmegszakadás esetén is továbbra működni tudjon minden.

- Lenne-e igény saját fájlmegosztásra és weboldalra?
- Igen.

Konfigurálunk egy saját  webszervert is, ami mellé teszünk egy dns szolgáltatást is, továbbá teszünk be egy FTP szervert is a cégen belüli fájlmegosztás érdekében is.

- Telefonról vagy laptopról is hozzá szeretnének férni a hálózathoz?
- Igen, lenne olyan eset, amikor azokról kéne felmenni a rendszerre

Ezért tervezünk bele vezeték nélküli hálózatot is, amit egy WLC segítségevel tudunk szabályozni és biztonságossá tenni.

- A dolgozók bedughatják saját eszközeiket a kapcsolókba?
- Nem, ezt el szeretnénk kerülni.

Ebből kifolyólag az összes switch-nek kiadjuk, hogy jegyezze meg a mi általunk csatlakoztatott gépeknek a MAC címét, a többi üres portot pedig letiltjuk. Fizikai értelemben pedig veszünk a portokra zárakat, hogy még csak lehetőségük se legyen bedugni a gépeiket.