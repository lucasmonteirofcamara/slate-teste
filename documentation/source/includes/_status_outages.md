<!-- Generator: Widdershins v4.0.1 -->

# APIs comuns v1.0.0

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

As APIs descritas neste documento são referentes as APIs da fase Open Data do Open Insurance Brasil.

Base URLs:

* <a href="https://api.organizacao.com.br/open-insurance/discovery/v1">https://api.organizacao.com.br/open-insurance/discovery/v1</a>

Web: <a href="https://openinsurance.susep.gov.br">Support</a> 

## API de status

### A descrição referente ao código de status retornado pelas APIs

<a id="opIdgetStatus"></a>

> Code samples

```javascript
const data = null;

const xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/discovery/v1/status");
xhr.setRequestHeader("Accept", "application/json");

xhr.send(data);
```

```python
import http.client

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = { 'Accept': "application/json" }

conn.request("GET", "/open-insurance/discovery/v1/status", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/discovery/v1/status")
  .header("Accept", "application/json")
  .asString();
```

`GET /status`

 Descrição referente ao código de status retornado pelas APIs

<h3 id="a-descrição-referente-ao-código-de-status-retornado-pelas-apis-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|Número da página que está sendo requisitada, sendo a primeira página 1.|
|page-size|query|integer|false|Quantidade total de registros por páginas.|

> Example responses

> 200 Response

```json
{
  "data": {
    "status": [
      {
        "code": "OK",
        "explanation": "Retorno com Sucesso",
        "detectionTime": "2021-07-21T08:30:00Z",
        "expectedResolutionTime": "2021-07-21T08:30:00Z",
        "updateTime": "2021-01-02T01:00:00Z",
        "unavailableEndpoints": [
          "https://api.seguradora.com.br/open-insurance/channels/v1/electronic-channels"
        ]
      }
    ]
  },
  "links": {
    "self": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "first": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "prev": "string",
    "next": "string",
    "last": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>"
  },
  "meta": {
    "totalRecords": 9,
    "totalPages": 3
  }
}
```

<h3 id="a-descrição-referente-ao-código-de-status-retornado-pelas-apis-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Código de status retornado pelas APIs|[ResponseDiscoveryStatusList](#schemaresponsediscoverystatuslist)|

<aside class="success">
This operation does not require authentication
</aside>

## API de outages

### a descrição referente a listagem de indisponibilidades agendadas para os serviços

<a id="opIdgetOutage"></a>

> Code samples

```javascript
const data = null;

const xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function () {
  if (this.readyState === this.DONE) {
    console.log(this.responseText);
  }
});

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/discovery/v1/outages");
xhr.setRequestHeader("Accept", "application/json");

xhr.send(data);
```

```python
import http.client

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = { 'Accept': "application/json" }

conn.request("GET", "/open-insurance/discovery/v1/outages", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/discovery/v1/outages")
  .header("Accept", "application/json")
  .asString();
```

`GET /outages`

a descrição referente a listagem de indisponibilidades agendadas para os serviços

<h3 id="a-descrição-referente-a-listagem-de-indisponibilidades-agendadas-para-os-serviços-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|Número da página que está sendo requisitada, sendo a primeira página 1.|
|page-size|query|integer|false|Quantidade total de registros por páginas.|

> Example responses

> 200 Response

```json
{
  "data": [
    {
      "outageTime": "2020-07-21T08:30:00Z",
      "duration": "PT2H30M",
      "isPartial": false,
      "explanation": "Atualização do API Gateway",
      "unavailableEndpoints": [
        "https://api.seguradora.com.br/open-insurance/channels/v1/electronic-channels"
      ]
    }
  ],
  "links": {
    "self": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "first": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "prev": "string",
    "next": "string",
    "last": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>"
  },
  "meta": {
    "totalRecords": 9,
    "totalPages": 3
  }
}
```

<h3 id="a-descrição-referente-a-listagem-de-indisponibilidades-agendadas-para-os-serviços-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|listagem de indisponibilidades agendadas para os serviços|[ResponseDiscoveryOutageList](#schemaresponsediscoveryoutagelist)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="schema_status">Schemas</h1>

<h2 id="tocS_ResponseDiscoveryStatusList">ResponseDiscoveryStatusList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsediscoverystatuslist"></a>
<a id="schema_ResponseDiscoveryStatusList"></a>
<a id="tocSresponsediscoverystatuslist"></a>
<a id="tocsresponsediscoverystatuslist"></a>

```json
{
  "data": {
    "status": [
      {
        "code": "OK",
        "explanation": "Retorno com Sucesso",
        "detectionTime": "2021-07-21T08:30:00Z",
        "expectedResolutionTime": "2021-07-21T08:30:00Z",
        "updateTime": "2021-01-02T01:00:00Z",
        "unavailableEndpoints": [
          "https://api.seguradora.com.br/open-insurance/channels/v1/electronic-channels"
        ]
      }
    ]
  },
  "links": {
    "self": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "first": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "prev": "string",
    "next": "string",
    "last": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>"
  },
  "meta": {
    "totalRecords": 9,
    "totalPages": 3
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|true|none|none|
|» status|[[Status](#schemastatus)]|true|none|none|
|links|[Links](#schemalinks)|true|none|none|
|meta|[Meta](#schemameta)|true|none|none|

<h2 id="tocS_ResponseDiscoveryOutageList">ResponseDiscoveryOutageList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsediscoveryoutagelist"></a>
<a id="schema_ResponseDiscoveryOutageList"></a>
<a id="tocSresponsediscoveryoutagelist"></a>
<a id="tocsresponsediscoveryoutagelist"></a>

```json
{
  "data": [
    {
      "outageTime": "2020-07-21T08:30:00Z",
      "duration": "PT2H30M",
      "isPartial": false,
      "explanation": "Atualização do API Gateway",
      "unavailableEndpoints": [
        "https://api.seguradora.com.br/open-insurance/channels/v1/electronic-channels"
      ]
    }
  ],
  "links": {
    "self": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "first": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
    "prev": "string",
    "next": "string",
    "last": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>"
  },
  "meta": {
    "totalRecords": 9,
    "totalPages": 3
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|[any]|true|none|none|
|» outageTime|string|true|none|Data e hora planejada do início da indisponibilidade|
|» duration|string|true|none|Duração prevista da indisponibilidade|
|» isPartial|boolean|true|none|Flag que indica se a indisponibilidade é parcial (atingindo apenas alguns end points) ou total (atingindo todos os end points)|
|» explanation|string|true|none|Explicação sobre os motivos da indisponibilidade.|
|» unavailableEndpoints|[string]|true|none|Endpoints com indisponibilidade.|
|links|[Links](#schemalinks)|true|none|none|
|meta|[Meta](#schemameta)|true|none|none|

<h2 id="tocS_Links">Links</h2>
<!-- backwards compatibility -->
<a id="schemalinks"></a>
<a id="schema_Links"></a>
<a id="tocSlinks"></a>
<a id="tocslinks"></a>

```json
{
  "self": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
  "first": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>",
  "prev": "string",
  "next": "string",
  "last": "https://api.seguradora.com.br/open-insurance/channels/v1/<resource>"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|self|string|false|none|URL da página atualmente requisitada|
|first|string|false|none|URL da primeira página de registros|
|prev|string|false|none|URL da página anterior de registros|
|next|string|false|none|URL da próxima página de registros|
|last|string|false|none|URL da última página de registros|

<h2 id="tocS_Meta">Meta</h2>
<!-- backwards compatibility -->
<a id="schemameta"></a>
<a id="schema_Meta"></a>
<a id="tocSmeta"></a>
<a id="tocsmeta"></a>

```json
{
  "totalRecords": 9,
  "totalPages": 3
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalRecords|integer|true|none|Total de registros encontrados|
|totalPages|integer|true|none|Total de páginas para os registros encontrados|

<h2 id="tocS_Status">Status</h2>
<!-- backwards compatibility -->
<a id="schemastatus"></a>
<a id="schema_Status"></a>
<a id="tocSstatus"></a>
<a id="tocsstatus"></a>

```json
{
  "code": "OK",
  "explanation": "Retorno com Sucesso",
  "detectionTime": "2021-07-21T08:30:00Z",
  "expectedResolutionTime": "2021-07-21T08:30:00Z",
  "updateTime": "2021-01-02T01:00:00Z",
  "unavailableEndpoints": [
    "https://api.seguradora.com.br/open-insurance/channels/v1/electronic-channels"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|true|none|Condição atual da API:<br>  * `OK` - A implementação é totalmente funcional<br>  * `PARTIAL_FAILURE` - Um ou mais endpoints estão indisponíveis<br>  * `UNAVAILABLE` - A implementação completa está indisponível<br>  * `SCHEDULED_OUTAGE` - Uma interrupção anunciada está em vigor|
|explanation|string|true|none|Fornece uma explicação da interrupção atual que pode ser exibida para um cliente final. Será obrigatoriamente preenchido se code tiver algum valor que não seja OK|
|detectionTime|string|false|none|A data e hora em que a interrupção atual foi detectada. Será obrigatoriamente preenchido se a propriedade code for PARTIAL_FAILURE ou UNAVAILABLE|
|expectedResolutionTime|string|false|none|A data e hora em que o serviço completo deve continuar (se conhecido). Será obrigatoriamente preenchido se code tiver algum valor que não seja OK|
|updateTime|string|false|none|A data e hora em que esse status foi atualizado pela última vez pelo titular dos dados.|
|unavailableEndpoints|[string]|false|none|Endpoints com indisponibilidade|

#### Enumerated Values

|Property|Value|
|---|---|
|code|OK|
|code|PARTIAL_FAILURE|
|code|UNAVAILABLE|
|code|SCHEDULED_OUTAGE|

