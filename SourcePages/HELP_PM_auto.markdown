<br/>

<table><tr><td>
![](../Upload/PM/menu10.png)
</td></tr></table>

E' una funzionalit� di _Validazione_ della scheda tecnica.<br/>
E' una videata accessibile solo per il profilo validatore e amministratore e consiste in una lista di schede tecniche che sono in stato di chiusura e che devono essere validate.<br/>
L'utente tramite questa maschera potr� validare o non validare la scheda, nel caso venga validata, la scheda passer� allo stato _ATTIVO_ e potr� essere stampata dalla videata [Stampe](HELP_PM_report).
Nel caso in cui, l'utente non ritenga idonea la validazione, la scheda torner� allo stato _BOZZA_ e l'operatore dovr� indicare una motivazione nell'apposito campo _Non Autorizzata_, il validatore potrebbe anche _ANNULARE_ la scheda sempre indicandone una motivazione (campo _Non Autorizzata_)
<br/><br/>
In questa videata sono visibili le schede tecniche che si trovano in stato _CHIUSO_.<br/>
- - -
Osserviamo meglio la videata. <br/>
Nella parte in alto si trova un campo descrittivo che verr� valorizzato dall'utente quando la scheda non sar� Autorizzata, a destra di tale campo troviamo 3 bottoni. 

<table><tr><td>
![](../Upload/PM/auto1.png)
</td></tr></table>

Tali bottoni eseguono la modifca dello stato della scheda tecnica, solo per le schede tecniche che sono state selezionate nella parte sottostante la videata, come riportato nella figura sottostante.

<table><tr><td>
![](../Upload/PM/auto2.png)
</td></tr></table>


* **Bozza**: � necessario inserire nel campo _Non Autorizzata_, la motivazione del pasaggio dallo stato _CHIUSO_ della scheda allo stato _BOZZA_. Il sistema memorizzer� la motivazione e porr� la scheda tecnica nuovamente in stato _BOZZA_, facendola sparire dall'elenco sottostante; 

* **Validata**: aggiorna la scheda o le schede selezionate dall'operatore, in stato _ATTIVA_, cio� pronta per la stampa e validate.

* **Annullata**: � necessario inserire nel campo _Non Autorizzata_, la motivazione del pasaggio dallo stato _CHIUSO_ della scheda allo stato _ANNULLATA_. Il sistema memorizzer� la motivazione e porr� la scheda tecnica in stato _ANNULLATA_, facendola sparire dall'elenco sottostante, e rendendola non modificabile dal pannello delle generale delle [Schede Tecniche](HELP_PM_tecnica).

L'elenco delle schede nella parte sotto della videata, permette di aprire la [Scheda Tecnica](HELP_PM_tecnica) completa tramite il pulsante ![](../Upload/PM/scheda.jpg), mentre il pulsante ![](../Upload/PM/motivo.jpg), � presente nella riga della scheda tecnica solo nel caso in cui la scheda ha avuto gi� in passato uno spostamento di stato _non autorizzato_ ed � ritornata in stato _CHIUSO_.<br/>

Il pulsante ![](../Upload/PM/motivo.jpg), apre la videata che racchiude le varie [Motivazione](HELP_PM_motivo) inserite dagli operatori per quella scheda tecnica.
