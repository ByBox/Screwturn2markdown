
## Il PDF e la certificazione legale dei documenti
Tramite il Portable Document Format � possibile crittografare e firmare digitalmente i file. Le differenze con i formati IRM e la posta elettronica certificata.

La sicurezza � fra i punti di forza del formato PDF, principalmente per due caratteristiche che rendono utilizzabile il formato documentale in un contesto professionale: la crittografia e la firma digitale. 

La crittografia � offerta da tutti i software PDF commerciali ed anche da soluzioni freeware. Due sono i tipi di crittografia utilizzabili nei file PDF: sino alla versione 4.0 del formato PDF esisteva solo la crittografia a 40 bit, mentre da Acrobat 5.0 in poi � possibile crittografare anche a 128 bit.

Il tipo di crittografia utilizzata adotta una combinazione degli algoritmi RC4 ed MD5 (Message-Digest algorithm 5) che � tra i pi� usati per garantire l'integrit� dei file tramite un hash a 128 bit. La crittografia di un PDF a 40 bit non dovrebbe essere mai usata, se non per ragioni di compatibilit� con Acrobat 4 e precedenti: essa pu� essere facilmente superata tramite attacchi "key search", ed esistono persino software come PDF Password Crack Pro in grado di superarla. 

### La firma digitale dei PDF con valore legale
La possibilit� di firmare digitalmente i PDF � un vantaggio enorme rispetto ad altri formati: la firma digitale consente non solo di verificare l'identit� di chi ha firmato il documento, ma anche di essere certi che il contenuto del PDF non sia stato modificato dopo la firma stessa, cosa non possibile con altri formati come il DOC di Word (il quale per esempio pu� includere macro che ne modificano il contenuto dopo la firma digitale). 

Per questo la firma digitale dei PDF ha anche valore legale in diversi paesi del mondo, cui recentemente si � aggiunta l'Italia tramite deliberazione CNIPA n. 4/2005 e Protocollo d'Intesa sottoscritto il 16 febbraio 2006 da CNIPA e Adobe. 

Le firme digitali in un PDF possono essere visibili o invisibili. Quelle visibili appaiono anche come immagini nel documento, che possono rappresentare la propria firma reale su carta, un timbro, un logo e cos� via a scelta di chi ha creato la firma digitale stessa. Quelle invisibili non appaiono sul documento, ma sono verificabili con la stessa procedura di quelle visibili ed hanno lo stesso valore. 

Per usare la firma digitale � necessario creare un file Digital ID che potr� essere usato per firmare i PDF, e un certificato di verifica che servir� per controllarne l'autenticit� e che verr� incluso nel documento PDF firmato: si tratta di un file creato dall'utente e che, una volta in possesso di terzi, consente loro di verificare l'autenticit� della firma digitale dell'utente contenuta nei documenti PDF. 

Invece di creare il Digital ID in proprio � possibile anche far certificare il proprio Digital ID da una Certification Autority (CA). Questa seconda modalit� (certificazione da parte di terzi, detta PKI) � considerata generalmente come pi� sicura della certificazione in proprio (PPK): � un po' come firmare il PDF davanti ad un notaio invece che da soli. 

La firma digitale pu� essere resa ancora pi� sicura legando l'uso del Digital ID ad un dispositivo hardware, ad esempio una smart card: in questo modo solo chi ha la smart card potr� usare il Digital ID per firmare i file PDF. Firmare digitalmente un PDF � possibile solo se esso contiene l'apposito campo dedicato alla firma digitale, campo creabile solo con Adobe Acrobat Standard/Professional e con pochi altri software professionali come FormRouter o PDFSignator. 

Con Adobe Acrobat Reader ed Acrobat Elements � possibile firmare un PDF solo se chi lo ha creato ha inserito i necessari �diritti� per poterlo fare sotto forma di Reader Extensions. Dal punto di vista tecnico la firma consiste nell'integrare il Digital ID in forma criptata nel file PDF firmato, da cui non sar� pi� separabile, cosa che ha il doppio vantaggio di non consentire a terzi di estrarla per utilizzarla e di poter garantire che il PDF non � stato modificato. 

Due sono i tipi di firma digitale utilizzabili in PDF: firma di approvazione e firma di certificazione. Nel primo caso � usata per approvare un documento, per esempio in fase di sottoscrizione di un contratto, mentre nel secondo caso esse certificano chi � l'autore del documento, garantiscono che esso � integro, ed � possibile specificare quali modifiche al documento sono consentite.

### La protezione e la certificazione dei documenti 
Il formato PDF non � l'unica modo per certificare con firma digitale un documento. Sul mercato esistono altre modalit� come ad esempio: 

l'IRM (Information Right Management) di Microsoft Office attraverso il quale si pu� impedire la visualizzazione, modifica, stampa, copia e inoltro di un documento 
P7M, formato usato per la �busta crittografica�, ovvero un file unico che contiene i documenti, creato in base alle norme del CNIPA (standard RFC2315-PKCS7 1.5) che ne garantiscono la validit�. Pu� essere creato da diverse applicazioni professionali per la firma digitale, come Trust Italia Verisign, solitamente tramite hardware con SmartCard 
PEC (Posta Elettronica Certificata), sorta di �raccomandata RR digitale� che garantisce con valore legale l'invio e la ricezione di documenti allegati ad una e-mail, si utilizza con i normali software di posta elettronica, ma � accessibile solo sottoscrivendo un contratto con un Gestore PEC accreditato 

Copia da http://searchsecurity.techtarget.it/01NET/HP/0,1254,18_ART_78536,00.html?lw=18

## Risorse
http://www.programmazione.it/index.php?entity=eitem&idItem=33923
http://www.lowagie.com/iText/
http://itextsharp.sourceforge.net/
http://sourceforge.net/projects/itextsharp/
