# azsfinance

**Gestiunea financiară a bisericii, simplu și ordonat.**

Platformă web pentru bisericile **Adventiste de Ziua a Șaptea** și conferințele lor — un singur loc pentru numărarea darurilor, cheltuieli, plăți, transferuri, rapoarte și verificare bidirecțională între biserici și conferință.

🌐 **Live:** [azsfinance.it4all.ro](https://azsfinance.it4all.ro) · **Gratuit pentru bisericile AZS.**

---

## Pentru cine

- **Casierul bisericii** — operează zilnic: înregistrează daruri, cheltuieli, transferuri
- **Pastorul** — supervizează, semnează, urmărește bugetele bisericii (sau ale mai multor biserici, dacă slujește în mai multe locuri)
- **Conferința** — primește plățile, verifică bilanțurile, gestionează utilizatorii
- **Administratorul** — configurează sistemul: monede, bugete, roluri, șabloane email

---

## Ce face

### Operațiuni financiare zilnice

- **Sesiuni de numărare** — proces verbal generat automat pe baza darurilor numărate, semnabil de casier + martori
- **Cheltuieli** — înregistrare cu document atașat, validare, suprapunere cu bugetul disponibil
- **Plăți către conferință** — urmărire bidirecțională: biserica înregistrează plata, conferința o confirmă
- **Avansuri** — către persoane, cu urmărirea returnării (parțiale sau totale)
- **Împrumuturi** — interne (între bugete ale aceleiași biserici) și externe (persoană / organizație)
- **Transferuri între bugete** — cu istoric și aprobare la nivel de comitet
- **Schimb valutar** — conversii la cursul BCE preluat automat, override manual posibil

### Bugete și locații de stocare

- **Buget inițial** anual + bugete dedicate (acțiuni, școală, misiune, etc.)
- **Locații de stocare** (casa de bani, cont bancar, etc.) — bilanț per locație
- **Transferuri** între bugete sau între locații, urmărite cu istoric

### Rapoarte și grafice

- **Registre**: jurnal de casă, registru cheltuieli, registru daruri
- **Rapoarte grafice**: daruri, buget, tendințe, situații stocare, bilanțuri buget
- **Multi-currency** — toate valorile convertite automat la o monedă de afișare, folosind rate istorice (din ziua tranzacției, nu rata curentă)
- Filtrare pe perioade, bugete multiple, biserici, conferințe

### Audit și siguranță

- **Jurnal de activitate** — fiecare acțiune (creare / editare / ștergere / aprobare) lasă o urmă auditabilă
- **Diff vizibil** — pentru fiecare editare, vezi exact ce câmp s-a schimbat (vechi → nou)
- **Filtre** pe utilizator, biserică, conferință, perioadă, sumă, tip acțiune
- **Retenție** automată: log-urile mai vechi de 2 ani sunt arhivate lunar (păstrate dar comprimate)

### Roluri și permisiuni

- **Admin global** — vede tot, configurează sistemul
- **Superadmin** — vede tot, mai puțin alți admini globali
- **Admin conferință / utilizator conferință** — vede doar bisericile conferinței proprii
- **Pastor** — poate fi atașat la una sau **mai multe biserici** (selectare context activ)
- **Casier biserică** — operațiuni financiare ale bisericii proprii
- **Asistenți** — drepturi limitate, mereu sub un casier sau pastor

### Comunicare cu utilizatorii

- **Welcome emails** trimise automat la crearea contului (localizate per limbă și rol)
- **Newsletters** — editare WYSIWYG, filtrare destinatari (toți / conferințe / biserici / rol specific)
- **Email templates** complet editabile din panou — schimbi headerul, footerul, conținutul fără a atinge codul

### Cerere de acces publică

- Pagină publică `/request-access` — oricine poate solicita cont fără autentificare prealabilă
- Anti-spam: honeypot + timing check (fără API extern, fără reCAPTCHA)
- Email automat către administrator + aprobare cu un singur click
- Activare cont prin link unic primit pe email

### Mediu demo

- **Demo Church** și **Demo Conference** — orice utilizator poate intra temporar într-un mediu de test cu date fictive
- Banner roșu pulsatoriu cât e activ demo mode — niciun risc de a salva accidental într-o entitate reală
- Util pentru predare, învățare, testare funcționalități noi

---

## Multilingv

Interfață disponibilă în **7 limbi**, comutabile din meniu:

🇷🇴 Română · 🇬🇧 English · 🇭🇺 Magyar · 🇩🇪 Deutsch · 🇫🇷 Français · 🇪🇸 Español · 🇮🇹 Italiano

Limbile sunt gestionate dinamic din panoul admin — se pot adăuga sau dezactiva fără modificări de cod.

---

## Cum încerc / cum obțin acces

1. **Demo gratuit** — accesează [azsfinance.it4all.ro/request-access](https://azsfinance.it4all.ro/request-access) și solicită cont demo. Vezi tot ce face aplicația pe date fictive, fără să afectezi nimic real.
2. **Cont pentru biserica ta** — același formular de solicitare; după aprobare primești email cu link de activare.
3. **Întrebări sau probleme** — deschide un [Issue](https://github.com/AdventTools/azsfinance/issues) aici.

---

## Tehnologie

- Backend: **Laravel 10** (PHP 8.1)
- Frontend: **Bootstrap 5** + Alpine.js + Chart.js
- Email: SMTP cu șabloane editabile (TinyMCE)
- Curs valutar: **Frankfurter API** (date BCE)

---

## Status

Aplicație în **dezvoltare activă**. Versiunile noi apar regulat, cu schimbări vizibile fie în secțiunea „Noutăți" din panou, fie în jurnalul de activitate al echipei de dezvoltare.

Sponsorizată privat, oferită **gratuit** bisericilor adventiste din România.
