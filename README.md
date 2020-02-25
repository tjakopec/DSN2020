# DSN2020
Razvoj android aplikacija kroz prizmu različitih predložaka dizajna na danima strukovnih nastavnika 2020

# Uvod
Prema statistikama [^1] broj mobilnih uređaja na svijetu ima minimalno 45% stanovništva dok je realna procjena kako 66 % ljudi na svijetu posjeduje pametni telefon. Na tom tržištu dvije su ključne platforme: Android i iOS. Ostala zastupljenost na tržištu je zanemariva. Prema izvorima [^2][^3] omjer se kreće otprilike 75 % zastupljenosti Android pametnih telefona naspram 25 % zastupljenosti iOS pametnih telefona. Prikladnije je uvoditi osnove razvoja mobilnih aplikacija strukovnim nastavnicima na Android platformi. Prvi razlog je navedena veća zastupljenost dok je drugi razlog činjenica kako razvoj aplikacija za iOS zahtjeva posjedovanje MacOS operativnog sustava za objavu aplikacija što povlači posjedovanje Apple računala. Apple računala su cjenovno skuplja od generičkih PC računala.
# Problematika
Razvoj mobilnih aplikacija moguće je na nekoliko načina [^4]. Razvojem aplikacija prilagođenim specifično jednoj platformi (eng. native) ili razvojem hibridnih aplikacija čijim generiranjem za  specifičnu platformu dobijemo aplikaciju koju možemo objaviti. Ukoliko se odabere razvoj hibridnih aplikacija na raspolaganju su nam razvojni alati koji su bazirani na HTML + CSS + JavaScript skupu tehnologija na osnovu čije se implementacija tada za svaku specifičnu platformu generiraju aplikacije. Ra raspolaganju nam je nekoliko različitih ranih okolina: Ionic, Apache Cordova, React Native, Flutter i dr. S druge strane razvoj aplikacija za jednu platformu uz mogućnost korištenja svi specifičnosti platforme opet nudi mogućnost odabira više programskih jezika. Na iOS platformi to su ObjectiveC (Nije moguće kreirati nove aplikacije ali postoji potreba održavanja koda na starijim aplikacijama) i SWIFT. Za Android platformu moguće je razvijati aplikacije koristeći Java ili Kotlin programski jezik. Prilikom razvoja mobilnih aplikacija većina aplikacija podatke pohranjuje u oblaku. Problem nastaje kod očekivanja korisnika kako im aplikacija treba omogućiti rad i kada mobilni uređaj nema pristup mreži. Po povratku pristupa mreži mobilne aplikacije sinkroniziraju podatke u pravilu bez utjecaja korisnika.
# Moguća rješenja
Lepeza dostupnih rješenja je zbilja široka. Za potrebe predavanja daje se prikaz mrežne infrastrukture s prikazom najbolje prakse pri realizaciji REST API[^5] sučelja. Prikazati će se korištenje HTTP metoda GET, PUT, POST i DELETE koje odgovaraju uobičajenim aktivnostima rada s podacima: čitanje, kreiranje, primjena i brisanje (eng. CRUD). na primjeru entiteta Osoba koji ima tri svojstva. U dijelu razvoja mobilnih aplikacija daje se osnovi pregled Android ekosustava koristeći Java programski jezik u razvojnom alatu Android studio. Upoznaje se s upraviteljem zavisnosti Gradle te daje popis korisnih alata prilikom razvoja i način kako se ti alati implementiraju u projekt. Prikazani alati u formi implementacije biblioteka koda su: Lombok, Butter Knife, Retrofit, Picasso i Room. Na primjeru mogućnosti pregleda, kreiranja, promjene i brisanja podataka entiteta Osoba prikazuje se implementacija dvaju dominantnih arhitekturalnih predložaka dizajna Model View Presenter (MVP) i Model View View Model (MVVM). Iako je tradicionalni predložak dizajna u Java programskom jeziku Model View Controller (MVC), on se pokazao manjkavim u razvoju Android aplikacija upravo zbog specifičnosti okruženja, potrebe za asinkronim načinom rada i ograničenjima koje osnovni koncepti Android razvoja (životni vijek Activity instance i dr.) donose. MVP se pokazao dao dobra evolucija, međutim zbog kompleksnije implementacije, Google se ipak odlučio implementirati MVVM za koji se predlaže razvoj aplikacija danas.  
# Ishodi predavanja
Ishod su mobilne aplikacije jednake funkcionalnosti s implementacijom različitih predložaka dizajna. Na repozitoriju otvorenog koda (github) dostupni su projekti:
1. Mrežna aplikacija koja omogućuje REST API koristeći PHP kao programski jezik dok je pohrana podataka u MariaDB bazi podataka 
2. Android aplikacija Osnovni pregled Android ekosustava s korištenje alata
3. Android aplikacija CRUD MVP
4. Android aplikacija CRUD MVVM

[1]: https://www.bankmycell.com/blog/how-many-phones-are-in-the-world
[2]: https://gs.statcounter.com/os-market-share/mobile/worldwide
[3]: https://deviceatlas.com/blog/android-v-ios-market-share
[4]: https://www.upwork.com/hiring/mobile/should-you-build-a-hybrid-mobile-app/
[5]: https://www.smashingmagazine.com/2018/01/understanding-using-rest-api/ 

Predavač: Tomislav Jakopec radi kao docent na Odsjeku za informacijske znanosti pri Filozofskom fakultetu Osijek. Voditelj je Dvopredmetnog diplomskog studija informacijske tehnologije. Nositelj je kolegija vezanih uz informacijske tehnologije u društvenom području. Kao vanjski suradnik izvodi nastavu na Stručnom studiju informacijskih tehnologija na Odjelu za informacijske znanosti pri Sveučilištu u Zadru na kolegiju Razvoj mobilnih aplikacija. Veliki je zaljubljenik u informacijske tehnologije općenito.