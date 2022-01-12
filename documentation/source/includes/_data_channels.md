<!-- Generator: Widdershins v4.0.1 -->

# API - Canais de Atendimento v1.0.0

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

As APIs descritas neste documento são referentes as APIs da fase Open Data do Open Insurance Brasil.

Base URLs:

* <a href="https://api.organizacao.com.br/open-insurance/channels/v1">https://api.organizacao.com.br/open-insurance/channels/v1</a>

Web: <a href="https://openinsurance.susep.gov.br">Support</a> 

<a href="files/swagger/canais_atendimento.yaml">Especificação em OAS</a> <br>

## Dependências próprias

### Obtém a listagem de dependências próprias da instituição.

<a id="opIdgetBranches"></a>

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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/channels/v1/branches");
xhr.setRequestHeader("Accept", "application/json");

xhr.send(data);
```

```python
import http.client

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = { 'Accept': "application/json" }

conn.request("GET", "/open-insurance/channels/v1/branches", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/channels/v1/branches")
  .header("Accept", "application/json")
  .asString();
```

`GET /branches`

Método para obter a listagem de dependências próprias da instituição.

<h3 id="obtém-a-listagem-de-dependências-próprias-da-instituição.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|Número da página que está sendo requisitada (o valor da primeira página é 1).|
|page-size|query|integer|false|Quantidade total de registros por páginas.|

> Example responses

> 200 Response

```json
{
  "data": {
    "brand": {
      "name": "Organização AZ",
      "companies": [
        {
          "name": "Empresa A1",
          "cnpjNumber": "45086338000178",
          "branches": [
            {
              "identification": {
                "type": "POSTO_ATENDIMENTO",
                "code": "0001",
                "checkDigit": "9",
                "name": "Marília"
              },
              "postalAddress": {
                "address": "Av Naburo Ykesaki 1270, bloco 35, fundos",
                "additionalInfo": "Loja B",
                "districtName": "Centro",
                "townName": "São Paulo",
                "ibgeCode": "3550308",
                "countrySubDivision": "SP",
                "postCode": "17500001",
                "country": "Brasil",
                "countryCode": "BRA",
                "geographicCoordinates": {
                  "latitude": "-90.8365180",
                  "longitude": "-180.836519"
                }
              },
              "availability": {
                "standards": [
                  {
                    "weekday": "SEGUNDA_FEIRA",
                    "openingTime": "10:00:57Z",
                    "closingTime": "16:00:57Z"
                  }
                ],
                "exception": "string",
                "isPublicAccessAllowed": true
              },
              "phones": [
                {
                  "type": "FIXO",
                  "countryCallingCode": "55",
                  "areaCode": "19",
                  "number": "35721199"
                }
              ],
              "services": [
                {
                  "name": "ENDOSSO",
                  "code": "01"
                }
              ]
            }
          ]
        }
      ]
    },
    "links": {
      "self": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>",
      "first": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>",
      "prev": "string",
      "next": "string",
      "last": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>"
    },
    "meta": {
      "totalRecords": 1,
      "totalPages": 1
    }
  }
}
```

<h3 id="obtém-a-listagem-de-dependências-próprias-da-instituição.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Lista de dependências próprias obtida com sucesso.|[ResponseBranchesList](#schemaresponsebrancheslist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|Lista de dependências próprias obtida com sucesso.|[ResponseBranchesList](#schemaresponsebrancheslist)|

<aside class="success">
This operation does not require authentication
</aside>

## Canais de atendimento eletrônico

### Obtém a listagem de canais eletrônicos de atendimento da instituição.

<a id="opIdgetElectronicChannels"></a>

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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels");
xhr.setRequestHeader("Accept", "application/json");

xhr.send(data);
```

```python
import http.client

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = { 'Accept': "application/json" }

conn.request("GET", "/open-insurance/channels/v1/electronic-channels", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels")
  .header("Accept", "application/json")
  .asString();
```

`GET /electronic-channels`

Método para obter a listagem de canais eletrônicos de atendimento da instituição.

<h3 id="obtém-a-listagem-de-canais-eletrônicos-de-atendimento-da-instituição.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|Número da página que está sendo requisitada (o valor da primeira página é 1).|
|page-size|query|integer|false|Quantidade total de registros por páginas.|

> Example responses

> 200 Response

```json
{
  "data": {
    "brand": {
      "name": "Organização A",
      "companies": [
        {
          "name": "Empresa A1",
          "cnpjNumber": "45086338000178",
          "urlComplementaryList": "https://empresaa1.com/branches-insurance",
          "electronicChannels": [
            {
              "identification": {
                "type": "INTERNET",
                "urls": [
                  "https://empresa1.com/insurance"
                ]
              },
              "services": [
                {
                  "name": "SEGUROS",
                  "code": "SEGUROS"
                }
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels",
    "first": "https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels",
    "prev": "null",
    "next": "null",
    "last": "https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels"
  },
  "meta": {
    "totalRecords": 1,
    "totalPages": 1
  }
}
```

<h3 id="obtém-a-listagem-de-canais-eletrônicos-de-atendimento-da-instituição.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Listagem de canais eletrônicos de atendimento obtida com sucesso.|[ResponseElectronicChannelsList](#schemaresponseelectronicchannelslist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|Listagem de canais eletrônicos de atendimento obtida com sucesso.|[ResponseElectronicChannelsList](#schemaresponseelectronicchannelslist)|

<aside class="success">
This operation does not require authentication
</aside>

## Canais de atendimento telefônico

### Obtém a listagem de canais telefônicos de atendimento da instituição.

<a id="opIdgetPhoneChannels"></a>

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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels");
xhr.setRequestHeader("Accept", "application/json");

xhr.send(data);
```

```python
import http.client

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = { 'Accept': "application/json" }

conn.request("GET", "/open-insurance/channels/v1/phone-channels", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels")
  .header("Accept", "application/json")
  .asString();
```

`GET /phone-channels`

Método para obter a listagem de canais telefônicos de atendimento da instituição.

<h3 id="obtém-a-listagem-de-canais-telefônicos-de-atendimento-da-instituição.-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer|false|Número da página que está sendo requisitada (o valor da primeira página é 1).|
|page-size|query|integer|false|Quantidade total de registros por páginas.|

> Example responses

> 200 Response

```json
{
  "data": {
    "brand": {
      "name": "Organização A",
      "companies": [
        {
          "name": "Empresa A1",
          "cnpjNumber": "45086338000178",
          "urlComplementaryList": "https://empresaa1.com/branches-insurance",
          "phoneChannels": [
            {
              "identification": {
                "type": "CENTRAL_TELEFONICA",
                "phones": [
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "35721199"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "997865532"
                  }
                ]
              },
              "services": [
                {
                  "name": "ALTERACOES_FORMA_PAGAMENTO",
                  "code": "01"
                },
                {
                  "name": "AVISO_SINISTRO",
                  "code": "02"
                },
                {
                  "name": "ENDOSSO",
                  "code": "05"
                }
              ]
            },
            {
              "identification": {
                "type": "SAC",
                "phones": [
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40044828",
                    "additionalInfo": "DDI '55'; DDD '11', 40044828, 'Para clientes no exterior'"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40044828",
                    "additionalInfo": "DDI '55'; DDD '11', 40044828, 'Para clientes no exterior'"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40044828",
                    "additionalInfo": "DDI '55'; DDD '11', 40044828, 'Para clientes no exterior'"
                  }
                ]
              },
              "services": [
                {
                  "name": "RECLAMACAO",
                  "code": "16"
                },
                {
                  "name": "PORTABILIDADE",
                  "code": "15"
                },
                {
                  "name": "ENDOSSO",
                  "code": "05"
                }
              ]
            },
            {
              "identification": {
                "type": "OUVIDORIA",
                "phones": [
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40045555"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40045555"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40045555"
                  }
                ]
              },
              "services": [
                {
                  "name": "RECLAMACAO",
                  "code": "16"
                },
                {
                  "name": "PORTABILIDADE",
                  "code": "15"
                }
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels",
    "first": "https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels",
    "prev": "null",
    "next": "null",
    "last": "https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels"
  },
  "meta": {
    "totalRecords": 1,
    "totalPages": 1
  }
}
```

<h3 id="obtém-a-listagem-de-canais-telefônicos-de-atendimento-da-instituição.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Listagem de canais telefônicos de atendimento obtida com sucesso.|[ResponsePhoneChannelsList](#schemaresponsephonechannelslist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|Listagem de canais telefônicos de atendimento obtida com sucesso.|[ResponsePhoneChannelsList](#schemaresponsephonechannelslist)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="schema_channels"> Schemas </h1>

<h2 id="tocS_ResponseBranchesList">ResponseBranchesList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsebrancheslist"></a>
<a id="schema_ResponseBranchesList"></a>
<a id="tocSresponsebrancheslist"></a>
<a id="tocsresponsebrancheslist"></a>

```json
{
  "data": {
    "brand": {
      "name": "Organização AZ",
      "companies": [
        {
          "name": "Empresa A1",
          "cnpjNumber": "45086338000178",
          "branches": [
            {
              "identification": {
                "type": "POSTO_ATENDIMENTO",
                "code": "0001",
                "checkDigit": "9",
                "name": "Marília"
              },
              "postalAddress": {
                "address": "Av Naburo Ykesaki 1270, bloco 35, fundos",
                "additionalInfo": "Loja B",
                "districtName": "Centro",
                "townName": "São Paulo",
                "ibgeCode": "3550308",
                "countrySubDivision": "SP",
                "postCode": "17500001",
                "country": "Brasil",
                "countryCode": "BRA",
                "geographicCoordinates": {
                  "latitude": "-90.8365180",
                  "longitude": "-180.836519"
                }
              },
              "availability": {
                "standards": [
                  {
                    "weekday": "SEGUNDA_FEIRA",
                    "openingTime": "10:00:57Z",
                    "closingTime": "16:00:57Z"
                  }
                ],
                "exception": "string",
                "isPublicAccessAllowed": true
              },
              "phones": [
                {
                  "type": "FIXO",
                  "countryCallingCode": "55",
                  "areaCode": "19",
                  "number": "35721199"
                }
              ],
              "services": [
                {
                  "name": "ENDOSSO",
                  "code": "01"
                }
              ]
            }
          ]
        }
      ]
    },
    "links": {
      "self": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>",
      "first": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>",
      "prev": "string",
      "next": "string",
      "last": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>"
    },
    "meta": {
      "totalRecords": 1,
      "totalPages": 1
    }
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|true|none|none|
|» brand|[BranchesBrand](#schemabranchesbrand)|true|none|none|
|» links|[LinksPaginated](#schemalinkspaginated)|false|none|none|
|» meta|[MetaPaginated](#schemametapaginated)|false|none|none|

<h2 id="tocS_BranchesBrand">BranchesBrand</h2>
<!-- backwards compatibility -->
<a id="schemabranchesbrand"></a>
<a id="schema_BranchesBrand"></a>
<a id="tocSbranchesbrand"></a>
<a id="tocsbranchesbrand"></a>

```json
{
  "name": "Organização AZ",
  "companies": [
    {
      "name": "Empresa A1",
      "cnpjNumber": "45086338000178",
      "branches": [
        {
          "identification": {
            "type": "POSTO_ATENDIMENTO",
            "code": "0001",
            "checkDigit": "9",
            "name": "Marília"
          },
          "postalAddress": {
            "address": "Av Naburo Ykesaki 1270, bloco 35, fundos",
            "additionalInfo": "Loja B",
            "districtName": "Centro",
            "townName": "São Paulo",
            "ibgeCode": "3550308",
            "countrySubDivision": "SP",
            "postCode": "17500001",
            "country": "Brasil",
            "countryCode": "BRA",
            "geographicCoordinates": {
              "latitude": "-90.8365180",
              "longitude": "-180.836519"
            }
          },
          "availability": {
            "standards": [
              {
                "weekday": "SEGUNDA_FEIRA",
                "openingTime": "10:00:57Z",
                "closingTime": "16:00:57Z"
              }
            ],
            "exception": "string",
            "isPublicAccessAllowed": true
          },
          "phones": [
            {
              "type": "FIXO",
              "countryCallingCode": "55",
              "areaCode": "19",
              "number": "35721199"
            }
          ],
          "services": [
            {
              "name": "ENDOSSO",
              "code": "01"
            }
          ]
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da Marca reportada pelo participante do Open Insurance. O conceito a que se refere a 'marca' é em essência uma promessa da empresa em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes.|
|companies|[[BranchesCompany](#schemabranchescompany)]|true|none|Companies traz uma lista de todas as instuituições da Marca.|

<h2 id="tocS_BranchesCompany">BranchesCompany</h2>
<!-- backwards compatibility -->
<a id="schemabranchescompany"></a>
<a id="schema_BranchesCompany"></a>
<a id="tocSbranchescompany"></a>
<a id="tocsbranchescompany"></a>

```json
{
  "name": "Empresa A1",
  "cnpjNumber": "45086338000178",
  "branches": [
    {
      "identification": {
        "type": "POSTO_ATENDIMENTO",
        "code": "0001",
        "checkDigit": "9",
        "name": "Marília"
      },
      "postalAddress": {
        "address": "Av Naburo Ykesaki 1270, bloco 35, fundos",
        "additionalInfo": "Loja B",
        "districtName": "Centro",
        "townName": "São Paulo",
        "ibgeCode": "3550308",
        "countrySubDivision": "SP",
        "postCode": "17500001",
        "country": "Brasil",
        "countryCode": "BRA",
        "geographicCoordinates": {
          "latitude": "-90.8365180",
          "longitude": "-180.836519"
        }
      },
      "availability": {
        "standards": [
          {
            "weekday": "SEGUNDA_FEIRA",
            "openingTime": "10:00:57Z",
            "closingTime": "16:00:57Z"
          }
        ],
        "exception": "string",
        "isPublicAccessAllowed": true
      },
      "phones": [
        {
          "type": "FIXO",
          "countryCallingCode": "55",
          "areaCode": "19",
          "number": "35721199"
        }
      ],
      "services": [
        {
          "name": "ENDOSSO",
          "code": "01"
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|none|
|cnpjNumber|string|true|none|Número completo do CNPJ da instituição responsável pela dependência - o CNPJ corresponde ao número de inscrição no Cadastro de Pessoa Jurídica.<br>Deve-se ter apenas os números do CNPJ, sem máscara|
|branches|[[Branch](#schemabranch)]|false|none|Lista de Dependências de uma Instituição|

<h2 id="tocS_ResponseElectronicChannelsList">ResponseElectronicChannelsList</h2>
<!-- backwards compatibility -->
<a id="schemaresponseelectronicchannelslist"></a>
<a id="schema_ResponseElectronicChannelsList"></a>
<a id="tocSresponseelectronicchannelslist"></a>
<a id="tocsresponseelectronicchannelslist"></a>

```json
{
  "data": {
    "brand": {
      "name": "Organização A",
      "companies": [
        {
          "name": "Empresa A1",
          "cnpjNumber": "45086338000178",
          "urlComplementaryList": "https://empresaa1.com/branches-insurance",
          "electronicChannels": [
            {
              "identification": {
                "type": "INTERNET",
                "urls": [
                  "https://empresa1.com/insurance"
                ]
              },
              "services": [
                {
                  "name": "SEGUROS",
                  "code": "SEGUROS"
                }
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels",
    "first": "https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels",
    "prev": "null",
    "next": "null",
    "last": "https://api.organizacao.com.br/open-insurance/channels/v1/electronic-channels"
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
|brand|[ElectronicChannelsBrand](#schemaelectronicchannelsbrand)|false|none|none|
|links|[LinksPaginated](#schemalinkspaginated)|true|none|none|
|meta|[MetaPaginated](#schemametapaginated)|true|none|none|

<h2 id="tocS_ElectronicChannelsBrand">ElectronicChannelsBrand</h2>
<!-- backwards compatibility -->
<a id="schemaelectronicchannelsbrand"></a>
<a id="schema_ElectronicChannelsBrand"></a>
<a id="tocSelectronicchannelsbrand"></a>
<a id="tocselectronicchannelsbrand"></a>

```json
{
  "name": "Marca A",
  "companies": [
    {
      "name": "Empresa da Marca A",
      "cnpjNumber": "stringstringst",
      "electronicChannels": [
        {
          "identification": {
            "type": "CHAT",
            "accessType": "EMAIL",
            "urls": [
              "string"
            ]
          },
          "services": [
            {
              "name": "ALTERACACOES_FORMA_PAGAMENTO",
              "code": "01",
              "additionalInfo": "SIC"
            }
          ],
          "availability": {
            "standards": [
              {
                "weekday": "SEGUNDA_FEIRA",
                "openingTime": "10:00:57Z",
                "closingTime": "16:00:57Z"
              }
            ]
          }
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da marca selecionada pela Organização proprietária da dependência (titular).|
|companies|[[ElectronicChannelsCompanies](#schemaelectronicchannelscompanies)]|true|none|Lista de instituições pertencentes à marca|

<h2 id="tocS_ElectronicChannelsCompanies">ElectronicChannelsCompanies</h2>
<!-- backwards compatibility -->
<a id="schemaelectronicchannelscompanies"></a>
<a id="schema_ElectronicChannelsCompanies"></a>
<a id="tocSelectronicchannelscompanies"></a>
<a id="tocselectronicchannelscompanies"></a>

```json
{
  "name": "Empresa da Marca A",
  "cnpjNumber": "stringstringst",
  "electronicChannels": [
    {
      "identification": {
        "type": "CHAT",
        "accessType": "EMAIL",
        "urls": [
          "string"
        ]
      },
      "services": [
        {
          "name": "ALTERACACOES_FORMA_PAGAMENTO",
          "code": "01",
          "additionalInfo": "SIC"
        }
      ],
      "availability": {
        "standards": [
          {
            "weekday": "SEGUNDA_FEIRA",
            "openingTime": "10:00:57Z",
            "closingTime": "16:00:57Z"
          }
        ]
      }
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da marca selecionada pela Organização proprietária da dependência (titular).|
|cnpjNumber|string|true|none|CNPJ da sociedade responsável pelo canal de atendimento - o CNPJ corresponde ao número de inscrição no Cadastro de Pessoa Jurídica.|
|electronicChannels|[[ElectronicChannels](#schemaelectronicchannels)]|true|none|Lista  de canais de atendimento eltrônico|

<h2 id="tocS_Branch">Branch</h2>
<!-- backwards compatibility -->
<a id="schemabranch"></a>
<a id="schema_Branch"></a>
<a id="tocSbranch"></a>
<a id="tocsbranch"></a>

```json
{
  "identification": {
    "type": "POSTO_ATENDIMENTO",
    "code": "0001",
    "checkDigit": "9",
    "name": "Marília"
  },
  "postalAddress": {
    "address": "Av Naburo Ykesaki 1270, bloco 35, fundos",
    "additionalInfo": "Loja B",
    "districtName": "Centro",
    "townName": "São Paulo",
    "ibgeCode": "3550308",
    "countrySubDivision": "SP",
    "postCode": "17500001",
    "country": "Brasil",
    "countryCode": "BRA",
    "geographicCoordinates": {
      "latitude": "-90.8365180",
      "longitude": "-180.836519"
    }
  },
  "availability": {
    "standards": [
      {
        "weekday": "SEGUNDA_FEIRA",
        "openingTime": "10:00:57Z",
        "closingTime": "16:00:57Z"
      }
    ],
    "exception": "string",
    "isPublicAccessAllowed": true
  },
  "phones": [
    {
      "type": "FIXO",
      "countryCallingCode": "55",
      "areaCode": "19",
      "number": "35721199"
    }
  ],
  "services": [
    {
      "name": "ENDOSSO",
      "code": "01"
    }
  ]
}

```

Dependência destinada à prática das atividades para as quais a instituição esteja regularmente habilitada.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|identification|[BranchIdentification](#schemabranchidentification)|false|none|none|
|postalAddress|[BranchPostalAddress](#schemabranchpostaladdress)|true|none|none|
|availability|[BranchAvailability](#schemabranchavailability)|true|none|none|
|phones|[[BranchPhone](#schemabranchphone)]|false|none|Listagem de telefones da Dependência própria|
|services|[[BranchService](#schemabranchservice)]|true|none|Traz a relação de serviços disponbilizados pelo Canal de Atendimento|

<h2 id="tocS_BranchPostalAddress">BranchPostalAddress</h2>
<!-- backwards compatibility -->
<a id="schemabranchpostaladdress"></a>
<a id="schema_BranchPostalAddress"></a>
<a id="tocSbranchpostaladdress"></a>
<a id="tocsbranchpostaladdress"></a>

```json
{
  "address": "Av Naburo Ykesaki 1270, bloco 35, fundos",
  "additionalInfo": "Loja B",
  "districtName": "Centro",
  "townName": "São Paulo",
  "ibgeCode": "3550308",
  "countrySubDivision": "SP",
  "postCode": "17500001",
  "country": "Brasil",
  "countryCode": "BRA",
  "geographicCoordinates": {
    "latitude": "-90.8365180",
    "longitude": "-180.836519"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|address|string|true|none|Deverá trazer toda a informação referente ao endereço da dependência informada. Tipo de logradouro + Nome do logradouro + Número do Logradouro (se não existir usar ' s/n') + complemento (se houver).|
|additionalInfo|string|false|none|Alguns logradouros ainda necessitam ser especificados por meio de complemento, conforme o exemplo a seguir.|
|districtName|string|true|none|Bairro é uma comunidade ou região localizada em uma cidade ou município de acordo com as suas subdivisões geográficas.|
|townName|string|true|none|O nome da localidade corresponde à designação da cidade ou município no qual o endereço está localizado.|
|ibgeCode|string|true|none|Código IBGE de Município. A Tabela de Códigos de Municípios do IBGE apresenta a lista dos municípios brasileiros associados a um código composto de 7 dígitos, sendo os dois primeiros referentes ao código da Unidade da Federação.|
|countrySubDivision|string|true|none|Enumeração referente a cada sigla da unidade da federação que identifica o estado ou o distrito federal, no qual o endereço está localizado. São consideradas apenas as siglas para os estados brasileiros.|
|postCode|string|true|none|Código de Endereçamento Postal. Composto por um conjunto numérico de oito dígitos, o objetivo principal do CEP é orientar e acelerar o encaminhamento, o tratamento e a entrega de objetos postados nos Correios, por meio da sua atribuição a localidades, logradouros, unidades dos Correios, serviços, órgãos públicos, empresas e edifícios.|
|country|string|false|none|Nome do país.|
|countryCode|string|false|none|Código do país de acordo com o código “alpha3” do ISO-3166.|
|geographicCoordinates|[BranchesGeographicCoordinates](#schemabranchesgeographiccoordinates)|false|none|Informação referente a geolocalização informada.|

<h2 id="tocS_BranchIdentification">BranchIdentification</h2>
<!-- backwards compatibility -->
<a id="schemabranchidentification"></a>
<a id="schema_BranchIdentification"></a>
<a id="tocSbranchidentification"></a>
<a id="tocsbranchidentification"></a>

```json
{
  "type": "POSTO_ATENDIMENTO",
  "code": "0001",
  "checkDigit": "9",
  "name": "Marília"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|false|none|Tipo de dependência.|
|code|string|false|none|Código identificador da dependência|
|checkDigit|string|false|none|Dígito verificador do código da dependência|
|name|string|false|none|Nome da dependência|

#### Enumerated Values

|Property|Value|
|---|---|
|type|POSTO_ATENDIMENTO|
|type|UNIDADE_ADMINISTRATIVA_DESMEMBRADA|

<h2 id="tocS_BranchAvailability">BranchAvailability</h2>
<!-- backwards compatibility -->
<a id="schemabranchavailability"></a>
<a id="schema_BranchAvailability"></a>
<a id="tocSbranchavailability"></a>
<a id="tocsbranchavailability"></a>

```json
{
  "standards": [
    {
      "weekday": "SEGUNDA_FEIRA",
      "openingTime": "10:00:57Z",
      "closingTime": "16:00:57Z"
    }
  ],
  "exception": "string",
  "isPublicAccessAllowed": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|standards|[any]|true|none|Lista disponibilidade padrão da depêndencia próprias por dias da semana|
|» weekday|string|true|none|Dia da semana de abertura da dependência|
|» openingTime|string|true|none|Horário de abertura da dependência (UTC)|
|» closingTime|string|true|none|Horário de fechamento da dependência (UTC)|
|exception|string|false|none|Em campo texto devem ser registradas todas as Exceções para o não atendimento.|
|isPublicAccessAllowed|boolean|false|none|Indica se a instalação da Dependência tem acesso restrito a clientes.|

#### Enumerated Values

|Property|Value|
|---|---|
|weekday|DOMINGO|
|weekday|SEGUNDA_FEIRA|
|weekday|TERCA_FEIRA|
|weekday|QUARTA_FEIRA|
|weekday|QUINTA_FEIRA|
|weekday|SEXTA_FEIRA|
|weekday|SABADO|

<h2 id="tocS_EletronicChannelsAvailability">EletronicChannelsAvailability</h2>
<!-- backwards compatibility -->
<a id="schemaeletronicchannelsavailability"></a>
<a id="schema_EletronicChannelsAvailability"></a>
<a id="tocSeletronicchannelsavailability"></a>
<a id="tocseletronicchannelsavailability"></a>

```json
{
  "standards": [
    {
      "weekday": "SEGUNDA_FEIRA",
      "openingTime": "10:00:57Z",
      "closingTime": "16:00:57Z"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|standards|[any]|true|none|Lista disponibilidade padrão da depêndencia próprias por dias da semana|
|» weekday|string|true|none|Dias de funcionamento em formato texto|
|» openingTime|string|true|none|Horário padrão de início de atendimento do canal eletrônico. (UTC)|
|» closingTime|string|true|none|Horário padrão de encerramento de atendimento do canal eletrônico (UTC)|

#### Enumerated Values

|Property|Value|
|---|---|
|weekday|DOMINGO|
|weekday|SEGUNDA_FEIRA|
|weekday|TERCA_FEIRA|
|weekday|QUARTA_FEIRA|
|weekday|QUINTA_FEIRA|
|weekday|SEXTA_FEIRA|
|weekday|SABADO|

<h2 id="tocS_PhoneChannelsAvailability">PhoneChannelsAvailability</h2>
<!-- backwards compatibility -->
<a id="schemaphonechannelsavailability"></a>
<a id="schema_PhoneChannelsAvailability"></a>
<a id="tocSphonechannelsavailability"></a>
<a id="tocsphonechannelsavailability"></a>

```json
{
  "standards": [
    {
      "weekday": "SEGUNDA_FEIRA",
      "openingTime": "10:00:57Z",
      "closingTime": "16:00:57Z"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|standards|[any]|true|none|Lista disponibilidade padrão da depêndencia próprias por dias da semana|
|» weekday|string|true|none|Dia da semana de abertura da dependência|
|» openingTime|string|true|none|Horário de abertura da dependência (UTC)|
|» closingTime|string|true|none|Horário de fechamento da dependência (UTC)|

#### Enumerated Values

|Property|Value|
|---|---|
|weekday|DOMINGO|
|weekday|SEGUNDA_FEIRA|
|weekday|TERCA_FEIRA|
|weekday|QUARTA_FEIRA|
|weekday|QUINTA_FEIRA|
|weekday|SEXTA_FEIRA|
|weekday|SABADO|

<h2 id="tocS_BranchService">BranchService</h2>
<!-- backwards compatibility -->
<a id="schemabranchservice"></a>
<a id="schema_BranchService"></a>
<a id="tocSbranchservice"></a>
<a id="tocsbranchservice"></a>

```json
{
  "name": "ENDOSSO",
  "code": "01"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome dos Serviços efetivamente prestados pelo Canal de Atendimento|
|code|string|true|none|Código dos Serviços efetivamente prestados pelo Canal de Atendimento|

#### Enumerated Values

|Property|Value|
|---|---|
|name|ALTERACOES_FORMA_PAGAMENTO|
|name|AVISO_SINISTRO|
|name|CANCELAMENTO_SUSPENSAO_PAGAMENTO_PREMIOS_CONTRIBUICAO|
|name|EFETIVACAO_APORTE|
|name|ENDOSSO|
|name|ENVIO_DOCUMENTOS|
|name|INFORMACOES_GERAIS_DUVIDAS|
|name|INFORMACOES_INTERMEDIARIOS|
|name|INFORMACOES_SOBRE_SERVICOS_ASSISTENCIAS|
|name|INFORMACOES_SOBRE_SORTEIOS|
|name|OUVIDORIA_RECEPCAO_SUGESTOES_ELOGIOS|
|name|OUVIDORIA_SOLUCAO_EVENTUAIS_DIVERGENCIAS_SOBRE_CONTRATO_SEGURO_CAPITALIZAÇÃO_PREVIDÊNCIA_APOS_ESGOTADOS_CANAIS_REGULARES_ATENDIMENTO_AQUELAS_ORIUNDAS_ORGAOS_REGULADORES_OU_INTEGRANTES_SISTEMA_NACIONAL_DEFESA_CONSUMIDOR|
|name|OUVIDORIA_TRATAMENTO_INSATISFACAO_CONSUMIDOR_RELACAO_ATENDIMENTO_RECEBIDO_CANAIS_REGULARES_ATENDIMENTO|
|name|OUVIDORIA_TRATAMENTO_RECLAMACOES_SOBRE_IRREGULARDADES_CONDUTA_COMPANHIA|
|name|PORTABILIDADE|
|name|RECLAMACAO|
|name|RESGATE|
|name|SEGUNDA_VIA_DOCUMENTOS_CONTRATUAIS|
|name|SUGESTOES_ELOGIOS|
|code|01|
|code|02|
|code|03|
|code|04|
|code|05|
|code|06|
|code|07|
|code|08|
|code|09|
|code|10|
|code|11|
|code|12|
|code|13|
|code|14|
|code|15|
|code|16|
|code|17|
|code|18|
|code|19|

<h2 id="tocS_ElectronicChannels">ElectronicChannels</h2>
<!-- backwards compatibility -->
<a id="schemaelectronicchannels"></a>
<a id="schema_ElectronicChannels"></a>
<a id="tocSelectronicchannels"></a>
<a id="tocselectronicchannels"></a>

```json
{
  "identification": {
    "type": "CHAT",
    "accessType": "EMAIL",
    "urls": [
      "string"
    ]
  },
  "services": [
    {
      "name": "ALTERACACOES_FORMA_PAGAMENTO",
      "code": "01",
      "additionalInfo": "SIC"
    }
  ],
  "availability": {
    "standards": [
      {
        "weekday": "SEGUNDA_FEIRA",
        "openingTime": "10:00:57Z",
        "closingTime": "16:00:57Z"
      }
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|identification|[ElectronicChannelsIdentification](#schemaelectronicchannelsidentification)|true|none|none|
|services|[[ElectronicChannelsServices](#schemaelectronicchannelsservices)]|true|none|Traz a relação de serviços disponbilizados pelo Canal de Atendimento|
|availability|[EletronicChannelsAvailability](#schemaeletronicchannelsavailability)|false|none|none|

<h2 id="tocS_ElectronicChannelsIdentification">ElectronicChannelsIdentification</h2>
<!-- backwards compatibility -->
<a id="schemaelectronicchannelsidentification"></a>
<a id="schema_ElectronicChannelsIdentification"></a>
<a id="tocSelectronicchannelsidentification"></a>
<a id="tocselectronicchannelsidentification"></a>

```json
{
  "type": "CHAT",
  "accessType": "EMAIL",
  "urls": [
    "string"
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|true|none|Tipo de canal de atendimento eletrônico|
|accessType|string|false|none|Tipo de acesso|
|urls|[[ElectronicChannelsUrl](#schemaelectronicchannelsurl)]|true|none|Lista das URLs que atendem um tipo de canal eletrônico selecionado|

#### Enumerated Values

|Property|Value|
|---|---|
|type|INTERNET|
|type|MOBILE|
|type|CHAT|
|type|WHATSAPP|
|type|CONSUMIDOR|
|type|OUTROS|
|accessType|EMAIL|
|accessType|INTERNET|
|accessType|APP|
|accessType|CHAT|
|accessType|WHATSAPP|
|accessType|CONSUMIDOR|
|accessType|OUTROS|

<h2 id="tocS_ElectronicChannelsUrl">ElectronicChannelsUrl</h2>
<!-- backwards compatibility -->
<a id="schemaelectronicchannelsurl"></a>
<a id="schema_ElectronicChannelsUrl"></a>
<a id="tocSelectronicchannelsurl"></a>
<a id="tocselectronicchannelsurl"></a>

```json
"string"

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|string|false|none|none|

<h2 id="tocS_ElectronicChannelsServices">ElectronicChannelsServices</h2>
<!-- backwards compatibility -->
<a id="schemaelectronicchannelsservices"></a>
<a id="schema_ElectronicChannelsServices"></a>
<a id="tocSelectronicchannelsservices"></a>
<a id="tocselectronicchannelsservices"></a>

```json
{
  "name": "ALTERACACOES_FORMA_PAGAMENTO",
  "code": "01",
  "additionalInfo": "SIC"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome dos Serviços efetivamente prestados pelo Canal de Atendimento|
|code|string|true|none|Código dos Serviços efetivamente prestados pelo Canal de Atendimento|
|additionalInfo|string|false|none|Texto livre para complementar informação relativa ao Serviço disponível, quando for selecionada a opção 'OUTROS_PRODUTOS_SERVICOS'|

#### Enumerated Values

|Property|Value|
|---|---|
|name|ALTERACACOES_FORMA_PAGAMENTO|
|name|AVISO_SINISTRO|
|name|CANCELAMENTO_SUSPENSAO_PAGAMENTO_PREMIOS_CONTRIBUICAO|
|name|EFETIVACAO_APORTE|
|name|ENDOSSO|
|name|ENVIO_DOCUMENTOS|
|name|INFORMACOES_GERAIS_DUVIDAS|
|name|INFORMACOES_INTERMEDIARIOS|
|name|INFORMACOES_SOBRE_SERVICOS_ASSISTENCIAS|
|name|INFORMACOES_SOBRE_SORTEIOS|
|name|OUVIDORIA_RECEPCAO_SUGESTOES_ELOGIOS|
|name|OUVIDORIA_SOLUCAO_EVENTUAIS_DIVERGENCIAS_SOBRE_CONTRATO_SEGURO_CAPITALIZAÇÃO_PREVIDÊNCIA_APOS_ESGOTADOS_CANAIS_REGULARES_ATENDIMENTO_AQUELAS_ORIUNDAS_ORGAOS_REGULADORES_OU_INTEGRANTES_SISTEMA_NACIONAL_DEFESA_CONSUMIDOR|
|name|OUVIDORIA_TRATAMENTO_INSATISFACAO_CONSUMIDOR_RELACAO_ATENDIMENTO_RECEBIDO_CANAIS_REGULARES_ATENDIMENTO|
|name|OUVIDORIA_TRATAMENTO_RECLAMACOES_SOBRE_IRREGULARDADES_CONDUTA_COMPANHIA|
|name|PORTABILIDADE|
|name|RECLAMACAO|
|name|RESGATE|
|name|SEGUNDA_VIA_DOCUMENTOS_CONTRATUAIS|
|name|SUGESTOES_ELOGIOS|
|code|01|
|code|02|
|code|03|
|code|04|
|code|05|
|code|06|
|code|07|
|code|08|
|code|09|
|code|10|
|code|11|
|code|12|
|code|13|
|code|14|
|code|15|
|code|16|
|code|17|
|code|18|
|code|19|

<h2 id="tocS_BranchPhone">BranchPhone</h2>
<!-- backwards compatibility -->
<a id="schemabranchphone"></a>
<a id="schema_BranchPhone"></a>
<a id="tocSbranchphone"></a>
<a id="tocsbranchphone"></a>

```json
{
  "type": "FIXO",
  "countryCallingCode": "55",
  "areaCode": "19",
  "number": "35721199"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|false|none|Identificação do Tipo de telefone da dependência. p.ex.FIXO, MOVEL.|
|countryCallingCode|string|false|none|Número de DDI (Discagem Direta Internacional) para  telefone de acesso ao Canal - se houver. p.ex. '55'|
|areaCode|string|false|none|Número de DDD (Discagem Direta à Distância) do telefone da dependência - se houver. p.ex. '19'|
|number|string|false|none|Número de telefone da dependência - se houver|

#### Enumerated Values

|Property|Value|
|---|---|
|type|FIXO|
|type|MOVEL|

<h2 id="tocS_ResponsePhoneChannelsList">ResponsePhoneChannelsList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsephonechannelslist"></a>
<a id="schema_ResponsePhoneChannelsList"></a>
<a id="tocSresponsephonechannelslist"></a>
<a id="tocsresponsephonechannelslist"></a>

```json
{
  "data": {
    "brand": {
      "name": "Organização A",
      "companies": [
        {
          "name": "Empresa A1",
          "cnpjNumber": "45086338000178",
          "urlComplementaryList": "https://empresaa1.com/branches-insurance",
          "phoneChannels": [
            {
              "identification": {
                "type": "CENTRAL_TELEFONICA",
                "phones": [
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "35721199"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "997865532"
                  }
                ]
              },
              "services": [
                {
                  "name": "ALTERACOES_FORMA_PAGAMENTO",
                  "code": "01"
                },
                {
                  "name": "AVISO_SINISTRO",
                  "code": "02"
                },
                {
                  "name": "ENDOSSO",
                  "code": "05"
                }
              ]
            },
            {
              "identification": {
                "type": "SAC",
                "phones": [
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40044828",
                    "additionalInfo": "DDI '55'; DDD '11', 40044828, 'Para clientes no exterior'"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40044828",
                    "additionalInfo": "DDI '55'; DDD '11', 40044828, 'Para clientes no exterior'"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40044828",
                    "additionalInfo": "DDI '55'; DDD '11', 40044828, 'Para clientes no exterior'"
                  }
                ]
              },
              "services": [
                {
                  "name": "RECLAMACAO",
                  "code": "16"
                },
                {
                  "name": "PORTABILIDADE",
                  "code": "15"
                },
                {
                  "name": "ENDOSSO",
                  "code": "05"
                }
              ]
            },
            {
              "identification": {
                "type": "OUVIDORIA",
                "phones": [
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40045555"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40045555"
                  },
                  {
                    "countryCallingCode": "55",
                    "areaCode": "14",
                    "number": "40045555"
                  }
                ]
              },
              "services": [
                {
                  "name": "RECLAMACAO",
                  "code": "16"
                },
                {
                  "name": "PORTABILIDADE",
                  "code": "15"
                }
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels",
    "first": "https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels",
    "prev": "null",
    "next": "null",
    "last": "https://api.organizacao.com.br/open-insurance/channels/v1/phone-channels"
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
|» brand|[PhoneChannelsBrand](#schemaphonechannelsbrand)|true|none|none|
|links|[LinksPaginated](#schemalinkspaginated)|true|none|none|
|meta|[MetaPaginated](#schemametapaginated)|true|none|none|

<h2 id="tocS_PhoneChannelsBrand">PhoneChannelsBrand</h2>
<!-- backwards compatibility -->
<a id="schemaphonechannelsbrand"></a>
<a id="schema_PhoneChannelsBrand"></a>
<a id="tocSphonechannelsbrand"></a>
<a id="tocsphonechannelsbrand"></a>

```json
{
  "name": "Marca A",
  "companies": [
    {
      "name": "Empresa da Marca A",
      "cnpjNumber": "45086338000178",
      "phoneChannels": [
        {
          "identification": {
            "type": "OUVIDORIA",
            "phones": [
              {
                "countryCallingCode": "55",
                "areaCode": "19",
                "number": "08007787788"
              }
            ]
          },
          "services": [
            {
              "name": "AVISO_SINISTRO",
              "code": "01"
            }
          ],
          "availability": {
            "standards": [
              {
                "weekday": "SEGUNDA_FEIRA",
                "openingTime": "10:00:57Z",
                "closingTime": "16:00:57Z"
              }
            ]
          }
        }
      ]
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da Marca reportada pelo participante do Open Insurance. O conceito a que se refere a 'marca' utilizada está em definição pelos participantes.|
|companies|[[PhoneChannelsCompanies](#schemaphonechannelscompanies)]|true|none|Lista de instituições pertencentes à marca|

<h2 id="tocS_PhoneChannelsCompanies">PhoneChannelsCompanies</h2>
<!-- backwards compatibility -->
<a id="schemaphonechannelscompanies"></a>
<a id="schema_PhoneChannelsCompanies"></a>
<a id="tocSphonechannelscompanies"></a>
<a id="tocsphonechannelscompanies"></a>

```json
{
  "name": "Empresa da Marca A",
  "cnpjNumber": "45086338000178",
  "phoneChannels": [
    {
      "identification": {
        "type": "OUVIDORIA",
        "phones": [
          {
            "countryCallingCode": "55",
            "areaCode": "19",
            "number": "08007787788"
          }
        ]
      },
      "services": [
        {
          "name": "AVISO_SINISTRO",
          "code": "01"
        }
      ],
      "availability": {
        "standards": [
          {
            "weekday": "SEGUNDA_FEIRA",
            "openingTime": "10:00:57Z",
            "closingTime": "16:00:57Z"
          }
        ]
      }
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da Instituição, pertencente à organização, responsável pelo Canal Telefônico.|
|cnpjNumber|string|true|none|Número completo do CNPJ da instituição responsável pela dependência - o CNPJ corresponde ao número de inscrição no Cadastro de Pessoa Jurídica.<br>Deve-se ter apenas os números do CNPJ, sem máscara|
|phoneChannels|[[PhoneChannels](#schemaphonechannels)]|true|none|Lista  de canais de atendimento telefônico|

<h2 id="tocS_PhoneChannels">PhoneChannels</h2>
<!-- backwards compatibility -->
<a id="schemaphonechannels"></a>
<a id="schema_PhoneChannels"></a>
<a id="tocSphonechannels"></a>
<a id="tocsphonechannels"></a>

```json
{
  "identification": {
    "type": "OUVIDORIA",
    "phones": [
      {
        "countryCallingCode": "55",
        "areaCode": "19",
        "number": "08007787788"
      }
    ]
  },
  "services": [
    {
      "name": "AVISO_SINISTRO",
      "code": "01"
    }
  ],
  "availability": {
    "standards": [
      {
        "weekday": "SEGUNDA_FEIRA",
        "openingTime": "10:00:57Z",
        "closingTime": "16:00:57Z"
      }
    ]
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|identification|[PhoneChannelsIdentification](#schemaphonechannelsidentification)|true|none|none|
|services|[[PhoneChannelsServices](#schemaphonechannelsservices)]|true|none|Traz a relação de serviços disponbilizados pelo Canal de Atendimento|
|availability|[PhoneChannelsAvailability](#schemaphonechannelsavailability)|false|none|none|

<h2 id="tocS_PhoneChannelsIdentification">PhoneChannelsIdentification</h2>
<!-- backwards compatibility -->
<a id="schemaphonechannelsidentification"></a>
<a id="schema_PhoneChannelsIdentification"></a>
<a id="tocSphonechannelsidentification"></a>
<a id="tocsphonechannelsidentification"></a>

```json
{
  "type": "OUVIDORIA",
  "phones": [
    {
      "countryCallingCode": "55",
      "areaCode": "19",
      "number": "08007787788"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|type|string|true|none|Tipo de canal telefônico de atendimento: <br>* `CENTRAL_TELEFONICA` <br>* `SAC` <br>* `OUVIDORIA`|
|phones|[[PhoneChannelsPhones](#schemaphonechannelsphones)]|false|none|Lista de telefones do Canal de Atendimento|

#### Enumerated Values

|Property|Value|
|---|---|
|type|CENTRAL_TELEFONICA|
|type|SAC|
|type|OUVIDORIA|

<h2 id="tocS_PhoneChannelsPhones">PhoneChannelsPhones</h2>
<!-- backwards compatibility -->
<a id="schemaphonechannelsphones"></a>
<a id="schema_PhoneChannelsPhones"></a>
<a id="tocSphonechannelsphones"></a>
<a id="tocsphonechannelsphones"></a>

```json
{
  "countryCallingCode": "55",
  "areaCode": "19",
  "number": "08007787788"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|countryCallingCode|string|true|none|Número de DDI (Discagem Direta Internacional) para telefone de acesso ao Canal - se houver.|
|areaCode|string|true|none|Número de DDD (Discagem Direta à Distância) para telefone de acesso ao Canal - se houver.|
|number|string|true|none|Número de telefone de acesso ao canal.|

<h2 id="tocS_PhoneChannelsServices">PhoneChannelsServices</h2>
<!-- backwards compatibility -->
<a id="schemaphonechannelsservices"></a>
<a id="schema_PhoneChannelsServices"></a>
<a id="tocSphonechannelsservices"></a>
<a id="tocsphonechannelsservices"></a>

```json
{
  "name": "AVISO_SINISTRO",
  "code": "01"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome dos Serviços efetivamente prestados pelo Canal de Atendimento|
|code|string|true|none|Código dos Serviços efetivamente prestados pelo Canal de Atendimento|

#### Enumerated Values

|Property|Value|
|---|---|
|name|ALTERACOES_FORMA_PAGAMENTO|
|name|AVISO_SINISTRO|
|name|CANCELAMENTO_SUSPENSAO_PAGAMENTO_PREMIOS_CONTRIBUICAO|
|name|EFETIVACAO_APORTE|
|name|ENDOSSO|
|name|ENVIO_DOCUMENTOS|
|name|INFORMACOES_GERAIS_DUVIDAS|
|name|INFORMACOES_INTERMEDIARIOS|
|name|INFORMACOES_SOBRE_SERVICOS_ASSISTENCIAS|
|name|INFORMACOES_SOBRE_SORTEIOS|
|name|OUVIDORIA_RECEPCAO_SUGESTOES_ELOGIOS|
|name|OUVIDORIA_SOLUCAO_EVENTUAIS_DIVERGENCIAS_SOBRE_CONTRATO_SEGURO_CAPITALIZAÇÃO_PREVIDÊNCIA_APOS_ESGOTADOS_CANAIS_REGULARES_ATENDIMENTO_AQUELAS_ORIUNDAS_ORGAOS_REGULADORES_OU_INTEGRANTES_SISTEMA_NACIONAL_DEFESA_CONSUMIDOR|
|name|OUVIDORIA_TRATAMENTO_INSATISFACAO_CONSUMIDOR_RELACAO_ATENDIMENTO_RECEBIDO_CANAIS_REGULARES_ATENDIMENTO|
|name|OUVIDORIA_TRATAMENTO_RECLAMACOES_SOBRE_IRREGULARDADES_CONDUTA_COMPANHIA|
|name|PORTABILIDADE|
|name|RECLAMACAO|
|name|RESGATE|
|name|SEGUNDA_VIA_DOCUMENTOS_CONTRATUAIS|
|name|SUGESTOES_ELOGIOS|
|code|01|
|code|02|
|code|03|
|code|04|
|code|05|
|code|06|
|code|07|
|code|08|
|code|09|
|code|10|
|code|11|
|code|12|
|code|13|
|code|14|
|code|15|
|code|16|
|code|17|
|code|18|
|code|19|

<h2 id="tocS_BranchesGeographicCoordinates">BranchesGeographicCoordinates</h2>
<!-- backwards compatibility -->
<a id="schemabranchesgeographiccoordinates"></a>
<a id="schema_BranchesGeographicCoordinates"></a>
<a id="tocSbranchesgeographiccoordinates"></a>
<a id="tocsbranchesgeographiccoordinates"></a>

```json
{
  "latitude": "-90.8365180",
  "longitude": "-180.836519"
}

```

Informação referente a geolocalização informada.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|latitude|string|false|none|Informação da latitude referente a geolocalização informada. Entre -90 e 90. Formato númerico 2 casas antes da vírgula, 11 posições.|
|longitude|string|false|none|Informação da longitude referente a geolocalização informada. Formato númerico 3 casas antes da vírgula, 11 posições.|

<h2 id="tocS_LinksPaginated">LinksPaginated</h2>
<!-- backwards compatibility -->
<a id="schemalinkspaginated"></a>
<a id="schema_LinksPaginated"></a>
<a id="tocSlinkspaginated"></a>
<a id="tocslinkspaginated"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>",
  "first": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/channels/v1/<resource>"
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

<h2 id="tocS_MetaPaginated">MetaPaginated</h2>
<!-- backwards compatibility -->
<a id="schemametapaginated"></a>
<a id="schema_MetaPaginated"></a>
<a id="tocSmetapaginated"></a>
<a id="tocsmetapaginated"></a>

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

<h2 id="tocS_ResponseError">ResponseError</h2>
<!-- backwards compatibility -->
<a id="schemaresponseerror"></a>
<a id="schema_ResponseError"></a>
<a id="tocSresponseerror"></a>
<a id="tocsresponseerror"></a>

```json
{
  "errors": [
    {
      "code": "string",
      "title": "string",
      "detail": "string",
      "requestDateTime": "2021-08-20T08:30:00Z"
    }
  ],
  "meta": {
    "totalRecords": 1,
    "totalPages": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|errors|[object]|true|none|none|
|» code|string|true|none|Código de erro específico do endpoint|
|» title|string|true|none|Título legível por humanos deste erro específico|
|» detail|string|true|none|Descrição legível por humanos deste erro específico|
|» requestDateTime|string(date-time)|true|none|Data e hora da consulta, conforme especificação RFC-3339, formato UTC.|
|meta|[MetaPaginated](#schemametapaginated)|false|none|none|

