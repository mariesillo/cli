---

copyright:

  years: 2018


lastupdated: "2018-06-21"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:tip: .tip}

# Comandos da CLI de sub-rede

<table summary="Comandos gerais de infraestrutura {{site.data.keyword.BluSoftlayer_notm}} em ordem alfabética que possuem links que levam você para mais informações sobre o comando">
<caption>Tabela 1. Comandos de sub-rede de infraestrutura do {{site.data.keyword.BluSoftlayer_notm}}</caption>
 <thead>
 <th colspan="5">Comandos da sub-rede de infraestrutura {{site.data.keyword.BluSoftlayer_notm}}</th>
 </thead>
 <tbody>
 <tr>
 <td>[ibmcloud sl subnet cancel](/docs/cli/reference/softlayer/sl_cli_subnet.html#sl_subnet_cancel)</td>
 <td>[ibmcloud sl subnet create](/docs/cli/reference/softlayer/sl_cli_subnet.html#sl_subnet_create)</td>
 <td>[ibmcloud sl subnet detail](/docs/cli/reference/softlayer/sl_cli_subnet.html#sl_subnet_detail)</td>
 <td>[ibmcloud sl subnet list](/docs/cli/reference/softlayer/sl_cli_subnet.html#sl_subnet_list)</td>
 <td>[ibmcloud sl subnet lookup](/docs/cli/reference/softlayer/sl_cli_subnet.html#sl_subnet_lookup)</td>
 </tr>
   </tbody>
 </table>
 
 ### ibmcloud sl subnet cancel
{: #sl_subnet_cancel}

Cancelar uma sub-rede.
```
Ibmcloud sl subnet cancel IDENTIFIER [ OPTIONS ]
```

<strong>Opções de comando</strong>:
<dl>
<dt>-f, --force</dt>
<dd>Forçar a operação sem confirmação.</dd>
</dl>

**Exemplos**:
```
ibmcloud sl subnet cancel 12345678 -f
```
Esse comando cancela a sub-rede com ID 12345678 sem solicitar confirmação.

### Ibmcloud sl subnet create
{: #sl_subnet_create}

Inclua uma nova sub-rede em sua conta.
```
ibmcloud sl subnet create NETWORK QUANTITY VLAN_ID [OPTIONS]
```

<strong>Opções de comando</strong>:
<dl>
<dt>--v6, --ipv6</dt>
<dd>Pedir endereços IPv6.</dd>
<dt>--test</dt>
<dd>Não pedir a sub-rede; obter apenas uma cota.</dd>
<dt>-f, --force</dt>
<dd>Forçar a operação sem confirmação.</dd>
</dl>

**Exemplos**:
```
ibmcloud sl subnet create public 16 567
```
Esse comando cria uma sub-rede pública com 16 endereços IP v4 e a coloca na vlan com ID 567.

### Sl subnet detail ibmcloud
{: #sl_subnet_detail}

Obter detalhes de uma sub-rede.
```
Sl subnet detail IDENTIFIER ibmcloud [ OPTIONS ]
```

<strong>Opções de comando</strong>:
<dl>
<dt>--no-vs</dt>
<dd>Ocultar listagem de servidor virtual.</dd>
<dt>--no-hardware</dt>
<dd>Ocultar listagem de hardware.</dd>
</dl>

**Exemplos**:
```
Ibmcloud sl subnet detail 12345678
```
Esse comando mostra informações detalhadas sobre a sub-rede com ID 12345678, incluindo informações de servidores virtuais e de hardware.

### Sl subnet list ibmcloud
{: #sl_subnet_list}

Listar todas as sub-redes em sua conta.
```
Sl subnet list ibmcloud [ OPTIONS ]
```

<strong>Opções de comando</strong>:
<dl>
<dt>--sortby</dt>
<dd>Coluna pela qual classificar. As opções são: id, identifier, type, network_space, datacenter, vlan_id, IPs, hardware, vs.</dd>
<dt>-d, --datacenter</dt>
<dd>Filtrar pelo nome abreviado do data center.</dd>
<dt>--identifier</dt>
<dd>Filtrar pelo identificador de rede.</dd>
<dt>-t, --subnet-type</dt>
<dd>Filtrar pelo tipo de sub-rede.</dd>
<dt>--network-space</dt>
<dd>Filtrar pelo espaço de rede.</dd>
<dt>--v4, --ipv4</dt>
<dd>Exibir somente sub-redes IPv4.</dd>
<dt>--v6, --ipv6</dt>
<dd>Exibir somente sub-redes IPv6.</dd>
<dt>--order</dt>
<dd>Filtrar pelo ID da ordem que comprou as sub-redes.</dd>
</dl>

**Exemplos**:
```
ibmcloud sl subnet list -d dal09 -t PRIMARY --network-space PUBLIC --v4
```
Esse comando lista sub-redes IP V4 na conta atual filtrando pelo data center dal09, tipo de sub-rede PRIMARY e espaço de rede PUBLIC.

### Sl subnet lookup ibmcloud
{: #sl_subnet_lookup}

Localizar um endereço IP e exibir suas informações de sub-rede e dispositivo.
```
Ibmcloud sl subnet lookup IP_ADDRESS
```


**Exemplos**:
```
Ibmcloud sl subnet lookup 9.125.235.255
```
Esse comando localiza o registro de endereço IP com endereço 9.125.235.255 e exibe suas informações sobre a sub-rede e o dispositivo.
