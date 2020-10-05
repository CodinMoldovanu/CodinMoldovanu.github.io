---
title: Cum să te cotești în 2019 de ochii albaștri
author: Moldovanu Codin
type: post
date: 2019-08-11T14:49:46+00:00
url: /cum-sa-te-cotesti-in-2019-de-ochii-albastri/
categories:
  - Not-Daily
  - Tech
tags:
  - cibernetica
  - comunicatii
  - criptare
  - crypt
  - cyber
  - cyber security
  - encriptie
  - huawei
  - monitorizare
  - secure
  - securitate
  - securitate cibernetica
  - security
  - signal
  - sigure
  - sts
  - trafic de date
  - whatsapp

---
A devenit din ce în ce mai greu să păstrăm securitatea datelor noastre, cu atât mai mult a anonimității noastre, așa că o să încerc să recomand foarte multe lucruri &#8211; majoritatea fiind catalogate drept paranoia, dar mai bine safe decât sorry, sau așa zice vorba. Cumva, în continuare, utilizatorul este cel mai vulnerabil &#8211; nu serviciile, așa că în ediția asta o să acopăr și protecția personală.

<!--more-->

_Disclaimerul de aici este în mod special pentru puținii băjeți buni cu ochi albaștri, și vă pot număra pe degete, cel puțin cei pe care îi știu: Chestiile astea ar trebui să ajute oameni _**care nu sunt oameni răi per se**_, ar trebui să ajute oameni care vor să schimbe lumea în moduri non-violente, și care vor să fie într-un plan izolat de tot ce înseamnă monitorizare activă sau pasivă, sau chiar oameni care sunt urmăriți pentru motive absolut cretine, indiferent că vorbim de organizarea unui protest sau de discuții neortodoxe despre sisteme de guvernare sau pedepsirea de către popor a unor fapte considerate greșite de mai sus amintitul popor. Skill-urile nu sunt ilegale, so yeah. În plus, jocul de-a șoarecele și pisica ajută ambele părți, deci spor la alergat._

Ne ajută să stabilim de acum cam care sunt vectorii de atac în funcție de categoriile de atacuri.

## Interceptări

  * Telefonie, mesagerie și trafic de date mobile (GSM)
  * Trafic de date (Wi-Fi, Wired)
  * Impersonare

## Amenințări active

  * Social Engineering
  * Phishing
  * Conturi pe diverse platforme
  * Device-uri &#8220;servite&#8221; (cabluri, laptopuri, telefoane, cam tot ce este electronic poate să trimită acasă urări de bine)

## Generalități

#### Password Managers

Da, din păcate am ajuns la momentul în care a devenit esențial să folosești un manager de parole care are grijă de credențialele tale. Practic un password manager este o unealtă care îți reține toate credențialele pentru diversele servicii, oferind astfel posibilitatea folosirii unor parole mult mai complexe fără riscul de a le uita. Majoritatea oferă și câteva opțiuni în plus, și majoritatea au un tier gratuit pentru care nu trebuie să plătești. Amintesc de aici de **KeePass** (de principiu pentru uz local) și **BitWarden** (self-hosted sau cloud-hosted) pentru uz general. Ambele opțiuni sunt open-source, BitWarden are și extensii pentru majoritatea browserelor, precum și pentru toate sistemele de operare &#8211; dezvoltate chiar de ei. Punctele mele în plus se duc la BitWarden și pentru o opțiune foarte facilă de a verifica dacă parola unui cont a fost regăsită în vreunul din dump-urile de parole ce au avut loc de-a lungul timpului. Nu recomand DashLane sau alte nebunii.

Deci un prim pas ar fi să iei toate conturile la rând și să te apuci să le schimbi parola pe care o știi cu o parolă mult mai lungă pe care nu o vei mai știi.

Evident, pe lângă asta activează opțiunile extra de securitate peste tot, fie că vorbim de 2 Factor Authentication sau de FIDO/YubiKey sau amprentă, dacă există &#8211; activează opțiunea. Mențiuni aici o să meargă pentru activarea opțiunii de confirmare a loginului pe Facebook și pe Google, dar majoritatea serviciilor online de astăzi dispun de această opțiune, așa că fuga la activare, mai bine investești 5 secunde în fiecare login decât să pierzi accesul pe vreo platformă pe unde te caută angajatorii, zic.

#### Public Wi-Fi

Evită să folosești orice fel de rețea publică WiFi, fie că vorbim de UPS Public WiFi sau de internetul gratuit oferit de cafeneaua ta preferată, la momentul actual datele mobile au un preț extrem de scăzut deci toți ne putem crea un hotspot când avem nevoie de internet pe un alt device. Din multe puncte de vedere este mai sigur să folosești datele mobile pentru trafic pe internet, dar în același timp dacă vectorul GSM este compromis, nimic nu te mai salvează decât mișcări mult mai complexe care au o șansă reală să îți păstreze în siguranță traficul de date efectuat. Totuși, o opțiune bună pentru conexiuni publice este să folosești un VPN &#8211; fie el self-hosted (dacă consideri că linia ta de acasa nu este compromisă) sau unul dintre marii provideri recunoscuți de astfel de servicii (recomandarea merge către NordVPN pentru posibilitatea achiziției cu BTC).

#### Conexiunea de acasă

Aici sincer problema este destul de complexă, și nu sunt încă 100% sigur dar una dintre opțiunile care îmi vin în minte este o &#8220;rețea privată&#8221; prin mai mulți provideri IaaS cu IP-uri în clase diferite pentru a obfusca pe cât de mult se poate traficul respectiv, astfel încât ce pleacă de la 23.0.0.10 ajunge la 42.50.10.1, trece la 199.13.51.12 și tot așa, securitatea prin obfuscare nu este sigură prin definiție, dar poate ajuta dacă este destul de mult gândită. Practic soluții există, cumva pe drum poți trimite traficul pe Onion sau I2P și să îl scoți mai târziu prin alte părți &#8211; practic mațele-ncurcate varianta IP & Routing. Puncte bonus pentru idei exotice gen drop box public în locuri precum McDonalds, Starbucks et.al., sau pentru idei foarte bine gândite care depind de negarea plauzibilă (e.g. mac spoofing în locuri publice ferite de camere de supraveghere).

#### Device-uri

Pentru telefoane în mod special absolut imperativ să ai un cod de deblocare, sau mai bine &#8211; amprentă pentru deblocare. Ajută de asemenea să activezi criptarea pe device-ul pe care îl folosești, și aici în mod absolut ciudat o să meargă multe recomandări către Apple, mai exact către iPhone care criptează by default toate datele stocate pe device. Muia de serviciu va merge către Huawei [care _**nu**_ oferă criptare în softul implicit al telefonului,][1] așa că singura soluție pentru posesorii de Huawei (inclusiv eu) este folosirea unui alt combo de rom și kernel care oferă aceste opțiuni (AOSP will do ținând cont că Android oferă by default opțiuni de criptare cu dm-crypt).

Aici, în funcție de ce faci cu telefonul o să vrei sau nu o să vrei să ai contul Google atașat, dar în cazul în care ți-ai securizat contul și folosești un Password Manager și 2FA, o să fii în siguranță (cu excepția cazului în care Google primește o cerere din partea unor autorități, caz în care se vor alinia și vor oferi datele cerute).

Nu uita că mai nou, fotografiile au în metadate inclusiv date despre locație cu GPS, deci relativă grijă aici, opțiunile existente erau Camera-V, dar observ că nu au mai fost updatate de ceva timp și nimic nu e mai nesigur decât o aplicație veche.

Pentru laptop de asemenea în funcție de sistemul de operare este o idee bună să criptezi hardul (BitLocker pe Windows, dm-crypt/luks pe GNU/Linux, whatever au pe MacBook-uri) și să folosești o metodă de autentificare biometrică sau terță precum YubiKey/FIDO sau altele asemenea opțiuni.

#### Accesorii

Până și cele mai banale lucruri au devenit niște fronturi la care trebuie să fim atenți, indiferent de dimensiunea lor &#8211; care până mai deunăzi ne făcea să zicem &#8220;ce poate să aibă în el, e doar un cablu&#8221;, dar cablul acela poate ascunde multe lucruri, și poate fi construit de [orice persoană cu un minim de experiență tehnică.][2] În plus, catalogul NSA ne arată o grămadă de device-uri create special pentru ofensivă cibernetică, și trebuie să reținem că majoritatea lucrurilor din catalogul ANT erau create și deja în uz în 2007, adică acum mai bine de 10 ani, între timp putem fi siguri că uneltele au devenit mai mici și mai puternice. Sfatul aici este să cumperi accesorii din locuri aleatorii și să fii foarte atent la ambalajul produsului &#8211; asigură-te că nu a fost deschis înainte și că este identic cu restul produselor de la raft. Nu ai niciun fel de confirmare, dar e posibil să ai mai mult succes decât prin alternativa unei comenzi online. Cazul ipotetic pe care îl văd este achiziționarea unui cablu mai ieftin de la un terț care vinde pe un oarecare magazin online, cablu care vine însoțit de gândăcei digitali care o să îți violeze intimitatea și paranoia.

#### Phishing

Serios nu vreau să scriu despre asta &#8211; nu-ți băga parola unde nu ți-ai băga p**a, e foarte simplu. Nu da click pe linkuri aiurea, nu deschide atașamente cretine și tot așa, n-am ce recomandări să fac pe tema asta. Dacă îți cere cineva parola de la contul de Binance pentru că vrea să îți dea 10BTC, spune-i că ai uitat-o și cere-i să facă 3 pași la stânga.

## Comunicații sigure

#### Mesagerie și Telefonie

În prezent ChatSecure nu mai există, redenumindu-se în Signal, și aceasta este la momentul prezent cea mai sigură metodă de comunicare criptată pe internet atât în categoria de mesagerie cât și în cea de voce. Pentru comunicații extrem de delicate este recomandat să verifici semnătura persoanei cu care comunici în cadrul unei întâlniri IRL pentru confirmarea securității, de asemenea are o opțiune pe care recomand &#8211; blocarea și deblocarea aplicației cu amprenta telefonului.

Demn de menționat că la acest moment și WhatsApp folosește protocolul Signal pentru criptarea comunicațiilor, dar ultima oară când m-am interesat (acum ceva timp) criptarea nu era activată în mod implicit, deci totuși exista șansa ca nu toate comunicațiile să fie criptate. Totuși, deși este folosit protocolul Signal, nu recomand WhatsApp strict datorită deținerii sale de Facebook &#8211; sunt absolut sigur că toate datele ce pot fi minate din WhatsApp sunt minate pentru training de NLP sau marketing.

Practic opțiunea de comunicații sigure se termină aici, nu recomand să folosești altceva în afară de Signal pe orice device pentru schimbul de text/voce cu conținut sensibil, Signal având clienți pentru majoritatea platformelor la momentul actual.

&nbsp;

### Încheiere

Principiile nu s-au schimbat, dar metodele au devenit mai complexe așa că față de acum câțiva ani &#8211; trebuie să investești în mod activ în securitatea ta, a comunicațiilor și a datelor tale, dar poți dormi liniștit știind că investiția asta îți intoarce doar liniște pe fir &#8211; dar totul poate fi compromis și trebuie să fii mereu conștient de asta, la fiecare nivel există vulnerabilitați, deci nu poți fi niciodată sigur de siguranța comunicațiilor tale.

 [1]: https://forum.xda-developers.com/showpost.php?s=aeaf9e0bd1bef1a4c4527be4c3014aed&p=77386602&postcount=4
 [2]: https://mg.lol/blog/omg-cable/