
##  Scopo 
* Riuscire ad avere un "sistema" riutilizzabile che invocato da pagine Asp Classic, Asp.net (1.1, 2.0, xxx) possa fare un HTML post di dati ad un'altra applicazione web remota, in particolare asp.net ma non solo

##  Problemi allo stato dell'arte 
* L'http post tra pagine asp.net non � ufficialmente supportato, vedi msdn, poich� interferisce con il meccanismo nativo dei postback. In ASP.NET 2.0 � stato quindi implementato un "Cross-Page Posting" funzionante solo per� tra web forms alla versione 2.0. 
* Se si vuole realizzare il sistema in asp.net rimane il problema della comunicazione con le pagine asp classic chiamanti, a livello di sessione non � possibile farlo


##  Soluzione 
* E' stato realizzata una pagina Asp.net ("Caller") che costruisce dinamicamente il "form html" da postare, in base a variabili di sessione valorizzate sul chiamante, che pu� essere una pagina ASP in una qualsiasi delle versioni (Classic o .NET)
* Il problema dei post tra asp.net � stato aggirato "mascherando" il viewstate del "caller"
* Il problema delle chiamate da pagine asp classic � stato superato utilizzando una "triangolazione" che utilizza una pagina asp classic che posta i dati in sessione alla pagina "Caller" in asp.net 
* Al fine di facilitare il deploy, per la codifica delle pagine "Caller" � stata scelta l'opzione "inline" (niente codice sottostante, il default su asp.net 1.1, o affiancato, il default su asp.net 2.0)
* E' stato fatto un prototipo, gi� in uso dal Team CRM di Apex-net, di cui riporto uno zip gi� utilizzabile e visionabile con Notepad, Example_Caller.zip; chi invece vuole vedere la solution originale collegarsi a VSS (progetti di test)

##  Riferimenti 
* [http://www.cs.tut.fi/~jkorpela/forms/methods.html Methods GET and POST in HTML forms](http://www.cs.tut.fi/~jkorpela/forms/methods.html Methods GET and POST in HTML forms)
* <http://msdn2.microsoft.com/en-us/library/x3x8t37x.aspx MSDN - Asp.net: Redirecting Users to Another Page>
* <http://msdn2.microsoft.com/en-us/library/ms178139.aspx MSDN - Asp.net: Cross-Page Posting in ASP.NET 2.0>
* <http://www.codeproject.com/aspnet/jsnopostback.asp CodeProject - Post an ASP.NET form with JavaScript>
* [http://www.eggheadcafe.com/articles/20021207.asp Transfer Session Variables from Classic ASP to ASP.NET](http://www.eggheadcafe.com/articles/20021207.asp Transfer Session Variables from Classic ASP to ASP.NET)

##  Allegati 
[Example_Caller.zip](../Upload/Example_Caller-1.zip)
