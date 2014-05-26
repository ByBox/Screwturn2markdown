
##  Scenario 
* Il .NET Framework dispone di una variet� di collezioni da utilizzare come contenitori di oggetti. Tutte le collezioni implementano l'interfaccia IEnumerable che viene estesa da ICollection. In particolare si distinguono due gruppi di collezioni che implementano due interfacce derivate da ICollection: IDictionary e IList
* Ci sono due ragioni per cui uno sviluppatore pu� desiderare di implementare una sua **collezione Custom**:
    * per implementare un oggetto di Business **contenitore** (relazioni tra Ordini e Ordine, tra Ordine e RigaOrdine e tra Cliente e Condizioni di Pagamento)
    * per implementare una collezione di Value-Type **efficente**

##  Soluzioni 
* E' sicuramente possibile partire da "scratch" scrivendo classi che implementano interfaccie come IEnumerable... ma la via � cosi abbastanza lunga
* Un metodo sicuramente pi� efficiente per implementare una collezione personalizzata in **C#** � quello di sfruttare l**'ereditariet�** a partire da classi base opportunamente fornite dal Framework nel namespace **System.Collections** e **System.Collections.Specialized**. Le classi base astratte forniscono gi� l'implementazione di tutti i metodi necessari (o comunque di gran parte).
    * **Esempio**:
*** si voglia ad esempio implementare una relazione messaggi-messaggio associati ad una mailbox di un server di posta
*** vogliamo realizzare una classe **messaggio** e una classe collection **messsaggi** 
*** creiamo la nostra classe collection ereditando dalla classe **CollectionBase**, che � gi� provvista di metodi come **Clear** e property come **Count**, dovremo implementare solo i metodi **Add**, **Remove** e l**'Item** property
*** � poi possibile accedere agli items di una collection tramite il costrutto **foreach** 
*** il processo pu� essere esteso considerando che un messaggio potrebbe avere come property uleriori collections di senders, attachments, ecc...

     csharp
    
    namespace ApexNet.Mailing.Pop3
    {
        public class Pop3Message
    ...
    


     csharp
    
    namespace ApexNet.Mailing.Pop3
    {
        public class Pop3Messages : CollectionBase
        {
            public void Add(Pop3Message message)
            {
                List.Add(message);
            }
    ...
 

     csharp
    ApexNet.Mailing.Pop3.Pop3Client email = new Pop3Client(user, psw, server, 110);
    email.Connect();
    email.Login();
    ApexNet.Mailing.Pop3.Pop3Messages messages;
    messages = email.GetAllMessages();
    foreach (ApexNet.Mailing.Pop3.Pop3Message item in messages)
    {
       foreach (Pop3MessageSender itemSender in item.Senders)
       {
          ...
       }
       foreach (Pop3MessageAttachment itemAttachment in item.Attachments)
       {
       ...


##  Riferimenti 
* [Using collection in .NET](http://www.15seconds.com/issue/030429.htm)
* [MSDN: Collection Classes Tutorial](http://msdn2.microsoft.com/en-us/library/aa288462(VS.71).aspx)
* [MSDN: Creating Your Own Collection Class](http://msdn2.microsoft.com/en-us/library/xth2y6ft(VS.71).aspx)
