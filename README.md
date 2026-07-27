Nella repository sono presenti:
- "interruttore crepuscolare.ipynb"
- "requirements.text"


## Controllo Fuzzy dell'Illuminazione

Questo progetto fornisce uno studio comparativo tra il *Trigger di Schmitt* (controllo ON/OFF binario con isteresi) e *sistemi di controllo logico Fuzzy* (*Mamdani, **TSK Ordine 0* e *TSK Ordine 1*) per la regolazione dinamica di un interruttore crepuscolare, il quale dell'illuminazione artificiale in base alla luce ambientale rilevata da un sensore Vf.

## Obiettivi del Progetto

1. *Fuzzificazione:* Modellare le funzioni di appartenenza dell'ingresso ($V_f$) nelle classi Buio, Penombra e Luce.
2. *Confronto tra Modelli Fuzzy:*
   - *Mamdani:* Basato sull'aggregazione delle aree e defuzzificazione tramite Centroide.
   - *TSK Ordine 0 (Takagi-Sugeno-Kang):* Conseguenze scalari fisse e defuzzificazione tramite media pesata.
   - *TSK Ordine 1:* Conseguenze lineari  per un controllo continuo e reattivo.
3. *Simulazione Dinamica & Consumo Energetico:*
   - Valutazione della risposta dinamica ad onde di luminosità ed evoluzione su un ciclo circadiano di 24 ore.
   - Analisi dell'efficienza energetica rispetto a un benchmark binario.
4. *Analisi delle Prestazioni Computazionali:* Benchmark sui tempi di esecuzione per verificare la fattibilità di deployment su microcontrollori/embedded.

---

## Struttura del Codice

Il file principale esegue sequenzialmente le seguenti fasi:

* *Fuzzificazione & Modelli:* Definizione delle membership function e dei motori d'inferenza Mamdani, TSK-0 e TSK-1.
* *Simulazioni:*
  * Simulazione Dinamica Breve: Risposta ad un segnale sinusoidale del sensore.
  * Simulazione Giornaliera: Modello della luce solare e calcolo del duty cycle del LED.
* *Visualizzazione Grafica:*
  - Funzioni di Appartenenza d'Ingresso.
  - Passaggi interni Mamdani (Implicazione MIN, Aggregazione MAX, Centroide).
  - Curve di Controllo Statico (PWM vs $V_f$) a confronto con il Trigger di Schmitt.
  - Risposta Dinamica e Consumo Energetico Cumulativo.
  - Simulazione Ciclo Solare Giornaliero.
  - Rappresentazione Stem dell'Inferenza TSK.
  - Benchmark Computazionale (Tempo di Esecuzione vs Numero di Iterazioni).

## Requisiti installazione
Consultare il file requirements.text per le necessarie versioni
