ASSICURAZIONE TRACKER - PROGETTO ANDROID APK

Questa cartella contiene il progetto Android Studio che impacchetta l'app come applicazione
Android locale. Non dipende da Netlify o Cloudflare e include direttamente la pagina web
nell'APK. I dati vengono conservati nella memoria privata dell'app tramite WebView
(localStorage e IndexedDB), e restano disponibili dopo chiusura e riapertura.

INTERFACCIA
- I pulsanti "Esporta copia di sicurezza" e "Importa copia di sicurezza" sono stati rimossi.
- Le altre funzioni e lo storico sono mantenuti.

COME OTTENERE L'APK
Per compilare serve Android Studio su un PC Windows, Mac o Linux:
1. Installa Android Studio: https://developer.android.com/studio
2. Estrai questo ZIP.
3. In Android Studio scegli Open e seleziona la cartella "AssicurazioneTrackerAndroid".
4. Attendi che Gradle termini la sincronizzazione (serve connessione internet la prima volta
   per scaricare i componenti Android).
5. Seleziona Build > Build Bundle(s) / APK(s) > Build APK(s).
6. L'APK di prova si trova in:
   app/build/outputs/apk/debug/app-debug.apk
7. Copia app-debug.apk sul telefono Android, aprilo e autorizza l'installazione da questa
   origine quando Android lo chiede.

AGGIORNAMENTI
Mantieni lo stesso applicationId (it.assicurazionetracker.app) per gli aggiornamenti futuri,
così Android può aggiornare l'app senza cancellare i suoi dati. Non disinstallare l'app per
aggiornarla: installa l'APK nuovo sopra la versione esistente.

DATI DELLA VECCHIA PWA
I dati memorizzati nel Chrome del sito Cloudflare non vengono trasferiti automaticamente
nell'APK: Android tiene separati i dati del sito e quelli dell'app. Prima di passare all'APK,
conserva la vecchia PWA e il suo indirizzo; se lo storico è ancora visibile lì, possiamo
preparare una migrazione dei dati. Non cancellare i dati di Chrome o la vecchia app.

NOTA TRASPARENTE
Questo ambiente non dispone dell'Android SDK/Gradle necessario per produrre e firmare un
file APK installabile. Per questo consegno il progetto Android Studio già pronto da compilare,
non un APK già compilato. La compilazione finale si esegue con i passaggi sopra.
