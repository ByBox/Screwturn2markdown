
##  Scenario 
* Una delle cose da **evitare** quando si rilascia un'applicazione ASP.NET in produzione � lasciare l'opzione **compilation debug=�true�** nel file web.config, cio� in debug release. Per esempio:

     xml
    <compilation defaultLanguage="c#" debug="true">


* Questa cosa causa un certo numero di problemi che possono accadere, tra gli altri:
    * Per la compilazione delle pagine ASP.NET occorrer� pi� tempo (alcune opzioni di ottimizzazione sono disabilitate)
    * Il codice sar� eseguito pi� lentamente
    * Una maggior quantit� di memoria sar� allocata dall'applicazione a run-time
    * Scripts e immagini saranno scaricate dai gestori tipo WebResources.axd ma non in modalita "cached"
* In ASP.NET AJAX gli scripts ed altre risorse sono ottimizzati nel caso di release version, vedi riferimento.

##  Soluzioni 
* La prima cosa che sicuramente si pu� fare � quella di **rilasciare** le applicazioni asp.net con il web.config nel quale � esplicitamente valorizzata la key: **compilation debug=�false"**
* Utilizzando l'add-in di VS2005 **Web Deployment** per compilare si pu� spuntare il corrispondente flag di compilazione in modo da rendere la cosa meno manuale. Si avr� cosi il web.config correttamente configurato nella opportuna cartella di deploy
* Nel caso di applicazioni almeno alla versione **ASP.NET V2.0** si pu� agire direttamente a livello di **machine.config** sul server di deploy. Cos� facendo vengono disabilitati, ad esempio, il trace output a livello di pagina e  ignorati tutti i debug=true delle varie web application attive sul server. 

Esempio:

**
     xml
    <configuration>
        <system.web>
              <deployment retail=�true�/>
        </system.web>
    </configuration>
 
**

##  Riferimenti 
* [Panoramica su Asp.net e Ajax Debugging](http://asp.net/ajax/documentation/live/overview/ASPNETAJAXDebuggingAndTracingOverview.aspx)
