# ⚔️🏰 Super Medieval Crossy Road — Multiplayer Kingdom Edition

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Play%20Live-f59e0b?style=for-the-badge&logo=github&logoColor=black)](https://<username>.github.io/<repo-name>/)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20ES6+-fde047?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5 Canvas](https://img.shields.io/badge/HTML5-Canvas%2060%20FPS-dc2626?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![WebRTC](https://img.shields.io/badge/Multiplayer-WebRTC%20P2P%20(PeerJS)-10b981?style=for-the-badge&logo=webrtc&logoColor=white)](https://peerjs.com/)

> **Descriere scurtă pentru secțiunea „About” de pe GitHub:**  
> ⚔️🏰 *Super Medieval Crossy Road – Joc arcade multiplayer în HTML5 Canvas & Vanilla JS. Include Lobby P2P (WebRTC), 4 biomuri medievale dinamice, evenimente globale sincronizate (Dragoni, Ploaie de Săgeți), artefacte magice, boți AI și mod spectator. Zero backend, 100% pregătit pentru GitHub Pages!*

**Topic-uri (Tags) recomandate pentru depozitul GitHub:**  
`javascript` `html5-canvas` `crossy-road` `medieval-game` `multiplayer-game` `webrtc` `peerjs` `p2p` `github-pages` `procedural-generation`

---

## 📖 Despre Proiect

**Super Medieval Crossy Road** este o reinterpretare completă, cu tematică **Medieval Fantasy**, a celebrului joc arcade *Crossy Road*, construită într-un singur fișier autonom (`index.html`), fără dependențe de server (zero backend).

Jocul îți permite să creezi o cetate (**Lobby**) și să te distrezi alături de prietenii tăi în timp real prin **WebRTC Peer-to-Peer**, explorând **4 tărâmuri medievale** pline de calești regale, catapulte draconice, râuri de lavă, artefacte magice și evenimente imprevizibile sincronizate pe ecranele tuturor jucătorilor.

---

## 🌟 Caracteristici Principale

### 👥 1. Taverna Multiplayer & Lobby Complet (Zero Backend)
* **Cod de Cetate din 5 Caractere:** Regele (Host-ul) creează lobby-ul și trimite codul prietenilor (ex: `KNG7X`) pentru conectare instantanee prin **PeerJS (WebRTC)**.
* **Sincronizare Multi-Tab Locală (`BroadcastChannel`):** Poți testa sau juca în mai multe tab-uri pe același PC fără latență.
* **Hartă & Evenimente 100% Deterministe (`Mulberry32 Seeded PRNG`):** Toți jucătorii din lobby primesc același `matchSeed` la începutul bătăliei — fiecare copac, monument Excalibur, caleașcă, plută și eveniment mondial apare simultan în același loc pentru toți participanții.
* **Cavaleri AI Competitivi:** Host-ul poate adăuga în lobby boți inteligenți (`Sir Lancelot [BOT]`, `Merlin Arcanul [BOT]`, `Ragnar Lothbrok [BOT]`, `Regele Arthur [BOT]`) care evită caleștile, se feresc de țintele ploii de săgeți și colectează artefacte.
* **Mod Spectator & Cronica Bătăliei (Podium):** Dacă ești eliminat, camera îl urmărește automat pe cavalerul supraviețuitor (poți comuta între prieteni cu tasta `Tab`). La finalul rundei este afișat podiumul complet și butonul de **Revanșă**.

### 🗺️ 2. Patru Biomuri Medievale Dinamice (Progresie la fiecare 25 de rânduri)
La fiecare 25 de pași înainte, tărâmul, obstacolele, apele și particulele atmosferice se transformă complet:
1. 🏰 **Ținutul Coroanei (Rândurile 0–24):** Pajiști de smarald cu stejari, săbii *Excalibur* înfipte în piatră, drumuri imperiale pavate cu calești regale, șanțuri de apărare cu plute de lemn și licurici aurii.
2. 🧪 **Mlaștina Blestemată (Rândurile 25–49):** Pământ întunecat cu arbori uscați, pietre funerare, ciuperci bioluminiscente, care ale ciumei, ape acide verzi și spori plutitori.
3. ❄️ **Trecătoarea Înghețată (Rândurile 50–74):** Câmpuri de zăpadă cu brazi înghețați, pietre runice vikinge strălucitoare, sănii de război, berbeci de asediu, sloiuri de gheață plutitoare și ninsoare.
4. 🔥 **Citadela Draconică (Rândurile 75–99, ciclic):** Rocă vulcanică de obsidian cu braziere aprinse, catapulte de asediu, râuri de lavă topită cu plăci de bazalt și scântei de foc.

### 🐉 3. Evenimente Aleatorii în Regat („Random Stuff Happening”)
Calculul bazat pe timpul meciului declanșează periodic evenimente dramatice sincronizate pentru toți jucătorii:
* 🐉 **Umbra Dragonului (Dragon Flyby):** Un dragon uriaș zboară în diagonală peste câmpul de luptă, întunecând pământul și lăsând în urmă un răget și scântei de foc.
* 🏹 **Ploaie de Săgeți Regale (Arrow Volley):** Pe hartă apar ținte roșii/aurii (`🎯`) cu numărătoare inversă; când timpul expiră, săgețile lovesc acele dale (eliminând jucătorii fără Scut Sfânt aflați pe țintă!).
* 🎺 **Decretul Regelui – Goana după Aur:** Timp de câteva secunde, fiecare pas înainte oferă **Glorie Dublă (+2 puncte/rând)**.
* ⚡ **Furtună Arcană:** Fulgere magice luminează cerul și încarcă plutele de pe râu cu energie arcană.

### 🛡️ 4. Artefacte & Power-Up-uri Medievale
* 🛡️ **Scutul Sfânt (Holy Aegis – 6s):** Imunitate la calești, catapulte și săgeți + creează automat un **Pod Sfânt de lumină** sub picioarele tale când pășești pe apă, acid sau lavă!
* ⏳ **Clepsidra Înghețului (Chrono Frost – 4.5s):** Încetinește toate vehiculele de pe drumuri cu 80% pentru toți jucătorii.
* 📜 **Pergamentul Regal (+5 Glorie):** Bonus instantaneu de +5 puncte.
* 🏆 **Pocalul de Aur (+2 Glorie):** Tezaur colectabil pentru urcare rapidă în clasament.

### 🦸 5. Șase Eroi Medievali & Vizibilitate Ultra-Clară
* **Eroi Selectabili:** *Cavalerul Templier*, *Arhimagul Arcan*, *Bufonul Regal*, *Berserkerul Nordului*, *Doctorul Ciumei* și *Regele Aurit*.
* **Vizibilitate Garantată:** Jucătorul local este evidențiat permanent printr-un **inel de țintă auriu pulsatoriu**, un fascicul vertical de lumină regală, contur întunecat pronunțat și etichetă flotantă deasupra capului. Tovarășii aflați în afara ecranului sunt indicați prin săgeți direcționale (`▲` / `▼`).

---

## 🕹️ Controale

| Acțiune | Tastatură PC | Mobil / Ecran Tactil |
| :--- | :--- | :--- |
| **Înainte** | `W` / `Săgeată Sus` / `Space` | Butonul **▲** (sau Tap pe ecran) |
| **Înapoi** | `S` / `Săgeată Jos` | Butonul **▼** (sau Swipe Jos) |
| **Stânga** | `A` / `Săgeată Stânga` | Butonul **◀** (sau Swipe Stânga) |
| **Dreapta** | `D` / `Săgeată Dreapta` | Butonul **▶** (sau Swipe Dreapta) |
| **Schimbă Jucătorul (Spectator)** | `Tab` | Butonul **Schimbă Cavalerul** |
| **Revanșă Rapidă** | `Enter` / `Space` | Butonul **Bătălie Nouă** |

---

## 🚀 Publicare pe GitHub Pages (În 2 Minute)

1. Creează un repository nou pe GitHub (ex: `super-medieval-crossy-road`).
2. Încarcă fișierele `index.html` și `README.md` în rădăcina proiectului:
   ```bash
   git init
   git add index.html README.md
   git commit -m "feat: release Super Medieval Crossy Road Multiplayer"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo-name>.git
   git push -u origin main
   ```
3. Intră pe GitHub în **Settings** ⚙️ -> **Pages**.
4. La **Build and deployment**, selectează **Deploy from a branch**, apoi alege ramura `main` și folderul `/ (root)` și apasă **Save**.
5. Trimite link-ul `https://<username>.github.io/<repo-name>/` tovarășilor tăi, creează un Lobby și începeți cruciada!

---

## 📄 Licență
Distribuit sub licența **MIT**. Liber pentru utilizare, modificare și distribuire.
