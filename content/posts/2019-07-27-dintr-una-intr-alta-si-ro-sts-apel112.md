---
title: Dintr-una într-alta și “ro.sts.Apel112”
author: Moldovanu Codin
type: post
date: 2019-07-26T22:17:04+00:00
url: /dintr-una-intr-alta-si-ro-sts-apel112/
categories:
  - Peculiar Shit
tags:
  - "112"
  - apel
  - apel112
  - caracal
  - cordova
  - cyber security
  - gps
  - javascript
  - romania
  - security
  - serviciul de telecomunicatii speciale
  - sts
  - stsisp
  - tracking
  - what-even-is-infosec

---
În realitate ar fi trebuit să se numească &#8220;ro.expertiza-it.Apel112&#8221; dar știți voi, software orientat către client și chestii, practic cedezi drepturile de autor către respectivul client, așa că ei își pot pune numele pe orice dezvolți tu pentru ei.

Evident, am ajuns aici în urma evenimentului de-a dreptul încredibil care a avut loc în Caracal &#8211; eveniment despre care nu vreau să discut sub nicio formă din 3000 de motive.

În tot haosul s-a vorbit foarte mult despre cum românii ar trebui să își instaleze pe telefoane aplicația &#8220;Apel 112&#8221; &#8211; și evident &#8211; paranoic fiind mi s-a părut prea dubios să le spui câtorva milioane de români să instaleze o aplicație pe telefon sub pretextul siguranței.

Așa că am aruncat un ochi pe mirifica aplicație. Inițial mă pregătisem mai serios, cu decompilator cu alea alea, fraier am fost pentru că aveam nevoie doar de un editor de text, aplicația fiind făcută cu Cordova. Adică jeg, și nu orice jeg, jeg JavaScript care rulează pe Android &#8211; kind of jeg.

Pot în primă fază să **confirm că aplicația nu trimite date acasă la fiecare zece minute**, nu îți copiază fiecare selfie nud, ci trimite niște date către un API doar la apăsarea butonului roșu.

Datele efective care sunt trimise sunt latitudinea, longitudinea, acuratețea GPS-ului, timpul via GPS și numărul de telefon completat de tine (deci există o șansă să greșești numărul de telefon și să nu te găsească iar STS-ul&#8230;).

<img loading="lazy" class="alignnone size-full wp-image-672" src="https://codin.ro/wp-content/uploads/2019/07/location_tracker.png" alt="" width="567" height="158" srcset="https://codin.ro/wp-content/uploads/2019/07/location_tracker.png 567w, https://codin.ro/wp-content/uploads/2019/07/location_tracker-300x84.png 300w" sizes="(max-width: 567px) 100vw, 567px" /> 

#### Hateresc deci exist

Trebuie să ne și luăm de ceva, așa că urmează:

**NOUĂZECIȘIȘAPTE (97)** de printări către consolă (console.log()) &#8211; pe o aplicație în producție, care n-are consolă, și care probabil n-ajung nicăieri, doar umplu memoria de nimicuri constante care ar putea fi furate de alte aplicații care și-ar pune mintea.

<img loading="lazy" class="alignnone size-full wp-image-677" src="https://codin.ro/wp-content/uploads/2019/07/infosec_lol.png" alt="" width="463" height="158" srcset="https://codin.ro/wp-content/uploads/2019/07/infosec_lol.png 463w, https://codin.ro/wp-content/uploads/2019/07/infosec_lol-300x102.png 300w" sizes="(max-width: 463px) 100vw, 463px" /> 

&nbsp;

**INFOSEC? NEVER HEARD OF IT**. Băi, aici e posibil să fiu eu ridicol, dar în același timp vorbim de un sistem care e destul de **critic** totuși, așa că mna, here goes. Serios, ați lăsat tokenul pentru requesturi chiar aici? Existau soluții mai decente decât un API în PHP și un token static, e oarecum ridicol că trebuie să zic asta. E oarecum ridicol că asta e o aplicație recomandată de STS (hahaha ăia care voiau să învețe clustere că se descurcă ei singuri hahahahahahaha MOR DE RÂS). Sper că apreciază lumea faptul că am cenzurat 99% din token-ul ăla. Serios. Am fost băiat bun.

Problema, în română pentru restul, e că un utilizator rău intenționat poate să &#8220;inunde&#8221; sistemul lor de localizare sau ce morții lor face prostia asta de aplicație, și să facă toată aplicația lor inutilă, pentru că &#8230;există metode, și loop-urile sunt niște ghimpi în coasta programatorilor care știu despre securitate doar că le trebuie parole cu peste 6 caractere și minim două numere. E **inimaginabil** de rea-practică ce vedem mai sus, practic aplicațiile terțe cărora le-ai dat tu acces la contul tău Google sunt mai sigure din punct de vedere al autentificării.

**RECLAME.** Da, găsim și o mică scăpare probabil a programatorilor de la &#8220;expertiza-it.ro&#8221; care aparent sunt ceva experți juridici pe probleme tehnice, dar sincer să fiu la cum arată aplicația asta, mai bine imi dați mie un semn. Am încercat să caut pe SEAP și SICAP ceva anunț de atribuire legat de aplicația asta dar ok UM 0319, keep your secrets.

### În concluzie

  * Aplicație scrisă în Javascript folosind Cordova (probabil pentru cross-platform).
  * Autentificare API la semi-liber, se ia bucată token și se folosește.
  * Console.log(console.log(console.log())).
  * Nu te urmărește când sforăi.

_**3.6, not great, not terrible.**_