---
title: "Vytváranie bezpečného systému"
date: 2023-12-17
tags: ["bezpecnost"]
author: "Marek Chyra"
# author: ["Me", "You"] # multiple authors
description: "Desc Text."
# weight: 1
# aliases: ["/first"]
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: false
disableShare: true
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: false
ShowWordCount: true
ShowCodeCopyButtons: true
ShowRssButtonInSectionTermList: true
UseHugoToc: false
cover:
    image: "<image path/url>" # image path/url
    alt: "<alt text>" # alt text
    caption: "<text>" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/<path_to_repo>/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

Bezpečnosť je cesta, nie cieľ. Prejdime si všetky spôsoby, ktorými nie ste zabezpečení, a ako môžete minimalizovať svoju stopu.
<!--more-->
Ak si myslíte, že stačí nainštalovať sieť VPN a ste v bezpečí... pravdepodobne ste ľahký cieľ.

## Hardvér

Väčšina hardvéru má v súčasnosti firmvér, ktorý sa načíta ešte pred načítaním operačného systému. Toto je najnebezpečnejšia bezpečnostná diera, pretože po zneužití môže napadnutý hardvér získať prístup na úrovni zmeny súborov, vzdialeného zapnutia a úplného prístupu mimo pásma. 

Spoločnosť Intel odviedla najhoršiu prácu pri zabezpečení svojho systému, pretože bol mnohokrát zneužitý, ako je zdokumentované tu: <https://en.wikipedia.org/wiki/Intel_Management_Engine#Security_vulnerabilities>.

Tieto útoky môžete zmierniť aktualizáciou Intel ME, ale jediným spôsobom, ako dieru odstrániť, je odstránenie Intel ME, ktoré zahŕňa flashovanie hardvérového firmvéru a ktoré sa v mnohých systémoch nedá vykonať. Vrelo odporúčam nástroj s otvoreným zdrojovým kódom <https://meshcentral.com/>, ktorý je zadarmo a dokáže za vás aktualizovať veľa týchto systémov bez väčších problémov. Ponúka tiež spôsoby, ako nastaviť tento mimopásmový prístup v systéme s možnosťami vPro. 

V serverovej sfére máte k dispozícii Dell iDRAC a HP iLO pre out of band prístup, ktoré tiež potrebujete zabezpečiť.

Spoločnosť AMD nemá toľko vulnurácií, ale má obavy o bezpečnosť s procesorom AMD Platform Security Processor (PSP), ktorý bol pridaný v roku 2013.

## Operačné systémy

Systém Windows je najproblematickejší s rozsiahlou telemetriou a najväčším počtom CVE pre vzdialené spustenie zo všetkých operačných systémov. Varoval by som však aj pred používaním základnej inštalácie Linuxu, pretože mnohé distribúcie, ako napríklad Arch Linux, nemajú ani firewall. Za najlepšiu voľbu považujem [QubesOS](https://www.qubes-os.org/), pretože má uzamknutý operačný systém a rozsiahlu kompartmentalizáciu prostredníctvom virtuálnych strojov a oddelených sietí. Je však náročné sa ho naučiť. 

## Prehliadače

Neexistuje webový prehliadač, ktorý by som odporúčal. V súčasnosti používam Brave, ale mohol by byť lepší. Všetky webové prehliadače majú svoje chyby a väčšina z nich vychádza z kódovej základne Google Chrome. 

Pravdepodobne najlepší by bol Firefox, ktorý si mozete nakonfigurovat pomocou: <https://github.com/arkenfox/user.js>. Alebo potom by som veľmi obporučil [Tor Browser](https://www.torproject.org/), ktorý je anonymný ale veľmi pomalý a veľa stránok vás bude blokovať. Ak by vás to veľmi limitovalo tak môžete vyskúšať [Mullvad Browser](), ktorý je verziou prehliadača Tor Browser s odstránenou integráciou siete Tor, ktorej cieľom je poskytnúť používateľom technológiu prehliadača Tor Browser proti odtlačkom prstov. Je vyvinutá projektom Tor a distribuovaná spoločnosťou Mullvad a nevyžaduje používanie siete VPN spoločnosti Mullvad. Pre viac odporúčaní môžete si pozrieť stránky ako: [PrivacyGuides](https://www.privacyguides.org/en/desktop-browsers/), [PrivacyTests.org](https://privacytests.org/), [Techlore.tech](https://www.techlore.tech/resources.html#desktop-browsers) alebo [The New Oil](https://thenewoil.org/en/guides/most-important/browser/).

## Správcovia hesiel

Najlepšie by bolo ukladanie do lokalného zašifrovaného miesta na bezpečnom mieste ([KeePassXC](https://keepassxc.org/)), ale pohodlnosť nás často dostane. Najviac odporúčam [Bitwarden](https://bitwarden.com/), ale varoval by som pred mnohými online správcami hesiel, pretože ak niekto získa vaše prihlasovacie meno, všetko bude ohrozené. Najlepším riešením by bol Yubikey alebo iné FIDO zariadenie na fyzické overenie všetkých nových prihasovaní alebo zariadení. Pre ďalšie odporúčaia môžete navšíviť stránky: [PrivacyGuides](https://www.privacyguides.org/en/passwords/) alebo [The New Oil](https://thenewoil.org/en/guides/most-important/passwords/).

## Sieťová brána a otvorené porty

Otestujte svoju sieť a zistite, ktoré porty sú otvorené pomocou [grc.com](https://www.grc.com/x/ne.dll?bh0bkyd2). Ak sa snažíte o bezpečnosť, nemali by ste v smerovači presmerovávať porty ani používať uPnP. Základný test shield up! by vám mal poskytnúť dobrú predstavu o otvorených portoch a oblastiach, v ktorých môžete svoju sieť zlepšiť. Hoci otvorený port nie je koniec sveta, predstavuje zväčšenú plochu na útok, ktorú možno zneužiť. 

## Nebuďte hlúpi

Sťahovanie hacknutých programov, klikanie na podvodné odkazy a inštalácia 50 rozšírení do prehliadača nie sú dobré postupy. Existuje niekoľko nástrojov, ktoré vám pomôžu trénovať sa, ale nie sú nepriestrelné. Bezpečnosť je o vrstvení a používaní zdravého rozumu. Nikdy nemôžete byť stopercentne zabezpečení a súkromní.
