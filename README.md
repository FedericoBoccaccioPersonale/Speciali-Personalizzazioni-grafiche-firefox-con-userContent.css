<h1>Speciali ✨ 🔥🦊 🇮🇹\<br>Personalizzazioni grafiche Firefox con userContent.css</h1>
https://federicoboccaccio.wordpress.com/

# Download
Questo repository non ha release. Scarica direttamente i sorgenti.

# Informazioni
Su GitHub c' è il repository principale, su GitLab è presente il suo clone per backup.

# Istallazione
Ho trovato un servizio online di condivisione note, ProtectedText.com, che però ha il pulsante di salvataggio poco visibile. Così ho cercato se esistesse un modo per evidenziarlo meglio in solo CSS, senza estensioni. Poi è venuto il resto.

Queste sono le istruzioni per Firefox funzionanti a dicembre 2025.

## 🔧 Passaggi per personalizzare un sito con `userContent.css`

1. **Attiva il supporto ai fogli di stile personalizzati**  
- Digita `about:config` nella barra degli indirizzi.  
- Cerca `toolkit.legacyUserProfileCustomizations.stylesheets`.  
- Imposta il valore su `true`.

2. **Trova la cartella del profilo Firefox**  
- Vai su `about:support`.  
- Nella sezione *Cartella del profilo*, clicca su *Apri cartella*.  
- Dentro, crea (se non esiste) una cartella chiamata `chrome`.

3. **Crea il file `userContent.css`**  
- Dentro la cartella `chrome`, crea un file chiamato `userContent.css`.

4. **Scrivi le regole CSS per un sito specifico**  
Usa la sintassi con `@-moz-document domain(...)` o `url(...)`.  

5. **Riavvia Firefox**  
Le modifiche diventano attive solo dopo il riavvio.<br>
Funziona anche chiudendo e riaprendo in una finestra anonima.

Le regole appariranno direttamente aprendo gli strumenti di sviluppo.

## 📌 Differenza chiave
- `userChrome.css` → interfaccia del browser.  
- `userContent.css` → contenuto dei siti web.  

## Sintassi del selettore di pagina
* `@-moz-document domain("example.com")` agisce sul dominio, va scritto senza http, www o barre
* `@-moz-document url-prefix("http")` agisce su tutti i siti che cominciano con quella stringa, in questo caso tutti
* `@-moz-document url("https://www.protectedtext.com/")` su quella specifica pagina
