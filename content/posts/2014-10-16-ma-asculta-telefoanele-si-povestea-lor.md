---
title: “Mă ascultă” – Telefoanele și povestea lor
author: Moldovanu Codin
type: post
date: 2014-10-16T18:42:43+00:00
url: /ma-asculta-telefoanele-si-povestea-lor/
categories:
  - Uncategorized
tags:
  - 3g
  - 4g
  - android
  - apeluri
  - cerberus
  - chat
  - chatsecure
  - encriptie
  - gsm
  - ios
  - mobil
  - mobila
  - open
  - open whisper
  - openwhisper
  - orbot
  - orweb
  - redphone
  - secure
  - securitate
  - signal
  - telefoane
  - text
  - text secure
  - textsecure
  - tor
  - whisper

---
Ne reauzim cu această ocazie și începem să ne mutăm în cipherspace.

După cum știm, sau ar trebui să știm, telefoanele sunt principalul mod de comunicare între oameni &#8211; cu excepția cazului în care ai stat sub o piatră în ultimii 50 de ani, caz în care poți să revii la minunatul tău băț aprins.

Revenind la cei care folosesc aceste invenții, înainte de orice trebuie să înțelegem cum funcționează, așa că voi da niște mici explicații înainte de orice altceva.

Telefoanele sunt niște terminale mobile prin care poți comunica cu o a doua parte care deține la rândul ei un astfel de terminal. În momentul de față există două tipuri, dacă le putem numi așa, smartphone-urile (aici intră tot ce înseamnă iOS, Android, Blackberry OS, Firefox și orice alte derivate/fork-uri ale acestor sisteme de operare mobile) și dumbphone-urile (Nokia 3510, 3310, Motorola StarTAC și restul telefoanelor care nu pot fi considerate deștepte.) O mică notă ar fi că deși unele telefoane vechi sunt smartphone-uri după anumite criterii, alte telefoane mai noi nu sunt smartphone-uri după aceleași criterii &#8211; adică doar pentru că poți să te uiți la filme pe el, nu înseamnă că e smart.

Mai departe, aceste telefoane funcționează pe baza unor cartele (ce vorbeam mai devreme despre ISP se aseamănă foarte mult) ale unor rețele (Vodafone, Orange, T-Mobile, etc.). Trecând rapid prin asta, menționăm că totul funcționează pe baza unor celule (relee la un nivel brut) care transmit mai departe informația, acele celule la rândul lor pot fi 2G, 3G și mai nou LTE. Întregul sistem poartă numele de GSM. De regulă în majoritatea orașelor mari vom găsi rețele 3G și LTE. Problema principală a GSM-ului este că encripția este învechită, deci un individ cu voință poate să audă tot ce auzi tu, prin urmare este nesigur întregul sistem. Astfel, nici mesajele SMS, nici datele mobile și în cele din urmă nici serviciul de voce nu este sigur.

Dacă vreți mai multe informații (pentru oarecare motive) vă invit să citiți prezentarea lui David Perez și Jose Pico de la conferința BlackHat DC din 2011 <a href="https://media.blackhat.com/bh-dc-11/Perez-Pico/BlackHat_DC_2011_Perez-Pico_Mobile_Attacks-wp.pdf" target="_blank">aici</a>. În principiu oamenii arată cât de ușor poți să interceptezi date GSM, cu niște unelte pe care le poți obține prin intermediul internetului. De atunci a apărut și HackRF și totul a devenit mai ușor &#8211; dar asta e altă discuție. (Merită menționat că deși oamenii de la ETSI, cei care au dezvoltat sistemul GSM, au fost avertizați în legătură cu securitatea precară a sistemelor, au ales să ignore în repetate rânduri aceste avertizări.)

Nu o să vorbim aici despre lege, mandatele de care este nevoie pentru a-ți fi ascultat telefonul și restul detaliilor legale, aici o să vorbim strict de ce trebuie să faci ca să poți evita orice astfel de întâmplare.

Pentru siguranță, niște paranoia nu strică &#8211; pleacă de la prezumția că totul este ascultat și totul este în pericol.

Acum că ești urmărit, urmărește la rândul tău câțiva pași simpli înainte să ne specializăm pe comunicare.

Te rog din suflet, schimbă-ți PIN-ul cartelei. Dacă e 1234 înseamnă că deja ai pierdut runda asta &#8211; așa că schimbă-l.

**Parola telefonului. **

Fără o parolă a telefonului, poți să instalezi și mama encripției, dacă nu ai cea mai simplă metodă de protecție. Da, nu o să îți citească nimeni datele furate, dar ce faci dacă ele nu sunt furate ? Tot ce e nevoie sunt câteva sticle de bere, și îi vei da telefonul tău unui amic, care îl va da unui amic, și cineva la sfârșit va intra în telefon și va vedea la prima mână datele pe care le caută. Cred că fiecare dintre noi știm să ne setăm o parolă simplă pe telefon, așa că abuzați de această cunoaștere și instaurați o parolă. De preferat nu un cod de 4 cifre, dar chiar și acela poate să te salveze în momente critice. Pe lângă această parolă, dacă telefonul vostru are o opțiune de encripție &#8211; activați acea opțiune. [<img loading="lazy" class="alignnone size-large wp-image-15" src="http://www.codin-moldovanu.com/wp-content/uploads/2014/10/Screenshot_2014-10-16-21-03-50-576x1024.png" alt="Screenshot_2014-10-16-21-03-50" width="576" height="1024" srcset="https://codin.ro/wp-content/uploads/2014/10/Screenshot_2014-10-16-21-03-50-576x1024.png 576w, https://codin.ro/wp-content/uploads/2014/10/Screenshot_2014-10-16-21-03-50-168x300.png 168w, https://codin.ro/wp-content/uploads/2014/10/Screenshot_2014-10-16-21-03-50-281x500.png 281w, https://codin.ro/wp-content/uploads/2014/10/Screenshot_2014-10-16-21-03-50.png 1080w" sizes="(max-width: 576px) 100vw, 576px" />][1]

Spre exemplu, în meniul de Setări -> Securitate pe un Galaxy S4 găsim opțiune de criptare a întregului dispozitiv, opțiune de criptare a cardului microSD, opțiune de schimbare a PIN-ului cartelei SIM.

Practica sigură este să le folosiți pe toate, în tandem. De ce? Pentru că în principiu dacă pot să văd un fișier care nu e criptat, înseamnă că pot vedea mai multe (A minore ad majus &#8211; Dacă mai puțin, atunci mai mult). Deci nu lăsați niciun fel de portiță pe care să intre cineva.

În concluzie, folosiți orice opțiune de siguranță pe care o aveți la dispoziție pe telefon, indiferent dacă e iPhone sau un Android Generic.

Mai departe, acum că dispozitivul e criptat și aveți și o parolă, deja siguranța e în zare.

Pentru securitatea comunicațiilor _per se_ avem nevoie de niște utilități gratuite, din fericire.

&nbsp;

**Android**

Pentru comunicații sigure pe Android, avem o multitudine de opțiuni de unde să alegem.

TextSecure &#8211; Mesaje securizate, asemănătoare SMS-urilor dar online, un WhatsApp sigur să spunem.

RedPhone &#8211; Apeluri securizate, precum și aplicația de mai sus &#8211; online. Aplicația îți va spune când suni o persoană care de asemenea deține aplicația și te va întreba dacă nu cumva ai vrea să comunici cu ea fără să mai știe alți oameni ce vorbiți voi. Puncte-n plus pentru ingeniozitate.

Pixelknot &#8211; Fotografii sigure, dar nu în principal. Principalul scop este steganografia, mai exact trimiterea de mesaje scurte, ascunse în spatele unor fotografii, pe care le poți descifra doar cu ajutorul unei parole (ideal ar fi un One Time Pad, dar discutăm mai târziu despre asta).

ObscuraCam &#8211; Fotografii criptate, opțiuni de distrugere a unor pixeli sau de criptare a imaginii. Merită știut că este un proiect susținut de WITNESS.org.

Orbot și Orweb &#8211; Aici devine puțin mai complicat, dar mult mai sigur &#8211; în principiu. Orbot acționează ca un fel de proxy ce îți redirecționează întreg traficul prin rețeaua Tor și ți-l pierde pe acolo până când ajunge unde vrei tu. (Din nou, o să vorbim și despre Tor când ajungem la sistemele de operare ale calculatoarelor) Ideal este să folosiți în tandem și aplicația Orweb care este un browser, pe scurt, care îți blochează acele cookie-uri care îți urmăresc anumite trenduri, activități, date sau istoricul site-urilor, istoricul formularelor completate, dezactivează Flash și împiedică analiza rețelei sau metodele de pentest care te-ar putea afecta în mod direct.

În final, pentru a te proteja de ochii din cer, sau de pe fir, cam asta e tot ce trebuie și poți face dacă deții un telefon cu sistem de operare Android &#8211; cam cel mai fericit caz. Bine, ar mai fi câteva lucruri, dar din nou &#8211; le discutăm cu altă ocazie. (Am cam rămas dator cu multe văd. OTP, Tor, Android ++)

**iOS**

Acesta este cazul mai nefericit. Datorită restricțiilor impuse de Apple asupra celor care dezvoltă și urcă aplicații pe AppStore, majoritatea aplicațiilor sunt/au fost dezvoltate cu greu de către developeri.

Lista este scurtă, așa că voi spune direct. Pentru apeluri criptate aveți la dispoziție fratele geamăn al RedPhone, Signal (dezvoltat tot de OpenWhisper &#8211; părintele RedPhone). Funcționează pe același sistem, oferă o protecție ridicată a apelurilor de voce și desigur necesită o conexiune stabilă la internet.

În ceea ce privește mesajele text, momentan singura opțiune demnă de luat în seamă este ChatSecure. O aplicație care folosește Google Talk, Facebook, MSN sau orice alt server XMPP pe care îl aveți la dispoziție pentru a furniza comunicații text sigure din orice punct de vedere. Desigur, comunicațiile tot trec prin niște puncte, deci cel mai indicat ar fi să folosiți Google Talk drept server sau dacă informațiile sunt extrem de importante, și ar putea ridica întrebări internaționale &#8211; puneți la punct un server XMPP și folosiți-l.

Cam astea sunt opțiunile pentru iPhone/iPad. Sunt puține, știu &#8211; dați vina pe Apple nu pe mesager. Există și alte aplicații asemănătoare dar securitatea pe care o oferă ridică multe întrebări.

&nbsp;

În concluzie, pentru o securitate sporită folosiți în primul rând cele mai simple opțiuni, în tandem și vorbim aici de encripția dispozitivului și a cardului microSD, parola dispozitivului și PIN-ul cartelei SIM. De asemenea încercați să activați și opțiunea de remote wipe sau instalați o aplicație gen Cerberus care vă poate reda controlul asupra unui telefon furat (multitudine de opțiuni &#8211; poză, locație, wipe, alarm, etc.) În al doilea rând, folosiți aplicațiile pe care vi le-am prezentat mai sus &#8211; pentru orice fel de comunicații sensibile.

&nbsp;

Ne revedem în următoarea parte a articolului, cea legată de securitatea calculatorului !

&nbsp;

&nbsp;

 [1]: http://www.codin-moldovanu.com/wp-content/uploads/2014/10/Screenshot_2014-10-16-21-03-50.png