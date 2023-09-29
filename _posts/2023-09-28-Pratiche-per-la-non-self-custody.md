---
title: Pratiche per la self-(non)custody
author: FiliTol
date: 2023-09-28 00:00:00
categories: [Guida, Bitcoin, Wallet, Self-custody, Satoshi]
tags: Guida
img_path: /assets/img/
---

## Introduzione

Custodire in sicurezza i propri <a href="https://en.bitcoin.it/wiki/Satoshi_(unit)" target="_blank">satoshi</a> è difficile?

No! Non è mai stato così facile e lo sarà sempre di più.

Centinaia di guide ormai hanno elaborato e sviscerato tutti gli aspetti della *self-custody*, esistono numerosissime soluzioni per prendere autonomamente i propri fondi in custodia, alcune più difficili altre più elaborate e dedicate ai più esperti.
Il minimo comun denominatore di queste guide è uno solo: **non perdere i propri satoshi, né per negligenza né a causa di fattori esogeni**.

L'esperimento mentale che si propone in questo articolo è di <a href="https://en.wikipedia.org/wiki/Perspective-taking" target="_blank">perspective taking</a>, un modo per cambiare prospettiva, 'guardare il mondo sottosopra' e cercare di capire quali sono i **migliori modi per perdere tutti i propri satoshi** (se possibile in pochissimo tempo). 

Certo, sembra un compito facile...tuttavia può essere molto utile per comprendere ancora meglio le **vere** prassi per la self-custody (quelle per difendere i satoshi, non per perderli!).

## 7 modi per perdere tutti i propri satoshi

### Metodi sicuri

I 'metodi sicuri' per perdere i propri satoshi sono quelle strategie che assicurano la perdita dei fondi in un intervallo di tempo relativamente breve. **Sono i metodi migliori per perdere tutto**.

<img src="ma-sei-sicuro.jpg" alt="Sicuro di essere sicuro?" width="400" height="500">

#### 1 - Indirizzi di Burn

Il modo migliore per *polverizzare* in pochissimo tempo tutti i propri satoshi è inviarli ad un <a href="https://bitcointalk.org/index.php?topic=5123840.0" target="_blank">indirizzo di burn</a>. Un indirizzo di burn è un indirizzo **impossibile da spendere** poichè nessuno dispone della chiave privata corrispondente. Fanno parte di questa categoria alcuni <a href="https://en.bitcoin.it/wiki/Vanitygen" target="_blank">vanity address</a> come `1CounterpartyXXXXXXXXXXXXXXXUWLpVr`, l'indirizzo di burn utilizzato dal protocollo Counterparty, oppure `venicexxxxxxxxxxxxxxxxxxxxy2p66hQ` un address creato da noi grazie a <a href="https://gobittest.appspot.com/ProofOfBurn" target="_blank">questo tool</a>.

Di fatto, inviare dei satoshi ad un indirizzo di burn significa **bruciarli** per sempre. Come recita un detto:

> Thank you for the deflation!

#### 2 - Brain wallet

Ventiquattro parole non sono poi così difficili da ricordare, soprattutto in condizioni di estrema necessità. Ma se si facesse il contrario? Se si cercasse di **generare** il **seed** sulla base di alcune parole/frasi **facilmente ricordabili**?

Questo 'stratagemma' è possibile ed è già stato utilizzato in passato diverse volte, tuttavia esso spezza il modello di **sicurezza della crittografia a due chiavi** su cui il protocollo Bitcoin si basa.

L'assunzione alla base della crittografia a due chiavi è che sia **impossibile** effettuare l'inversa della moltiplicazione sulla curva ellittica. Ciò è valido poichè il uno tra i fattori della moltiplicazione è sconosciuto (la chiave privata) e l'unico modo per ricavarlo è di cercare di **indovinarlo** all'interno dell'intervallo [0, 2^256].

Raccomandiamo di dare un'occhiata a <a href="https://youtu.be/S9JGmA5_unY?feature=shared" target="_blank">questo video</a> per comprendere l'effettiva grandezza di questo intervallo, per lo scopo di questo articolo basti sapere che questo numero è approssimabile al **numero di atomi contenuti nell'universo conosciuto**. Ciò implica che l'unico modo per recuperare una specifica chiave privata sia di **provarle tutte**.

> In altre parole, è (praticamente) impossibile ricavare una chiave privata a partire da una chiave pubblica.
{: .prompt-info }

 <img src="guess.gif" alt="I'll tell you if you guess" width="400" height="500"> 

Recuperando il concetto di **brain wallet**, si può ora comprendere come una **combinazione nota** di lettere e numeri sia una **pessima fonte di rumore casuale**; da ciò quindi ne consegue che una mnemonica generata a partire da una fonte simile sia **facilmente indovinabile**.

Il massiccio utilizzo dei **brain wallet** nel corso degli anni è documentato in <a href="https://discovery.ucl.ac.uk/id/eprint/10154816/" target="_blank">questo paper</a>; esistono anche numerosi tool online che permettono il <a href="https://it.wikipedia.org/wiki/Cracking_(informatica)" target="_blank">cracking</a> di brain wallet, come <a href="https://github.com/ryancdotorg/brainflayer" target="_blank">questo</a>. E disponbile online addirittura un <a href="https://privatekeys.pw/brainwallet/bitcoin/1" target="_blank">database completo di tutti i brain wallet craccati ad oggi</a>.

In conclusione, utilizzare un brain wallet è un ottimo modo per avere una chiave privata **poco sicura** (poco privata!), esporre i nostri fondi su un database online e di farsi **rubare** tutti i satoshi. 

Geniale, no?

#### 3 - Memorizzare la mnemonica senza backup

Questa strategia è molto facile da comprendere e si basa sull'**inaffidabilità** del **cervello umano** nel conservare informazioni dettagliate nel **lungo periodo**.

Una **mnemonica** è generalmente composta da **12, 18 o 24 parole**, in alcuni casi ci si spinge fino a 25 parole con l'utilizzo di una <a href="https://en.bitcoin.it/wiki/Seed_phrase#Two-factor_seed_phrases" target="_blank">passphrase</a>; è importante inoltre ricordare che anche l'**ordine delle parole** è rilevante.
Di certo, per un breve periodo di tempo, un simile numero di parole può essere facile da ricordare; tuttavia il cervello umano è **inaffidabile** per simili compiti, soprattutto se il contovalore di satoshi custodito dalla mnemonica è elevato (per lo meno gli autori non si fiderebbero del proprio cervello!).

Per supplire alle mancanze del cervello umano, si è sviluppata la **prassi** di conservare un **backup** della mnemonica su un **supporto fisico**, il che alleggerisce il compito di memorizzazione oltre che trasformare il problema della custodia da **'problema di memorizzazione'** a 'problema di sicurezza fisica', ovvero il problema di **dove nascondere il backup**.

Non possedere un backup nella propria mnemonica può essere una bella sfida, ma può diventare un **incubo per la sicurezza dei fondi** nel lungo termine.

 <img src="no_backup.gif" alt="No backup plan" width="400" height="500"> 

### Metodi (quasi) sicuri per perdere tutti i propri satoshi

I metodi (quasi) sicuri per perdere i propri satoshi sono quelle strategie che **potenzialmente** permettono di **perdere l'accesso ai fondi** in un'intervallo di tempo più o meno variabile. La perdita non sarà quindi immediata poichè alcuni eventi sono più probabili di altri.

Poco male, la pazienza è la virtù dei forti :-)

#### 4 - Mnemonica su carta

Memorizzare la mnemonica e non tenere alcuna copia del backup è uno tra i **metodi sicuri** per perdere i fondi, per questo motivo la prassi più consolidata è quella di **effettuare il backup su un supporto fisico**, per esempio trascrivendo la mnemonica su un **foglio di carta**.

I latini stessi suggeriscono questa prassi con il loro:

> Verba volant, scripta manent

ma è necessario aggiungere che più **solido** è il supporto su cui si effettua il backup della mnemonica, più si abbatte la probabilità che **eventi naturali** possano rovinare il foglio di carta. 

Più la *scripta* è resistente, più il contenuto *manent*.

 <img src="ahahaha.gif" alt="Ahahaha" width="300" height="300"> 

Dalla tazza di caffè sul tavolo all'**alluvione**, dal cortocircuito della stufetta all'**incendio** boschivo, tutto potrebbe **minacciare** il nostro patrimonio di satoshi se il nostro unico backup rimane annotato su un semplice foglio di **carta**.

A questo proposito quindi, le prassi di custodia più *avanzate* prescrivono di utilizzare per il backup dei **supporti metallici**, o almeno **plastificare** il foglio di carta; consigliamo di consultare la lista di supporti metallici e le rispettive recensioni a <a href="https://jlopp.github.io/metal-bitcoin-storage-reviews/" target="_blank">questo link</a>, mantenuta da Jameson Lopp, un esperto di sicurezza informatica.

Come ci testimoniano gli ultimi eventi di cronaca, un'alluvione non è così improbabile, come anche altri <a href="https://it.wikipedia.org/wiki/Teoria_del_cigno_nero" target="_blank">**cigni neri**</a> naturali. Quindi, per perdere (quasi) sicuramente i propri satoshi basta semplicemente **maneggiare** la propria **mnemonica** quando si è nella **vasca da bagno**, durante una <a href="https://www.urbandictionary.com/define.php?term=Boating%20accident" target="_blank">**gita in barca**</a> o semplicemente mentre si beve una bella **tazza di caffè**.

 <img src="coffee.gif" alt="Coffee on the desk" width="400" height="400"> 

#### 5 - Schema di backup

Con riferimento alla custodia di bitcoin e cryptoasset, uno schema di backup è il sistema secondo il quale un individuo ha **organizzato la conservazione dei propri fondi**, incluso il **backup della mnemonica** e l'eventuale collocazione di **hardware wallet** o **software wallet**. Ogni individuo necessita di uno schema di backup personalizzato basato sulla propria **propensione al rischio**, al controvalore che possiede ed alle capacità tecniche.

In questo senso, la minaccia più grande è la **convinzione di avere uno schema perfetto, inviolabile e sicurissimo**.
Il percorso di sovranità individuale che si affonta quando si decide di prendere custodia dei propri satoshi non finisce dopo aver creato un backup fisico della mnemonica, ma continua anche in seguito. E' necessario infatti decidere dove collocare il backup, quante copie del backup effettuare ecc. 

Ed è fondamentale **non strafare**: inutile inventarsi **strani nascondigli**, passphrase impossibili da ricordare ed altri **stratagemmi insoliti**, poichè questo aumenterà solo la **difficoltà** nel recuperare i fondi in caso di necessità

Infine a cose fatte è necessario...

...**testarlo a cadenza regolare!!**

Tornando ai metodi (quasi) sicuri per perdere tutti i propri satoshi è evidente quindi come:

- creare uno schema di custodia **complicato**,
- nascondere il backup in **posti improbabili**,
- **non testare** mai il backup,

siano gli addendi perfetti per il risultato che si va cercando con questo articolo, cioè dei **satoshi persi per sempre**.

<img src="wiped_out.gif" alt="Wiped out" width="400" height="400">

#### 6 - Scambio di indirizzi

Molto spesso si attinge ai propri satoshi utilizzando dei **software wallet**, che siano mobile o desktop. Molto spesso i software wallet sono anche **hot wallet**, nel senso che essi operano su un hardware costantemente a **contatto con la rete internet**, esponendo il wallet ad una grande superficie di possibili attacchi.

Una tra le minacce maggiori è rappresentata dai cosiddetti <a href="https://bitcoin.org/it/wallets/desktop/windows/?platform=windows&step=5" target="_blank">malware clipper</a>, cioè dei malware che sorvegliano la **clipboard** del dispositivo (la cronologia di **copia-incolla**) alla ricerca di **indirizzi bitcoin**. Un malware simile è in grado di **sostituire l'indirizzo** in clipboard con un indirizzo dell'**hacker**.

Prevenire un'attacco simile è semplice, è sufficiente **ricontrollare** attentamente l'indirizzo del destinatario prima di **confermare** la transazione.

Se il lettore è un utilizzatore del sistema operativo <a href="https://nonciclopedia.org/wiki/Windows" target="_blank">winzo</a>...ops, **Windows**, naviga costantemente su **siti poco raccomandabili** per guardare film in streaming e sullo stesso dispositivo possiede anche un **wallet bitcoin**...beh, ha già tutti gli strumenti per essere **vittima** di questo attacco.

 <img src="winzoz.gif" alt="Windows error" width="400" height="400"> 

#### 7 - Eredità

> Cosa non ha dissolto dunque il tempo
che disperde ogni cosa? 
L'età dei nostri padri,
che fu peggiore di quella degli avi,
ha partorito in noi figli ancora più inetti:
noi che daremo a nostra volta vita
a discendenti sempre più corrotti...

Così scrive Orazio (Odi, III, 6) e questo passo delle Odi ricorda parte di un aforisma molto noto nella comunità Bitcoin (<a href="https://www.goodreads.com/quotes/8751435-hard-times-create-strong-men-strong-men-create-good-times" target="_blank">e non solo</a>).

L'**immortalità** del protocollo Bitcoin non è assicurata, ma ogni blocco ne conferma la capacità di **sopravvivenza**.
Appurato quindi che il protocollo (probabilmente) resisterà alla **prova del tempo**, è necessario che anche i propri satoshi facciano altrettanto.

Il modo migliore per permettere ai propri satoshi di resistere negli anni, anche per orizzonti temporali decennali o centenari, è **educare** i propri cari ed i propri **eredi**. Dare loro gli strumenti per **accedere ai fondi** e saperli **gestire** è fondamentale per evitare che vadano persi per sempre.

Il tema dell'**eredità dei criptoasset** è affrontato in modo approfondito nel libro *'Cryptoasset Inheritance Planning: a simple guide for owners'* (Morgan P., Antonopoulos A.M.), il quale, oltre che essere fuori dalla nostra portata, contraddice anche il maldestro obiettivo di questo articolo.

 <img src="inheritance.png" alt="Inheritance" width="400" height="400"> 

## Conclusioni

Le prime strategie presentate si sono dimostrate facili ed efficaci: in pochi secondi si **perde** veramente **tutto il proprio patrimonio!** Tuttavia con il susseguirsi dei paragrafi le tecniche si sono fatte più complicate ed il risultato sempre più improbabile...d'altronde non tutti sono così accorti dall'andare in **gita al lago** con la propria **mnemonica** in **tasca**!

Da ultimo si è presentata una strategia davvero lungimirante già proposta in un <a href="https://darthcoin.substack.com/p/darth-bitcoins-after-death" target="_blank">altro articolo recuperabile online</a>, nel quale le intenzioni dell'autore sembrano ben più evidenti: *«Roba mia, vientene con me!»*.

Nel corso di questo nostro articolo sono stati presentati, tra le righe, anche **consigli utili** per comprendere come avvicinarsi al mondo della **self-custody** e come prendere **responsabilmente** possesso dei propri fondi. Non vorremmo avervi confuso troppo, ma incidentalmente vi abbiamo spiegato anche alcuni tra i principi per una **corretta custodia dei propri satoshi**!

Il che non era l'obiettivo di questo articolo, ma sicuramente è l'**obiettivo di ogni bitcoiner**.


