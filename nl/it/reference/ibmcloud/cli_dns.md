---

copyright:

  years: 2018


lastupdated: "2018-09-06"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:tip: .tip}

# DNS

Utilizza i seguenti comandi per gestire le zone nel servizio DNS dell'infrastruttura {{site.data.keyword.Bluemix_notm}}.
{: shortdesc}

<table summary="Comandi DNS dell'infrastruttura  {{site.data.keyword.Bluemix_notm}} riportati in ordine alfabetico con dei link a ulteriori informazioni sul comando">
 <tbody>
 <tr>
 <td>[ibmcloud sl dns import](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_import)</td>
 <td>[ibmcloud sl dns record-add](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_record_add)</td>
 <td>[ibmcloud sl dns record-edit](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_record_edit)</td>
 <td>[ibmcloud sl dns record-list](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_record_list)</td>
 <td>[ibmcloud sl dns record-remove](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_record_remove)</td>
 <td>[ibmcloud sl dns zone-create](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_zone_create)</td>
 </tr>
 <tr>
   <td>[ibmcloud sl dns zone-delete](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_zone_delete)</td>
   <td>[ibmcloud sl dns zone-list
](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_zone_list)</td>
   <td>[ibmcloud sl dns zone-print](/docs/cli/reference/ibmcloud/cli_dns.html#sl_dns_zone_print)</td>
 </tr>
   </tbody>
 </table>

## ibmcloud sl dns import
{: #sl_dns_import}

Importa una zona in base a un file di zona BIND.
```
ibmcloud sl dns import FILEDIZONA [OPZIONI]
```

<strong>Opzioni del comando</strong>:
<dl>
<dt>--dry-run</dt>
<dd>Non creare al momento i record.</dd>
</dl>

**Esempi**:
```
ibmcloud sl dns import ~/ibm.com.txt
```
Questo comando importa la zona e i suoi record della risorsa dal file: ~/ibm.com.txt.

## ibmcloud sl dns record-add
{: #sl_dns_record_add}

Aggiungi il record della risorsa in una zona.
```
ibmcloud sl dns record-add ZONA RECORD TIPO DATI [OPZIONI]
```

<strong>Opzioni del comando</strong>:
<dl>
<dt>--ttl</dt>
<dd>Valore TTL (Time-To-Live) in secondi, come: 86400; il valore predefinito è: 7200.</dd>
</dl>

**Esempi**:
```
ibmcloud sl dns record-add ibm.com ftp A 127.0.0.1 --ttl 86400
```
Questo comando aggiunge un record A alla zona: ibm.com; il suo host è "ftp", i dati sono "127.0.0.1" e TTL è 86400 secondi.

## ibmcloud sl dns record-edit
{: #sl_dns_record_edit}

Aggiorna i record della risorsa in una zona.
```
ibmcloud sl dns record-edit ZONA [OPZIONI]
```

<strong>Opzioni del comando</strong>:
<dl>
<dt>--by-record</dt>
<dd>Modifica per record host, ad esempio www.</dd>
<dt>--by-id</dt>
<dd>Modifica un solo record dal suo ID</dd>
<dt>--data</dt>
<dd>Dati di record, ad esempio un indirizzo IP.</dd>
<dt>--ttl</dt>
<dd>Valore TTL in secondi, ad esempio: 86400.</dd>
</dl>

**Esempi**:
```
ibmcloud sl dns record-edit ibm.com --by-id 12345678 --data 127.0.0.2 --ttl 3600
```
Questo comando modifica i record nella zona: ibm.com, dove l'ID è 12345678 e imposta i suoi dati su "127.0.0.2" e TTL su 3600.

## ibmcloud sl dns record-list
{: #sl_dns_record_list}

Elenca tutti i record della risorsa in una zona.
```
ibmcloud sl dns record-list ZONA [OPZIONI]
```

<strong>Opzioni del comando</strong>:
<dl>
<dt>--data</dt>
<dd>Filtra per dati di record, ad esempio un indirizzo IP.</dd>
<dt>--record</dt>
<dd>Filtra per record host, ad esempio www.</dd>
<dt>--ttl</dt>
<dd>Filtra per valore TTL in secondi, ad esempio 86400.</dd>
<dt>--type</dt>
<dd>Filtra in base al tipo di record, ad esempio A o CNAME.</dd>
</dl>

**Esempi**:
```
ibmcloud sl dns record-list ibm.com --record elasticsearch --type A --ttl 900
```
Questo comando elenca tutti i record A nella zona: ibm.com, il filtro in base all'host è elasticsearch e TTL è 900 secondi.

## ibmcloud sl dns record-remove
{: #sl_dns_record_remove}

Rimuovi il record della risorsa da una zona.
```
ibmcloud sl dns record-remove ID_RECORD
```


**Esempi**:
```
ibmcloud sl dns record-remove 12345678
```
Questo comando rimuove il record della risorsa con ID 12345678.

## ibmcloud sl dns zone-create
{: #sl_dns_zone_create}

Crea una zona.
```
ibmcloud sl dns zone-create ZONA
```


**Esempi**:
```
ibmcloud sl dns zone-create ibm.com
```
Questo comando crea una zona denominata ibm.com.

## ibmcloud sl dns zone-delete
{: #sl_dns_zone_delete}

Elimina una zona.
```
ibmcloud sl dns zone-delete ZONA
```


**Esempi**:
```
ibmcloud sl dns zone-delete ibm.com
```
Questo comando elimina una zona denominata ibm.com.

## ibmcloud sl dns zone-list
{: #sl_dns_zone_list}

Elenca tutte le zone del tuo account.
```
ibmcloud sl dns zone-list
```


**Esempi**:
```
ibmcloud sl dns zone-list
```
Questo comando elenca tutte le zone nell'account corrente.

## ibmcloud sl dns zone-print
{: #sl_dns_zone_print}

Stampa la zona e i record della risorsa nel formato BIND.
```
ibmcloud sl dns zone-print ZONA
```


**Esempi**:
```
ibmcloud sl dns zone-print ibm.com
```
Questo comando stampa la zona denominata ibm.com in formato BIND.
