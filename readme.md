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

[Media]: https://latex.codecogs.com/svg.latex?%5Cmu%20%3D%20%5Cfrac%7B1%7D%7BN%7D%5Csum_i%20x_i
[Varianza]: https://latex.codecogs.com/svg.latex?%5Csigma%5E2%20%3D%20%5Cfrac%7B1%7D%7BN-1%7D%5Csum%20(x_i%20-%20%5Cmu)%5E2
[Incertezza misura]: https://latex.codecogs.com/svg.latex?%5Cpm%20(%5C%%20lettura%20+%20%5C%%20fondo%5C_scala)
[Esempio incertezza]: https://latex.codecogs.com/svg.latex?R%20%3D%20(4700%20%5Cpm%2047)%20%5COmega
[Errore assoluto]: https://latex.codecogs.com/svg.latex?y%20%3D%20f(x_1,%20x_2,%20...)%20%5Cto%20%5Cdelta%20y%20%20%3D%20%5Csum_i%20%5CBigg%20|%5Cfrac%7B%5Cpartial%20f(%5Cvec%7Bx%7D)%7D%7B%5Cpartial%20x_i%7D%5CBigg%20|_%7Bx%3Dx_%7Bmis%7D%7D%20%5Cdelta%20x_i
[Errore relativo]: https://latex.codecogs.com/svg.latex?y$%20misura%20$%5Cto%20%5Cepsilon_r%20%3D%20%5Cfrac%7B%5Cdelta%20y%7D%7By%7D%20%5C%20%5C%20(%5Cepsilon_%7Br,%20%5C%%7D%20%3D%20100%5Ccdot%5Cepsilon_r)
[Somma o Differenza]: https://latex.codecogs.com/svg.latex?y%20%3D%20a%20%5Cpm%20b%20%5Cto%20%5Cdelta%20y%20%3D%20%5Cdelta%20a%20+%20%5Cdelta%20b
[Prodotto o Divisione]: https://latex.codecogs.com/svg.latex?y%20%3D%20a%5Ccdot%20b%5E%7B%5Cpm%201%7D%20%5Cto%20%5Cepsilon_y%20%3D%20%5Cepsilon_a%20+%20%5Cepsilon_b
[Potenza o Radice]: https://latex.codecogs.com/svg.latex?y%20%3D%20x%5E%7B%5Cpm%20n%7D%20%5Cto%20%5Cepsilon_y%20%3D%20n%5E%7B%5Cpm%201%7D%5Cepsilon_x

| -                                                                   | Formula                                                      |
|:------------------------------------------------------------------- |:------------------------------------------------------------ |
| **Incertezza Tipica**                                               | ![Incertezza misura]                                         |
| **Strumento di classe x**                                           | lo strumento ha una precisione pari ad x% del fondo scala    |
| *L'incertezza va riportata con **al più** due cifre significative.* | (e.g.: ![Esempio incertezza]                                 |
| **Errore Qualunque (Derivate Parziali)**                            | ![Errore assoluto]                                           |
| **Errore Relativo**                                                 | ![Errore Relativo]                                           |
| **Somma** o **Differenza**                                          | ![Somma o Differenza]                                        |
| **Prodotto** o **Divisione**                                        | ![Prodotto o Divisione]                                      |
| **Potenza** o **Radice**                                            | ![Potenza o Radice]                                          |

## Attrezzature

[Full-Scale Range]: https://latex.codecogs.com/svg.latex?FSR%20%3D%20V_%7Bmax%7D%20-%20V_%7Bmin%7D
[Quantizzazione su N bit]: https://latex.codecogs.com/svg.latex?N%20%3D%20log_2(M)
[Uscita Ricostruita]: https://latex.codecogs.com/svg.latex?y%20%3D%20%5Csum_%7Bi%3D0%7D%5E%7Bn-1%7D%202%5Ei%5Ccdot%20B_i%20%5C%20%5C%20(B%20%3D%200%20%5Clor%20B%20%3D%201)
[MSB]: https://latex.codecogs.com/svg.latex?B_%7Bn-1%7D
[LSB]: https://latex.codecogs.com/svg.latex?B_0
[Teorema del Campionamento (B banda del segnale)]: https://latex.codecogs.com/svg.latex?f_c%20%5Cge%202%5Ccdot%20B
[Prodotto Banda Guadagno]: https://latex.codecogs.com/svg.latex?B%5Ccdot%20t_%7Bsalita%7D%20%3D%200.35
[Relazione Salita-Visualizzato]: https://latex.codecogs.com/svg.latex?t_%7Bs,%20visualizzato%7D%5E2%20%3D%20t_%7Bs,%20segnale%7D%5E2%20+%20t_%7Bs,%20circuito%7D%5E2%20+%20t_%7Bs,%20oscilloscopio%7D%5E2
[t_so]: https://latex.codecogs.com/svg.latex?t_%7Bs,o%7D

| -                                                                   | Formula                                                      |
|:------------------------------------------------------------------- |:------------------------------------------------------------ |
| **Errore di Lettura** (Parallasse)                                  | Valore di una "tacchetta"                                    |
| **Prodotto Banda Guadagno** (varia col modello dell'oscilloscopio)  | ![Prodotto Banda Guadagno]                                   |
| **Relazione Salita-Visualizzato**                                   | ![Relazione Salita-Visualizzato]                             |
| *Solitamente il ![t_so] è trascurabile.*                                                                                           |

[v_m]: https://latex.codecogs.com/svg.latex?v_m%20%3D%20%5Cfrac%7B1%7D%7BT%7D%20%5Cint_%7Bt_0%7D%5E%7Bt_0+T%7D%20v(t)dt
[v_rms]: https://latex.codecogs.com/svg.latex?v_%7Brms%7D%3D%20%5Csqrt%7B%5Cfrac%7B1%7D%7BT%7D%20%5Cint_%7Bt_0%7D%5E%7Bt_0+T%7D%20v%5E2(t)dt%7D

| **Valor-Medio** | **Valore Efficace** |
| --------------- | ------------------- |
| ![v_m]          | ![v_rms]            |

[Duty-Cycle]: https://latex.codecogs.com/svg.latex?D%20%3D%20%5Cfrac%7Bt_%7Balto%7D%7D%7BT%7D
[Lettura]: https://latex.codecogs.com/svg.latex?V_pp%20%3D%20k_v%5Ccdot%20n_%7Bdiv%7D
[k_v]: https://latex.codecogs.com/svg.latex?k_v
[Voltmetro a Doppia Rampa]: https://latex.codecogs.com/svg.latex?V_x%20%3D%20-%5Cfrac%7BT_2%7D%7BT_1%7DV_%7Brif%7D
[Incertezza di Quantizzazione]: https://latex.codecogs.com/svg.latex?%5Cdelta%20f_q%20%3D%20%5Cfrac%7B1%7D%7BT_%7Bmis%7D%7D
[Frequenzimetro a Misura Diretta]: https://latex.codecogs.com/svg.latex?f_x%20%3D%20%5Cfrac%7B1%7D%7Bt_x%7D%20%3D%20%5Cfrac%7Bn%7D%7BT_c%7D,%20%5C%20%5C%20T_x%20%3D%20nT_c
[Risoluzione]: https://latex.codecogs.com/svg.latex?%5Cdelta%20f_x%20%3D%20%5Cfrac%7B1%7D%7BT_c%7D
[Risoluzione Relativa]: https://latex.codecogs.com/svg.latex?%5Cfrac%7B%5Cdelta%20f_x%7D%7Bf_x%7D%20%3D%20%5Cfrac%7B1%7D%7Bn%7D
[T_1]: https://latex.codecogs.com/svg.latex?T_1
[Valore T_1]: https://latex.codecogs.com/svg.latex?T%20%5Cto%20T_1%20%3D%20T
[Riscaldamento di un Resistore]: https://latex.codecogs.com/svg.latex?T_%7Bfin%7D%20-%20T_%7Bamb%7D%20%3D%20R_%7Btermica%7D%5Ccdot%20P_%7Bdissipata%7D
[Potenza]: https://latex.codecogs.com/svg.latex?P%20%3D%20%5Cfrac%7Bv_%7Beff%7D%5E2%7D%7BR%7D
[v_eff]: https://latex.codecogs.com/svg.latex?v_%7Beff%7D%20%3D%20%5Cfrac%7BA%7D%7B%5Csqrt%7B2%7D%7D
[Valor-Medio Segnale Raddrizzato (Singola/Doppia Semionda)]: https://latex.codecogs.com/svg.latex?v_m%20%3D%20%5Cfrac%7B2%5Ccdot%20V_p%7D%7B%5Cpi%7D%20%5Cneq%20v_%7Brms%7D
[Valore Efficace Segnale Raddrizzato]: https://latex.codecogs.com/svg.latex?v_%7Beff%7D%20%3D%20%5Cfrac%7BV_p%7D%7B%5Csqrt%7B2%7D%7D%20%3D%20k_s%5Ccdot%5Cfrac%7B2%5Ccdot%20V_p%7D%7B%5Cpi%7D
[k_s]: https://latex.codecogs.com/svg.latex?k_s%20%3D%20%5Cleft%5C%7B%20%20%20%20%5Cbegin%7Barray%7D%7Bll%7D%20%20%20%20%20%20%20%201.11%20&%20%5Ctext%7Bsemionda%20doppia%7D%20%5C%5C%20%20%20%20%20%20%20%202.22%20&%20%5Ctext%7Bsemionda%20singola%7D%20%20%20%20%5Cend%7Barray%7D%5Cright.

| -                                                                   | Formula                                                      |
|:------------------------------------------------------------------- |:------------------------------------------------------------ |
| **Duty-Cycle**                                                      | ![Duty-Cycle]                                                |
| **Sensibilità** (![k_v])                                            | *altezza*, solitamente in *mV*, di un "quadratino".          |
| **Lettura**                                                         | ![Lettura]                                                   |
| **Voltmetro a Doppia Rampa**                                        | ![Voltmetro a Doppia Rampa]                                  |
| **Incertezza di Quantizzazione**                                    | ![Incertezza di Quantizzazione]                              |
| **Frequenzimetro a Misura Diretta**                                 | ![Frequenzimetro a Misura Diretta]                           |
| **Risoluzione**                                                     | ![Risoluzione]                                               |
| **Risoluzione Relativa**                                            | ![Risoluzione Relativa]                                      |
| **Scelta di ![T_1]**                                                | *n(t)* ruomore di periodo. ![Valore T_1] (spesso *50 Hz*)    |
| **Riscaldamento di un Resistore**                                   | ![Riscaldamento di un Resistore]                             |
| **Ponte di Wheatstone**                                             | All'equilibrio, la *ddp* ai due nodi centrali è nulla.       |
| **Potenza**                                                         | ![Potenza], per segnali sinusoidali ![v_eff]                 |
| **Costante Strumentale**                                            | ![k_s]                                                       |

Gli strumenti spesso riportano il valore efficace di un segnale.
Questo valore è pari alla costante strumentale moltiplicata per valor medio del segnale.

**!** Nel calcolo del valor medio con voltmetro a semionda semplice della semionda semplice la parte negativa del segnale viene azzerata.

**Condensatore in ingresso / Voltmetri TRMS**: I voltmetri TRMS restituiscono la lettura reale del valore efficace di un segnale. Tuttavia vengono spesso **accoppiati in AC** (filtro sulla componente DC), riportando così il **valore efficace del segnale originale traslato in basso del suo valor medio**.

**Valori Efficaci noti**: **solo** per ampiezze **simmetriche** (![V_eff noti](https://latex.codecogs.com/svg.latex?-V_p%20%5Cto%20V_p,%20%5C%20-5V%20%5Cto%205V,%20...)):

[Onda Quadra]: https://latex.codecogs.com/svg.latex?v_%7Beff%7D%20%3D%20V_p
[Sinusoidi]: https://latex.codecogs.com/svg.latex?v_%7Beff%7D%20%3D%20%5Cfrac%7BV_p%7D%7B%5Csqrt%7B2%7D%7D
[Triangolari]: https://latex.codecogs.com/svg.latex?v_%7Beff%7D%20%3D%20%5Cfrac%7BV_p%7D%7B%5Csqrt%7B3%7D%7D

| **Onda Quadra** | **Sinusoidi** | **Triangolari** |
| --------------- | ------------- | --------------- |
| ![Onda Quadra]  | ![Sinusoidi]  | ![Triangolari]  |

**Circuito equivalente d'ingresso DSO**: è rappresentato dal parallelo tra un condensatore (decine di *pF*) e una resistenza (solitamente *1 MΩ*).

# Elettronica

## Segnali

[SNR]: https://latex.codecogs.com/svg.latex?SNR%20%3D%20%5Cfrac%7BP_%7Bsegnale%7D%7D%7BP_%7Brumore%7D%7D%20%3D%20%5Cfrac%7Bv%5E2%7D%7Bn%5E2%7D
[SNR_dB]: https://latex.codecogs.com/svg.latex?SNR_%7BdB%7D%20%3D%2010log_%7B10%7D(SNR)%20%3D%2020log_%7B10%7D%20%5Cleft(%5Cfrac%7Bv%7D%7Bn%7D%5Cright)
[Eq]: https://latex.codecogs.com/svg.latex?%5Cepsilon_q%20%3D%20%5Cfrac%7BS%7D%7B2%5E%7BN+1%7D%7D%20%3D%20%5Cfrac%7B1%7D%7B2%7DLSB

| -                                                                   | Formula                                                      |
|:------------------------------------------------------------------- |:------------------------------------------------------------ |
| **Signal-to-Noise Ratio**                                           | ![SNR]                                                       |
| **SNR in dB**                                                       | ![SNR_dB]                                                    |
| **Errore di Quantizzazione**                                        | ![Eq], con *S* dinamica del segnale                          |

## Diodi

[v_D]: https://latex.codecogs.com/svg.latex?v_D
[i_D]: https://latex.codecogs.com/svg.latex?i_D
[Diodo Reale]: https://latex.codecogs.com/svg.latex?i_D%20%3D%20I_s(e%5E%7B%5Cfrac%7Bv_D%7D%7B%5Ceta%20V_T%7D%7D-%201)
[Diodo Ideale]: https://latex.codecogs.com/svg.latex?%5Cbegin%7Barray%7D%7Bll%7Di_D%20%3E%200%20%5Cto%20v_D%20%3D%200%20&%20ON%20%5C%5Cv_D%20%3C%200%20%5Cto%20i_D%20%3D%200%20&%20OFF%5Cend%7Barray%7D
[Diodo Semi-Ideale]: https://latex.codecogs.com/svg.latex?%5Cbegin%7Barray%7D%7Bll%7Di_D%20%3E%200%20%5Cto%20v_D%20%3D%20V_%5Cgamma%20&%20ON%20%5C%5Cv_D%20%3C%20V_%5Cgamma%20%5Cto%20i_D%20%3D%200%20&%20OFF%5Cend%7Barray%7D

| Diodo                  | Valori                                      |
| ---------------------- | ------------------------------------------- |
| **Diodo Reale**        | ![Diodo Reale]                              |
| **Diodo Ideale**       | ![Diodo Ideale] (nel circuito: generatore)  |
| **Diodo Semi-Ideale**  | ![Diodo Semi-Ideale] (nel circuito: corto)  |

[PD]: https://latex.codecogs.com/svg.latex?v_D%20%3E%200,%20i_D%20%5Cto%20%5Cinfty
[Curva verticale]: https://latex.codecogs.com/svg.latex?v_D%20%3E%20V_%5Cgamma%20%5Csimeq%200.6-0.7%20%5C%20V
[PI]: https://latex.codecogs.com/svg.latex?v_D%20%3C%200
[Resistenza di un Diodo]: https://latex.codecogs.com/svg.latex?g_D%20%3D%20%5Cfrac%7B1%7D%7Br_D%7D%20%3D%20%5Cfrac%7BI_D%7D%7B%5Ceta%20V_T%7D

| -                                                                   | Formula                                                      |
|:------------------------------------------------------------------- |:------------------------------------------------------------ |
| **Polarizzazione Diretta**                                          | ![PD], curva verticale per ![Curva verticale]                |
| **Polarizzazione Inversa**                                          | ![PI], ![i_D] satura a valori piccoli e negativi (*pA-fA*)   |
| **Resistenza di un Diodo (Piccolo Segnale)**                        | ![Resistenza di un Diodo]                                    |

## Transistors

[Corrente di Gate]: https://latex.codecogs.com/svg.latex?i_G%20%3D%200

**Corrente di Gate**: ![Corrente di Gate] in condizioni statiche per *NMOS* e *PMOS*. (*BJT* > 0)

[v_GS]: https://latex.codecogs.com/svg.latex?v_%7BGS%7D
[v_SG]: https://latex.codecogs.com/svg.latex?v_%7BSG%7D
[v_DS]: https://latex.codecogs.com/svg.latex?v_%7BDS%7D
[v_SD]: https://latex.codecogs.com/svg.latex?v_%7BSD%7D
[v_XY]: https://latex.codecogs.com/svg.latex?v_%7BXY%7D

**nMOS**: ![v_GS], ![v_DS]; **pMOS**: ![v_SG], ![v_SD]

***Trucco Mnemonico***:

* Il **S**ource è sempre dov'è la corrente.
* Il **G**ate sempre la sbarra.
* Il **D**rain il rimanente.

Per capire se usare ![v_GS] o ![v_SG], bisogna posizionare due tensioni verso l'alto, una tra le due "gambe" del transistor (che sarà ![v_DS] o ![v_SD]) e una tra *Gate* e *Source* (che sarà ![v_GS] o ![v_SG]), ricordando che ![v_XY] è una tensione con la punta in *X* e la coda in *Y*.

[Condizioni Saturazione]: https://latex.codecogs.com/svg.latex?v_%7BGS/SG%7D%20%3E%20V_%7BTH%7D,%20%5C%20v_%7BDS/SD%7D%20%3E%20v_%7BGS/SG%7D%20-%20V_%7BTH%7D

**Condizioni Saturazione**: ![Condizioni Saturazione]

[OFF]: https://latex.codecogs.com/svg.latex?i_D%20%3D%200
[ON]: https://latex.codecogs.com/svg.latex?i_D%20%3D%20%5Cbeta%20v_%7BDS%7D%5Cleft(v_%7BGS%7D-V_%7BTH%7D-%5Cfrac%7Bv_%7BDS%7D%7D%7B2%7D%5Cright)
[SAT]: https://latex.codecogs.com/svg.latex?i_D%20%3D%20%5Cfrac%7B%5Cbeta%7D%7B2%7D(v_%7BGS%7D-V_%7BTH%7D)%5E2(1+%5Clambda%20v_%7BDS%7D)

**Corrente di Drain** (xMOS):

| **OFF** | **ON** | **Saturazione** |
|:-------:|:------:|:---------------:|
| ![OFF]  | ![ON]  | ![SAT]          |

[Resistenze]: https://latex.codecogs.com/svg.latex?g_m%20%3D%20%5Csqrt%7B2I_D%5Cbeta%7D%20%3D%20%5Cbeta(v_%7BGS%7D-v_%7BTH%7D)%5C%5C%20%5C%5C%20%5C%5C%20g_o%20%3D%20%5Clambda%20I_D

**Resistenze**: ![Resistenze]

## Stadi Amplificatori

[Tensione ideale]: https://latex.codecogs.com/svg.latex?R_%7Bin%7D%20%5Cto%20%5Cinfty,%20%5C%20R_%7Bout%7D%20%5Cto%200
[Corrente ideale]: https://latex.codecogs.com/svg.latex?R_%7Bin%7D%20%5Cto%200,%20%5C%20R_%7Bout%7D%20%5Cto%20%5Cinfty
[Transconduttanza]: https://latex.codecogs.com/svg.latex?i_%7Bout%7D%20%3D%20g_mv_%7Bgs%7D
[Transconduttanza ideale]: https://latex.codecogs.com/svg.latex?R_%7Bin%7D%20%5Cto%20%5Cinfty,%20%5C%20R_%7Bout%7D%20%5Cto%20%5Cinfty
[Transresistenza]: https://latex.codecogs.com/svg.latex?v_%7Bout%7D%20%3D%20R_mi_s
[Transresistenza ideale]: https://latex.codecogs.com/svg.latex?R_%7Bin%7D%20%5Cto%200,%20R_%7Bout%7D%20%5Cto%200

| **Tensione Ideale** | **Corrente Ideale** | **Transconduttanza**                  | **Transresistenza**                  |
| ------------------- | ------------------- | ------------------------------------- | ------------------------------------ |
| ![Tensione Ideale]  | ![Corrente Ideale]  | ![Transconduttanza]                   | ![Transresistenza]                   |
|                     |                     | ideale se: ![Transconduttanza ideale] | ideale se: ![Transresistenza ideale] |

[Efficienza Amplificatore Potenza]: https://latex.codecogs.com/svg.latex?%5Ceta%20%3D%20%5Cfrac%7BP_%7Bout%7D%7D%7BP_%7Bal%7D+P_%7Bin%7D%7D%20%5Csimeq%20%5Cfrac%7BP_%7Bout%7D%7D%7BP_%7Bal%7D%7D

**Efficienza Amplificatore Potenza**: ![Efficienza Amplificatore Potenza]

[CS]: https://latex.codecogs.com/svg.latex?A_v%20%3C%200,%20%5C%20R_%7Bin%7D%20%5Cto%20%5Cinfty,%20%5C%20R_%7Bout%7D%20%5Cin%20%5Cmathbb%7BR%7D
[CD]: https://latex.codecogs.com/svg.latex?A_v%20%3C%201,%20%5C%20R_%7Bin%7D%20%5Cto%20%5Cinfty,%20%5C%20R_%7Bout%7D%20%5Csimeq%20%5Cfrac%7B1%7D%7Bg_m%7D
[CG]: https://latex.codecogs.com/svg.latex?A_v%20%5Csimeq%20g_m%20(R%20%5Cparallel%20r_o),%20R_%7Bin%7D%20%5Csimeq%20%5Cfrac%7B1%7D%7Bg_m%7D,%20R_%7Bout%7D%20%3D%20R%20%5Cparallel%20r_o

| **Common Source** | **Common Drain** | **Common Gate** |
| ----------------- | ---------------- | --------------- |
| ![CS]             | ![CD]            | ![CG]           |

[R_in]: https://latex.codecogs.com/svg.latex?R_%7Bin%7D
[R_out]: https://latex.codecogs.com/svg.latex?R_%7Bout%7D
[R_S]: https://latex.codecogs.com/svg.latex?R_S
[R_L]: https://latex.codecogs.com/svg.latex?R_L
[v_in]: https://latex.codecogs.com/svg.latex?v_%7Bin%7D
[v_out]: https://latex.codecogs.com/svg.latex?v_%7Bout%7D
[i_in]: https://latex.codecogs.com/svg.latex?i_%7Bin%7D
[i_out]: https://latex.codecogs.com/svg.latex?i_%7Bout%7D

**Effetti di Carico**: Uno stadio si comporta come un amplificatore con generatore pilotato. Trovate ![R_in] e ![R_out], rappresenta il blocco centrale di un circuito di mezzo tra un generatore in ingresso ![v_in] con resistenza ![R_S] e un'uscita ![v_out] con resistenza ![R_L]. Si può ricavare l'uscita ![v_out] in funzione dell'ingresso ![v_in] (e quindi la funzione di trasferimento ![A](https://latex.codecogs.com/svg.latex?A_%7Bv,s%7D)) eseguendo semplici partitori.

Esempio: se lo stadio è un partitore di tensione, allora ![Esempio](https://latex.codecogs.com/svg.latex?v_%7Bout%7D%20%3D%20v_%7Bin%7D%5Cfrac%7BR_%7Bin%7D%7D%7BR_%7Bin%7D+R_S%7DA_v%5Cfrac%7BR_L%7D%7BR_L+R_%7Bout%7D%7D)

## Amplificatori Operazionali

[Relazione Fondamentale]: https://latex.codecogs.com/svg.latex?v_d%20%3D%200%20%5Cto%20v%5E+%20%3D%20v%5E-,%20%5C%20%5C%20%5C%20i%5E+%20%3D%20i%5E-%20%3D%200
[Amplificatore di Tensione]: https://latex.codecogs.com/svg.latex?A_v%20%3D%201+%5Cfrac%7BR_2%7D%7BR_1%7D,%20R_%7Bin%7D%20%5Cto%20%5Cinfty,%20R_%7Bout%7D%20%5Cto%200
[Amplificatore di Transconduttanza]: https://latex.codecogs.com/svg.latex?G_m%20%3D%20%5Cfrac%7B1%7D%7BR%7D%20%5C%20$(quella%20in%20retroazione)$,%20R_%7Bin%7D%20%5Cto%20%5Cinfty,%20R_%7Bout%7D%20%5Cto%20%5Cinfty
[Amplificatore di Transresistenza]: https://latex.codecogs.com/svg.latex?R_m%20%3D%20R%20%5C%20$(quella%20in%20retroazione)$,%20R_%7Bin%7D%20%5Cto%200,%20R_%7Bout%7D%20%5Cto%200
[Amplificatore di Corrente]: https://latex.codecogs.com/svg.latex?A_i%20%3D%201+%5Cfrac%7BR_2%7D%7BR_1%7D,%20R_%7Bin%7D%20%5Cto%200,%20R_%7Bout%7D%20%5Cto%20%5Cinfty
[Voltage-Follower]: https://latex.codecogs.com/svg.latex?v_%7Bout%7D%20%3D%20v_%7Bin%7D,%20R_%7Bin%7D%20%5Cto%20%5Cinfty,%20R_%7Bout%7D%20%5Cto%200
[Invertente]: https://latex.codecogs.com/svg.latex?A_v%20%3D%20-%5Cfrac%7BR_2%7D%7BR_1%7D,%20R_%7Bin%7D%20%3D%20R_1,%20R_%7Bout%7D%20%5Cto%200

**Relazione Fondamentale** (ideale): ![Relazione fondamentale]

| Amplificatore                          | Valori                                |
|:---------------------------------------|:------------------------------------- |
| **Amplificatore di Tensione**          | ![Amplificatore di Tensione]          |
| **Amplificatore di Transconduttanza**  | ![Amplificatore di Transconduttanza]  |
| **Amplificatore di Transresistenza**   | ![Amplificatore di Transresistenza]   |
| **Amplificatore di Corrente**          | ![Amplificatore di Corrente]          |
| **Voltage-Follower**                   | ![Voltage-Follower]                   |
| **Invertente**                         | ![Invertente]                         |

[R_1]: https://latex.codecogs.com/svg.latex?R_1
[R_2]: https://latex.codecogs.com/svg.latex?R_2

Con ![Condizioni](https://latex.codecogs.com/svg.latex?R_%7Bout%7D%20%3D%200):

* **Esponenziale**: Diodo su ![R_1]
* **Logaritmico**: Diodo su ![R_2]
* **Integratore**: Condensatore su ![R_2]
* **Derivatore**: Condensatore su ![R_1]

[Sommatore Generalizzato]: https://latex.codecogs.com/svg.latex?v_%7Bout%7D%20%3D%20%5Cfrac%7B%5Csum_%7Bi%3D0%7D%5EM%20G_%7Bi%5E-%7D%20+%20G_f%7D%7B%5Csum_%7Bi%3D0%7D%5EN%20G_%7Bi%5E+%7D%7D%20%5Csum_%7Bi%3D1%7D%5EN%20%5Cfrac%7BG_%7Bi%5E+%7D%7D%7BG_f%7Dv_%7Bi%5E+%7D-%5Csum_%7Bi%3D1%7D%5EM%5Cfrac%7BG_%7Bi%5E-%7D%7D%7BG_f%7Dv_%7Bi%5E-%7D
[CMRR]: https://latex.codecogs.com/svg.latex?%5Cbigg%20|%5Cfrac%7BA_d%7D%7BA_%7Bcm%7D%7D%20%5Cbigg%20|,%20%5C%20v_%7Bcm%7D%20%3D%20%5Cfrac%7Bv%5E++v%5E-%7D%7B2%7D,%20%5C%20v_d%20%3D%20v%5E+-v%5E-

**Sommatore Generalizzato**: ![Sommatore Generalizzato]

*(Non usare questa formula, meglio **sovrapposizione** e/o **Millman**)*

**Common-Mode Rejection Ratio** (**CMRR**): ![CMRR]

## Limiti Amplificatori Operazionali

[Circuito Eq. in Linearità]: https://latex.codecogs.com/svg.latex?v_%7Bout%7D%20%3D%20A_dv_d%20+A_%7Bcm%7Dv_%7Bcm%7D+A_%7Bps%7Dv_%7Bps%7D
[Amplificazione Differenziale Finita]: https://latex.codecogs.com/svg.latex?A_v%20%3D%20%5Cfrac%7B%5Cbeta%20A_d%7D%7B1+%5Cbeta%20A_d%7D%5Cfrac%7B1%7D%7B%5Cbeta%7D%20%3D%20%5Cfrac%7B1%7D%7B%5Cbeta%7D$%20se%20$A_d%20%5Cto%20%5Cinfty
[Prodotto Banda-Guadagno]: https://latex.codecogs.com/svg.latex?B%20%3D%20%5Cbeta%20f_T
[Parametro Beta]: https://latex.codecogs.com/svg.latex?%5Cbeta%20%3D%20-%5Cfrac%7Bv_d%7D%7B%5Chat%7Be%7D%7D%20%3D%20-%5Cfrac%7Bv_d%7D%7BA_dv_d%20+%20A_%7Bcm%7Dv_%7Bcm%7D%20+%20...%7D

| -                                          | Formula                                 |
|:-------------------------------------------|:--------------------------------------- |
| **Circuito Eq. in Linearità**              | ![Circuito Eq. in Linearità]            |
| **Amplificazione Differenziale Finita**    | ![Amplificazione Differenziale Finita]  |
| **Prodotto Banda-Guadagno**                | ![Prodotto Banda-Guadagno]              |
| **Parametro Beta**                         | ![Parametro Beta]                       |

[Parametri]: https://latex.codecogs.com/svg.latex?A_%7Bcm%7D%20%5Csimeq%200,%5C%20R_%7Bin%7D%20%5Cto%20%5Cinfty,%20...
[Beta]: https://latex.codecogs.com/svg.latex?%5Cbeta%20%3D%201%20+%20%5Cfrac%7BR_2%7D%7BR_1%7D
[A_d]: https://latex.codecogs.com/svg.latex?A_d%20%3D%20-9
[Rapporto]: https://latex.codecogs.com/svg.latex?%5Cfrac%7BR_2%7D%7BR_1%7D%20%3D%209
[Risultato]: https://latex.codecogs.com/svg.latex?%5Cbeta%20%3D%201%20+%20%5Cfrac%7BR_2%7D%7BR_1%7D%20%3D%2010
[Slew-Rate]: https://latex.codecogs.com/svg.latex?%5Cbigg%20|%5Cfrac%7Bdv%7D%7Bdt%7D%5Cbigg%20|_%7Bmax%7D%20%5Cleq%20%5Cbigg%20|SR%5Cbigg%20|
[V_OFF]: https://latex.codecogs.com/svg.latex?V_%7BOFF%7D
[Corrente]: https://latex.codecogs.com/svg.latex?I%5E+/I%5E-%20%3D%20I_%7BBIAS%7D+%5Cfrac%7BI_%7BOFF%7D%7D%7B2%7D
[Corrente uscente]: https://latex.codecogs.com/svg.latex?I_%7BBIAS%7D%20%3D%20%5Cfrac%7BI%5E++I%5E-%7D%7B2%7D,%20%5C%20I_%7BOFF%7D%20%3D%20I%5E++I%5E-

**Casi Particolari**: Ad esempio operazionale ideale con parametri canonici (![Parametri]) allora ![Beta], per invertenti e non-invertenti.

(Esempio: se invertente con ![A_d], allora ![Rapporto] da cui ![Risultato])

**Slew-Rate** (**SR**): ![Slew-Rate]. Ipotizziamo sinusoide in ingresso amplificata all'uscita.

![dv/dt](https://latex.codecogs.com/svg.latex?%5Cbigg%20|%5Cfrac%7B%5Cpartial%7D%7B%5Cpartial%7Bt%7D%7D%20V_%7Bin%7DA_vsin(%5Comega%20t)%5Cbigg%20|_%7Bmax%7D%5Cleq%20%5Cbigg%20|SR%5Cbigg%20|%20%5Cimplies%20%5Cdisplaystyle%20%5Cbigg%20|%5Comega%20A_vV_%7Bin%7D%5Cbigg%20|%20%3D%20%5Cbigg%20|2%5Cpi%20fA_vV_%7Bin%7D%5Cbigg%20|%20%5Cleq%20%5Cbigg%20|%20SR%20%5Cbigg%20|)

**Offset di Tensione**: ![V_OFF] collegata al morsetto *+*

**Correnti di Polarizzazione**: Corrente ![Corrente] ai due morsetti, uscente ![Corrente uscente]

## Comparatori

***Ottenuti con retroazione positiva.***

**Soglie**:

[V_S1 inv.]: https://latex.codecogs.com/svg.latex?V_%7BS1%7D%20%3D%20V_S%5Cfrac%7BR_2%7D%7BR_2+R_1%7D+V_%7BOH%7D%5Cfrac%7BR_1%7D%7BR_1+R_2%7D
[V_S2 inv.]: https://latex.codecogs.com/svg.latex?V_%7BS2%7D%20%3D%20V_%7BS1%7D$%20ma%20con%20$OL,%20V_S$%20sul%20$%27+%27
[V_S1 non inv.]: https://latex.codecogs.com/svg.latex?V_%7BS1%7D%20%3D%20V_S%20%5Cleft(1+%5Cfrac%7BR1%7D%7BR2%7D%5Cright)%20-%20V_%7BOL%7D%5Cfrac%7BR1%7D%7BR2%7D
[V_S2 non inv.]: https://latex.codecogs.com/svg.latex?V_%7BS2%7D%20%3D%20V_%7BS1%7D$%20ma%20con%20$OH,%20V_S$%20sul%20$%27-%27
[Comparatori Reali]: https://latex.codecogs.com/svg.latex?V_%7BS1/2,%20reale%7D%20%3D%20V_%7BS1/2,%20ideale%7D-V_%7BOFF%7D

| **Invertente**  | **Non Invertente**  |
| --------------- | ------------------- |
| ![V_S1 inv.]    | ![V_S1 non inv.]    |
| ![V_S2 inv.]    | ![V_S2 non inv.]    |

**Comparatori Reali**: ![Comparatori Reali]

## Oscillatori

*da fare*
