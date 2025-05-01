# Szolgáltatás katalógus

## Rendszerszolgáltatások

### Router-eken kiadott szolgáltatások
|Megnevezés|Feladat|
|-|-|
| DHCP | Dinamikusan oszt IP címeket a dolgozóknak és eszközöknek |
| DHCP snooping | Mivel nem lesz miden helyen DHCP szerver, ezért a legtöbb forgalomirányítóra ki kell adni, hogy melyik utvonalon éri el a DHCP szervert |
| OSPF | A forgalomirányatók megosztják egymással a saját általuk által ismert hálózatokat és kiszámolja a legrövidebb utakat egyes célokhoz |
| HSRP | Redundánsá teszi a forgalomirányítókat esetleges kapcsolatmegszakadás esetén |
| SSH | A rendszergazda számára bekonfigurált biztonságos távoli elérési módszer |

### Switch-en kiadott szolgáltatások
| Megnevezés | Feladat |
|-|-|
| VTP | Az egyes hálózatokban kijelölt kapcsolók megtanítják a többi kapcsolónak az ő konfigurált vlan-jait | 
| STP | A kapcsolókat redundánsá alakítjuk ezzel, ahol minden vlan-nak kiadunk egy vezető kapcsolót, amely annak a vlan-nak a forgalmával fog foglalkozni |
| Etherchannel | A további redundancia érdekében néhány kapcsolót duplán kötöttük össze, hogy az egyik kábel esetleges megsérülése után, a másik akadálymentesen tudja továbbítani a forgalmat |
| SSH | A rendszergazda számára bekonfigurált biztonságos távoli elérési módszer |

### Egyéb rendszerszolgáltatások
| Megnevezés | Feladat |
|-|-|
| TFTP | A rendszermentéseket erre a szerverre fogjuk menteni |
| WLC | A vezeték nélküli hálózatok összefogó alakja, amivel külön szegmensekre tudjuk bonatni a hálózatra kapcsoltakat |

## Üzleti szolgéltatások
| Megnevezés | Feladat |
|-|-|
| Mail | A dolgozóknak részesített levelező szolgáltatás, amellyel tudnak beszélni egymással |
| FTP | Egy saját fájlmegosztó szolgáltatás |
| DNS | Egy névfeloldó szolgáltatás, hogy ne IP címeket kelljen beírni a weboldal helyett |
| Nyomtató | Dolgozók számára nyújtott nyomtatók |
| IP telefon | Minden dolgozónak adott telefon, ahol tud hangalapon kommunikálni a többiekkel |
| Web | A cég saját webodalát futtassa egy szerver, ami folyton elérhető legyen |

Az üzleti szolgáltatások az év minden napján 0-24-ben működőképes, elérhető állapotban lesznek.

## Biztonsági intézkedések

Minden switch-en konfigurálunk portbiztonságot, amivel megjegyzi az általunk bedugott gép MAC címét, ezzel megakadályozva a jövőbeli idegen gépek használatát. Emellett minden nem használt portra fizikailag ráillesztünk egy port dugót, amit kulccsal lehet csak leszedni. Ezt a módszert alkalamzzuk a használt portokra is, ahol egy hasonló zárat rakunk a kábel csatlakozójára, ami által nem lehet kihúzni azt a kábelt.

## Kritikus szolgáltatások
Ezek a szolgáltatások, amelyekre különös hangsúlyt fordítottunk, hiszen ezek járulnak hozzá leginkább a cég életéhez, mint szakmai oldalról, mint vásárlói nézetből.

**TFTP**

A szerver mellé elhelyeztünk egy szünetmentes tápot, hogy folyamatosan áram alatt tudjon lenni, biztosítva működését, illetve kritikus üzenetek esetén a rendszergazda külön értesítést kap, hogy mielőbb orvosolni tudja a felmerülő problémát.
A rendszergazda külön feladata lesz, hogy figyelje, illetve hetente ellenőrizze a szerver megfelelő működését.

**Mail**

Mivel a vásárlók elektronikusan is felvehetik a céggel és a cég non-stop technikai segélyt nyújt, ezért fontos, hogy a nap bármely pillanatában működjön a szolgáltatás, hogy ne legyenek nagy csúszások. Illetve, ha bármi hiba is előfordulna, akkor az e-mail küldési ideje alapján vissza lehet követni a hiba fellépésének időpontját.



