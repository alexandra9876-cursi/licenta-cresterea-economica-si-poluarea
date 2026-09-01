# Capitolul 2 — Date și metodologie

Acest capitol prezintă datele utilizate în analiza empirică, variabilele
incluse în model și metodologia aplicată pentru investigarea relației dintre
creșterea economică și nivelul poluării în Uniunea Europeană.

---

## 2.1 Descrierea datelor

Analiza empirică se bazează pe date secundare preluate din baza de date
**Eurostat**, care oferă indicatori statistici comparabili la nivelul
statelor membre ale Uniunii Europene.

### Eșantion

| Caracteristică | Detalii |
|---|---|
| State analizate | 27 state membre ale Uniunii Europene |
| Perioada | 2008–2022 |
| Frecvența datelor | Anuală |
| Număr de observații | 405 |
| Structura datelor | Date de tip panel |
| Sursa | Eurostat |

Datele de tip panel combină dimensiunea transversală, reprezentată de
statele analizate, cu dimensiunea temporală, reprezentată de perioada
2008–2022.

Utilizarea datelor Eurostat permite comparabilitatea între state datorită
metodologiilor europene unitare de colectare și raportare.

Majoritatea indicatorilor sunt exprimați sub forma unor ponderi relative
sau valori per capita, facilitând comparația între economii cu dimensiuni
și structuri diferite.

---

## 2.2 Descrierea variabilelor

Modelul utilizează o variabilă dependentă și opt variabile independente,
care surprind dimensiuni economice, energetice, structurale și demografice.

### Variabila dependentă

#### Emisiile de gaze cu efect de seră — CO₂ per capita

Variabila dependentă este reprezentată de emisiile de gaze cu efect de
seră exprimate în tone per capita.

Indicatorul agregă principalele gaze cu efect de seră în echivalent CO₂,
permițând utilizarea unui indicator comun pentru analiza impactului
activității economice asupra mediului.

În modelul econometric, variabila este utilizată sub forma logaritmică:

**lnCO₂**

Transformarea logaritmică urmărește reducerea dispersiei datelor și
diminuarea influenței valorilor extreme.

---

### Variabile independente

| Variabilă | Rol în model | Descriere |
|---|---|---|
| PIB per capita | Economică | Indicator al nivelului de dezvoltare economică |
| PIB² | Economică | Surprinde caracterul neliniar al relației PIB–poluare |
| Energie regenerabilă | Energetică | Ponderea energiei regenerabile în consumul final brut |
| Consum de energie | Energetică | Nivelul utilizării resurselor energetice |
| Industria în PIB | Structurală | Ponderea sectorului industrial în PIB |
| Populație | Demografică | Indicator demografic utilizat ca variabilă de control |
| Comerț | Economică | Indicator al deschiderii comerciale |
| Intensitatea energetică | Energetică | Indicator asociat eficienței utilizării energiei |

---

### PIB per capita

PIB-ul pe cap de locuitor reprezintă principalul indicator utilizat pentru
măsurarea nivelului de dezvoltare economică.

Acesta permite compararea economiilor cu dimensiuni diferite ale populației
și este utilizat ca variabilă explicativă principală în testarea ipotezei
Curbei Kuznets de Mediu.

---

### PIB²

PIB² reprezintă pătratul PIB-ului per capita și este introdus pentru a
surprinde caracterul neliniar al relației dintre dezvoltarea economică și
poluare.

Prezența simultană a PIB și PIB² permite testarea formei relației dintre
creșterea economică și degradarea mediului.

Pentru ipoteza clasică EKC, relația așteptată este de tip **U inversat**.

---

### Consumul de energie per capita

Consumul de energie per capita reflectă nivelul utilizării resurselor
energetice într-o economie.

Indicatorul include consumul principalilor utilizatori finali, precum
industria, transporturile, gospodăriile, serviciile și agricultura, precum
și consumul sectorului energetic necesar producerii și transformării
energiei.

În modelul econometric, variabila este utilizată sub forma:

**lnConsum_energie**

Transformarea logaritmică este aplicată pentru reducerea dispersiei și
îmbunătățirea proprietăților statistice ale modelului.

---

### Ponderea industriei în PIB

Ponderea industriei în PIB reflectă structura economică și gradul de
industrializare al unei țări.

Indicatorul este exprimat ca procent din PIB și este utilizat pentru a
surprinde influența structurii economice asupra nivelului emisiilor.

---

### Ponderea energiei regenerabile

Ponderea energiei regenerabile în consumul final brut de energie reprezintă
un indicator al tranziției către surse de energie mai sustenabile.

Variabila este inclusă pentru a analiza rolul utilizării energiei
regenerabile în reducerea nivelului emisiilor de gaze cu efect de seră.

---

### Populația

Populația este inclusă ca variabilă de control pentru a surprinde
dimensiunea demografică a economiilor analizate.

În modelul econometric, variabila este utilizată sub forma logaritmică:

**lnPopulație**

---

### Comerțul

Comerțul este utilizat pentru a surprinde influența deschiderii comerciale
și a globalizării economice asupra nivelului emisiilor.

Intensificarea comerțului poate influența poluarea atât prin extinderea
activității economice, cât și prin facilitarea accesului la tehnologii mai
eficiente și transferul de inovație.

---

### Intensitatea energetică

Intensitatea energetică este utilizată ca indicator asociat eficienței
utilizării energiei.

Aceasta reflectă relația dintre activitatea economică și utilizarea
resurselor energetice și permite analiza rolului eficienței energetice
în explicarea nivelului emisiilor.

---

## 2.3 Metodologia cercetării

Cercetarea utilizează o abordare cantitativă bazată pe metode statistice
și econometrice aplicate datelor de tip panel.

Analiza urmărește atât variațiile dintre statele membre, cât și evoluția
indicatorilor în timp.

### Transformarea datelor

Pentru îmbunătățirea proprietăților statistice ale modelului, anumite
variabile au fost transformate logaritmic.

Transformarea a fost aplicată:

- emisiilor de CO₂;
- consumului de energie;
- populației.

Scopul transformării este reducerea asimetriei și a influenței valorilor
extreme și stabilizarea varianței.

---

## Modelul econometric

Pentru testarea ipotezei Curbei Kuznets de Mediu este utilizat un model de
regresie multivariată.

Modelul estimat este:

**lnCO₂ᵢₜ = β₀ + β₁PIBᵢₜ + β₂PIB²ᵢₜ + β₃Energie_regenerabilăᵢₜ
+ β₄lnConsum_energieᵢₜ + β₅Industria_în_PIBᵢₜ
+ β₆lnPopulațieᵢₜ + β₇Comerțᵢₜ
+ β₈Intensitatea_energeticăᵢₜ + εᵢₜ**

unde:

- **i** reprezintă statul membru analizat;
- **t** reprezintă perioada analizată;
- **β₀** reprezintă termenul liber;
- **β₁...β₈** reprezintă coeficienții variabilelor explicative;
- **εᵢₜ** reprezintă termenul de eroare.

---

## Estimarea prin OLS

Coeficienții modelului sunt estimați prin metoda **Ordinary Least Squares
(OLS)**, utilizată pentru evaluarea relațiilor dintre variabile.

Introducerea simultană a PIB per capita și PIB² permite investigarea
caracterului neliniar al relației dintre dezvoltarea economică și poluare.

Semnele coeficienților celor două variabile economice sunt utilizate
pentru evaluarea formei relației și, implicit, pentru testarea ipotezei
EKC.

---

## Analiza clusterelor

Pentru aprofundarea analizei și identificarea diferențelor dintre statele
membre, este utilizată metoda **K-Means Cluster**.

Clusterizarea urmărește gruparea statelor cu caracteristici economice,
energetice și de mediu similare.

Analiza utilizează valorile medii pentru perioada 2008–2022 și patru
variabile:

1. PIB per capita mediu
2. Emisii CO₂ per capita medii
3. Ponderea medie a energiei regenerabile
4. Intensitatea energetică medie

Variabilele sunt standardizate prin transformarea în **scoruri
standardizate (z-score)** pentru a asigura o contribuție comparabilă în
procesul de clusterizare.

Soluția aleasă în cercetare este formată din **3 clustere**.

---

## Analiza spațială

Pentru reprezentarea geografică a grupurilor rezultate din analiza
clusterelor este utilizat **GeoDa**.

Reprezentarea spațială permite vizualizarea distribuției teritoriale a
clusterelor și completarea analizei statistice cu o perspectivă
geografică.

---

## Validarea modelului

Validitatea modelului econometric este analizată prin verificarea
principalelor ipoteze ale regresiei liniare:

- normalitatea reziduurilor;
- homoscedasticitatea;
- multicoliniaritatea;
- autocorelația.

Pentru aceasta sunt utilizate:

- histograma reziduurilor;
- Normal P-P Plot;
- scatterplot-ul reziduurilor standardizate;
- indicatorul VIF;
- statistica Durbin–Watson.

---

## Fluxul metodologic

```text
Date Eurostat
      ↓
27 state UE × 2008–2022
      ↓
405 observații
      ↓
Pregătirea și transformarea datelor
      ↓
Analiză descriptivă
      ↓
Corelații Pearson
      ↓
Regresie multiplă OLS
      ↓
Testarea EKC
      ↓
Validarea modelului
      ↓
K-Means Cluster
      ↓
Analiză spațială în GeoDa
      ↓
Interpretarea rezultatelor
