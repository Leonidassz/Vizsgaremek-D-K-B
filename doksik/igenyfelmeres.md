# Felkérés

Felkeresett minket a Gandiegyszálse, amely egy technikus segítséget nyújtó cég, hogy Magyarországon is szeretnének egy központot kialakítani. 
A vállalat már vett két irodai emeletet, emellett egy üzlethelyiség is van már a nevükön, ahol az ügyfelek be tudják vinni a hibás termékeiket.
Feladatunk ezeknek a helységeknek a teljes kitervelése, megvalósítása.

A felkérés után egyeztettünk egy időpontot, hogy megtudjuk beszélni a feltételeket, kéréseket, illetve felmérni a helyet, hogy tudnánk fizikailag megvalósítani az egészet.

## Helyzetfelmérés

A két irodai közeg az egyikben a vezetőség és a dolgozók egy térségben helyezkednek el, ebből kifolyólag felosztjuk az embereket a beosztásuk szerint külön csoportoba, hogy egymás forgalmát ne akadályozzák, illetve ne lássanak bele. Emellett a rendszergazdáknak és a telefonoknak is lesz külön csoportjuk. Ezt a csoportbesoztást vlan-onként fogjuk megoldani mindkettő irodai közegben.

A rendszergazdák viszont nem járnak be a hét minden napján, ezáltal ki kell nekik is alakítani egy home office környezetet, amivel hozzá tudnak férni a céges hálózathoz, illetve a legtöbb forgalomirányítón és kapcsolón telepítünk SSH-t, amivel távolról is el tudjanak érni ezeket az eszközöket és az esetleges hibajavításokat otthonról is tudják intézni.

A rendszergazákkal szemben a dolgozók nem férhetnek hozzá mindenhez, nem rakhatják saját gépeiket a kapcsolókba, forgalomirányítókba, ezért biztonsági lépéseket is meg kell tennünk, mint például a portbiztonság és a nem használt portok letiltását vagy fizikailag hozzáférés ellehetetlenítése zárakkal. Viszont vannak a cégnek olyan pontjai, helyei, ahol elkerülhetetlen lesz, hogy idegen gépet kelljen felcsatlakoztatni a rendszerre, itt fizikailag elérhetőek lesznek a portok és a logikai biztonsággal fogjuk ellensúlyozni.

A cég kért egy web szolgáltatást is, hogy a meglévő és a leendő ügyfelek meg tudják őket találni interneten keresztül is. Ezt egy saját web szerverrel tervezzük megvalósítani, amelyhez egy DNS szolgáltatást is rakunk, hogy a weboldal IP címét össze tudjuk kötni egy URL-el. A web mellett a cég egy saját fájlmegosztó szolgáltatást is szeretne, szóval egy saját FTP szervert is rakunk bele, hogy a cégen belül legyen egy fájl tároló egység, ahol el tudják érni a céges adatokat.

A vállalat 0-24-es szolgáltatást szeretne nyújtani, ennek érdekében figyelnünk kell a redundanciára, hogy esetleges fizikai kapcsolat megszakadás se állítsa le a forgalmat és akadálymentesen működjön minden továbbra is. A tervezésben közben erre figyeltünk, hogy minden közegben legyen redundancia.

Az egész helyen szeretnék, hogy legyen vezeték nélküli hálózat a dolgozók és főképp a rendszergazda számára, hogy tudjon csatlakozni tudjon az internethez a laptopjával vagy telefonjával. Ezt számításba véve több LAP-t is rakunk le a teljes lefedettség miatt. 