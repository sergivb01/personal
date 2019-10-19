+++
date = "2019-10-19"
title = "Censura de Tsunami Democràtic"
slug = "tsunami-censorship"
description = "Com s'ha aplicat la censura de Tsunami Democràtic i com evitar-la."
+++
# Què és Tsunami Democràtic
-- PER FER

## Dominis
L'organització té diversos dominis, com `tsunamidemocratic.cat` i `democratictsunami.eu`. Ambdós es van comprar mitjançant *TuCows Domains Inc.* el **13 de juliol del 2019** i utilitzen els servidors DNS de [Cloudflare](https://cloudflare.com) per protegir-se de possibles atacs.

La pàgina web de l'organització estava feta per dues pàgines, una per distribuir i publicar l'aplicació utilitzada per organitzar manifestacions i l'altre per l'organització en si. Pocs dies després de l'inici de les manifestacions ambdues pàgines es van fusionar en una.

## Allotjament
La pàgina de l'aplicació (`app.tsunamidemocratic.cat`) estava allotjada a [GitHub Pages](https://pages.github.com) utilitzant el compte de [s3rrallonga](https://github.com/s3rrallonga), un bandoler Català semblant a *Robin Hood* ([més informació](https://www.sapiens.cat/temes/personatges/qui-era-serrallonga_17330_102.html)). El repositori [s3rrallonga.github.io](https://github.com/s3rrallonga/s3rrallonga.github.io) té més de **32 forks** i **40 estrelles**, tot i que l'organització en si no ha publicitat el repositori. També té alguns *problemes* on la gent ha demanat una versió de l'aplicació per a *iOS* i alguns altres problemes menors de l'aplicació.

L'allotjament de la primera versió de la pàgina principal (`tsunamidemocratic.cat`) segueix desconegut, però l'última versió (la fusionada amb la de l'aplicació) també està allotjada utilitzant **GitHub Pages** mitjançant l'organització de [tsunamidemocratic](https://github.com/tsunamidemocratic), que no té membres adherits. L'únic [repositori que té l'organització](https://github.com/tsunamidemocratic/tsunamidemocratic.github.io) és el que conté la pàgina i que, en diferència a l'altre repositori, té els **issues deshabilitats** però accepta **pull requests** (només hi ha una, que sembla ser una broma).

L'historial de *commits* (o canvis) dels dos repositoris ens deixa saber que hi ha varia gent treballant en aquestes pàgines perquè els autors d'aquests són diferents (s3rrallonga, **root** i **Jean**), tot i que només un d'aquests té el perfil vinculat a GitHub.

## Com es va efectuar el tancament
La Justícia espanyola ha començat una investigació de *Tsunami Democràtic* per terrorisme i com a conseqüència ha decidit tancar les seves pàgines. Per fer-ho, els [Servidors DNS](https://www.cloudflare.com/learning/dns/what-is-a-dns-server) dels principals proveïdors d'Internet a Espanya han **alterat les respostes DNS** dels diferents dominis que portaven a les pàgines, incloent-hi un grapat de [mirrors](https://en.wikipedia.org/wiki/Mirror_website) publicats al [Canal de Telegram](https://t.co/anoncatalonia) d'Anonymous Catalunya.

{{< figure src="/images/tsunami-mirrors.jpg" caption="Missatge del canal de Telegram d'Anonymous Catalunya on es comparteixen Mirrors de la pàgina" link="http://tsunamidemocratic.github.io" target="blank" >}}

Piulada de [@Guardiacivil](https://twitter.com/guardiacivil) anunciant el tancament de les pàgines web.
{{< tweet 1185201502694137858 >}}

La censura va afectar a aquells qui els seus proveïdors d'Internet van participar en l'alteració dels servidors DNS i no havien canviat la configuració DNS en els seus dispositius. Com la imatge següent mostra, utilitzant els [servidors DNS de Cloudflare](https://1.1.1.1) pots accedir a les diferents pàgines web, mentre utilitzant els de [Movistar](https://www.movistar.es) (també conegut com a Telefónica) no hi pots accedir.

{{< figure src="/images/tsunami-takedown-notaffected.jpg" caption="Pàgina original, el que veien els que no estaven afectats per la censura" link="http://tsunamidemocratic.github.io" target="blank" >}}

Prou divertit és que el domini `tsdem.org`, després de ser censurat, ha estat redirigit a la [Declaració dels Drets Humans](https://www.un.org/en/universal-declaration-human-rights) de Nacions Unides, mitjançant una *Cloudflare Web Rule* (com mostra la següent imatge).

{{< figure src="/images/tsunami-redirect-humanrights.jpg" caption="Captura de pantalla d'una peitició cap a tsdem.org, utilitzant les eines de desenvolupador de Chrome" >}}

## Pàgina de censura
Com he comentat prèviament, els usuaris afectats són redirigits a `http://82.223.97.47`, que sembla que està allotjada a [Ionos](https://www.ionos.es), també conegut com a *1and1*, i utilitza [Nginx](https://www.nginx.com) com a servidor web i [Plesk](https://www.plesk.com) per la gestió del lloc (perquè el port `8443` està obert i mitjançant aquest pots accedir al panell de Plesk).

{{< figure src="/images/tsunami-takedown.jpg" caption="Pàgina web a la que eres redirigit si estaves afectat per la censura" link="http://82.223.97.47" target="blank" >}}
