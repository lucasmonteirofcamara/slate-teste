<!-- Generator: Widdershins v4.0.1 -->

# APIs Open Data do Open Insurance Brasil v1.0.0

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

As API's administrativas são recursos que podem ser consumidos apenas pelo diretório para avaliação e controle da qualidade dos serviços fornecidos pelas instituições

Base URLs:

* <a href="http://api.organizacao.com.br/open-insurance/admin/v1">http://api.organizacao.com.br/open-insurance/admin/v1</a>

Web: <a href="https://http://novosite.susep.gov.br">Support</a> 

## Metrics

### Obtém as métricas de disponibilidade das APIs

<a id="opIdgetMetrics"></a>

<a href="files/swagger/metrics.yaml">Especificação em OAS</a> <br>

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

xhr.open("GET", "http://api.organizacao.com.br/open-insurance/admin/v1/metrics");
xhr.setRequestHeader("Accept", "application/json");
xhr.setRequestHeader("cache-control", "string");
xhr.setRequestHeader("Content-Security-Policy", "string");
xhr.setRequestHeader("content-Type", "string");
xhr.setRequestHeader("Strict-Transport-Security", "string");
xhr.setRequestHeader("X-Content-Type-Options", "string");
xhr.setRequestHeader("X-Frame-Options", "string");

xhr.send(data);
```

```python
import http.client

conn = http.client.HTTPConnection("api.organizacao.com.br")

headers = {
    'Accept': "application/json",
    'cache-control': "string",
    'Content-Security-Policy': "string",
    'content-Type': "string",
    'Strict-Transport-Security': "string",
    'X-Content-Type-Options': "string",
    'X-Frame-Options': "string"
    }

conn.request("GET", "/open-insurance/admin/v1/metrics", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("http://api.organizacao.com.br/open-insurance/admin/v1/metrics")
  .header("Accept", "application/json")
  .header("cache-control", "string")
  .header("Content-Security-Policy", "string")
  .header("content-Type", "string")
  .header("Strict-Transport-Security", "string")
  .header("X-Content-Type-Options", "string")
  .header("X-Frame-Options", "string")
  .asString();
```

`GET /metrics`

Obtém as métricas de disponibilidade das APIs

<h3 id="obtém-as-métricas-de-disponibilidade-das-apis-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|cache-control|header|string|true|Controle de cache para evitar que informações confidenciais sejam armazenadas em cache.|
|Content-Security-Policy|header|string|false|Campo para proteção contra ataques clickjack do estilo - drag and drop.|
|content-Type|header|string|false|Especificar o tipo de conteúdo da resposta.|
|Strict-Transport-Security|header|string|false|Campo para exigir conexões por HTTPS e proteger contra certificados falsificados.|
|X-Content-Type-Options|header|string|false|Campo para evitar que navegadores executem a detecção de MIME e interpretem respostas como HTML de forma inadequada.|
|X-Frame-Options|header|string|false|Campo indica se o navegador deve ou não renderizar um frame.|
|page|query|integer|false|Número da página que está sendo requisitada (o valor da primeira página é 1).|
|page-size|query|integer|false|Quantidade total de registros por páginas.|
|period|query|string|false|Período a ser consultado|

#### Detailed descriptions

**period**: Período a ser consultado
  * `CURRENT` - Métricas do dia atual.
  * `ALL` - Métricas de todo o período disponível.

#### Enumerated Values

|Parameter|Value|
|---|---|
|period|CURRENT|
|period|ALL|

> Example responses

> 200 Response

```json
{
  "data": {
    "requestTime": "2019-08-24T14:15:22Z",
    "availability": {
      "uptime": {
        "generalUptimeRate": "string",
        "endpoints": [
          {
            "url": "string",
            "uptimeRate": "string"
          }
        ]
      },
      "downtime": {
        "generalDowntime": 0,
        "scheduledOutage": 0,
        "endpoints": [
          {
            "url": "string",
            "partialDowntime": 0
          }
        ]
      }
    },
    "invocations": {
      "unauthenticated": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "highPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "mediumPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "unattended": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      }
    },
    "averageResponse": {
      "unauthenticated": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "highPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "mediumPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "unattended": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      }
    },
    "averageTps": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    },
    "peakTps": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    },
    "errors": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    },
    "rejections": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>",
    "first": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>"
  },
  "meta": {
    "totalRecords": 1,
    "totalPages": 1
  }
}
```

<h3 id="obtém-as-métricas-de-disponibilidade-das-apis-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dados das métricas|[ResponseMetricsList](#schemaresponsemetricslist)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="schema_admin">Schemas</h1>

<h2 id="tocS_ResponseMetricsList">ResponseMetricsList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsemetricslist"></a>
<a id="schema_ResponseMetricsList"></a>
<a id="tocSresponsemetricslist"></a>
<a id="tocsresponsemetricslist"></a>

```json
{
  "data": {
    "requestTime": "2019-08-24T14:15:22Z",
    "availability": {
      "uptime": {
        "generalUptimeRate": "string",
        "endpoints": [
          {
            "url": "string",
            "uptimeRate": "string"
          }
        ]
      },
      "downtime": {
        "generalDowntime": 0,
        "scheduledOutage": 0,
        "endpoints": [
          {
            "url": "string",
            "partialDowntime": 0
          }
        ]
      }
    },
    "invocations": {
      "unauthenticated": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "highPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "mediumPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "unattended": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      }
    },
    "averageResponse": {
      "unauthenticated": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "highPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "mediumPriority": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      },
      "unattended": {
        "currentDay": 0,
        "previousDays": [
          0
        ]
      }
    },
    "averageTps": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    },
    "peakTps": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    },
    "errors": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    },
    "rejections": {
      "currentDay": 0,
      "previousDays": [
        0
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>",
    "first": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>"
  },
  "meta": {
    "totalRecords": 1,
    "totalPages": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|true|none|none|
|» requestTime|string(date-time)|true|none|Data e hora que as métricas foram requisitadas.|
|» availability|[AvailabilityMetrics](#schemaavailabilitymetrics)|true|none|none|
|» invocations|[InvocationMetrics](#schemainvocationmetrics)|true|none|none|
|» averageResponse|[AverageMetrics](#schemaaveragemetrics)|true|none|none|
|» averageTps|[AverageTPSMetrics](#schemaaveragetpsmetrics)|true|none|none|
|» peakTps|[PeakTPSMetrics](#schemapeaktpsmetrics)|true|none|none|
|» errors|[ErrorMetrics](#schemaerrormetrics)|true|none|none|
|» rejections|[RejectionMetrics](#schemarejectionmetrics)|true|none|none|
|links|[Links](#schemalinks)|true|none|none|
|meta|[Meta](#schemameta)|false|none|none|

<h2 id="tocS_AvailabilityMetrics">AvailabilityMetrics</h2>
<!-- backwards compatibility -->
<a id="schemaavailabilitymetrics"></a>
<a id="schema_AvailabilityMetrics"></a>
<a id="tocSavailabilitymetrics"></a>
<a id="tocsavailabilitymetrics"></a>

```json
{
  "uptime": {
    "generalUptimeRate": "string",
    "endpoints": [
      {
        "url": "string",
        "uptimeRate": "string"
      }
    ]
  },
  "downtime": {
    "generalDowntime": 0,
    "scheduledOutage": 0,
    "endpoints": [
      {
        "url": "string",
        "partialDowntime": 0
      }
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|uptime|object|true|none|none|
|» generalUptimeRate|string|true|none|Taxa de disponibilidade (considerando todos os serviços ativos ao mesmo tempo).|
|» endpoints|[EndpointUptime](#schemaendpointuptime)|true|none|none|
|downtime|object|true|none|none|
|» generalDowntime|integer|true|none|Quantidade de segundos de downtime (considerando qualquer api em downtime).|
|» scheduledOutage|integer|true|none|Quantidade de segundos de indisponibilidade agendada.|
|» endpoints|[EndpointDowntime](#schemaendpointdowntime)|true|none|none|

<h2 id="tocS_EndpointUptime">EndpointUptime</h2>
<!-- backwards compatibility -->
<a id="schemaendpointuptime"></a>
<a id="schema_EndpointUptime"></a>
<a id="tocSendpointuptime"></a>
<a id="tocsendpointuptime"></a>

```json
[
  {
    "url": "string",
    "uptimeRate": "string"
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|url|string|true|none|URL do endpoint|
|uptimeRate|string|true|none|Taxa de disponibilidade do endpoint.|

<h2 id="tocS_EndpointDowntime">EndpointDowntime</h2>
<!-- backwards compatibility -->
<a id="schemaendpointdowntime"></a>
<a id="schema_EndpointDowntime"></a>
<a id="tocSendpointdowntime"></a>
<a id="tocsendpointdowntime"></a>

```json
[
  {
    "url": "string",
    "partialDowntime": 0
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|url|string|true|none|URL do endpoint|
|partialDowntime|integer|true|none|Quantidade de segundos de indisponibilidade do endpoint.|

<h2 id="tocS_InvocationMetrics">InvocationMetrics</h2>
<!-- backwards compatibility -->
<a id="schemainvocationmetrics"></a>
<a id="schema_InvocationMetrics"></a>
<a id="tocSinvocationmetrics"></a>
<a id="tocsinvocationmetrics"></a>

```json
{
  "unauthenticated": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  },
  "highPriority": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  },
  "mediumPriority": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  },
  "unattended": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|unauthenticated|object|true|none|Número de chamadas não autenticadas.|
|» currentDay|integer|true|none|Número de chamadas não autenticadas no dia atual.|
|» previousDays|[integer]|true|none|Número de chamadas não autenticadas nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|
|highPriority|object|true|none|Número de chamadas para o nível de alta prioridade.|
|» currentDay|integer|true|none|Número de chamadas no dia atual para o nível de alta prioridade.|
|» previousDays|[integer]|true|none|Número de chamadas nos dias anteriores para o nível de alta prioridade. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|
|mediumPriority|object|true|none|Número de chamadas para o nível de média prioridade.|
|» currentDay|integer|true|none|Número de chamadas no dia atual para o nível de média prioridade.|
|» previousDays|[integer]|true|none|Número de chamadas nos dias anteriores para o nível de média prioridade. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|
|unattended|object|true|none|Número de chamadas para o nível não acompanhado.|
|» currentDay|integer|true|none|Número de chamadas no dia atual para o nível não acompanhado.|
|» previousDays|[integer]|true|none|Número de chamadas nos dias anteriores para o nível não acompanhado. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|

<h2 id="tocS_AverageMetrics">AverageMetrics</h2>
<!-- backwards compatibility -->
<a id="schemaaveragemetrics"></a>
<a id="schema_AverageMetrics"></a>
<a id="tocSaveragemetrics"></a>
<a id="tocsaveragemetrics"></a>

```json
{
  "unauthenticated": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  },
  "highPriority": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  },
  "mediumPriority": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  },
  "unattended": {
    "currentDay": 0,
    "previousDays": [
      0
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|unauthenticated|object|true|none|Tempo médio de resposta para chamadas não autenticadas.|
|» currentDay|integer|true|none|Tempo médio de resposta em milissegundos para chamadas no dia atual.|
|» previousDays|[integer]|true|none|Tempo médio de resposta em milissegundos para chamadas nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|
|highPriority|object|true|none|Tempo médio de resposta de chamadas para o nível de alta prioridade.|
|» currentDay|integer|true|none|Tempo médio de resposta em milissegundos para chamadas no dia atual.|
|» previousDays|[integer]|true|none|Tempo médio de resposta em milissegundos para chamadas nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|
|mediumPriority|object|true|none|Tempo médio de resposta para chamadas para o nível de média prioridade.|
|» currentDay|integer|true|none|Tempo médio de resposta em milissegundos para chamadas no dia atual.|
|» previousDays|[integer]|true|none|Tempo médio de resposta em milissegundos para chamadas nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|
|unattended|object|true|none|Tempo médio de resposta para chamadas para o nível não acompanhado.|
|» currentDay|integer|true|none|Tempo médio de resposta em milissegundos para chamadas no dia atual.|
|» previousDays|[integer]|true|none|Tempo médio de resposta em milissegundos para chamadas nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|

<h2 id="tocS_AverageTPSMetrics">AverageTPSMetrics</h2>
<!-- backwards compatibility -->
<a id="schemaaveragetpsmetrics"></a>
<a id="schema_AverageTPSMetrics"></a>
<a id="tocSaveragetpsmetrics"></a>
<a id="tocsaveragetpsmetrics"></a>

```json
{
  "currentDay": 0,
  "previousDays": [
    0
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|currentDay|integer|true|none|Número médio de chamadas por segundo no dia.|
|previousDays|[integer]|true|none|Número médio de chamadas por segundo nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|

<h2 id="tocS_PeakTPSMetrics">PeakTPSMetrics</h2>
<!-- backwards compatibility -->
<a id="schemapeaktpsmetrics"></a>
<a id="schema_PeakTPSMetrics"></a>
<a id="tocSpeaktpsmetrics"></a>
<a id="tocspeaktpsmetrics"></a>

```json
{
  "currentDay": 0,
  "previousDays": [
    0
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|currentDay|integer|true|none|Pico de chamadas por segundo no dia.|
|previousDays|[integer]|true|none|Pico de chamadas por segundo nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|

<h2 id="tocS_ErrorMetrics">ErrorMetrics</h2>
<!-- backwards compatibility -->
<a id="schemaerrormetrics"></a>
<a id="schema_ErrorMetrics"></a>
<a id="tocSerrormetrics"></a>
<a id="tocserrormetrics"></a>

```json
{
  "currentDay": 0,
  "previousDays": [
    0
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|currentDay|integer|true|none|Número de chamadas com erro no dia atual.|
|previousDays|[integer]|true|none|Número de chamadas com erro nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|

<h2 id="tocS_RejectionMetrics">RejectionMetrics</h2>
<!-- backwards compatibility -->
<a id="schemarejectionmetrics"></a>
<a id="schema_RejectionMetrics"></a>
<a id="tocSrejectionmetrics"></a>
<a id="tocsrejectionmetrics"></a>

```json
{
  "currentDay": 0,
  "previousDays": [
    0
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|currentDay|integer|true|none|Número de chamadas rejeitadas no dia atual.|
|previousDays|[integer]|true|none|Número de chamadas rejeitadas nos dias anteriores. O primeiro item do array é referente a ontem, e assim por diante. Devem ser retornados no máximo sete dias caso estejam disponíveis.|

<h2 id="tocS_Links">Links</h2>
<!-- backwards compatibility -->
<a id="schemalinks"></a>
<a id="schema_Links"></a>
<a id="tocSlinks"></a>
<a id="tocslinks"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>",
  "first": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/admin/v1/<resource>"
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
  "totalRecords": 1,
  "totalPages": 1
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalRecords|integer|true|none|Total de registros encontrados|
|totalPages|integer|true|none|Total de páginas para os registros encontrados|

