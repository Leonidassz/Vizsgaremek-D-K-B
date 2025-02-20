# Szolgáltatás katalógus

## Rendszer
|Zsargonszó|Feladat|
|-|-|
| DHCP | Dinamikusan oszt IP címeket a dolgozóknak és eszközöknek |
| DHCP snooping | Mivel nem lesz midenhol DHCP szerver, ezért a legtöbb forgalomirányítóra ki kell adni, hogy merre keresse a szervert |
| OSPF | A forgalomirányatók megtaniítják egymásnak a saját útvonaljaikat |
| HSRP | Redundánsá teszi a forgalomirányítókat esetleges kapcsolatmegszakadás esetén |
| SSH | A rendszergazda számára bekonfigurált távoli elérési módszer a forgalomirányítókon és a kapcsolókon |
| VLAN | A kapcsolókon létrehozott csoportok az emberek beosztottsága szerint |
| VTP | A kijelölt kapcsolók megtanítják a többi kapcsolónka az általa ismert vlan-okat | 
| Etherchannel | A további redundancia érdekében néhány kapcsolót duplán kötöttük össze, hogy az egyik kábel esetleges megsérülése után, a másik akadálymentesen tudja továbbítani a forgalmat |
| STP | A kapcsolókat redundánsá alakítjuk ezzel, ahol minden vlan-nak adunk egy főnököt, ami továbbítja annak forgalmát |
| TFTP | A rendszermentéseket erre a szerverre fogjuk menteni |
| WLC | A vezeték nélküli hálózatok vezető alakja lesz |

## Üzlet
|Szakszó|Feladat|
|-|-|
| Mail | A dolgozóknak részesített levelező szolgáltatás, amellyel tudnak beszélni egymással |
| FTP | Egy saját fájlmegosztó szolgáltatás |
| DNS | Egy névfeloldó szolgáltatás, hogy ne IP címeket kelljen beírni a weboldal helyett |
| Nyomtató | Dolgozók számára nyújtott nyomtatók |
| IP telefon | Minden dolgozónak adott telefon, ahol tud hangalapon kommunikálni a többiekkel |
| Web | A cég saját webodalát futtassa egy szerver, ami folyton elérhető legyen |