# My Webradio with Shoutcast

## Descrizione del Progetto
Crea la tua webradio utilizzando Shoutcast. Questo progetto permette di impostare uno streaming audio che può essere ascoltato online tramite un player personalizzabile.

## Requisiti
- **Server Shoutcast**: installato e configurato su un server remoto o locale.
- **Software di Streaming**: es. Winamp con Shoutcast DSP, Mixxx, ecc.
- **Player**: per ascoltare la radio direttamente sul tuo sito.

## Installazione

### 1. Scarica e installa Shoutcast
Scarica l'ultima versione di Shoutcast dal [sito ufficiale](https://www.shoutcast.com/). Segui le istruzioni per configurare il server.

### 2. Configura Shoutcast
1. Estrai i file di Shoutcast.
2. Apri il file `sc_serv.conf` e configura i seguenti parametri:
   ```ini
   password=YOUR_PASSWORD
   portbase=YOUR_PORT
   maxuser=YOUR_MAX_LISTENERS
   ```
3. Avvia Shoutcast con il comando:
   ```bash
   ./sc_serv sc_serv.conf
   ```

### 3. Configura il Software di Streaming
Usa un software di streaming per connetterti a Shoutcast:
- Imposta l'indirizzo del server Shoutcast, la porta e la password.
- Seleziona le impostazioni di qualità del flusso audio (bitrate, codec, ecc.).

### 4. Integra il Player nel Sito
Aggiungi un player al tuo sito per permettere agli utenti di ascoltare lo streaming. Puoi usare un player HTML5 come questo:
```html
<audio controls>
  <source src="http://YOUR_SERVER_IP:YOUR_PORT/;stream.mp3" type="audio/mpeg">
  Il tuo browser non supporta l'elemento audio.
</audio>
```

## Esempi di Configurazione
### Configurazione del Server Shoutcast (sc_serv.conf)
```ini
adminpassword=adminpass
password=streampass
portbase=8000
maxuser=100
```

## Troubleshooting
- **Errore di Connessione**: Verifica che il server e il software di streaming siano configurati con gli stessi parametri.
- **Buffering o Lag**: Riduci la qualità dello streaming o aumenta il `maxuser` nel file di configurazione se il tuo server ha capacità sufficienti.

## Autore
Creato da **Giuseppe Mastronardi** - [GitHub](https://github.com/allsafeitalia)
