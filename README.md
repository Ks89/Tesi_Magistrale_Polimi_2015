# Tesi di Laurea Magistrale (2015)

## ANALISI DEI LIMITI DELL’IMPLEMENTAZIONE DI WI-FI DIRECT IN ANDROID PER RETI OPPORTUNISTICHE

#### Sommario

I dispositivi mobili come Smartphone e Tablet hanno rivoluzionato il concetto di mobilità, dando vita a nuovi scenari di utilizzo. Uno tra i più interessanti ed ampi è quello delle Opportunistic Networks, cioè reti che non richiedono un'infrastruttura preesistente, ma permettono la nascita di comunicazioni spontanee e caratterizzate da una forte dinamicità. Il problema principale è che i protocolli di comunicazione disponibili sono troppo giovani ed ancora da perfezionare in tale ambito.

Questo lavoro di tesi tratta nello specifico uno di essi, cioè Wi-Fi Direct, che non è stato pensato per scenari di questo tipo e soprattutto, la corrispondente implementazione in Android presenta grosse limitazioni. L'obiettivo è quello di studiare tali limiti nel dettaglio e proporre una soluzione per estendere il protocollo. L'approccio adottato consiste nell'analisi dell'architettura di Android, dall'alto livello, fino a quello più vicino all'hardware, iniziando dalla presentazione della soluzione progettata.

Nel corso di questo lavoro di tesi sarà mostrata, inoltre, la progettazione di due app Android con lo scopo di verificare i limiti del protocollo Wi-Fi Direct in Android e proporre uno scenario specifico di utilizzo in cui essi non sono significativi, creando un'app utilizzabile a tutti gli effetti.

La pagina ufficiale di PoliTesi con il PDF scaricabile dal sito del Politecnico di Milano è [QUI](http://hdl.handle.net/10589/107204)


## Aggiornamento Marzo 2016

Ho verificato su un Nexus 6P con Android Marshmallow 6.0.1 se si potessero create più gruppi Wi-Fi Direct su uno stesso dispositivo, seguendo esattamente la procedura descritta nella tesi.
I log risultanti sono [QUI](https://github.com/Ks89/Tesi_Magistrale_Polimi_2015/tree/master/nexus6P_screenshots_updated_march_2016).
**Come si può vedere, sono presenti ancora le stesse limitazioni.**

Gli stessi file binari, compilati in precedenza, sono funzionanti anche su Nexus 6P Marshmallow 6.0.1 (ovviamente quelli a 64 bit).


## Aggiornamento Ottobre 2015

Ho verificato su un Nexus 9 con Android Marshmallow 6.0 se si potessero create più gruppi Wi-Fi Direct su uno stesso dispositivo, seguendo esattamente la procedura descritta nella tesi.
I log risultanti sono [QUI](https://github.com/Ks89/Tesi_Magistrale_Polimi_2015/tree/master/nexus9_screenshots_updated_october_2015).
**Come si può vedere, sono presenti ancora le stesse limitazioni.**

Attenzione: ho riscontrato grossi problemi nell'eseguire la stessa procedura su Nexus 9 con versioni di Android 5.x.x e su Nexus5 con Android 5.1.x.
Nel caso di Android 6.0, la procedura utilizzata in questa tesi è tornata ad essere valida. E' possibile anche compilare "iw" sia a 32bit (Nexus5) sia a 64bit (Nexus 9) senza problemi.

In caso di dubbi sul percorso da aggiungere in wpa_supplicant.conf e/o p2p_supplicant.conf, fare riferimento al file Android.mk nella repository ufficiale di wpa_supplicant [QUI](http://w1.fi/cgit/hostap/tree).
Riporto qui un estratto:
```
# Use Android specific directory for control interface sockets
L_CFLAGS += -DCONFIG_CTRL_IFACE_CLIENT_DIR=\"/data/misc/wifi/sockets\"
L_CFLAGS += -DCONFIG_CTRL_IFACE_DIR=\"/data/misc/wifi/sockets\"
```
Per completezza ho aggiunto [QUI](https://github.com/Ks89/Tesi_Magistrale_Polimi_2015/tree/master/my_compiled_bins) i file binari per Android 6.0 a 32 e a 64 bit di wpa_supplicant, wpa_cli ed iw.


## Credits
- Template LYX di [POUL.ORG](https://www.poul.org/)
- .... non so chi altro citare
- **nella bibliografia e nei rigraziamenti ho citato più o meno tutti :)**


## Regole per usare questo materiale
- Questo progetto riflette esattamanente nel suo contenuto la tesi pubblicata su [POLITESI](http://hdl.handle.net/10589/107204). Il motivo per cui l'ho caricata qui è per rendere pubblico il template LyX che ho utilizzato e le mie personalizzazioni. Ripeto il contenuto testuale e grafico è esattamente lo stesso.
- Per utilizzare il template LyX in questione valgono le regole definite dalla licenza Apache v2 (inoltre, ricordo che il template originale è stato creato da POUL.ORG)
- Per utilizzare il contenuto (testo e immagini) di questa tesi, valgono le regole generali definite dal Politecnico di Milano
- **In caso di dubbi contattatemi, rispondo subito. Sono molto aperto all'uso di questo materiale, è sufficiente una breve email con gentilezza e io risponderò con altrettanta gentilezza.**
- Nel progetto ho caricato anche il Kernel (basato su quello di Faux123) che ho modificato e compilato per Nexus 5 con Android KitKat 4.4.4 ([QUI](https://github.com/Ks89/Tesi_Magistrale_Polimi_2015/blob/master/Tesi%20LYX%202.1.3/capitolo-5/printk_mac_address/k-kernel-4.4.4-printk-macaddress-hammerhead-based_on_faux123-021u.zip)). E' qui solo per completezza. Per favore non spacciatelo per vostro, perchè è facile verificare chi l'ha compilato. Se avete problemi a creare la vostra versione, piuttosto di copiare, contattatemi che magari vi posso aiutare.


## Licenza per il template LyX e l'altro materiale di mia creazione/modifica (testo escluso)

Copyright 2014-2016 Stefano Cappa

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

<br/>
**Stefano Cappa**
