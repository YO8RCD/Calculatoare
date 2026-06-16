# Calculator Antenă EFHW (160m - 80m - 40m)

Acest proiect pune la dispoziție un calculator utilitar dedicat radioamatorilor pentru dimensionarea antenelor **EFHW (End-Fed Half-Wave)** multibandă pentru benzile de 160, 80 și 40 de metri. 

Sunt incluse două versiuni ale algoritmului:
1. **Versiunea Web (HTML/JS/CSS):** Gata de integrat în bloguri sau site-uri (dezvoltată inițial pentru blogul [YO8RCD]([URL-ul complet al site-ului](https://yo8rcd.blogspot.com/2026/06/calculator-efhw.html)).
2. **Versiunea Terminal (Python):** Pentru teste și rulare rapidă direct pe calculator.

---

## 🛠️ Caracteristici și Variabile de Calcul

Spre deosebire de calculatoarele matematice simple, acest algoritm aplică factori de corecție empirici pe baza mediului de instalare:
* **Frecvența centrală:** Introducere exactă în kHz pentru acord fin pe segmentul dorit (CW/Data/SSB).
* **Izolația firului:** Corectează factorul de viteză ($V_f$) dacă se folosește fir izolat în PVC (MYF/FY), care scurtează antena cu ~3%.
* **Înălțimea față de sol:** Calculează capacitatea parazită față de pământ la înălțimi mai mici de $0.25\,\lambda$ și ajustează lungimea radiantului.
* **Grosimea firului:** Ia în calcul efectul de formă pentru fire mai groase de $2.5\text{ mm}^2$.

### Rezultate generate:
* Lungimea fizică a radiantului ($\lambda/2$).
* Lungimea optimă a contragreutății dedicate ($\sim0.05\,\lambda$).
* Impedanța estimată la capăt și cea reflectată prin transformatorul UNUN (49:1 sau 64:1).
* SWR-ul teoretic aproximat.

---

## 🚀 Cum se utilizează

### 1. Versiunea Python (în terminal)
Asigură-te că ai Python instalat în sistem, descarcă fișierul scriptului și rulează-l din terminal:

```bash
python calculator_efhw.py
