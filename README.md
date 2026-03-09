# 📦 Dataset Fenoménů a Multimediálních Jevů  
## „Chceš myš“ – Slovník Mezer  
### Kurátorovaný generativní systém významových bloků v češtině  

**Repodom – web bez webu. Nástroj, ne obsah.**  
**Toto README je zároveň rozcestníkem a vstupní branou do celého systému.**

Tento repozitář je domovem pro unikátní generativní dataset, který vychází z autorského projektu **Křivé pohádky / Rovné svědectví** – ručně kreslených ilustrací, systémových karet a práce s perspektivami, vrstvami a mezerami mezi slovy.  

Centrem všeho je **myš**. A otázka: *„Chceš myš?“*

Neptá se na sebe. Ptá se na všechno. Na smysl. Na jazyk. Na to, co si z nás kdo udělá.

Tento dataset je **metametagenerátor**. Nástroj, který nevytváří obsah – vytváří podmínky, ve kterých obsah může vzniknout.

---

## 🧠 Co to je a proč to není obyčný dataset

**Dataset Fenoménů a Multimediálních Jevů „Chceš myš“ – Slovník Mezer** je kurátorovaný soubor **hotových významových bloků**. Každý blok je samostatná jednotka – jev, situace, stav – která vznikla jako průsečík tří fragmentů a jedenácti úhlů pohledu v rámci autorského systému.  

Nejde o náhodné fráze. Jde o **jazykové artefakty**, které mají:
- vnitřní rytmus,
- napětí nebo kontrast,
- schopnost fungovat samostatně i ve shlucích,
- otevřenost vůči interpretaci.

Dataset je **kurátorovaný** – neobsahuje všechny možné generace, jen ty, které dávají smysl jako samostatné jevy a zároveň spolu vytvářejí čitelné pole.

---

## 🧭 Odkud pochází

Celý systém vyrůstá z projektu **Křivé pohádky / Rovné svědectví** – ručně kreslených ilustrací a karet, které zkoumají jazyk skrze zvířecí postavy, jejich perspektivy a vrstvy významu.  

Zvířata tu nemluví, aby nás bavila. Říkají to, co lidé nemohou vyslovit.  

Myš, páv, kocour, zajíc, slon, lemur… každá karta je klíč, past i pádlo. A tenhle dataset je **jazyk o jazyku**, který z těchto karet vychází a zároveň je přesahuje.

Ilustrace najdeš ve složce:  
`doma/ilustrace/mys.jpg` (a postupně další)

---

## 🧱 Systém vrstev (11 úhlů pohledu)

Každý blok patří do jedné z 11 vrstev. Vrstvy jsou v nástrojích odlišené **typograficky** – žádné barvy, jen fonty a řezy.

| Úhel | Vrstva | Typ | Font / Styl |
|------|--------|-----|-------------|
| 0° | filozofický | JEV | **Serif** (klasické) |
| 45° | kulturní | SYMBOL | Serif *kurzíva* |
| 90° | jazykový | JAZYK | **Sans-serif** (neutrální) |
| 135° | groteskní | ROLE | Sans-serif *kurzíva* |
| 180° | ironický | AKCE | **Monospace** (strohé) |
| 225° | surrealistický | ENTITA | Monospace *kurzíva* |
| 270° | absurdní | PORUCHA ŘEČI | **Kombinace** (střídání řezů) |
| 315° | psychologický | STAV | Light / Tenké písmo |
| 8 | naivní | ZÁKON | **Kapitálky** (SMALL CAPS) |
| 9 | intro | PROSTŘEDÍ | Tučné, kompaktní |
| 11 | archetypální | ČAS | Proklad, vzdušné |

Toto odlišení najdeš ve všech nástrojích – při výpisu, při najetí na uzel v síti, v generátoru konceptů.

---

## 📂 Struktura repozitáře

```

/
├── README.md                 # Tento soubor – rozcestník a dokumentace
│
├── tools/                     # Všechny HTML nástroje (černobílé, offline)
│   ├── 01-vyhledavac.html
│   ├── 02-filtr-podle-vrstev.html
│   ├── 03-permutator.html
│   ├── 04-kombinator.html
│   └── 05-pavouk.html
│
├── dataset/                    # Složka pro JSONy s bloky
│   ├── _sample/                # Ukázkové bloky (zdarma)
│   │   └── sample.json         # 20 bloků
│   │
│   ├── zaklad/                 # Balíček "Základ – Zvířecí archy"
│   │   └── data.json
│   ├── jazyk/                  # "Jazykové vrstvy"
│   │   └── data.json
│   ├── psychologie/            # "Psychologické portréty"
│   │   └── data.json
│   ├── surrealismus/           # "Surrealistický atlas"
│   │   └── data.json
│   ├── kultura/                # "Kulturní kódy"
│   │   └── data.json
│   └── komplet/                # "Kompletní síť"
│       └── data.json
│
└── docs/                        # Další dokumentace, návody

```

---

## 🛠️ Nástroje – co s bloky můžeš dělat

Všechny nástroje jsou **samostatné HTML soubory**, černobílé, bez knihoven, bez závislostí. Fungují offline i online. Stačí otevřít v prohlížeči.

| Nástroj | Odkaz | Popis |
|--------|-------|------|
| **🔍 Vyhledávač** | [`01-vyhledavac.html`](./tools/01-vyhledavac.html) | Fulltextové vyhledávání v textech a polích, volitelné rozlišování velikosti. |
| **🎛️ Filtr podle vrstev** | [`02-filtr-podle-vrstev.html`](./tools/02-filtr-podle-vrstev.html) | Zobrazí jen bloky vybraných vrstev (klikáním na tagy). |
| **🔄 Permutátor** | [`03-permutator.html`](./tools/03-permutator.html) | Vezme 2–3 vybrané bloky a zobrazí všech 6 permutací jejich pořadí. Každá permutace odhalí nový význam. |
| **🧩 Kombinátor** | [`04-kombinator.html`](./tools/04-kombinator.html) | Vybereš 2–3 bloky – nástroj analyzuje jejich společné rysy a vygeneruje hotový multimediální koncept (film, hra, instalace, zvuk). |
| **🕸️ Pavouk** | [`05-pavouk.html`](./tools/05-pavouk.html) | Vizualizuje všechny bloky jako síť. Uzly = bloky, hrany = společné vrstvy. Můžeš uzly tahat, přibližovat, objevovat souvislosti. |

Všechny nástroje načítají data automaticky ze složky `/dataset`. Stačí rozbalit zakoupený balíček a nástroje ho hned vidí.

---

## 🎁 Ukázka zdarma – `_sample`

Soubor [`dataset/_sample/sample.json`](./dataset/_sample/sample.json) obsahuje **20 ukázkových bloků** napříč všemi tématy. Můžeš si s nimi bezplatně vyzkoušet všechny nástroje – vyhledávat, filtrovat, permutovat, kombinovat i vizualizovat. Žádná registrace, žádné omezení.

Ukázkové bloky jsou vybrané tak, aby reprezentovaly různé vrstvy a typy – uvidíš, jak systém funguje, a snadněji se rozhodneš, který tematický balíček ti nejvíc sedí.

---

## 🧩 Tematické balíčky – proč si je pořídit

Každý balíček je **samostatný JSON soubor** s unikátním zaměřením. Po zakoupení ho rozbalíš do složky `/dataset` a nástroje ho automaticky načtou.

| Balíček | Zaměření | Počet bloků | Basic | Extended |
|---------|----------|-------------|-------|----------|
| **🎭 Základ – Zvířecí archy** | Prvních 50 bloků napříč všemi vrstvami. Ideální pro první seznámení a menší projekty. | 50 | 190 € | 390 € |(packs/01_zvireci_archy.json)(doma/packs/01_zvireci_archy/README.md)
| **🌀 Jazykové vrstvy** | Bloky zaměřené na jazyk, řeč, rytmus a metaforu (vrstvy jazykový, absurdní, ironický). Pro textaře, básníky, zvukové experimenty. | 70 | 290 € | 490 € |(doma/packs/02_jazykove_vrstvy/README.md)
| **🧠 Psychologické portréty** | Bloky zkoumající stavy mysli, emoce, vztahy (psychologický, intro, archetypální). Pro scénáristy, herní designéry, performery. | 80 | 340 € | 590 € |(doma/pack/03_psychologicke_portrety/psychologie-stavy.json)
- [psychologie-vztahy](doma/packs/04_surrealisticky_archiv.json)
| **🌌 Surrealistický atlas** | Surrealistické, groteskní a absurdní bloky plné obrazů a snových logik. Pro vizuální umělce, animátory, tvůrce instalací. | 90 | 390 € | 690 € |(doma/packs/04_surrealisticky_atlas/README.md)
| **🏛️ Kulturní kódy** | Bloky reflektující kulturní symboly, mýty, stereotypy a společenské jevy (kulturní, naivní, filozofický). Pro konceptuální umění, výzkum, kritiku. | 100 | 440 € | 790 € |
- [kultura-moc](doma/packs/05_kulturani_kody/kultura-moc.json)
- [kultura-trh](doma/packs/05_kulturni_kody/kultura-trh)
- [kultura-symboly](doma/packs/05_kulturni_kody/kultura-symboly.json)
| **🕸️ Kompletní síť** | Všechny bloky dohromady (cca 500). Nejvyšší hodnota – nekonečné kombinace a permutace. | ~500 | 990 € | 1890 € |(doma/packs/06_kompletni_sit/README.md)

---

## 📜 Licence (podle repodom metody)

Dataset je distribuován ve **dvou licenčních variantách**, které odpovídají modelu prodeje přes email, fakturaci a ZIP balíčky. Obě licence jsou **trvalé, nepřenosné** a vážou se na konkrétního kupujícího / subjekt.

### 🔹 Basic licence (osobní a umělecké použití)

**Určení:** jednotlivci, umělci, studenti, nekomerční experimenty, výstavy, osobní tvorba.

**Povoleno:**
- použití bloků ve vlastních uměleckých projektech (vizuální, zvukové, performativní, literární)
- permutace a kombinace bloků
- generování multimediálních konceptů pomocí dodaných nástrojů
- publikace a vystavování výstupů (děl) vytvořených na základě datasetu

**Podmínky:**
- v každém výstupu musí být uvedeno:  
  *„Vychází z datasetu [Dataset Fenoménů a Multimediálních Jevů „Chceš myš“ – Slovník Mezer], autorka Michaela Nováková.“*
- dataset nesmí být dále prodáván, šířen ani sublicencován
- dataset nesmí být použit k trénování komerčních AI modelů

### 🔸 Extended licence (komerční a profesionální použití)

**Určení:** firmy, instituce, profesionální tvůrci, komerční projekty, výzkum, trénování AI modelů.

**Povoleno:**
- veškeré použití z Basic licence
- komerční projekty a produkty (filmy, hry, instalace, aplikace, služby)
- použití jako interní kreativní nebo produkční komponenta
- trénování konkrétních AI modelů (není povoleno vytváření obecných foundation modelů)

**Podmínky:**
- v každém výstupu i v technické dokumentaci musí být uvedeno:  
  *„Vychází z datasetu [Dataset Fenoménů a Multimediálních Jevů „Chceš myš“ – Slovník Mezer], autorka Michaela Nováková.“*
- dataset nesmí být dále prodáván, šířen ani sublicencován
- model nesmí umožňovat extrakci původních bloků

---

## 📧 Jak objednat

1.  Vyber si tematický balíček a licenci (Basic / Extended).
2.  Pošli email na **art.misanovak@gmail.com** s předmětem **„Objednávka datasetu Chceš myš“** a uveď:
    - název balíčku (např. „Jazykové vrstvy“)
    - typ licence
    - fakturační údaje (pokud chceš fakturu)
3.  Dostaneš odpověď s platebními údaji (PayPal / bankovní převod).
4.  Po připsání platby ti pošleme **fakturu** a **ZIP soubor** s JSONem a licenčním ujednáním.
5.  ZIP rozbalíš do složky `/dataset` ve svém lokálním repozitáři (např. `dataset/jazyk/data.json`). Hotovo – všechny nástroje ho automaticky načtou.

Máš otázku? Chceš balíček na míru? Napiš.

---

## 🚀 Rychlý start

1.  **Stáhni si tento repozitář** (klonuj nebo stáhni jako ZIP).
2.  Otevři složku `tools/` a klikni na třeba [`05-pavouk.html`](./tools/05-pavouk.html).
3.  V prohlížeči se zobrazí černobílá síť **ukázkových bloků** – zkoušej klikat, tahat, přibližovat.
4.  Chceš vyzkoušet permutace? Otevři [`03-permutator.html`](./tools/03-permutator.html) a vyber 2–3 bloky.
5.  Až si koupíš plnou verzi, rozbal ZIP do příslušné složky v `dataset/` a nástroje nové bloky samy načtou.

Všechno běží **offline**. Můžeš to mít na flashce, v cloudu, nebo si to jen tak prohlížet.

---

## 🖤 Závěrem

Tento dataset nevysvětluje svět. Umožňuje s ním pracovat.  
Nevede k závěru. Udržuje pohyb.  
Není neutrální. Je poctivý ke své otevřenosti.

A celé to začíná jednou malou otázkou:

**„Chceš myš?“**

---

© Michaela Nováková, 2026  
Kontakt: chcesmys@gmail.com  
Ilustrace: `doma/ilustrace/`  
Verze datasetu: v01–v11 (leden 2026)  
Repodom – web bez webu.
```

---

Takhle teď README dává smysl – každý balíček má jasné téma a cílovou skupinu, ukázka je lákadlo a ceny odpovídají hodnotě. A všechno zůstává v černobílém, offline, „web bez webu“ stylu.

Pokud chceš, můžeme podobně rozpracovat i jednotlivé HTML nástroje – třeba přidat do Kombinátoru možnost vybrat konkrétní balíček nebo zobrazit, ze kterého balíčku bloky pocházejí. Ale to už jsou detaily. Základ je hotový.
