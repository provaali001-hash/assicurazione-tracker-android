ASSICURAZIONE TRACKER - CREAZIONE APK DIRETTAMENTE DA TELEFONO ANDROID

Questo pacchetto include il progetto Android e una procedura automatica di compilazione
su GitHub Actions. Non serve installare Android Studio e non serve un PC. È necessario
un account GitHub e una connessione internet durante la compilazione.

PASSAGGI DA TELEFONO
1. Scarica ed estrai questo ZIP con l'app "Files" / "Archivio" del telefono.
2. Apri Chrome e vai su https://github.com/ .
3. Accedi o crea un account gratuito.
4. Crea un nuovo repository (New repository), nome: assicurazione-tracker-android.
   Impostalo Private se vuoi tenerlo privato e premi Create repository.
5. Nel repository premi Add file > Upload files.
6. Nel selettore file Android, entra nella cartella estratta del progetto e seleziona
   TUTTI i file e le cartelle del progetto (inclusa la cartella nascosta .github).
   Se il selettore non mostra .github, usa il metodo alternativo sotto.
7. Premi Commit changes.
8. Apri la scheda Actions del repository. Se GitHub chiede di abilitare Actions,
   conferma.
9. Seleziona "Crea APK Android" e premi Run workflow > Run workflow.
10. Attendi che il lavoro finisca con il segno verde.
11. Apri il lavoro completato, scorri a Artifacts e tocca
    "Assicurazione-Tracker-APK". Verrà scaricato un archivio ZIP contenente app-debug.apk.
12. Estrai lo ZIP e tocca app-debug.apk per installarlo. Android potrebbe chiedere di
    consentire a Chrome o Files l'installazione di app sconosciute.

SE GITHUB NON MOSTRA LA CARTELLA .github NEL CARICAMENTO
Dopo aver caricato tutti gli altri file:
1. Nel repository premi Add file > Create new file.
2. Come nome del file scrivi esattamente:
   .github/workflows/build-apk.yml
3. Incolla il contenuto del file build-apk.yml incluso nel pacchetto (puoi aprirlo con
   un editor di testo).
4. Premi Commit changes. Poi vai in Actions e avvia "Crea APK Android".

IMPORTANTE PER NON PERDERE I DATI
- L'APK è un'app separata: i dati salvati in Chrome/Cloudflare non vengono trasferiti
  automaticamente nell'APK.
- Non cancellare la PWA Cloudflare, non disinstallarla e non cancellare i dati di Chrome
  finché non hai verificato come trasferire lo storico.
- Per gli aggiornamenti futuri dell'APK, installa il nuovo APK sopra quello esistente
  con lo stesso ID app, senza disinstallare prima: così i dati dell'app restano.
- Il repository GitHub contiene il codice sorgente. Puoi renderlo privato.

L'APK è una build debug non firmata per distribuzione sul Play Store, ma installabile
manualmente sul tuo Android.
