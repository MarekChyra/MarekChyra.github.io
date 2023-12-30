---
title: "Ako Bezpečne Spravovať Hesla"
date: 2023-12-22
# weight: 1
# aliases: ["/first"]
tags: ["hesla", "bezpecnost", "spravca hesiel"]
author: "Marek Chyra"
# author: ["Me", "You"] # multiple authors
showToc: true
TocOpen: true
draft: false
hidemeta: false
comments: false
#description: "Desc Text."
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

# Čo je to správca hesiel?

Správca hesiel je program alebo služba, ktorá umožňuje zaznamenávať prihlasovacie údaje, ako je používateľské meno, heslo, odkaz na prihlásenie a ďalšie údaje.

Vaša databáza hesiel je uložená v zašifrovanom formáte.

Ďalšie bezpečnostné opatrenia sa v jednotlivých službách líšia.

# Prečo potrebujem správcu hesiel?

**Najdôležitejšia vec, ktorú môžete urobiť na ochranu svojich účtov, je používať silné, jedinečné heslá, ktoré sa nikde nepoužívajú opakovane.**

**Silné heslo by malo pozostávať zo šestnástich alebo viacerých znakov, ktoré sa skladajú z veľkých a malých písmen, číslic a špeciálnych znakov a nemalo by sa opakovane používať na iných účtoch.**

Táto posledná rada je poistkou: ak služba nešifrovala - alebo zle šifrovala - vaše heslo, nepoužívanie hesiel (a používateľských mien) zabráni útočníkovi v tom, aby mal ľahký prístup ku všetkým vašim ostatným účtom. Tomuto postupu sa hovorí credential stuffing.

Samozrejme, to znamená, že dobré heslo si nemožno zapamätať, takže riešením je používanie správcu hesiel.

Používaním správcu hesiel si vždy musíte pamätať len jedno heslo: hlavné heslo na prihlásenie.

# Čo by som mal hľadať v správcovi hesiel?

**Najdôležitejšie je hľadať službu, ktorá má "Zero knowledge". Môžu tiež používať výrazy ako "Zero access" Alebo "End-to-end encrypted".**

(Poznámka: toto sa líši od bežného šifrovania. To znamená, že žiadny zamestnanec spoločnosti nemôže vidieť vaše heslá a informácie.

Pamätajte: ak ich vidí on, môže ich vidieť aj zločinec, ktorý získa prístup.

**Mali by ste tiež zvážiť či sú cloudové služby pre vás vhodné.**

Cloudové služby ponúkajú také vymoženosti, ako je synchronizácia medzi zariadeniami, ale zároveň riskujete, že úspešný zločinec si stiahne vašu databázu a potom bude mať všetok čas na svete, aby našiel slabiny v šifrovaní.

Naopak, lokálne uložené databázy sú bezpečnejšie pred únikom údajov, ale hrozí riziko, že sa vymažú, stratia alebo poškodia, ak nebudete udržiavať spoľahlivé zálohy.

# Odporúčania pre správu hesiel

| Názov | Výhody | Nevýhody |
| --- | --- | --- |
| ![](https://upload.wikimedia.org/wikipedia/commons/c/cc/Bitwarden_logo.svg) | Auditované, K dispozícii na všetkých operačných systémoch, Podpora passkey | Cloudové |
| ![](https://keepassxc.org/assets/img/keepassxc.svg) KeePass | Niektoré klienty sú auditované, Dostupné na všetkých operačných systémoch, Populárne klienty sú KeePass XC, KeePassDX (Android) a Strongbox (iOS) | Nie všetky klieny sú auditované, Nie je cloudové, Veľmi limotovaná podpora passkey |
| ![](https://res.cloudinary.com/dbulfrlrz/image/upload/v1693233226/static/logos/proton-pass-icon-alone_d9lfmx.svg) Proton Pass | Auditované, K dispozícii na všetkých operačných systémoch, Súčasťou konta Proton je bezplatný kalendár, cloudové úložisko, e-mail a VPN | Cloudové, Žiadna desktop aplikácia, Žiadna porpora passkey |
