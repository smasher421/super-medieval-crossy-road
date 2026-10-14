# 🍊 Super Mega Orange Crossy Road

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live%20Demo-FF7900?style=for-the-badge&logo=github)](https://<username>.github.io/<repo-name>/)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![HTML5 Canvas](https://img.shields.io/badge/HTML5-Canvas%2060%20FPS-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![WebRTC](https://img.shields.io/badge/Multiplayer-WebRTC%20P2P%20(PeerJS)-333333?style=for-the-badge&logo=webrtc)](https://peerjs.com/)

O reimplementare modernă, multiplayer și fără backend a clasicului joc **Crossy Road**, personalizată într-o identitate vizuală vibrantă **Orange** (`#FF7900`). 

Jocul rulează la 60 FPS exclusiv în browser (HTML5 Canvas + Vanilla JavaScript) și include un **sistem complet de lobby cu cod de cameră**, sincronizare P2P prin **WebRTC**, generare procedurală deterministă a hărții (**zero desync**), power-up-uri dinamice, boți AI și mod spectator.

---

## 🎮 Caracteristici Principale

### 👥 Sistem Multiplayer & Lobby (Zero Backend)
* **Lobby cu Cod de 5 Caractere:** Creează o cameră ca Host și trimite codul prietenilor tăi pentru conectare directă prin WebRTC (PeerJS).
* **Multi-Tab Fallback (`BroadcastChannel`):** Suport nativ pentru testare locală instantanee între mai multe tab-uri pe același calculator.
* **Hărți 100% Sincronizate (Deterministic Seeded PRNG):** Host-ul generează un seed unic la începutul rundei (`Mulberry32`), garantând că toți jucătorii văd exact aceiași copaci, râuri, bușteni și mașini.
* **Poziționare bazată pe Timp:** Vehiculele și buștenii își calculează poziția matematic în funcție de timpul scurs (`elapsedTime`), eliminând orice latență de mișcare.
* **Boți AI Competitivi:** Host-ul poate adăuga sau elimina în timp real boți inteligenți capabili să evite traficul și să colecteze power-up-uri.
* **Mod Spectator Automat:** Dacă ești eliminat, camera comută automat pe liderul rămas în viață. Poți schimba jucătorul urmărit cu tasta `Tab`.
* **Podium & Revanșă:** Clasament complet la finalul fiecărei runde, cu reluare instantă a meciului direct din lobby.

### ⚡ Power-Up-uri Tematice pe Hartă
* 🛡️ **Scutul Orange (6 secunde):** Imunitate totală la impactul cu vehiculele și abilitatea de a păși pe apă pe o platformă energetică.
* ❄️ **Înghețare Trafic (4.5 secunde):** Reduce viteza tuturor mașinilor și camioanelor cu 80%, sincronizat pentru toți jucătorii.
* ⚡ **Turbo 5G (+5 Puncte):** Boost instantaneu în clasamentul rundei.
* 🪙 **Monedă Orange (+2 Puncte):** Puncte suplimentare pentru avans rapid.

### 🎨 6 Skin-uri Tematice
1. 🐔 **Puiul Orange** (Ediția clasică de brand)
2. 🤖 **Agentul 5G** (Costum tech cu antenă)
3. 🦊 **Fiber Fox** (Viteza fibrei optice)
4. 🐓 **Rooster B2B** (Stil corporate elegant)
5. ⚡ **Neon Jumper** (Contrast ultra-modern)
6. 🦆 **Cyber Duck** (Stil futurist)

---

## 🕹️ Controale

| Acțiune | Tastatură PC | Ecran Tactil / Mobil |
| :--- | :--- | :--- |
| **Înainte** | `W` / `Săgeată Sus` / `Space` | Butonul **▲** pe D-Pad |
| **Înapoi** | `S` / `Săgeată Jos` | Butonul **▼** pe D-Pad |
| **Stânga** | `A` / `Săgeată Stânga` | Butonul **◀** pe D-Pad |
| **Dreapta** | `D` / `Săgeată Dreapta` | Butonul **▶** pe D-Pad |
| **Schimbă Spectator** | `Tab` | Butonul dedicat din interfață |
| **Revanșă rapidă** | `Enter` / `Space` | Butonul **Runda Următoare** |

---

## 🚀 Ghid de Lansare pe GitHub Pages (Pas cu Pas)

Proiectul este gândit să funcționeze **complet autonom**, fără pași de compilare (`npm run build`), dependențe de backend sau servere Node.js.

1. **Creează un depozit nou pe GitHub** (ex: `super-mega-orange-crossy-road`).
2. Adaugă fișierul jocului sub numele **`index.html`** în rădăcina depozitului:
   ```bash
   git init
   git add index.html README.md
   git commit -m "feat: initial commit - super mega orange crossy road"
   git branch -M main
   git remote add origin [https://github.com/](https://github.com/)<username>/<repo-name>.git
   git push -u origin main
