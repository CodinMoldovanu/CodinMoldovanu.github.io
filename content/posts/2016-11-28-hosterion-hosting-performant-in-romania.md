---
title: Hosterion – Hosting performant în România
author: Moldovanu Codin
type: post
date: 2016-11-28T18:48:28+00:00
url: /hosterion-hosting-performant-in-romania/
dsq_thread_id:
  - "5632959742"
categories:
  - Linux
  - Reviews
  - Tech
tags:
  - gazduire
  - gazduire ieftina
  - host
  - hosterion
  - hosting
  - pachete
  - romania

---
Cu siguranță nu sunt singurul care la ore târzii din noapte își lasă haterul interior să iasă la suprafață și să comenteze haterisme la postările oamenilor. Aseară pe la 2 haterul meu interior își făcea de cap și comenta legat de un plugin LetsEncrypt al unei companii de hosting. De obicei comentariile astea de la cretini ca mine sunt șterse sau lăsate în pace &#8211; pentru că sunt două mari modalități de a rezolva problemele astea &#8211; ori nu le bagi în seamă, ori le faci să dispară, modalitatea a 3-a e să combați efectiv comentariul. Lucru pe care l-au făcut și cei de la Hosterion.

Înainte de toate, n-am primit nici măcar un leu pentru ce scriu acum, am primit în schimb o zi de acces gratuit la serviciile lor.

Hosterion este o firmă de hosting adresată mai degrabă segmentului superior al pieței de hosting din România, dar prețurile planurilor nu te omoară și încep de la 3€ pe lună, deci servicii și suport premium la prețuri decente (pentru cei care nu știu, una din marile probleme cu găzduirea unui site stă în cât de sictirită e persoana de la suport tehnic când ți-e lumea mai dragă, suport premium înseamnă că persoana aia nu e sictirită). Aflați în Cluj, sunt pe piață din 2004 și recent s-au rebranduit din Elvsoft în Hosterion.

Ca diversitate a produselor oferă cam tot ce ai putea să îți dorești, de la planuri mici de hosting pentru un blog/site de prezentare până la VPS-uri cu putere mare de procesare și hosting specializat pentru Magento.

Toate pachetele de găzduire ale Hosterion oferă stocare pe SSD ceea ce duce la o viteză remarcabil de mare a tuturor operațiilor de la instalarea scripturilor în terminal, până la upload și download.

## Păreri

Aș putea să înșir aici toate specificațiile serviciilor lor dar cu siguranță site-ul lor e mai bun pentru asta, așa că dacă vreți detaliile astea mergeți pe [hosterion.ro][1] și dați citire acolo. Au tot ce ați putea să vreți, și mai mult.

Câteva lucruri în mod special sunt de remarcat:

  * Până și cel mai ieftin pachet de găzduire oferă acces prin SSH &#8211; trebuie doar să trimiți un ticket la suport și se activează. Nu multe firme oferă acces prin SSH din cauza posibilelor escalări de privilegii care pot avea loc, dar din ce mi s-a spus, sunt protejați pe partea asta destul de bine. Chestiile alea basic de securitate gen logare doar cu RSA sunt în efect, deci pe partea de securitate nu ar trebui să vă faceți griji. În contextul în care ai nevoie de terminal în aproape orice astăzi, treaba asta reprezintă un mare plus. Instalează tu Angular/Laravel pe un shared hosting unde n-ai SSH, npm install nema. N-am avut răbdare să deschid un ticket pentru asta dar am reușit să instalez Django prin modulul de creare aplicație Python din cPanel.
  * Viteze mari și ping mic. <img loading="lazy" class="alignnone size-full wp-image-545" src="http://codin.ro/wp-content/uploads/2016/11/ping-hosterion.png" alt="ping-hosterion" width="784" height="450" srcset="https://codin.ro/wp-content/uploads/2016/11/ping-hosterion.png 784w, https://codin.ro/wp-content/uploads/2016/11/ping-hosterion-300x172.png 300w, https://codin.ro/wp-content/uploads/2016/11/ping-hosterion-768x441.png 768w" sizes="(max-width: 784px) 100vw, 784px" />Artemis e serverul pe care mi s-a alocat contul, ping mediu de 10.27ms. Pe upload viteza medie e de 31.6MB/s (fișier de 900MB) și pe download undeva la 60MB/s. Absolut perfect pentru doar 3€ pe lună. (Vorbim totuși de cel mai ieftin pachet de găzduire, nu știu vitezele la pachetele superioare.)
  * Oferă LetsEncrypt prin intermediul unui plugin dezvoltat de ei, conform lor. Mare plus, în ultima perioadă au fost mai multe ocazii în care companiile de găzduire (și din .ro și din .com) au aruncat cu noroi pe LetsEncrypt pentru că le cam fură piața de certificate SSL. De aici pornise și hate-ul meu, dar după ce am văzut mai exact toată treaba nu prea mai am hate deloc, dimpotrivă. (_later edit_*de aici ca topic, nu ca motiv. E lăudabil faptul că promovează SSL, eram eu de-a dreptul calomnios referitor la pluginul pe care îl prezentau ei.)
  * Am instalat pe host Django, Magento și WordPress &#8211; nu e cea mai bună metodă să testezi un pachet de găzduire, dar toate mergeau perfect. Fără nimic pe el Magento s-a încărcat în ~220ms (cu toate cele, nu doar index.php/), și Magento e cunoscut pentru cât de multe resurse înghite &#8211; au un pachet specializat pentru găzduire Magento tocmai din motivul ăsta. Din nou, nu e modul ideal în care să testezi un host, n-am de unde să aduc useri și nici n-am de gând să trag cu LOIC în hostul lor oferit gratuit ca să zic ceva. Dacă nu cade cu alea trei pe el atunci vă promit eu că vă ține un WordPress cu >500 unici pe zi.
  * 3€ pe lună e un preț al naibii de mic, atât de mic încât efectiv oricine poate să își facă prezența online, oamenii oferă și _**email **(am ținut un training pe personal branding recent și un punct din prezentare era legat de cât de bine e să ai o adresă gen personal@persoana.ro__, ăștia 3€ pe lună + un domeniu reprezintă fix tot ce ai nevoie ca să scapi de adresa aia lungă de mail.)_ și FTP și cam tot ce ai putea avea nevoie. Nu știu dacă există cineva mai ieftin, n-am stat să fac cercetare de piață dar chiar dacă ar exista tot pe Hosterion îmi pun banii. După ce mi s-a explicat cum funcționează ei am înțeles că sunt una din puținele companii de la noi care încearcă să meargă pe un stil occidental în care serviciile lor trebuie să fie cele mai bune și eficiente, chiar dacă asta înseamnă X bani peste cel mai ieftin competitor.
  * CEO-ul lor și-a rupt din timp să îmi povestească lucruri, și așa am aflat că au și o parte de VPS-uri unmanaged sub egida [intoVPS.com][2]. Evident datorită părții cu &#8220;unmanaged&#8221; sunt mai ieftine decât pachetele CloudManaged de pe Hosterion, dar puteți să vă așteptați la aceeași calitate și personal de suport tehnic foarte ok &#8211; fiind aceiași oameni în spate.(Aparent aici o să urmeze ceva oferte noi cu prețuri mai mici și un update la tehnologii deci băgați la bookmarks și stați geană dacă vroiați să cumpărați un VPS zilele astea.)

Alte lucruri demne de menționat ar fi că dezvoltă acum o platformă de billing pentru OpenStack sub numele de [fleio][3].

_În concluzie, dacă aveți de schimbat un host în curând &#8211; aruncați un ochi și pe la ei că arată tare bine businessul lor. (*almost forgot, oferă migrare gratuită !!!) Even better, tell your friends about it. Până la urmă, de ce ai hosta site-ul tău în Texas când targetul tău e România?_

***Chiar n-am fost plătit pentru părere, doar că îmi plac (deja) foarte tare oamenii ăștia. Pe vremuri îmi hostam chestiile la Dreamhost pentru că erau cei mai no-frills easy hosting provider de pe piață (în opinia mea), acum le hostez pe un server dedicat, dar dacă n-aș face asta probabil aș merge la Hosterion. Mi se par echivalentul în mentalitate cu cei de la Namecheap (care sunt în principal specializați pe domenii, dar oferă și host) în sensul că totul este cât mai facil posibil pentru utilizatorul final &#8211; de la designul website-ului până la migrarea datelor.**

##

 [1]: http://hosterion.ro
 [2]: http://intovps.com
 [3]: http://fleio.com