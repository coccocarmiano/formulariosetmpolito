# Formulario Sistemi Elettronici, Tecnologie e Misure
  - [Misure](#misure)
    - [Errori](#errori)
    - [Attrezzature](#attrezzature)
  - [Elettronica](#elettronica)
    - [Segnali](#segnali)
    - [Diodi](#diodi)
    - [Transistors](#transistors)
    - [Stadi amplificatori](#stadi-amplificatori)
    - [Amplificatori operazionali](#amplificatori-operazionali)
    - [Limiti amplificatori operazionali](#limiti-amplificatori-operazionali)
    - [Comparatori](#comparatori)
    - [Oscillatori](#oscillatori)

# Misure

## Errori

[Media]: https://latex.codecogs.com/svg.latex?\mu%20=%20\frac{1}{N}\sum_i%20x_i
[Varianza]: https://latex.codecogs.com/svg.latex?\sigma^2%20=%20\frac{1}{N-1}\sum%20(x_i%20-%20\mu)^2
[Incertezza misura]: https://latex.codecogs.com/svg.latex?\pm%20(\%%20lettura%20+%20\%%20fondo\_scala)
[Esempio incertezza]: https://latex.codecogs.com/svg.latex?R%20=%20(4700%20\pm%2047)%20\Omega
[Errore assoluto]: https://latex.codecogs.com/svg.latex?y%20=%20f(x_1,%20x_2,%20...)%20\to%20\delta%20y%20%20=%20\sum_i%20\Bigg%20|\frac{\partial%20f(\vec{x})}{\partial%20x_i}\Bigg%20|_{x=x_{mis}}%20\delta%20x_i
[Errore relativo]: https://latex.codecogs.com/svg.latex?y$%20misura%20$\to%20\epsilon_r%20=%20\frac{\delta%20y}{y}%20\%20\%20(\epsilon_{r,%20\%}%20=%20100\cdot\epsilon_r)
[Somma/Differenza]: https://latex.codecogs.com/svg.latex?y%20=%20a%20\pm%20b%20\to%20\delta%20y%20=%20\delta%20a%20+%20\delta%20b
[Prodotto/Divisione]: https://latex.codecogs.com/svg.latex?y%20=%20a\cdot%20b^{\pm%201}%20\to%20\epsilon_y%20=%20\epsilon_a%20+%20\epsilon_b
[Potenza Radice]: https://latex.codecogs.com/svg.latex?y%20=%20x^{\pm%20n}%20\to%20\epsilon_y%20=%20n^{\pm%201}\epsilon_x

| ---                                       | Formula                                                      |
|:----------------------------------------- |:------------------------------------------------------------ |
| **Incertezza Tipica**                     | ![Incertezza misura]                                         |
| **Strumento di classe x**                 | lo strumento ha una precisione pari ad x% del fondo scala    |
| *L'incertezza va riportata con **al più** due cifre significative.* (e.g.: ![Esempio incertezza]         |
| **Errore Qualunque (Derivate Parziali)**  | ![Errore assoluto]                                           |
| **Errore Relativo**                       | ![Errore Relativo]                                           |
| **Somma/Differenza**                      | ![Somma/Differenza]                                          |
| **Prodotto/Divisione**                    | ![Prodotto/Divisione]                                        |
| **Potenza/Radice**                        | ![Potenza Radice]                                            |

## Attrezzature

<!-- **Full-Scale Range**: ![Full-Scale Range](https://latex.codecogs.com/svg.latex?FSR%20=%20V_{max}%20-%20V_{min}) -->

<!-- **Quantizzazione su N bit**: ![Quantizzazione su N bit](https://latex.codecogs.com/svg.latex?N%20=%20log_2(M)) -->

<!-- **Uscita Ricostruita**: ![Uscita Ricostruita](https://latex.codecogs.com/svg.latex?y%20=%20\sum_{i=0}^{n-1}%202^i\cdot%20B_i%20\%20\%20(B%20=%200%20\lor%20B%20=%201)) -->

<!-- **MSB**: ![MSB](https://latex.codecogs.com/svg.latex?B_{n-1}) -->

<!-- **LSB**: ![LSB](https://latex.codecogs.com/svg.latex?B_0) -->

<!-- **Teorema del Campionamento** (B banda del segnale): ![Teorema del Campionamento](https://latex.codecogs.com/svg.latex?f_c%20\ge%202\cdot%20B) -->

**Errore di Lettura** (Parallasse): valore di una "tacchetta"

**Prodotto Banda Guadagno**: ![Prodotto Banda Guadagno](https://latex.codecogs.com/svg.latex?B\cdot%20t_{salita}%20=%200.35) (varia col modello dell'oscilloscopio)

**Relazione Salita-Visualizzato**: ![Relazione Salita-Visualizzato](https://latex.codecogs.com/svg.latex?t_{s,%20visualizzato}^2%20=%20t_{s,%20segnale}^2%20+%20t_{s,%20circuito}^2%20+%20t_{s,%20oscilloscopio}^2)

Solitamente il ![Tso](https://latex.codecogs.com/svg.latex?t_{s,o}) è trascurabile.

[v_m]: https://latex.codecogs.com/svg.latex?v_m%20=%20\frac{1}{T}%20\int_{t_0}^{t_0+T}%20v(t)dt
[v_rms]: https://latex.codecogs.com/svg.latex?v_{rms}=%20\sqrt{\frac{1}{T}%20\int_{t_0}^{t_0+T}%20v^2(t)dt}

| **Valor-Medio** | **Valore Efficace** |
| --------------- | ------------------- |
| ![v_m]          | ![v_rms]            |

**Duty-Cycle**: ![Duty-Cycle](https://latex.codecogs.com/svg.latex?D%20=%20\frac{t_{alto}}{T})

**Sensibilità**: ![k_v](https://latex.codecogs.com/svg.latex?(k_v)) "altezza", solitamente in *mV*, di un "quadratino".

**Lettura**: ![V_pp](https://latex.codecogs.com/svg.latex?V_{pp}) del segnale, ottenuta come ![Lettura](https://latex.codecogs.com/svg.latex?k_v\cdot%20n_{div}), ![n_div](https://latex.codecogs.com/svg.latex?n_{div}) altezza del segnale in "quadratini"

**Voltmetro a Doppia Rampa**: ![Voltmetro a Doppia Rampa](https://latex.codecogs.com/svg.latex?V_x%20=%20-\frac{T_2}{T_1}V_{rif})
**Incertezza di Quantizzazione**: ![Incertezza di Quantizzazione](https://latex.codecogs.com/svg.latex?\delta%20f_q%20=%20\frac{1}{T_{mis}})

**Frequenzimetro a Misura Diretta**: ![Frequenzimetro a Misura Diretta](https://latex.codecogs.com/svg.latex?f_x%20=%20\frac{1}{t_x}%20=%20\frac{n}{T_c},%20\%20\%20T_x%20=%20nT_c)

**Risoluzione**: ![Risoluzione](https://latex.codecogs.com/svg.latex?\delta%20f_x%20=%20\frac{1}{T_c})
**Risoluzione Relativa**: ![Risoluzione Relativa](https://latex.codecogs.com/svg.latex?\frac{\delta%20f_x}{f_x}%20=%20\frac{1}{n})

**Scelta di ![T_1](https://latex.codecogs.com/svg.latex?T_1)**: ![n(t)](https://latex.codecogs.com/svg.latex?n(t)) ruomore di periodo ![T](https://latex.codecogs.com/svg.latex?T%20\to%20T_1%20=%20T) (spesso *50 Hz*)

**Riscaldamento di un Resistore**: ![Riscaldamento di un Resistore](https://latex.codecogs.com/svg.latex?T_{fin}%20-%20T_{amb}%20=%20R_{termica}\cdot%20P_{dissipata})

**Ponte di Wheatstone**: All'equilibrio, la *ddp* ai due nodi centrali è nulla.

**Potenza**: ![Potenza](https://latex.codecogs.com/svg.latex?P%20=%20\frac{v_{eff}^2}{R}), per segnali sinusoidali ![v_eff](https://latex.codecogs.com/svg.latex?v_{eff}%20=%20\frac{A}{\sqrt{2}})

<!-- **Valor-Medio Segnale Raddrizzato** (Singola/Doppia Semionda): ![Valor-Medio Segnale Raddrizzato](https://latex.codecogs.com/svg.latex?v_m%20=%20\frac{2\cdot%20V_p}{\pi}%20\neq%20v_{rms}) -->

<!-- **Valore Efficace Segnale Raddrizzato**: ![Valore Efficace Segnale Raddrizzato](https://latex.codecogs.com/svg.latex?v_{eff}%20=%20\frac{V_p}{\sqrt{2}}%20=%20k_s\cdot\frac{2\cdot%20V_p}{\pi}) -->

**Costante Strumentale**: ![k_s](https://latex.codecogs.com/svg.latex?k_s%20=%20\left\{%20%20%20%20\begin{array}{ll}%20%20%20%20%20%20%20%201.11%20&%20\text{semionda%20doppia}%20\\%20%20%20%20%20%20%20%202.22%20&%20\text{semionda%20singola}%20%20%20%20\end{array}\right.)

Gli strumenti spesso riportano il valore efficace di un segnale.
Questo valore è pari alla costante strumentale moltiplicata per valor medio del segnale.
**!** Nel calcolo del valor medio con voltmetro a semionda semplice della semionda semplice la parte negativa del segnale viene azzerata.

**Condensatore in ingresso / Voltmetri TRMS**: I voltmetri TRMS restituiscono la lettura reale del valore efficace di un segnale. Tuttavia vengono spesso **accoppiati in AC** (filtro sulla componente DC), riportando così il **valore efficace del segnale originale traslato in basso del suo valor medio**.

**Valori Efficaci noti**: **solo** per ampiezze **simmetriche** (![V_eff noti](https://latex.codecogs.com/svg.latex?-V_p%20\to%20V_p,%20\%20-5V%20\to%205V,%20...)):

| **Onda Quadra** | **Sinusoidi** | **Triangolari** |
| --------------- | ------------- | --------------- |
| ![Onda Quadra](https://latex.codecogs.com/svg.latex?v_{eff}%20=%20V_p) | ![Sinusoidi](https://latex.codecogs.com/svg.latex?v_{eff}%20=%20\frac{V_p}{\sqrt{2}}) | ![Triangolari](https://latex.codecogs.com/svg.latex?v_{eff}%20=%20\frac{V_p}{\sqrt{3}}) |

**Circuito equivalente d'ingresso DSO**: è rappresentato dal parallelo tra un condensatore (decine di *pF*) e una resistenza (solitamente *1 MΩ*).

# Elettronica

## Segnali

**Signal-to-Noise Ratio**: ![SNR](https://latex.codecogs.com/svg.latex?SNR%20=%20\frac{P_{segnale}}{P_{rumore}}%20=%20\frac{v^2}{n^2})

**SNR in dB**: ![SNR_dB](https://latex.codecogs.com/svg.latex?SNR_{dB}%20=%2010log_{10}(SNR)%20=%2020log_{10}%20\left(\frac{v}{n}\right))

**Errore di Quantizzazione**: ![Errore di Quantizzazione](https://latex.codecogs.com/svg.latex?\epsilon_q%20=%20\frac{S}{2^{N+1}}%20=%20\frac{1}{2}LSB), con *S* dinamica del segnale

## Diodi

**Polarizzazione Diretta**: ![Polarizzazione Diretta](https://latex.codecogs.com/svg.latex?v_D%20%3E%200,%20i_D%20\to%20\infty), curva verticale per ![Polarizzazione Diretta (condizioni)](https://latex.codecogs.com/svg.latex?v_D%20%3E%20V_\gamma%20\simeq%200.6-0.7%20\%20V)

**Polarizzazione Inversa**: ![Polarizzazione Inversa](https://latex.codecogs.com/svg.latex?v_D%20%3C%200,%20i_D) satura a valori piccoli e negativi (*pA-fA*)

**Diodo Reale**: ![Diodo Reale](https://latex.codecogs.com/svg.latex?i_D%20=%20I_s(e^{\frac{v_D}{\eta%20V_T}}-%201))

**Diodo Ideale**: ![Diodo Ideale](https://latex.codecogs.com/svg.latex?i_D%20%3E%200%20\to%20v_D%20=%200,%20ON%20\%20\big%20|%20\%20v_D%20%3C%200%20\to%20i_D%20=%200,%20OFF) (nel circuito: generatore)

**Diodo Semi-Ideale**: ![Diodo Semi-Ideale](https://latex.codecogs.com/svg.latex?i_D%20%3E%200%20\to%20v_D%20=%20V_\gamma,%20ON%20\%20\big%20|%20\%20v_D%20%3C%20V_\gamma%20\to%20i_D%20=%200,%20OFF) (nel circuito: corto)

**Resistenza di un Diodo (Piccolo Segnale)**: ![Resistenza di un Diodo](https://latex.codecogs.com/svg.latex?g_D%20=%20\frac{1}{r_D}%20=%20\frac{I_D}{\eta%20V_T})

## Transistors

**Corrente di Gate**: ![Corrente di Gate](https://latex.codecogs.com/svg.latex?i_G%20=%200) in condizioni statiche per *NMOS* e *PMOS*. (*BJT* > 0)

| **nMOS**: ![nMOS](https://latex.codecogs.com/svg.latex?v_{GS},%20\%20v_{DS}) | **pMOS**: ![pMOS](https://latex.codecogs.com/svg.latex?v_{SG},%20\%20v_{SD}) |

***Trucco Mnemonico***:

[v_GS]: https://latex.codecogs.com/svg.latex?v_{GS}
[v_SG]: https://latex.codecogs.com/svg.latex?v_{SG}
[v_DS]: https://latex.codecogs.com/svg.latex?v_{DS}
[v_SD]: https://latex.codecogs.com/svg.latex?v_{SD}
[v_XY]: https://latex.codecogs.com/svg.latex?v_{XY}

* Il **S**ource è sempre dov'è la corrente.
* Il **G**ate sempre la sbarra.
* Il **D**rain il rimanente.

Per capire se usare ![v_GS] o ![v_SG], bisogna posizionare due tensioni verso l'alto, una tra le due "gambe" del transistor (che sarà ![v_DS] o ![v_SD]) e una tra *Gate* e *Source* (che sarà ![v_GS] o ![v_SG]), ricordando che ![v_XY] è una tensione con la punta in *X* e la coda in *Y*.

**Condizioni Saturazione**: ![Condizioni Saturazione](https://latex.codecogs.com/svg.latex?v_{GS/SG}%20%3E%20V_{TH},%20\%20v_{DS/SD}%20%3E%20v_{GS/SG}%20-%20V_{TH})

[OFF]: https://latex.codecogs.com/svg.latex?i_D%20=%200
[ON]: https://latex.codecogs.com/svg.latex?i_D%20=%20\beta%20v_{DS}\left(v_{GS}-V_{TH}-\frac{v_{DS}}{2}\right)
[SAT]: https://latex.codecogs.com/svg.latex?i_D%20=%20\frac{\beta}{2}(v_{GS}-V_{TH})^2(1+\lambda%20v_{DS})

**Corrente di Drain** (xMOS):

| **OFF** | **ON** | **Saturazione** |
|:-------:|:------:|:---------------:|
| ![OFF]  | ![ON]  | ![SAT]          |

**Resistenze**: ![Resistenze](https://latex.codecogs.com/svg.latex?g_m%20=%20\sqrt{2I_D\beta}%20=%20\beta(v_{GS}-v_{TH})\%20\%20\%20g_o%20=%20\lambda%20I_D)

## Stadi Amplificatori

[Tensione ideale]: https://latex.codecogs.com/svg.latex?R_{in}%20\to%20\infty,%20\%20R_{out}%20\to%200
[Corrente ideale]: https://latex.codecogs.com/svg.latex?R_{in}%20\to%200,%20\%20R_{out}%20\to%20\infty
[Transconduttanza]: https://latex.codecogs.com/svg.latex?i_{out}%20=%20g_mv_{gs}
[Transconduttanza ideale]: https://latex.codecogs.com/svg.latex?R_{in}%20\to%20\infty,%20\%20R_{out}%20\to%20\infty
[Transresistenza]: https://latex.codecogs.com/svg.latex?v_{out}%20=%20R_mi_s
[Transresistenza ideale]: https://latex.codecogs.com/svg.latex?R_{in}%20\to%200,%20R_{out}%20\to%200

| **Tensione Ideale** | **Corrente Ideale** | **Transconduttanza** | **Transresistenza** |
| ------------------- | ------------------- | -------------------- | ------------------- |
| ![Tensione Ideale]  | ![Corrente Ideale]  | ![Transconduttanza]  | ![Transresistenza]  |
|   |   | ideale se: ![Transconduttanza ideale] | ideale se: ![Transresistenza ideale] |

**Efficienza Amplificatore Potenza**: ![Efficienza Amplificatore Potenza](https://latex.codecogs.com/svg.latex?\eta%20=%20\frac{P_{out}}{P_{al}+P_{in}}%20\simeq%20\frac{P_{out}}{P_{al}})

[CS]: https://latex.codecogs.com/svg.latex?A_v%20%3C%200,%20\%20R_{in}%20\to%20\infty,%20\%20R_{out}%20\in%20\mathbb{R}
[CD]: https://latex.codecogs.com/svg.latex?A_v%20%3C%201,%20\%20R_{in}%20\to%20\infty,%20\%20R_{out}%20\simeq%20\frac{1}{g_m}
[CG]: https://latex.codecogs.com/svg.latex?A_v%20\simeq%20g_m(R%20||%20r_o),%20\%20R_{in}%20\simeq%20\frac{1}{g_m},%20\%20R_{out}%20=%20R%20||%20r_o

| **Common Source** | **Common Drain** | **Common Gate** |
| ----------------- | ---------------- | --------------- |
| ![CS]             | ![CD]            | ![CG]           |

[R_in]: https://latex.codecogs.com/svg.latex?R_{in}
[R_out]: https://latex.codecogs.com/svg.latex?R_{out}
[R_S]: https://latex.codecogs.com/svg.latex?R_S
[R_L]: https://latex.codecogs.com/svg.latex?R_L
[v_in]: https://latex.codecogs.com/svg.latex?v_{in}
[v_out]: https://latex.codecogs.com/svg.latex?v_{out}
[i_in]: https://latex.codecogs.com/svg.latex?i_{in}
[i_out]: https://latex.codecogs.com/svg.latex?i_{out}

**Effetti di Carico**: Uno stadio si comporta come un amplificatore con generatore pilotato. Trovate ![R_in] e ![R_out], rappresenta il blocco centrale di un circuito di mezzo tra un generatore in ingresso ![v_in] con resistenza ![R_S] e un'uscita ![v_out] con resistenza ![R_L]. Si può ricavare l'uscita ![v_out] in funzione dell'ingresso ![v_in] (e quindi la funzione di trasferimento ![A](https://latex.codecogs.com/svg.latex?A_{v,s})) eseguendo semplici partitori.

Esempio: se lo stadio è un partitore di tensione, allora ![Esempio](https://latex.codecogs.com/svg.latex?v_{out}%20=%20v_{in}\frac{R_{in}}{R_{in}+R_S}A_v\frac{R_L}{R_L+R_{out}})

## Amplificatori Operazionali

**Relazione Fondamentale** (ideale): ![Relazione fondamentale](https://latex.codecogs.com/svg.latex?v_d%20=%200%20\to%20v^+%20=%20v^-,%20\%20\%20\%20i^+%20=%20i^-%20=%200)

**Amplificatore di Tensione**: ![Amplificatore di Tensione](https://latex.codecogs.com/svg.latex?A_v%20=%201+\frac{R_2}{R_1},%20R_{in}%20\to%20\infty,%20R_{out}%20\to%200)

**Amplificatore di Transconduttanza**: ![Amplificatore di Transconduttanza](https://latex.codecogs.com/svg.latex?G_m%20=%20\frac{1}{R}%20\%20$(quella%20in%20retroazione)$,%20R_{in}%20\to%20\infty,%20R_{out}%20\to%20\infty)

**Amplificatore di Transresistenza**: ![Amplificatore di Transresistenza](https://latex.codecogs.com/svg.latex?R_m%20=%20R%20\%20$(quella%20in%20retroazione)$,%20R_{in}%20\to%200,%20R_{out}%20\to%200)

**Amplificatore di Corrente**: ![Amplificatore di Corrente](https://latex.codecogs.com/svg.latex?A_i%20=%201+\frac{R_2}{R_1},%20R_{in}%20\to%200,%20R_{out}%20\to%20\infty)

**Voltage-Follower**: ![Voltage-Follower](https://latex.codecogs.com/svg.latex?v_{out}%20=%20v_{in},%20R_{in}%20\to%20\infty,%20R_{out}%20\to%200)

**Invertente**: ![Invertente](https://latex.codecogs.com/svg.latex?A_v%20=%20-\frac{R_2}{R_1},%20R_{in}%20=%20R_1,%20R_{out}%20\to%200)

[R_1]: https://latex.codecogs.com/svg.latex?R_1
[R_2]: https://latex.codecogs.com/svg.latex?R_2

* **Esponenziale**: Diodo su ![R_1]
* **Logaritmico**: Diodo su ![R_2]
* **Integratore**: Condensatore su ![R_2]
* **Derivatore**: Condensatore su ![R_1]

*(Per tutti e 4: ![Condizioni](https://latex.codecogs.com/svg.latex?R_{out}%20=%200))*

**Sommatore Generalizzato**: ![Sommatore Generalizzato](https://latex.codecogs.com/svg.latex?v_{out}%20=%20\frac{\sum_{i=0}^M%20G_{i^-}%20+%20G_f}{\sum_{i=0}^N%20G_{i^+}}%20\sum_{i=1}^N%20\frac{G_{i^+}}{G_f}v_{i^+}-\sum_{i=1}^M\frac{G_{i^-}}{G_f}v_{i^-})

*(Non usare questa formula, meglio **sovrapposizione** e/o **Millman**)*

**Common-Mode Rejection Ratio** (**CMRR**): ![CMRR](https://latex.codecogs.com/svg.latex?\bigg%20|\frac{A_d}{A_{cm}}%20\bigg%20|,%20\%20v_{cm}%20=%20\frac{v^++v^-}{2},%20\%20v_d%20=%20v^+-v^-)

## Limiti Amplificatori Operazionali

**Circuito Eq. in Linearità**: ![Circuito Eq. in Linearità](https://latex.codecogs.com/svg.latex?v_{out}%20=%20A_dv_d%20+A_{cm}v_{cm}+A_{ps}v_{ps})

**Amplificazione Differenziale Finita**: ![Amplificazione Differenziale Finita](https://latex.codecogs.com/svg.latex?A_v%20=%20\frac{\beta%20A_d}{1+\beta%20A_d}\frac{1}{\beta}%20=%20\frac{1}{\beta}$%20se%20$A_d%20\to%20\infty)

**Prodotto Banda-Guadagno**: ![Prodotto Banda-Guadagno](https://latex.codecogs.com/svg.latex?B%20=%20\beta%20f_T)
**Parametro Beta**: ![Beta](https://latex.codecogs.com/svg.latex?\beta%20=%20-\frac{v_d}{\hat{e}}%20=%20-\frac{v_d}{A_dv_d%20+%20A_{cm}v_{cm}%20+%20...})

**Casi Particolari**: Ad esempio operazionale ideale con parametri canonici (![Parametri](https://latex.codecogs.com/svg.latex?A_{cm}%20\simeq%200,\%20R_{in}%20\to%20\infty,%20...)) allora ![Beta](https://latex.codecogs.com/svg.latex?\beta%20=%201%20+%20\frac{R_2}{R_1}), per invertenti e non-invertenti.

(Esempio: se invertente con ![A_d](https://latex.codecogs.com/svg.latex?A_d%20=%20-9), allora ![Rapporto](https://latex.codecogs.com/svg.latex?\frac{R_2}{R_1}%20=%209) da cui ![Beta](https://latex.codecogs.com/svg.latex?\beta%20=%201%20+%20\frac{R_2}{R_1}%20=%2010))

**Slew-Rate**: ![Slew-Rate](https://latex.codecogs.com/svg.latex?\bigg%20|\frac{dv}{dt}\bigg%20|_{max}%20\leq%20\bigg%20|SR\bigg%20|). Ipotizziamo sinusoide in ingresso amplificata all'uscita.

![dv/dt](https://latex.codecogs.com/svg.latex?\bigg%20|\frac{\partial}{\partial{t}}%20V_{in}A_vsin(\omega%20t)\bigg%20|_{max}\leq%20\bigg%20|SR\bigg%20|). Quindi: ![Risultato](https://latex.codecogs.com/svg.latex?\bigg%20|\omega%20A_vV_{in}\bigg%20|%20=%20\bigg%20|2\pi%20fA_vV_{in}\bigg%20|%20\leq%20\bigg%20|%20SR%20\bigg%20|)

**Offset di Tensione**: ![V_OFF](https://latex.codecogs.com/svg.latex?V_{OFF}) collegata al morsetto *+*

**Correnti di Polarizzazione**: Corrente ![Corrente](https://latex.codecogs.com/svg.latex?I^+/I^-%20=%20I_{BIAS}+\frac{I_{OFF}}{2}) ai due morsetti, uscente ![Corrente uscente](https://latex.codecogs.com/svg.latex?I_{BIAS}%20=%20\frac{I^++I^-}{2},%20\%20I_{OFF}%20=%20I^++I^-)

## Comparatori

***Ottenuti con retroazione positiva.***

**Soglie**:

[V_S1 inv.]: https://latex.codecogs.com/svg.latex?V_{S1}%20=%20V_S\frac{R_2}{R_2+R_1}+V_{OH}\frac{R_1}{R_1+R_2}
[V_S2 inv.]: https://latex.codecogs.com/svg.latex?V_{S2}%20=%20V_{S1}$%20ma%20con%20$OL,%20V_S$%20sul%20$%27+%27
[V_S1 non inv.]: https://latex.codecogs.com/svg.latex?V_{S1}%20=%20V_S%20\left(1+\frac{R1}{R2}\right)%20-%20V_{OL}\frac{R1}{R2}
[V_S2 non inv.]: https://latex.codecogs.com/svg.latex?V_{S2}%20=%20V_{S1}$%20ma%20con%20$OH,%20V_S$%20sul%20$%27-%27

| **Invertente**  | **Non Invertente**  |
| --------------- | ------------------- |
| ![V_S1 inv.]    | ![V_S1 non inv.]    |
| ![V_S2 inv.]    | ![V_S2 non inv.]    |

**Comparatori Reali**: ![Comparatori Reali](https://latex.codecogs.com/svg.latex?V_{S1/2,%20reale}%20=%20V_{S1/2,%20ideale}-V_{OFF})

## Oscillatori

*da fare*
