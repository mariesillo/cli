---
copyright:

  years: 2018

lastupdated: "2018-06-21"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}  
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}  

# Configurazione della CLI {{site.data.keyword.dev_cli_notm}}
{: #add-cli}

La CLI {{site.data.keyword.dev_cli_short}} è un approccio della riga di comando per la creazione, lo sviluppo e la distribuzione delle applicazioni per gli sviluppatori che desiderano utilizzare una riga di comando per sviluppare le applicazioni web end-to-end, mobile e del microservizio. Inizia rapidamente a lavorare con l'insieme di strumenti consigliato eseguendo uno di questi script.
{: shortdesc}

## Prerequisiti per {{site.data.keyword.dev_cli_notm}}
{: #prereq}

Registrati per [{{site.data.keyword.Bluemix_notm}}](http://ibm.biz/ibm-registration).

*  Se stai utilizzando Microsoft Windows&trade;, devi utilizzare Windows 10 o successivi.

* Devi utilizzare il canale stabile per Docker, con una versione minima di 1.13.1.

## Come installare {{site.data.keyword.dev_cli_notm}}
{: #installation}

Per installare l'insieme di strumenti, puoi eseguire il comando pertinente per avviare il programma di installazione. Questo installa i seguenti strumenti consigliati per lo sviluppo {{site.data.keyword.Bluemix_notm}} (se non sono già installati): `Homebrew` (solo Mac), `Git`, `Docker`, `Helm`, `kubectl`, `curl`, CLI {{site.data.keyword.Bluemix_notm}}, plugin {{site.data.keyword.dev_cli_notm}}, plugin Cloud Functions, plugin Container Registry, plugin Container Service e plugin `sdk-gen`. Per installare, utilizza questa procedura di installazione:

**Mac e Linux:**

```
curl -sL https://ibm.biz/idt-installer | bash
```
{: codeblock}


**Windows 10:**

* Nota: apri Windows PowerShell facendo clic con il tasto destro sull'icona PowerShell e selezionando "Run as Administrator".

```
Set-ExecutionPolicy Unrestricted; iex(New-Object Net.WebClient).DownloadString('http://ibm.biz/idt-win-installer')
```
{: codeblock}

## Verifica l'installazione
Per verificare l'installazione, esegui il comando `help`:

```
ibmcloud dev help
```
{: codeblock}

Se l'installazione ha avuto esito positivo, l'output dovrebbe elencare le istruzioni di utilizzo, la versione corrente e i comandi supportati.

La sezione [Reinstallazione degli strumenti](/docs/troubleshoot/ts_createapps.html#appendix) contiene informazioni per installare singolarmente tutte le dipendenze.

## Configura il tuo ambiente
{: #configure-environment}

1. Stabilisci una connessione a un endpoint API nella tua regione {{site.data.keyword.Bluemix_notm}}. Ad esempio, immetti il seguente comando per stabilire una connessione alla regione Stati Uniti Sud {{site.data.keyword.Bluemix_notm}}:

	```
	ibmcloud api https://api.ng.bluemix.net
	```
	{: codeblock}

2. Accedi a {{site.data.keyword.Bluemix_notm}} con il tuo ID IBM.

	```
	ibmcloud login
	```
	{: codeblock}

	**Nota:** se le tue credenziali vengono rifiutate, puoi utilizzare un ID federato. Segui questa procedura per l'autenticazione utilizzando l'ID federato.

	1. Accedi a [{{site.data.keyword.iamshort}} ![Icona link esterno](../../icons/launch-glyph.svg "Icona link esterno")](https://www.bluemix.net/iam/#/apikeys){: new_window}.
	2. Seleziona **Crea chiave API**.
		* Immetti un nome e una descrizione per apiKey
	3. Scarica la tua apiKey.
	4. Apri il file e copia il valore dal campo `apiKey`.
	5. Accedi utilizzando il seguente comando:

		```
		ibmcloud login --apikey <value>
		```
		{: codeblock}

3. Imposta la tua ORGANIZZAZIONE e SPAZIO utilizzando:

	```
	ibmcloud target -o <value> -s <value>
	```
	{: codeblock}

## Ulteriori informazioni
{: #learn}

Ora che hai installato la tua CLI {{site.data.keyword.dev_cli_short}}, puoi imparare come essere efficace con questo potente strumento:
- [Introduzione alla CLI IDT](index.html)
- [Comandi IDT (ibmcloud dev)](commands.html)
- [Developer Tools per il codice VS](vscode.html)
- [Developer Tools per l'IDE Jetbrains](jetbrains.html)

Controlla le [esercitazioni](/docs/apps/tutorials/tutorial_bff.html) che mostrano come creare le applicazioni native cloud che utilizzano la CLI {{site.data.keyword.dev_cli_short}}.

## Documentazione aggiuntiva
{: #learn-more}

Le seguenti risorse possono essere utili quando sviluppi le applicazioni native cloud con la CLI di IBM Developer Tools:

- [Pagina di destinazione principale di IBM Cloud Developer Tools](https://www.ibm.com/cloud/cli) - Pagina del prodotto principale per la CLI IDT
- [IBM Developer Tools Installer](https://github.com/IBM-Bluemix/ibm-cloud-developer-tools) - Repository GitHub pubblico con le istruzioni di installazione dettagliate
- [IBM Cloud App Service](https://console.bluemix.net/developer/appservice) - Pagina della console IBM Cloud, che è complementare agli strumenti IDT per la creazione e gestione delle applicazioni native cloud
- [Segnala problemi su GitHub](https://github.com/IBM-Cloud/ibm-cloud-developer-tools/issues)
- [IBM Cloud Tech's Slack - Canale #developer-tools](https://ibm-cloud-tech.slack.com) - Richiedi l'accesso al team [qui](https://slack-invite-ibm-cloud-tech.mybluemix.net/)

**Incentrati sul linguaggio**

- [Node.js on IBM Cloud](https://developer.ibm.com/node/cloud/)
- [Spring @ IBM Cloud](https://developer.ibm.com/java/spring/)
- [Swift @ IBM](https://developer.ibm.com/swift)

**Blog ed esercitazioni**

- [Deploying to IBM Cloud Private with IBM Cloud Developer Tools CLI](https://www.ibm.com/blogs/bluemix/2017/09/deploying-ibm-cloud-private-ibm-cloud-developer-tools-cli/)
- [Enable existing projects for IBM Cloud with the IBM Cloud Developer Tools CLI](https://www.ibm.com/blogs/bluemix/2017/09/enable-existing-projects-ibm-cloud-ibm-cloud-developer-tools-cli/)
- [Deploying to Kubernetes on IBM Cloud with the IBM Cloud Developer Tools CLI](https://www.ibm.com/blogs/bluemix/2017/09/deploying-kubernetes-ibm-cloud-ibm-cloud-developer-tools-cli/)
