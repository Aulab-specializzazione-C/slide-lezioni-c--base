Intro C# Le origini C# (si legge "C sharp") nasce alla fine degli anni
ʼ90 allʼinterno di Microsoft. Il linguaggio fu progettato principalmente
da Anders Hejlsberg (già autore di Turbo Pascal e Delphi) come parte
della strategia per creare una nuova piattaforma di sviluppo moderna: il
.NET Framework. Le origini di C# sono strettamente legate a Java.
Allʼepoca Microsoft stava collaborando con Sun Microsystems su Java, ma
dopo dispute legali decise di sviluppare un linguaggio proprio, che
mantenesse una sintassi familiare ai programmatori C/C++ e Java, ma
fosse profondamente integrato con lʼecosistema Windows e .NET. La prima
versione ufficiale di C# (1.0) fu rilasciata nel 2002, insieme a .NET
Framework 1.0. Fin dallʼinizio C# si presentò come: un linguaggio
fortemente tipizzato, orientato agli oggetti, progettato per essere più
sicuro e semplice rispetto a C++ (con gestione automatica della memoria
tramite garbage collection). Negli anni successivi, poi, C# si è evoluto
rapidamente. Oggi C# è un linguaggio maturo, moderno e multipiattaforma,
grazie a.NET, ed è usato per applicazioni desktop, web, cloud, mobile e
videogiochi (in particolare con Unity). Cenni storici Il .NET Framework
è la versione "storica" della piattaforma Microsoft, introdotta nei
primi anni 2000. È stato per molti anni il punto di riferimento per lo
sviluppo di applicazioni in ambiente Windows. Funziona esclusivamente su
Windows ed è fortemente integrato con le tecnologie tipiche di questo
ecosistema, come WPF, Windows Forms e Core "classico". Ancora oggi è
mantenuto da Microsoft, soprattutto per garantire compatibilità con
applicazioni esistenti, ma non riceve più nuove funzionalità
significative: viene aggiornato principalmente per motivi di sicurezza e
stabilità. Nel 2016 Microsoft ha introdotto .NET Core, una versione
completamente ripensata della piattaforma. Lʼobiettivo era creare un
ambiente moderno, open source e soprattutto multipiattaforma. A
differenza del .NET Framework, .NET Core può essere eseguito non solo su
Windows, ma anche su macOS e Linux. È più leggero, modulare e
performante, ed è stato progettato con particolare attenzione agli
scenari cloud, ai microservizi e allʼutilizzo in container come Docker.
Questo lo ha reso rapidamente la scelta preferita per i nuovi progetti.
A partire dal 2020, con lʼuscita di .NET 5, Microsoft ha unificato
definitivamente la piattaforma: .NET Core è stato rinominato
semplicemente .NET. Le versioni successive (.NET 6, .NET 7, .NET 8 e
così via) rappresentano lʼevoluzione diretta di .NET Core. Oggi, quando
si parla di ".NET", ci si riferisce alla piattaforma moderna e
multipiattaforma, che è anche quella consigliata per lo sviluppo di
nuove applicazioni. Cos'è C# Linguaggio di alto livello C# è un
linguaggio di programmazione ad alto livello, cioè un linguaggio
progettato per essere più vicino al linguaggio dell' uomo, piuttosto che
dalla macchina.ASP.NET\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Un linguaggio di basso livello, di contro, è più vicino alla macchina
come l'assembly, famoso per le cpu 8086 e 8088 di Intel. Se volete
potete utilizzare emulatori come Emu8086 o similari per provare. C# e
.Net C# è un linguaggio di programmazione moderno, orientato agli
oggetti e fortemente tipizzato, sviluppato da Microsoft. È pensato per
funzionare sulla piattaforma .NET, che fornisce un ambiente di
esecuzione con garbage collection, sicurezza della memoria e una ricca
libreria standard. C# combina la sintassi familiare di C/C++ e Java con
funzionalità moderne che favoriscono produttività e leggibilità, come
LINQ, async/await e il pattern matching. Oggi C# è multipiattaforma e
viene usato per creare applicazioni web, desktop, cloud, mobile e
videogiochi, offrendo un buon equilibrio tra prestazioni, semplicità e
potenza espressiva. Gestione della memoria C# ha una gestione della
memoriaautomatica tramite garbage collector, ma consente (in casi
avanzati) codice unsafe con puntatori. Il Garbage Collector di C# è un
meccanismo automatico che gestisce la memoria per gli oggetti allocati
sullo heap gestito. Il programmatore non deve liberare manualmente la
memoria: il GC individua gli oggetti non più utilizzati e li rimuove. Il
suo compito è semplice: trovare gli oggetti che il programma non usa più
e liberare la memoria che occupano. Per farlo, il GC controlla quali
oggetti sono ancora "raggiungibili" dalle variabili attive o dai
riferimenti principali. Gli oggetti che nessuno può più raggiungere
diventano spazzatura e vengono eliminati. C# usa un approccio chiamato
heap generazionale: la memoria è divisa in tre gruppi, o "generazioni".
Gli oggetti appena creati finiscono nella Gen 0, quelli che sopravvivono
a qualche ciclo vengono promossi in Gen 1 e Gen 2. Lʼidea è semplice: la
maggior parte degli oggetti vive poco, quindi conviene liberare
rapidamente quelli nuovi e preoccuparsi meno di quelli longevi. Per
oggetti molto grandi cʼè unʼarea speciale chiamata Large Object Heap,
che viene gestita meno spesso, perché spostare oggetti grandi è costoso.
Infine, se un oggetto usa risorse esterne come file o connessioni, è
meglio usare IDisposable e il costrutto using per liberarle subito,
perché il GC si occupa solo della memoria gestita, non delle risorse
esterne. In pratica, il Garbage Collector semplifica la vita del
programmatore, riduce i bug legati alla memoria e rende C# più sicuro e
produttivo rispetto al C++ dove tutto va gestito a mano. Paradigmi e
stile C# è un linguaggio principalmente orientato agli oggetti, ma
supporta anche molte caratteristiche della programmazione funzionale,
come le lambda, le espressioni LINQ e il pattern matching. Questo lo
rende molto espressivo: con poche righe di codice puoi fare operazioni
complesse in modo chiaro. Rispetto a Java, C# tende a essere meno
verboso, quindi il codice è spesso più compatto e leggibile senza
sacrificare chiarezza o sicurezza. Inoltre, funzionalità come
async/await rendono naturale scrivere codice asincrono senza
complicazioni. Prestazioni\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Dal punto di vista delle prestazioni, C# è comparabile a Java: offre
tempi di esecuzione rapidi e, con le versioni più recenti di .NET, le
performance sono in costante miglioramento. In alcuni scenari
particolarmente ottimizzati, può anche avvicinarsi molto a quelle del
C++, pur mantenendo la sicurezza e la gestione automatica della memoria.
Portabilità Per quanto riguarda la portabilità, C# inizialmente era
legato soprattutto a Windows. Oggi, grazie a .NET multipiattaforma, è
possibile sviluppare e far girare applicazioni anche su Linux e macOS,
senza dover riscrivere il codice. Ecosistemi di utilizzo Lʼecosistema di
utilizzo di C# è molto ampio: viene usato per creare applicazioni
desktop e web, sviluppare servizi cloud e microservizi, programmare
videogiochi con Unity e realizzare diversi tool aziendali. Questa
versatilità lo rende uno dei linguaggi più diffusi e moderni per
sviluppare software in diversi contesti. Type system di C# In C#, ogni
classe, struct o interfaccia che dichiariamo diventa un tipo. Il type
system di un linguaggio è lʼinsieme dei tipi di dato disponibili e delle
regole con cui questi vengono gestiti. Serve a capire come C# tratta i
dati e quali operazioni possiamo fare su di essi. Possiamo suddividerlo
in due aspetti principali: Verifiche sui tipi di dato e sulle operazioni
Verifiche sulla correttezza dei dati che stiamo utilizzando Verifiche
sui tipi di dato e sulle operazioni C# effettua controlli sui tipi in
due modalità: Statica: Il controllo avviene a compile time, cioè quando
scriviamo il codice e lo compiliamo con il compilatore C#. Il
compilatore verifica che le variabili, le funzioni e le operazioni sono
coerenti con i tipi dichiarati. Questo riduce gli errori a runtime,
rendendo C# affidabile per applicazioni critiche, videogiochi o software
aziendali complessi. Dinamica: Alcuni controlli possono avvenire a
runtime, durante lʼesecuzione del programma. Questo accade soprattutto
con i tipi dynamic o tramite reflection, una funzionalità di C# (e del
.NET in generale) che permette a un programma di ispezionare sé stesso
mentre è in esecuzione, dove C# verifica il tipo di un oggetto in tempo
reale.\[! https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Verifiche sulla correttezza dei dati Esistono due tipologie di verifica
tramite controllo sulla tipizzazione Tipizzazione forte Vuol dire che
dobbiamo: Indicare il tipo delle variabili quando le dichiari.
Specificare il tipo di ritorno di una funzione. Indicare il tipo dei
parametri che la funzione riceve. Non ci sono conversioni implicite tra
tipi incompatibili (a meno di cast espliciti). Tipizzazione debole Vuol
dire che: Il tipo delle variabili può cambiare nel tempo. Non è sempre
necessario dichiarare esplicitamente il tipo. Le funzioni non richiedono
necessariamente un tipo di ritorno dichiarato. I parametri delle
funzioni non hanno un tipo fisso. Sono permesse conversioni implicite
automatiche tra tipi diversi, anche se logicamente incompatibili. Molti
errori di tipo vengono rilevati solo a runtime. C# è a tipizzazione
forte e statica, come Java. Il type system di C# è forte, sicuro e
statico, con controlli che avvengono principalmente a compile time, ma
con la flessibilità di poter effettuare alcune verifiche dinamiche
quando serve. Questo lo rende ideale per sviluppare applicazioni robuste
e sicure, mantenendo comunque la possibilità di operare in modo dinamico
se necessario. Linguaggi interpretati e compilati Compilati Nei
linguaggi compilati viene prima tradotto tutto il codice e poi eseguito.
Il compilatore è lo strumento che legge e traduce il codice in binario e
poi lo esegue. Se non vi sono errori nella compilazione viene generato
un file utilizzabile dal processore. Ma cosa succede se commetto un
errore, anche banale, come dimenticare un ";"? Il compilatore segnalerà
l'errore e il file eseguibile non verrà creato. Di conseguenza, devo
correggere l'errore, rilanciare la compilazione e, se tutto è corretto,
verrà generato il file eseguibile. Interpretati Un linguaggio
interpretato è un linguaggio in cui il codice viene letto ed eseguito
riga per riga, come ad esempio JavaScript o Python. Quando un programma
viene avviato (run), ogni singola riga di codice viene letta, tradotta
ed eseguita.\[! https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT
oUSkC- VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Per "tradotta" si intende che il codice viene trasformato in un
linguaggio comprensibile alla macchina (codice binario o istruzioni a
basso livello). Nei linguaggi interpretati, lʼesecuzione continua finché
non viene incontrato un errore oppure finché il programma termina
correttamente. Se si verifica un errore: lʼesecuzione si ferma in quel
punto tutto il codice scritto prima dellʼerrore viene comunque eseguito
le istruzioni successive non verranno eseguite Ad esempio, in
JavaScript, se cʼè un errore a una certa riga, tutte le istruzioni
precedenti vengono eseguite senza problemi, mentre quelle successive non
verranno eseguite. E C# che tipo di linguaggio è? C# non è né puramente
compilato né puramente interpretato. È un linguaggio compilato in modo
intermedio, perché utilizza un modello a doppia compilazione. Come
funziona in C# / .NET 1. Il codice C# viene compilato dal compilatore in
un linguaggio intermedio chiamato IL (Intermediate Language). 2. LʼIL
non è ancora codice macchina specifico per un sistema operativo. 3.
Quando il programma viene eseguito, entra in gioco una Virtual Machine
chiamata CLR (Common Language Runtime). 4. La CLR traduce lʼIL in codice
macchina reale tramite un compilatore chiamato JIT (Just-In-Time
compiler). 5. Solo a questo punto il codice viene eseguito dal
processore. Cosʼè lʼIL (Intermediate Language)? LʼIL è un linguaggio
intermedio indipendente dalla piattaforma. Significa che: non è codice
binario puro per Windows, Linux o macOS è un codice "universale" che può
essere tradotto in codice macchina su qualunque sistema supportato da
.NET Questo è uno dei motivi per cui .NET è multipiattaforma. Cosʼè la
Virtual Machine (CLR)? La CLR (Common Language Runtime) è la macchina
virtuale di .NET. Si occupa di: tradurre lʼIL in codice macchina
(tramite JIT) gestire la memoria (Garbage Collector) controllare la
sicurezza gestire le eccezioni gestire thread e processi In pratica, la
CLR è lʼambiente che permette al programma C# di funzionare.\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

HelloWorld: Creazione del file Scriviamo quindi le nostre prime righe di
codice in C#. Ovviamente, per far funzionare il tutto, abbiamo bisogno
di installare lʼambiente .NET necessario. Oggi non si parla più di ".NET
Core" come prodotto separato, ma semplicemente di .NET (versioni 6, 7,
8, ecc.), che rappresenta lʼevoluzione moderna e multipiattaforma della
piattaforma Microsoft. Per installare .NET è sufficiente scaricare lʼSDK
dal sito ufficiale Microsoft, scegliere la versione consigliata
(preferibilmente una LTS, come .NET 8), selezionare il proprio sistema
operativo e avviare lʼinstaller seguendo la procedura guidata. Una volta
completata lʼinstallazione, lʼambiente sarà pronto per creare e
compilare applicazioni C#. (Installazione dettagliata rimandata ad un
materiale specifico) Abbiamo due modi per inizializzare un progetto C#.
Il primo è inserendo una serie di comandi. CREAZIONE MANUALE: crea un
nuovo solution file. Un solution file (.sln) in C# .NET è un contenitore
logico che raggruppa uno o più progetti (.csproj). Serve a organizzare,
gestire le configurazioni di build e coordinare i progetti quando lavori
in Visual Studio o VS Code. In pratica, la solution è la "cartella
madre" che dice a .NET come tutti i pezzi del software stanno insieme.
crea il nuovo template di progetto. Un template di progetto in C# .NET è
uno scheletro predefinito con cartelle, file e impostazioni di base,
pronto per iniziare subito un nuovo progetto (console, web, libreria,
ecc.). Questo comando aggiunge un progetto (ConsoleApp.csproj) alla
solution SpecNet.sln. "collega questo progetto alla solution", senza
collegamento, il progetto esiste da solo, ma la solution non sa che
esiste e non può usarlo nel build/debug coordinato. Fatti questi
passaggi avremo un progetto strutturato in questo modo. Questo è un
progetto ben strutturato e già perfettamente funzionante. 1dotnet new
sln --name SpecNet 1dotnet new console --name ConsoleApp 1dotnet sln
SpecNet.sln add ConsoleApp/ConsoleApp.csproj \[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

CREAZIONE TRAMITE VS CODE: Altro modo più veloce per creare una app
console in C# è utilizzare lʼestensione di VsCode che ci consentirà di
creare tutta la struttura necessaria. Creiamo una cartella e dirigiamoci
al suo interno aprendola con VsCode. Allʼinterno di VsCode spingiamo
contemporaneamente i tasti Si aprirà la command palette allʼinterno
della quale dovremo cercare e dare invio sulla voce fatto questo ci
verrà richiesto che tipo di applicazione vogliamo creare quindi
cerchiamo "console" e ci comparirà Selezioniamo ed andiamo avanti.
Arrivati qui, ci chiederà di inserire il nome del nostro piccolo
progetto diamogli un qualsiasi nome e procediamo. Step successivo ci
chiederà in quale directory vogliamo memorizzare il nostro progetto
Selezionando default, gli stiamo dicendo di crearlo allʼinterno del
folder in cui ci troviamo, diversamente possiamo scegliere unʼaltra
directory. Dopo aver scelto il nome ci chiederà che tipo di solution
format vogliamo creare e noi sceglieremo "sln" Ultimo passaggio è
proprio quello di confermare la creazione del nuovo progetto
1ctrl+shift+p \[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Eseguiti tutti questi passaggi avremo un progetto strutturato in questo
modo Abbiamo ottenuto anche in questo caso un progetto ben strutturato e
funzionante. SINTASSI E STRUTTURA DEL PROGETTO: Analizziamo la struttura
e la sintassi del condice Console È una classe predefinita di
.NET(appartenente allo spazio dei nomi "System") che rappresenta il
terminale o la console. Serve per leggere input o scrivere output.
WriteLine È un metodo della classe "Console" che stampa sul terminale e
va a capo alla fine. Esiste anche "Write", che stampa senza andare a
capo. ("Hello, World!") È lʼargomento passato al metodo: la stringa da
stampare. Per quanto riguarda la struttura del progetto invece .sln E'
il solution del progetto, contenitore di progetti .csproj E' la
configurazione del progetto Program.cs E' il codice principale del
nostro progetto bin Contiene tutto lʼoutput compilato
1Console.WriteLine("Hello, World!");\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

obj E la cartella che contiene tutti i file temporanei .vscode Presente
anche in altre tipologie di progetti, contiene la configurazione del
nostro editor Build e avvio del progetto Arrivati a questo punto
possiamo avviare il nostro progetto, ma C# essendo un linguaggio
compilato dobbiamo prima "buildarlo" e poi possiamo mandarlo in "run"
Abbiamo due strade che possiamo seguire una manuale ed una direttamente
tramite VsCode. AVVIO MANUALE: Per poter costruire il nostro codice
dobbiamo lanciare il comando: Il comando dotnet build compila il
progetto o la solution .NET. Controlla che il codice sia corretto,
risolve le dipendenze e genera i file compilati (DLL o EXE) nella
cartella bin, che vedremo infatti popolarsi con i file appena buildati.
In breve: trasforma il codice sorgente in un programma pronto per essere
eseguito. Per poter lanciare il pacchetto appena buildato lanciamo il
comando Prima di poter lanciare questo comando però assicuriamoci di
essere allʼinterno della cartella del nostro progetto altrimenti andrà
in errore poichè non trova i file da lanciare. Avviamo il nostro
progetto e vedremo la striga stampata in console. AVVIO TRAMITE VS CODE:
Abbiamo anche un altro metodo più veloce per poter avviare il nostro
progetto, utilizzando il nostro VsCode appositamente configurato per C#.
Andiamo sul comando run di VsCode confermiamo "run without debugging",
ci verrà chiesto quale debugger utilizzare e selezioniamo "C#" poi vorrà
indicazioni sul launch configuration 1dotnet build 1dotnet run \[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

e selezioniamo "C#:ConcoleApp1" dove "ConsoleApp1" è il nome del nostro
progetto. Questa operazione ci verrà chiesta una sola volta, tutte le
volte successive partirà direttamente. Stesso procedimento si avvierà
se, invece di utilizzare la barra dei menu di VsCode, clicchiamo sul
file di progetto del nostro codice e una volta selezionato, andiamo a
cliccare sullʼicona del "play" che vediamo in alto a destra. Al primo
avvio del nostro progetto avremo lo stesso procedimento del lancio
tramite "run" dopo il secondo avvio, il progetto partirà in automatico.
Anche questa volta avviamo il nostro progetto e vedremo la striga
stampata in console Codice Hello world con una classe Abbiamo anche un
altro modo per poter scrivere il nostro codice "hello world" La classe
HelloWorld In C#, tutto il codice vive allʼinterno di una classe. Qui
stiamo dichiarando una classe chiamata HelloWorld. La classe può essere
vista come un contenitore che racchiude il nostro codice. In questo caso
il nome HelloWorld è solo un nome simbolico, scelto per tradizione nei
primi esempi. Il metodo Main Questo è il punto più importante del
programma. Il metodo Main è il punto di ingresso dellʼapplicazione:
quando avviamo il programma, C# parte sempre da qui. 1classHelloWorld 2{
3 staticvoidMain(string\[\] args) 4{ 5 string ciao_mondo ="HelloWorld";
6 Console.WriteLine(ciao_mondo); 7} 8} 9 1classHelloWorld 2{ 3
1staticvoidMain(string\[\] args) 2{ 3\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

static indica che il metodo appartiene alla classe e non a un oggetto
specifico void indica che il metodo non restituisce alcun valore
string\[\] args è un array di stringhe che può contenere eventuali
parametri passati da riga di comando (per ora possiamo ignorarlo)
Dichiarazione della stringa Qui stiamo: 1. dichiarando una variabile di
tipo string 2. chiamandola ciao_mondo 3. assegnandole il valore
"HelloWorld" La stringa è racchiusa tra doppi apici perché rappresenta
testo, capiremo meglio più avanti le stringe. Stampa a console Questa
istruzione serve per stampare a video il contenuto della variabile
ciao_mondo. Console rappresenta la console (il terminale) WriteLine è un
metodo che stampa il testo e va a capo Il risultato dellʼesecuzione del
programma sarà: I commenti Quando scriviamo codice, non lo facciamo solo
per il computer ma anche per noi stessi e per chi leggerà il codice
dopo. I commenti servono proprio a questo: spiegare cosa sta succedendo,
senza influenzare lʼesecuzione del programma. Normalmente useremo le
shortcut dellʼeditor, ma vediamo come funzionano manualmente. Commento
per riga Il primo commento base è quello per riga. Il secondo tipo di
commenti è quello per blocco o meglio per righe multiple. Terzo e
ultimo, se volessimo scrivere della documentazione allʼinterno del
codice possiamo usare questa convenzione. 1string ciao_mondo
="HelloWorld"; 2 1Console.WriteLine(ciao_mondo); 2 1HelloWorld 2 1//
questo è un commento per riga in C# 2 1/* 2le righe di codice nel mezzo
di questi caratteri verranno ignorate 3*/ 4 1/* 2* qui posso scrivere
dei pezzi di documentazione del codice\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Tipi di dato Interi C# ha diverse rappresentazioni per i numeri interi,
sono quattro: long -- 8 bytes → -9 quintilioni a +9 quintilioni int -- 4
bytes → -2 miliardi a +2 miliardi short -- 2 bytes → -32768 a +32767
byte -- 1 byte → 0 a 255 Notazione Literals Long: Hex: Binary: Decimali
float -- 4 bytes → numeri con al max 7 cifre decimali double -- 8 bytes
→ numeri con al max 15 cifre decimali Notazione Literals Char Non è una
stringa ma è un singolo carattere. Esempio: È diverso dalla stringa che
si identifica utilizzando i doppi apici. 'a' != "a" Tips: il tipo di
dato char, quindi il singolo carattere, va racchiuso tra singoli apici.
Un solo carattere racchiuso tra doppi apici è una stringa. Booleani true
o false 3\* per poter spiegare cosa fa una certa porzione 4\*/ 5 1long
numero =4000000000L; 2 1int hex =0xCBBA; 2 1int bin
=0b0001_0100_0010_0100_0000; 2 1float f =0.5F; 2 1char c ='a'; 2\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Final (Costanti) La parola chiave const in C# viene utilizzata per
dichiarare una costante. Una volta assegnato un valore a una variabile
dichiarata come const, quel valore non può essere modificato in seguito.
In altre parole, è un modificatore che indica che la variabile è
"costante" e il suo valore rimarrà immutato durante il programma. Enum
Sta per enumerazione → insieme di valori fissi, molto simile
allʼoggetto. Solitamente definito anche come un insieme di costanti.
Operatori Matematici Gli operatori matematici come sappiamo servono per
effettuare operazioni su dati e restituirne un valore. Come operatori
abbiamo: somma "+" sottrazione "-" moltiplicazione "\*" divisione "/"
modulo → se è divisibile "%", è il resto della divisione Altri operatori
Molto spesso, quando scriviamo codice, ci capita di dover aumentare o
diminuire una variabile di una sola unità. Pensiamo ad esempio a un
contatore, a un punteggio, al numero di tentativi fatti o al numero di
giri di un ciclo. Se volessimo incrementare un numero aggiungendo un
valore: ma esiste un modo più rapido per scrivere lo stesso concetto, in
forma contratta: 1bool t =true; 2bool f =false; 3 1// è una costante
2constint num =5; 3 1constint ivaIT =22; 2Console.WriteLine("l'iva in
Italia e': "+ ivaIT); 3 1// questo è un tipo di dato 2enumSize{ Small,
Medium, Large, XL } 3 4classHelloWorld 5{ 6 staticvoidMain(string\[\]
args) 7{ 8 Size taglia = Size.Small; 9 Console.WriteLine("la taglia
selezionata è: "+ taglia); 10} 11} 12 1x = x +2; 2\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Questa istruzione significa letteralmente: prendi il valore attuale di
x, aggiungici 1 e riassegnalo di nuovo a x. Dal momento che questa
operazione è estremamente comune, il linguaggio mette a disposizione una
sintassi più compatta e più leggibile. Per incrementare di 1 una
variabile possiamo scrivere: Questa istruzione fa esattamente la stessa
cosa di x = x + 1, ma in modo più breve. È molto usata, soprattutto
allʼinterno dei cicli, perché rende il codice più pulito e immediato da
leggere. Allo stesso modo, se vogliamo diminuire di 1 il valore di una
variabile, possiamo usare: Anche in questo caso, il significato è:
Quindi possiamo riassumere dicendo che: x++ incrementa il valore di x di
1 x-- decrementa il valore di x di 1 Questa sintassi è molto utile
quando lavoriamo con contatori, indici di array o cicli, ed è una delle
prime forme di "scorciatoia" che si impara quando si inizia a
programmare. Naturalmente se abbiamo lʼincremento abbiamo anche il modo
per scrivere il decremento ed altri operatori. -= → decremento \*= →
moltiplicato /= → diviso %= → modulo Operatori di relazione Gli
operatori di relazione sono operatori che servono a confrontare due
valori tra loro. Il risultato di questo confronto non è un numero, ma un
valore booleano, quindi true oppure false. In C# li usiamo ogni volta
che dobbiamo prendere una decisione, ad esempio in un if, in un while o
in un for. 1x +=2; 2 1x++; 2 1x--; 2 1x = x -1; 2 1// a uguale b 2a ==
b; 3 1// a diverso da b 2a != b; 3\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

I principali operatori di relazione sono: == → verifica se due valori
sono uguali != → verifica se due valori sono diversi \< → verifica se un
valore è minore di un altro \> → verifica se un valore è maggiore di un
altro \<= → verifica se un valore è minore o uguale \>= → verifica se un
valore è maggiore o uguale Operatori di logica booleana Il loro
comportamento è derivato dallʼalgebra di Boole e dalle cosiddette porte
logiche, dove il valore 1 rappresenta una verità ovvero true e lo zero
rappresenta il valore di falsità false. Ne abbiamo alcune principali: or
→ \|\| and → && not → ! xor (or esclusivo) → \^ Ma andiamo a capire il
funzionamento di questi operatori e facciamo qualche esempio concreto.
OR → \|\| Lʼoperatore logico OR dà una verità se almeno una delle due
espressioni messe a confronto è vera. Esempio in codice: AND → &&
Lʼoperatore logico AND mi restituisce una verità se entrambe le
espressioni sono vere. NOT → ! Lʼoperatore logico NOT indica "non è". Se
ho un valore a true, questo sarà false. 1staticvoidMain(string\[\] args)
2{ 3 bool a =true; 4 bool b =false; 5 6 bool confrontoOR = a \|\| b; 7 8
Console.WriteLine("il risultato del confronto OR fra a e b e':"+ 9} 10
1staticvoidMain(string\[\] args) 2{ 3 bool a =true; 4 bool b =false; 5 6
bool confrontoAND = a && b; 7 8 Console.WriteLine("il risultato del
confronto AND fra a e b e':"+ 9} 10\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

XOR → \^ Lʼoperatore logico XOR detto anche OR esclusivo restituisce una
verità solo se uno dei due operatori è true. Conditional operator
(operatori ternari) Gli operatori condizionali in C#, noti anche come
operatori ternari, sono operatori speciali che ci consentono di valutare
espressioni condizionali in modo conciso. Questi operatori sono spesso
utilizzati per semplificare la scrittura di istruzioni condizionali in
una singola riga. Sono spesso utilizzati nelle istruzioni if e nelle
assegnazioni condizionali. In questo esempio, se età è maggiore o uguale
a 18, verrà restituita la stringa "Maggiorenne", altrimenti verrà
restituita la stringa "Minorenne". Conversioni di tipo In C# è possibile
trasformare un valore da un tipo ad un altro. Alcune conversioni sono
automatiche ma vanno specificate con un cast. Facciamo degli esempi.
Casting esplicito È unʼoperazione in cui si forza una variabile o
unʼespressione a diventare di un tipo specifico. Questo è fatto mettendo
il tipo tra parentesi tonde (). Il casting esplicito è spesso utilizzato
quando si vuole convertire un tipo più ampio in uno più specifico, ad
esempio da double a int. In soldoni il tipo più piccolo in quello più
grande ma non il contrario. 1staticvoidMain(string\[\] args) 2{ 3 bool a
=true; 4 bool logic_not =!a; 5 6 Console.WriteLine("il risultato del
operatore logico not su a: `\n`{=tex}"+ 7} 8 1staticvoidMain(string\[\]
args) 2{ 3 bool a =true; 4 bool b =false; 5 bool c =true; 6 bool d
=false; 7 8 bool confrontoXOR_diversi = a \^ b; 9 bool
confrontoXOR_uguali_true = a \^ c; 10 bool confrontoXOR_uguali_false = b
\^ d; 11 12 Console.WriteLine("il risultato del confronto XOR fra a e b
e':"+ 13 Console.WriteLine("il risultato del confronto XOR fra a e c
entramb 14 Console.WriteLine("il risultato del confronto XOR fra b e d
entramb 15} 16 1int eta =20; 2string messaggio =(eta
\>=18)?"Maggiorenne":"Minorenne"; 3Console.WriteLine("Sei"+ messaggio);
4 1double numeroDouble =5.67; 2int numeroIntero =(int)numeroDouble; 3\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Casting implicito Noto anche come "widening conversion" è una
conversione che avviene automaticamente quando si passa da un tipo più
piccolo a uno più grande. Ad esempio, da int a double. Non è necessario
fare nulla di speciale per eseguire un casting implicito. Attenzione
però: quando si effettua una conversione da un tipo più grande come il
double ad un integer può verificarsi una perdita di dati. Casting tra
tipi incompatibili Non tutti i tipi possono essere convertiti
direttamente in altri. Alcune conversioni potrebbero richiedere una
logica aggiuntiva. Ad esempio, se volessimo convertire una stringa in un
numero, dobbiamo utilizzare metodi di parsing specifici come int.Parse()
o double.Parse(). Questo tipo di conversione funziona solo se la stringa
contiene effettivamente un numero valido. Se la stringa contiene
caratteri non numerici, il programma lancerà unʼeccezione e andrà in
errore. Per evitare questo problema, C# mette a disposizione un metodo
più sicuro chiamato TryParse(). TryParse() prova a convertire la stringa
e restituisce un valore booleano: true se la conversione è andata a buon
fine false se la conversione non è possibile Il valore convertito viene
restituito tramite un parametro out. Esempio: 1// CONVERSIONI DI TIPO
2byte b =19; 3short x =(short)b; 4int i = x; 5long l = i; 6double d = i;
7char c ='c'; 8int cc =(int)c; 9float f =1.77f; 10double dd = f; 11 1int
numeroIntero =42; 2double numeroDouble = numeroIntero; 3 1string testo
="123"; 2int numero =int.Parse(testo); 3 1string testo ="123"; 2bool
conversioneRiuscita =int.TryParse(testo,outint numero); 3
4if(conversioneRiuscita) 5{ 6 Console.WriteLine("Conversione riuscita,
numero ="+ numero); 7} 8else 9{ 10 Console.WriteLine("Conversione
fallita, la stringa non è un numero v 11}\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

In questo caso il programma non va in errore, anche se la stringa non
contiene un numero. Questo rende TryParse() particolarmente utile quando
leggiamo dati dallʼutente o da fonti esterne, dove non abbiamo la
certezza che lʼinput sia corretto. In sintesi: Parse() è più semplice ma
può generare errori TryParse() è più sicuro ed è preferibile nei casi
reali La classe Convert In C#, la classe Convert è una classe di
supporto che serve per convertire un valore da un tipo di dato a un
altro. È molto usata quando: leggiamo dati dallʼutente lavoriamo con
input testuali riceviamo valori da file, database o servizi esterni In
pratica, Convert ci aiuta a trasformare i dati nel formato che ci serve
per lavorare nel programma. Convert è più generale e più flessibile. Il
cast funziona solo tra tipi compatibili Parse() lavora solo con le
stringhe Convert gestisce molti tipi diversi, anche tra loro molto
distanti Un esempio semplice La classe Convert contiene molti metodi
statici, tra cui: Convert.ToInt32() Convert.ToDouble()
Convert.ToBoolean() Convert.ToString() Ogni metodo prende un valore e lo
converte nel tipo desiderato. Type inference La type inference avviene
quando un linguaggio riesce autonomamente ad assegnare il tipo di dato
ad una variabile. Ricordando che in C# bisogna indicare il tipo della
variabile quando la stiamo dichiarando. Il linguaggio tuttavia è in
grado di stabilire il tipo di una variabile quando non viene indicato
staticamente dal programmatore. 12 1string testo ="123"; 2int numero =
Convert.ToInt32(testo); 1var score =0;// int di default 2var hello
="hello world";\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

String Le stringhe sono una sequenza di caratteri testuali delimitati da
doppi apici. In C# sono una sequenza di caratteri UNICODE. In C#, la
stringa non è un tipo primitivo, ma è a tutti gli effetti un oggetto.
Più precisamente, ogni stringa che utilizziamo nel codice è unʼistanza
della classe String, che fa parte del namespace System. Quando
scriviamo: in realtà stiamo facendo due cose importanti: string è solo
un alias (una scorciatoia sintattica) per System.String "ciao mondo" è
un oggetto String creato in memoria Se volessimo scriverlo in modo più
esplicito, sarebbe perfettamente equivalente a: Questo significa che le
stringhe in C#: hanno metodi (come Length, Substring, Replace, ecc.)
hanno proprietà seguono le regole degli oggetti Ed è proprio per questo
motivo che possiamo scrivere: Senza dover fare nulla di speciale. Metodi
delle e sulle stringhe Le substring Prendendo la stringa "ciao mondo"
voglio estrapolare solo i primi 5 caratteri. Conoscere il carattere ad
una posizione specifica 3 4// molto utile in situazioni come questa 5var
starShip = GameEngine.BuildStarShip(); 6// lo utilizziamo quando non
siamo certi del tipo che ci restituirà una f 7 1"ciao sono una stringa"
2 1string saluta ="ciao mondo"; 2 1System.String saluta ="ciao mondo"; 2
1Console.WriteLine(saluta.Length); 2Console.WriteLine(saluta.ToUpper());
3 1string ciao_mondo ="ciao mondo";
2Console.WriteLine(ciao_mondo.Substring(0,4)); 3 1string ciao_mondo
="ciao mondo"; 2Console.WriteLine(ciao_mondo\[0\]); 3\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Concatenazione tra stringhe Vediamo ora come concatenare le stringhe
Uguaglianza tra stringhe In C#, lʼuguaglianza tra stringhe può essere
verificata sia tramite lʼoperatore "==" sia tramite il metodo Equals().
Lʼoperatore "==" è sovraccaricato (overloaded) per il tipo string, vuol
dire che per questa tipologia di linguaggio confronta il contenuto delle
stringhe, non il riferimento in memoria. Esempio con "==" In questo caso
il risultato sarà: Anche se s1 e s2 sono due variabili distinte,
lʼoperatore == restituisce true perché confronta il contenuto testuale
delle stringhe. Esempio con Equals: StringComparison è un enum fornito
da C#. Serve per dire al metodo Equalscome deve essere effettuato il
confronto tra le stringhe. In pratica, stiamo dando al metodo una sorta
di "istruzione extra". OrdinalIgnoreCase Possiamo scomporre il nome:
Ordinal indica che il confronto viene fatto carattere per carattere,
basandosi sul valore Unicode dei caratteri, quindi è un confronto
diretto, veloce e non influenzato da regole linguistiche IgnoreCase
indica che il confronto ignora la differenza tra maiuscole e minuscole
Quindi StringComparison.OrdinalIgnoreCase significa: 1string benvenuto
="Benvenuto nel Corso di specializzazione C#"; 2string nome ="Luigi"; 3
4Console.WriteLine("Ciao ci siamo:"+ benvenuto +" "+ nome); 5 1string s1
="Hello"; 2string s2 = "Hello"; 3 4if (s1 == s2) 5{ 6
Console.WriteLine("Le stringhe sono uguali"); 7} 1Le stringhe sono
uguali 1Console.WriteLine("ciao".Equals("Ciao"));// false 2 1string
minuscolo ="messaggio"; 2string maiuscolo ="MESSAGGIO"; 3
4Console.WriteLine( 5 minuscolo.Equals(maiuscolo,
StringComparison.OrdinalIgnoreCase) 6);// true 7\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

"Confronta le stringhe carattere per carattere, ignorando il fatto che
siano maiuscole o minuscole." Ma perchè "==" non funziona correttamente
per poter vedere se due stringhe sono uguali? Perchè "Equals" fa un
controllo sui valori delle stringhe, "==" vede solo i riferimenti delle
cariabili, cioè a quale valore punta una specifica variabile (questo
concetto vi sarà chiaro più avanti quando parleremo di memoria) Le
stringhe sono immutabili Dire che una stringa è immutabile significa
che: una stringa, una volta creata, non può essere cambiata; ogni
operazione che sembra modificarla crea in realtà una nuova stringa in
memoria, nello heap (la memoria usata per gli oggetti,capiremo più
avanti cosa è). La stringa originale rimane dove si trovava, intatta.
Quello che cambia non è la stringa, ma la variabile che la stava usando.
Caratteri di escape Sono alcuni escape character, cioè sequenze speciali
che iniziano con  e che permettono di rappresentare caratteri
particolari allʼinterno delle stringhe. Ad esempio: `\n `{=tex}→ va a
capo `\t →`{=tex} tabulazione \" → virgolette doppie \\ → backslash vero
e proprio Stringa con virgolette escapate 1classProgram 2{ 3
staticvoidMain(string\[\] args) 4{ 5 // Qui creiamo una stringa con
valore"Ciao" 6 // In memoria viene creato un oggetto stringa con scritto
"Ciao 7 string testo ="Ciao"; 8 9 // In questo momento la variabile
'testo' 10 // punta alla stringa "Ciao" 11 Console.WriteLine(testo);//
Ciao 12 13 // Ora "modifichiamo" la stringa aggiungendo " mondo" 14 //
ATTENZIONE: la stringa "Ciao" NON viene modificata 15 testo = testo +"
mondo"; 16 17 // Cosa succede davvero: 18 // 1) C# crea una NUOVA
stringa in memoria con valore "Ciao mon 19 // 2) la variabile 'testo'
viene aggiornata e ora punta alla nu 20 // 3) la vecchia stringa"Ciao"
rimane in memoria, ma non viene 21 22 Console.WriteLine(testo);// Ciao
mondo 23} 24} 25 26 1// `\t \n `{=tex}\" \\ =\
2\[! https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Qui stiamo creando una stringa che contiene delle virgolette doppie al
suo interno. Normalmente le virgolette " " servono a delimitare la
stringa, quindi per scriverle dentro la stringa dobbiamo escapearle
usando \". Il risultato stampato sarà: Stringa con percorso di file ed
escape character Qui vediamo più cose insieme: \\ → serve per scrivere
un singolo  nella stringa `\n `{=tex}→ inserisce una nuova riga Quindi:
il percorso viene scritto correttamente Questa è una nuova riga viene
stampato a capo Quando questa stringa viene stampata, lʼoutput sarà
simile a: Proviamo la stampa Verbatim string (@"") In C# esiste un tipo
particolare di stringa chiamato verbatim string, riconoscibile dal
simbolo @ posto davanti alle virgolette. Le verbatim string servono
principalmente a rendere il codice più leggibile, soprattutto quando
lavoriamo con percorsi di file o testi che contengono molti backslash.
Normalmente, allʼinterno di una stringa, il carattere  ha un significato
speciale e deve essere "escapato" scrivendo \\. Con le verbatim string
questo non è necessario, perché il backslash viene interpretato così
comʼè, senza significati speciali. Per questo motivo, una stringa come:
1string speech ="Ciao \"Studente c#!\""; 2 1Ciao "Studente c#!" 2
1string path ="C:\\Users\\Pluto\\Desktop\\Specializzazione
c#`\n `{=tex}Questa è 2
1C:`\Users`{=tex}`\Pluto`{=tex}`\Desktop`{=tex}`\Specializzazione `{=tex}c#
2Questa è una nuova riga 1Console.WriteLine(path);
2Console.WriteLine(speech); 3 1path
=@"C:`\Users`{=tex}`\Pluto`{=tex}`\Desktop`{=tex}`\Specializzazione `{=tex}c#"+"`\nQuesta `{=tex}è
una n 2
1@"C:`\Users`{=tex}`\Pluto`{=tex}`\Desktop`{=tex}`\Specializzazione `{=tex}c#"
2\[! https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

risulta molto più chiara e naturale da leggere rispetto alla versione
con gli escape. In questo esempio specifico: la prima parte della
stringa è una verbatim string, usata per il percorso la seconda parte è
una stringa normale che utilizza `\n `{=tex}per andare a capo Le due
stringhe vengono poi concatenate insieme. Stampando il valore di path,
otteniamo lo stesso risultato visivo visto in precedenza, ma con un
codice più pulito e leggibile. Le verbatim string sono uno strumento
molto utile in C# quando vogliamo: evitare lʼuso ripetuto di \\ scrivere
percorsi di file in modo più chiaro migliorare la leggibilità del codice
senza cambiarne il comportamento Verbatim string con virgolette doppie
Qui vediamo una regola importante delle verbatim string: per scrivere
una virgoletta " bisogna raddoppiarla ("") Questa stringa produrrà:
Stringa normale con apici singoli Qui vediamo che: gli apici singoli '
non hanno nessun significato speciale nelle stringhe quindi possono
essere usati liberamente senza escape È il modo più semplice se non
servono virgolette doppie. String formatting in C# Lo string formatting
è un modo per inserire valori (variabili) allʼinterno di una stringa
senza dover concatenare tutto a mano con il simbolo +. Serve a: rendere
il codice più leggibile evitare stringhe lunghe e difficili da capire
separare il testo dai valori vediamo un esempio:
1Console.WriteLine(path); 2 1string name =@"Hello ""someone""";
2Console.WriteLine(name); 1Hello"someone" 2 1name ="Hello 'someone'";
2Console.WriteLine(name);\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Qui succedono alcune cose importanti. Le parentesi graffe {} Allʼinterno
della stringa troviamo: Questi non sono valori reali, ma segnaposto
(placeholder). {0} indica: "qui andrà il primo valore" {1} indica: "qui
andrà il secondo valore" I valori reali vengono passati dopo la stringa,
separati da virgole: Quindi: {0} viene sostituito con name {1} viene
sostituito con age Come viene costruita la stringa finale? Se: Questo
codice: produrrà: Vediamo un altro esempio Qui cʼè una cosa in più:
`\n `{=tex}→ va a capo Il risultato sarà: Perché usare lo string
formatting? Se vedessimo un codice equivalente che non possiede lo
string formatting 1Console.WriteLine("Your name is {0}, and your age is
{1}", name, age); 2 1{0}{1} 2 1name, age 2 1string name ="Andrea"; 2int
age =30; 3 1Console.WriteLine("Your name is {0}, and your age is {1}",
name, age); 2 1Your name isAndrea,and your age is30 2
1Console.WriteLine("Name: {0}`\nAge`{=tex}: {1}", name, age); 2 1Name:
Andrea 2Age: 30 3 1Console.WriteLine("Name:"+ name +"`\nAge`{=tex}:"+
age);\[! https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

il codice funziona, ma: è più lungo è meno leggibile diventa
confusionario con tante variabili Lo string formatting, invece: mantiene
il testo compatto rende chiaro dove va ogni valore è più ordinato Ti
spiego la String Interpolation in C# in modo discorsivo, semplice e
graduale, come se fossi uno studente alle prime armi, partendo
esattamente dal codice che vedi nellʼimmagine. String interpolation in
C# La string interpolation è un modo moderno e molto leggibile per
inserire il valore delle variabili direttamente dentro una stringa,
senza usare il simbolo + e senza i segnaposto {0}, {1}. È uno dei modi
più chiari e intuitivi per costruire stringhe in C#. partiamo da un
esempio Il simbolo \$ La prima cosa da notare è il simbolo \$ davanti
alla stringa. Il \$ dice a C#: "Questa stringa contiene delle variabili
che devono essere valutate." Senza il
$, il contenuto tra {} verrebbe trattato come semplice testo. Le parentesi graffe {} Allʼinterno della stringa vediamo: Queste parentesi indicano a C# dove inserire il valore delle variabili. È come dire: “qui metti il valore di name” “qui metti il valore di age” 2 1string name ="Andrea"; 2int age =30; 3Console.WriteLine($"Your
name is {name} and your age is {age}"); 4 1\$"..." 2 1{name} 2{age} 3\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Non servono indici ({0}, {1}), perché usiamo direttamente il nome della
variabile. Come viene costruita la stringa finale Se abbiamo: Questa
riga: produrrà: Rispetto ad altri modi, la string interpolation è: più
leggibile più naturale molto simile a come scriviamo una frase in
italiano o in inglese Confronto: Confrontiamo i tre metodi visti per
creare stringhe "dinamiche" Concatenazione String formatting String
interpolation Lʼultimo è quello che si legge meglio. Un vantaggio
importante Con la string interpolation possiamo: inserire variabili
inserire espressioni fare calcoli al volo Esempio: METODI COMUNI DELLE
STRINGHE 1string name ="Andrea"; 2int age =30; 3
1Console.WriteLine($"Your name is {name} and your age is {age}"); 2 1Your name is Andrea and your age is 30 2 1"Your name is "+ name +" and your age is "+ age 2 1"Your name is {0} and your age is {1}", name, age 2 1$"Your
name is {name} and your age is {age}" 2 1Console.WriteLine(\$"Next year
you will be {age +1} years old"); 2 1string name ="Andrea"; 2 3//
confronto tra stringhe\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Gli statement di controllo di flusso Rivediamo velocemente i controlli
di flusso, cioè quegli strumenti che ci permettono di decidere come e
quando viene eseguito il codice in base a delle condizioni. if if else
else if 4// restituisce true se le due stringhe sono identiche
(case-sensitive) 5name.Equals("Andrea"); 6 7// confronto tra stringhe
ignorando maiuscole e minuscole 8// in questo caso "Andrea" e "AndRea"
vengono considerate uguali 9name.Equals("AndRea",
StringComparison.OrdinalIgnoreCase); 10 11// proprietà della stringa
12// restituisce il numero di caratteri della stringa 13name.Length; 14
15// accesso a un singolo carattere della stringa 16// restituisce il
carattere in posizione 2 (si parte sempre da 0) 17name\[2\]; 18 19//
ricerca 20// restituisce l'indice della prima occorrenza del carattere
'd' 21name.IndexOf('d'); 22 23// restituisce l'indice dell'ultima
occorrenza del carattere 'a' 24name.LastIndexOf('a'); 25 26// controlli
corretti sulle stringhe 27// restituisce true se la stringa è null
oppure vuota ("") 28string.IsNullOrEmpty(name); 29 30// restituisce true
se la stringa è null, vuota o contiene solo spazi
31string.IsNullOrWhiteSpace(name); 32 33// pulizia della stringa 34//
rimuove gli spazi all'inizio e alla fine della stringa 35name.Trim(); 36
37// sostituzione di caratteri 38// sostituisce tutte le occorrenze di
'b' con 'w' 39// restituisce una nuova stringa (la stringa originale non
cambia) 40name.Replace('b','w'); 41 1int cleverPoints =6;
2if(cleverPoints \>=5) 3{ 4 Console.WriteLine("puoi hackerare il
terminale"); 5} 6 1int eta =16; 2if(eta \>=18) 3{ 4
Console.WriteLine("Sei maggiorenne"); 5} 6else 7{ 8
Console.WriteLine("Sei minorenne"); 9} 10 1int voto =75; 2 3if(voto
\>=90) 4{ 5 Console.WriteLine("Eccellente"); 6} 7elseif(voto \>=80)
8{\[! https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

switch I cicli Passiamo ai cicli, strumenti fondamentali della
programmazione che ci permettono di ripetere lʼesecuzione di un blocco
di codice più volte, in base a una condizione o a un numero di
iterazioni stabilito while do while for foreach 9
Console.WriteLine("Buono"); 10} 11elseif(voto \>=70) 12{ 13
Console.WriteLine("Sufficiente"); 14} 15else 16{ 17
Console.WriteLine("Insufficiente"); 18} 19 1int giorno =3; 2string
nomeGiorno; 3 4switch(giorno) 5{ 6 case1: 7 nomeGiorno ="Lunedì"; 8
break; 9 case2: 10 nomeGiorno ="Martedì"; 11 break; 12 case3: 13
nomeGiorno ="Mercoledì"; 14 break; 15 default: 16 nomeGiorno ="Altro
giorno"; 17 break; 18} 19 20Console.WriteLine("Oggi è"+ nomeGiorno); 21
1int contatore =0; 2while(contatore \<5) 3{ 4
Console.WriteLine("Iterazione"+ contatore); 5 contatore++; 6} 7 1int
contatore =0; 2do 3{ 4 Console.WriteLine("Iterazione"+ contatore); 5
contatore++; 6} 7while(contatore \<5); 8 1for(int i =0; i \<20; i++) 2{
3 Console.WriteLine("Giro numero"+ i); 4} 5 1string\[\] nomi
={"Fallout","Starfield","The Elder Scroll","Doom"}; 2 3foreach(string
nome in nomi)\[! https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT
oUSkC- VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

break l break è una parola chiave che permette di interrompere
immediatamente lʼesecuzione di un ciclo o di uno switch, facendo uscire
dal blocco anche se la condizione non è ancora terminata. continue Il
continue è una parola chiave che permette di saltare lʼiterazione
corrente di un ciclo e passare direttamente a quella successiva, senza
interrompere completamente il ciclo. Gli Array Gli array sono strutture
dati fondamentali in C# e in molti altri linguaggi di programmazione.
Contengono un insieme di valori dello stesso tipo e sono utili per
memorizzare dati in modo organizzato. Un array è una sequenza ordinata
di elementi dello stesso tipo, ordinato poichè ogni elemento in un array
è identificato da un indice, che rappresenta la sua posizione
nellʼarray. Gli indici degli array iniziano sempre da zero. Gli array
sono utilizzati per memorizzare una raccolta di dati simili, come
numeri, stringhe o oggetti, allʼinterno di una sola variabile. Creazione
di un array Per creare un array in C#, è necessario dichiararlo
specificando: il tipo degli elementi la dimensione dellʼarray Ad
esempio, per creare un array di interi con 5 elementi: In questo caso:
lʼarray può contenere 5 numeri interi i valori iniziali saranno 0
(valore di default per int) 4{ 5 Console.WriteLine("Nome:"+ nome); 6} 7
1for(int i =0; i \<10; i++) 2{ 3 if(i ==5) 4 break; 5 6
Console.WriteLine(i); 7} 8 1for(int i =0; i \<10; i++) 2{ 3 if(i ==5) 4
continue; 5 6 Console.WriteLine(i); 7} 8 1// Dichiarazione di un array
di interi con 5 elementi 2int\[\] numeri =newint\[5\]; 3\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Inizializzazione diretta con valori In alternativa, possiamo
inizializzare direttamente lʼarray con dei valori: Qui: la dimensione
dellʼarray viene dedotta automaticamente gli elementi vengono inseriti
nellʼordine indicato Accesso agli elementi di un array Per accedere a un
elemento dellʼarray utilizziamo lʼindice. Ricordiamo che: il primo
elemento è in posizione 0 numeri\[2\] indica il terzo elemento Stampa di
un array In C#, per stampare un array in modo leggibile, possiamo usare
la classe string con Join, oppure la classe Array con i suoi metodi
utili, come ad esempio il metodo ForEach della classe, oppure usando
semplicemente i cicli. Un metodo molto semplice e veloce è con il join:
Questo converte lʼarray in una stringa separando gli elementi con una
virgola. Esempio completo Output: Array nidificati (array di array) Un
array può contenere al suo interno altri array. 1// Inizializzazione di
un array di interi con valori 2int\[\] numeri ={1,2,3,4,5}; 3 1int
terzoElemento = numeri\[2\];// Accesso al terzo elemento (indice 2) 2
1Console.WriteLine(string.Join(",", numeri)); 2
1classArrayPrintingExample 2{ 3 staticvoidMain(string\[\] args) 4{ 5 //
esempio con un array di interi 6 int\[\] intArray ={1,2,3,4,5}; 7
Console.WriteLine(string.Join(",", intArray)); 8 9 // esempio con un
array di stringhe 10 string\[\] strArray ={"John","Mary","Bob"}; 11
Console.WriteLine(string.Join(",", strArray)); 12} 13} 14 11, 2, 3, 4, 5
2John, Mary, Bob 3 1string\[\]\[\] deepArray =\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Qui abbiamo: un array principale ogni elemento è a sua volta un array di
stringhe Stampa di array nidificati Se proviamo a stampare direttamente
un array nidificato con string.Join, non otteniamo un risultato utile.
Per questo motivo, in C# si usa spesso una stampa manuale o cicli
foreach. Esempio semplice: Output: Questo approccio "scava" negli array
interni e permette di visualizzare correttamente i dati. Metodi e
proprietà degli array Length Restituisce la lunghezza dellʼarray.
Attenzione però, Length è una proprietà, non un metodo (niente
parentesi) della classe Array, ma una proprietà dellʼarray. Copy In C#,
per copiare un array utilizziamo Array.Copy. Fill Assegna un valore
specifico a tutti gli elementi dellʼarray. Sort 2{ 3
newstring\[\]{"John","Mary"}, 4 newstring\[\]{"Alice","Bob"} 5}; 6
1foreach(var innerArray in deepArray) 2{ 3
Console.WriteLine(string.Join(",", innerArray)); 4} 5 1John, Mary
2Alice, Bob 3 1int\[\] numeri ={1,2,3,4,5}; 2int lunghezza =
numeri.Length;// lunghezza è 5 3 1int\[\] vecchioArray ={1,2,3};
2int\[\] nuovoArray =newint\[5\]; 3 4Array.Copy(vecchioArray,
nuovoArray, vecchioArray.Length); 5// nuovoArray → \[1, 2, 3, 0, 0\] 6
1int\[\] numeri =newint\[5\]; 2Array.Fill(numeri,7); 3// numeri → \[7,
7, 7, 7, 7\] 4\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Ordina gli elementi dellʼarray. Conversione in stringa Uguaglianza tra
array SequenceEqual In C#, due array non sono uguali solo perché
contengono gli stessi valori. Dobbiamo confrontarli elemento per
elemento. SequenceEqual confronta: lunghezza contenuto ordine degli
elementi Array.Reverse() Array.Reverse() è utile per invertire lʼordine
degli elementi di un array. Esempio Attenzione però,
Array.Reverse()modifica direttamente lʼarray originale, non ne crea uno
nuovo. Array.Clear() Array.Clear() è utile per azzerare una parte o
tutto lʼarray, impostando gli elementi al valore di default del tipo.
Esempio 1int\[\] numeri ={5,2,8,1,4}; 2Array.Sort(numeri); 3// numeri →
\[1, 2, 4, 5, 8\] 4 1int\[\] numeri ={1,2,3,4,5}; 2string arrayStringa
=string.Join(",", numeri); 3// "1, 2, 3, 4, 5" 4 1classHelloWorld 2{ 3
staticvoidMain(string\[\] args) 4{ 5 // dichiarazione del primo array 6
int\[\] arr ={10,20,30}; 7 8 // creazione di una copia 9 int\[\] copy
=newint\[arr.Length\]; 10 Array.Copy(arr, copy, arr.Length); 11 12 //
verifica dell'uguaglianza 13 bool sonoUguali = arr.SequenceEqual(copy);
14 15 Console.WriteLine("gli array sono uguali? risposta"+ sonoUgua 16}
17} 18 1int\[\] numeri ={1,2,3,4,5}; 2 3// Invertiamo l'ordine degli
elementi dell'array 4Array.Reverse(numeri); 5 6// Stampiamo il risultato
7Console.WriteLine(string.Join(",", numeri)); 8\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]

Esempio di azzeramento parziale Array.IndexOf() Array.IndexOf() è utile
per trovare la posizione (indice) di un elemento allʼinterno dellʼarray.
Esempio Caso in cui lʼelemento NON esiste Se IndexOf restituisce -1,
significa che lʼelemento non è presente nellʼarray. Questi sono alcuni
dei metodi che possiamo utilizzare, la classe Array ne possiede degli
altri come ForEach LastIndexOf Exists Find FindAll FindIndex Resize
BinarySearch (Da far provare in autonomia agli studenti) 1int\[\] numeri
={10,20,30,40,50}; 2 3// Azzeriamo tutti gli elementi dell'array
4Array.Clear(numeri,0, numeri.Length); 5 6// Stampiamo il risultato
7Console.WriteLine(string.Join(",", numeri)); 8 1int\[\] numeri = { 10,
20, 30, 40, 50 }; 2 3// Azzeriamo solo i primi 3 elementi
4Array.Clear(numeri, 0, 3); 5 6Console.WriteLine(string.Join(",",
numeri)); 7 1int\[\] numeri = { 3, 5, 7, 5, 9 }; 2 3// Cerchiamo il
valore 5 nell'array 4int indice = Array.IndexOf(numeri, 5); 5
6Console.WriteLine(indice); 7 1int indice = Array.IndexOf(numeri, 100);
2Console.WriteLine(indice); 3\[!
https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT oUSkC-
VWcC2rQW1QLZJqzq2zIp0dgfaxT aQ&s \]
