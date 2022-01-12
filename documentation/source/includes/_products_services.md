<!-- Generator: Widdershins v4.0.1 -->

# API - Produtos e serviços v1.0.0

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

As APIs descritas neste documento são referentes as APIs da fase Open Data do Open Insurance Brasil.

Base URLs:

* <a href="https://api.organizacao.com.br/open-insurance/products-services/v1">https://api.organizacao.com.br/open-insurance/products-services/v1</a>

Web: <a href="https://openinsurance.susep.gov.br">Support</a> 

## life-pension

### Obtém a lista dos produtos do tipo vida e previdência.

<a id="opIdgetLifePension"></a>

<a href="files/swagger/life-pension.yaml">Especificação em OAS</a> <br>

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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/products-services/v1/life-pension");
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

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = {
    'Accept': "application/json",
    'cache-control': "string",
    'Content-Security-Policy': "string",
    'content-Type': "string",
    'Strict-Transport-Security': "string",
    'X-Content-Type-Options': "string",
    'X-Frame-Options': "string"
    }

conn.request("GET", "/open-insurance/products-services/v1/life-pension", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/products-services/v1/life-pension")
  .header("Accept", "application/json")
  .header("cache-control", "string")
  .header("Content-Security-Policy", "string")
  .header("content-Type", "string")
  .header("Strict-Transport-Security", "string")
  .header("X-Content-Type-Options", "string")
  .header("X-Frame-Options", "string")
  .asString();
```

`GET /life-pension`

Obtém a lista dos produtos do tipo vida e previdência.

<h3 id="obtém-a-lista-dos-produtos-do-tipo-vida-e-previdência.-parameters">Parameters</h3>

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

> Example responses

> 200 Response

```json
[
  {
    "identification": {
      "brand": "Brasilprev",
      "societyName": "Brasilprev Seguros e Previdência S.A",
      "cnpjNumber": "27665207000131"
    },
    "products": [
      {
        "name": "Brasilprev Private Multimercado 2020",
        "code": "1234",
        "segment": "PREVIDENCIA",
        "type": "PGBL",
        "modality": "CONTRIBUICAO_VARIAVEL",
        "optionalCoverage": "string",
        "productDetails": [
          {
            "susepProcessNumber": "15414.614141/2020-71",
            "contractTermsConditions": "https://example.com/mobilebanking",
            "defferalPeriod": {
              "interestRate": 0.25123,
              "updateIndex": "IPCA",
              "otherMinimumPerformanceGarantees": "SELIC",
              "reversalFinancialResults": 5.123,
              "minimumPremiumAmount": [
                {
                  "minimumPremiumAmountValue": 250,
                  "minimumPremiumAmountDescription": ""
                }
              ],
              "premiumPaymentMethod": [
                "CARTAO_CREDITO"
              ],
              "permissionExtraordinaryContributions": true,
              "permissonScheduledFinancialPayments": true,
              "gracePeriodRedemption": 100,
              "gracePeriodBetweenRedemptionRequests": 30,
              "redemptionPaymentTerm": 10,
              "gracePeriodPortability": 12,
              "gracePeriodBetweenPortabilityRequests": 15,
              "portabilityPaymentTerm": 20,
              "investimentFunds": [
                {
                  "cnpjNumber": "13.456.789/0001-12",
                  "companyName": "EYPREV",
                  "maximumAdministrationFee": 20.1,
                  "typePerformanceFee": [
                    "DIRETAMENTE"
                  ],
                  "maximumPerformanceFee": 20,
                  "eligibilityRule": true,
                  "minimumContributionAmount": 1000,
                  "minimumMathematicalProvisionAmount": 1000
                }
              ]
            },
            "grantPeriodBenefit": {
              "incomeModality": [
                "RENDA_VITALICIA"
              ],
              "biometricTable": [
                "AT_2000_FEMALE_SUAVIZADA_15"
              ],
              "interestRate": 3.225,
              "updateIndex": "IPCA",
              "reversalResultsFinancial": 13.252,
              "investimentFunds": [
                {
                  "cnpjNumber": "13.456.789/0001-12",
                  "companyName": "EYPREV",
                  "maximumAdministrationFee": 20.1,
                  "typePerformanceFee": [
                    "DIRETAMENTE"
                  ],
                  "maximumPerformanceFee": 20,
                  "eligibilityRule": true,
                  "minimumContributionAmount": 1000,
                  "minimumMathematicalProvisionAmount": 1000
                }
              ]
            },
            "costs": {
              "loadingAntecipated": {
                "minValue": 4.122,
                "maxValue": 10
              },
              "loadingLate": {
                "minValue": 4.122,
                "maxValue": 10
              }
            }
          }
        ],
        "minimumRequirements": {
          "contractType": "INDIVIDUAL",
          "participantQualified": true,
          "minRequirementsContract": "https://example.com/mobile-banking"
        },
        "targetAudience": "PESSOA_NATURAL"
      }
    ],
    "links": {
      "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
      "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
      "prev": "string",
      "next": "string",
      "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
    },
    "meta": {
      "totalRecords": 10,
      "totalPages": 1
    }
  }
]
```

<h3 id="obtém-a-lista-dos-produtos-do-tipo-vida-e-previdência.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dados dos produtos de Vida e Previdência|[ResponseLifePensionList](#schemaresponselifepensionlist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|Dados dos produtos de Vida e Previdência|[ResponseLifePensionList](#schemaresponselifepensionlist)|

<aside class="success">
This operation does not require authentication
</aside>

## pension-plan

### Obtém informações de plano de previdência com cobertura de risco

<a id="opIdgetPensionPlan"></a>

<a href="files/swagger/pension-plan.yaml">Especificação em OAS</a> <br>

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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/products-services/v1/pension-plan/");
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

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = {
    'Accept': "application/json",
    'cache-control': "string",
    'Content-Security-Policy': "string",
    'content-Type': "string",
    'Strict-Transport-Security': "string",
    'X-Content-Type-Options': "string",
    'X-Frame-Options': "string"
    }

conn.request("GET", "/open-insurance/products-services/v1/pension-plan/", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/products-services/v1/pension-plan/")
  .header("Accept", "application/json")
  .header("cache-control", "string")
  .header("Content-Security-Policy", "string")
  .header("content-Type", "string")
  .header("Strict-Transport-Security", "string")
  .header("X-Content-Type-Options", "string")
  .header("X-Frame-Options", "string")
  .asString();
```

`GET /pension-plan/`

Obtém informações de plano de previdência com cobertura de risco

<h3 id="obtém-informações-de-plano-de-previdência-com-cobertura-de-risco-parameters">Parameters</h3>

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

> Example responses

> 200 Response

```json
{
  "requestTime": "2021-08-20T08:30:00Z",
  "data": {},
  "brand": {
    "name": "EMPRESA",
    "companies": {
      "name": "EMPRESA Seguros",
      "cnpjNumber": 45086338000178,
      "products": [
        {
          "name": "Nome comercial do Produto",
          "code": "123456789_cap",
          "modality": "PENSAO",
          "coverages": [
            {
              "coverage": "INVALIDEZ",
              "coveragesAttributes": {
                "indenizationPaymentMethod": "Pagamento Único",
                "minValue": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "maxValue": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "indemnifiablePeriod": "Prazo",
                "indemnifiableDeadline": 48,
                "currency": "BRL",
                "gracePeriod": {
                  "amount": 0,
                  "unit": "DIAS"
                },
                "excludedRisk": [
                  "ATO_RECONHECIMENTO_PERIGOSO"
                ],
                "excludedRiskURL": "string"
              },
              "coveragePeriod": "Vitalícia"
            }
          ],
          "additional": "SORTEIO",
          "additionalOthers": "string",
          "assistanceType": [
            "Funeral"
          ],
          "assistanceTypeOthers": [
            "string"
          ],
          "termAndCondition": [
            {
              "susepProcessNumber": "15414.622222/2222-22",
              "definition": "wwww.seguradora.com.br/termos"
            }
          ],
          "updatePMBaC": {
            "interestRate": 14,
            "updateIndex": "IPCA(IBGE)"
          },
          "premiumUpdateIndex": "IPCA",
          "ageReframing": {
            "reframingCriterion": "Após período em anos",
            "reframingPeriodicity": 10
          },
          "financialRegimeContractType": "Repartição Simples",
          "reclaim": {
            "reclaimTable": [
              {
                "initialMonthRange": 0,
                "finalMonthRange": 0,
                "percentage": "string"
              }
            ],
            "differentiatedPercentage": "string",
            "gracePeriod": "20/Não se aplica"
          },
          "otherGuarateedValues": "Saldamento",
          "profitModality": "PAGAMENTO_UNICO",
          "contributionPayment": {
            "contributionPaymentMethod": [
              "Cartão de crédito"
            ],
            "contributionPeriodicity": [
              "Mensal"
            ]
          },
          "contributionTax": "string",
          "minimumRequirements": {
            "minRequirementsContractType": "Individual",
            "minRequirementsContract": "wwww.seguradora.com.br/termos"
          },
          "targetAudience": "Pessoa Natural"
        }
      ]
    }
  },
  "linksPaginated": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "metaPaginated": {
    "totalRecords": 10,
    "totalPages": 1
  }
}
```

<h3 id="obtém-informações-de-plano-de-previdência-com-cobertura-de-risco-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dados dos Plano de Previdência com cobertura de risco|[ResponsePensionPlanList](#schemaresponsepensionplanlist)|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|A operação resulta na criação de um novo recurso.|None|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|none|None|
|304|[Not Modified](https://tools.ietf.org/html/rfc7232#section-4.1)|none|None|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|410|[Gone](https://tools.ietf.org/html/rfc7231#section-6.5.9)|none|None|
|415|[Unsupported Media Type](https://tools.ietf.org/html/rfc7231#section-6.5.13)|none|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Se aplicável ao endpoint, espera-se que esse erro resulte em um payload de erro.|None|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|503|[Service Unavailable](https://tools.ietf.org/html/rfc7231#section-6.6.4)|none|None|
|504|[Gateway Time-out](https://tools.ietf.org/html/rfc7231#section-6.6.5)|Retornado se ocorreu um tempo limite, mas um reenvio da solicitação original é viável (caso contrário, use 500 Internal Server Error).|None|
|default|Default|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## person

### Obtém a lista dos produtos do tipo seguro de pessoas.

<a id="opIdgetPerson"></a>

<a href="files/swagger/person.yaml">Especificação em OAS</a> <br>


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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/products-services/v1/person/");
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

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = {
    'Accept': "application/json",
    'cache-control': "string",
    'Content-Security-Policy': "string",
    'content-Type': "string",
    'Strict-Transport-Security': "string",
    'X-Content-Type-Options': "string",
    'X-Frame-Options': "string"
    }

conn.request("GET", "/open-insurance/products-services/v1/person/", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/products-services/v1/person/")
  .header("Accept", "application/json")
  .header("cache-control", "string")
  .header("Content-Security-Policy", "string")
  .header("content-Type", "string")
  .header("Strict-Transport-Security", "string")
  .header("X-Content-Type-Options", "string")
  .header("X-Frame-Options", "string")
  .asString();
```

`GET /person/`

Obtém a lista dos produtos do tipo seguro de pessoas.

<h3 id="obtém-a-lista-dos-produtos-do-tipo-seguro-de-pessoas.-parameters">Parameters</h3>

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

> Example responses

> 200 Response

```json
{
  "data": {
    "brand": {
      "name": "Marca",
      "companies": [
        {
          "name": "Seguradora",
          "cnpjNumber": 45086338000178,
          "products": [
            {
              "name": "Seguro Pessoal",
              "code": "123456789_cap",
              "category": "TRADICIONAL",
              "insuranceModality": "FUNERAL",
              "coverages": [
                {
                  "coverage": "AUXILIO_CESTA_BASICA",
                  "coverageOthers": [
                    "string"
                  ],
                  "coverageAttributes": {
                    "indemnityPaymentMethod": [],
                    "indemnityPaymentFrequency": [],
                    "minValue": {},
                    "maxValue": {},
                    "indemnifiablePeriod": [],
                    "maximumQtyIndemnifiableInstallments": 0,
                    "currency": "BRL",
                    "gracePeriod": {},
                    "differentiatedGracePeriod": {},
                    "deductibleDays": 0,
                    "differentiatedDeductibleDays": 0,
                    "deductibleBRL": 0,
                    "differentiatedDeductibleBRL": "string",
                    "excludedRisks": [],
                    "excludedRisksURL": "string",
                    "allowApartPurchase": true
                  }
                }
              ],
              "assistanceType": [
                "ACOMPANHANTE_CASO_HOSPITALIZACAO_PROLONGADA"
              ],
              "additional": [
                "SORTEIO"
              ],
              "assistanceTypeOthers": [
                "string"
              ],
              "termsAndConditions": [
                {
                  "susepProcessNumber": "string",
                  "definition": "string"
                }
              ],
              "globalCapital": true,
              "validity": [
                "VITALICIA"
              ],
              "pmbacRemuneration": {
                "interestRate": 0,
                "pmbacUpdateIndex": "IPCA"
              },
              "benefitRecalculation": {
                "benefitRecalculationCriteria": "INDICE",
                "benefitUpdateIndex": "IPCA"
              },
              "ageAdjustment": {
                "criterion": "APOS_PERIODO_EM_ANOS",
                "frequency": 0
              },
              "contractType": "REPARTICAO_SIMPLES",
              "reclaim": {
                "reclaimTable": [
                  {
                    "initialMonthRange": 1,
                    "finalMonthRange": 12,
                    "percentage": 0
                  }
                ],
                "differentiatedPercentage": "string",
                "gracePeriod": {
                  "amount": 60,
                  "unit": "DIAS"
                }
              },
              "otherGuaranteedValues": "SALDAMENTO",
              "allowPortability": true,
              "portabilityGraceTime": 0,
              "indemnityPaymentMethod": [
                "UNICO"
              ],
              "indemnityPaymentIncome": [
                "CERTA"
              ],
              "premiumPayment": {
                "paymentMethod": [
                  "CARTAO_CREDITO"
                ],
                "frequency": [
                  "DIARIA"
                ],
                "premiumTax": "string"
              },
              "minimunRequirements": {
                "contractingType": "COLETIVO",
                "contractingMinRequirement": "string"
              },
              "targetAudience": "PESSOA_NATURAL"
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}
```

<h3 id="obtém-a-lista-dos-produtos-do-tipo-seguro-de-pessoas.-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dados dos Plano de Seguro de Pessoas|[ResponsePersonList](#schemaresponsepersonlist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## auto-insurance

### Obtém informações de seguros de automóveis

<a href="files/swagger/auto-insurance.yaml">Especificação em OAS</a> <br>


<a id="opIdgetAutoInsurance"></a>

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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/products-services/v1/auto-insurance/string/string/string");
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

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = {
    'Accept': "application/json",
    'cache-control': "string",
    'Content-Security-Policy': "string",
    'content-Type': "string",
    'Strict-Transport-Security': "string",
    'X-Content-Type-Options': "string",
    'X-Frame-Options': "string"
    }

conn.request("GET", "/open-insurance/products-services/v1/auto-insurance/string/string/string", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/products-services/v1/auto-insurance/string/string/string")
  .header("Accept", "application/json")
  .header("cache-control", "string")
  .header("Content-Security-Policy", "string")
  .header("content-Type", "string")
  .header("Strict-Transport-Security", "string")
  .header("X-Content-Type-Options", "string")
  .header("X-Frame-Options", "string")
  .asString();
```

`GET /auto-insurance/{commercializationArea}/{fipeCode}/{year}`

Obtém informações de seguros de automóveis

<h3 id="obtém-informações-de-seguros-de-automóveis-parameters">Parameters</h3>

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
|commercializationArea|path|string|true|Area de comercialização.|
|fipeCode|path|string|true|Código FIPE|
|year|path|string|true|Ano de comercialização do veículo|

> Example responses

> 200 Response

```json
{
  "data": {
    "brand": {
      "name": "string",
      "company": [
        {
          "name": "string",
          "cnpjNumber": "string",
          "products": [
            {
              "name": "string",
              "code": "string",
              "coverages": [
                {
                  "coverage": "VIDROS",
                  "coverageDetail": "Roubo total",
                  "coveragePermissionSeparteAcquisition": true,
                  "coverageAttributes": {
                    "minLMI": {},
                    "maxLMI": {},
                    "contractBase": [],
                    "newCarMaximumCalculatingPeriod": 12,
                    "newCarContractBase": [],
                    "fullIndemnityPercentage": {},
                    "deductibleType": [],
                    "fullIndemnityDeductible": true,
                    "deductiblePaymentByCoverage": true,
                    "deductiblePercentage": {},
                    "mandatoryParticipation": "Casco - RCF-V Danos",
                    "geographicScopeCoverage": [],
                    "geographicScopeCoverageOthers": "string"
                  }
                }
              ],
              "carParts": [
                {
                  "carPartCondition": "NOVAS",
                  "carPartType": "ORIGINAIS"
                }
              ],
              "carModels": [
                {
                  "manufacturer": "FORD",
                  "model": "KA",
                  "year": 2018,
                  "fipeCode": "string"
                }
              ],
              "vehicleOvernightZipCode": 1311000,
              "additional": [
                "SORTEIO GRATUITO"
              ],
              "additionalOthers": "string",
              "assistanceServices": [
                {
                  "assistanceServicesPackage": [
                    "ATE_10_SERVICOS"
                  ],
                  "assistanceServicesDetail": "Perda Parcial - Colisão",
                  "chargeTypeSignaling": "GRATUITA"
                }
              ],
              "termsAndConditions": [
                {
                  "susepProcessNumber": "15414.622222/2222-22",
                  "definition": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
                }
              ],
              "terms": [
                "ANUAL"
              ],
              "customerService": [
                "REDE REFERECIADA"
              ],
              "premiumPayment": {
                "paymentMethod": [
                  "CARTÃO DE CRÉDITO"
                ],
                "paymentType": [
                  "PARCELADO"
                ],
                "paymentDetail": "string"
              },
              "minimumRequirements": {
                "contractingType": [
                  "COLETIVO"
                ],
                "contractingMinRequirement": "https://example.com/mobile-banking"
              },
              "targetAudiences": [
                "PESSOA_NATURAL"
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}
```

<h3 id="obtém-informações-de-seguros-de-automóveis-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dados dos Seguros de Automóveis|[ResponseAutoInsuranceList](#schemaresponseautoinsurancelist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## home-insurance

### Obtém informações de seguros residenciais

<a id="opIdgetResidentialInsurance"></a>

<a href="files/swagger/home-insurance.yaml">Especificação em OAS</a> <br>

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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/products-services/v1/home-insurance/commercializationArea/0");
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

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = {
    'Accept': "application/json",
    'cache-control': "string",
    'Content-Security-Policy': "string",
    'content-Type': "string",
    'Strict-Transport-Security': "string",
    'X-Content-Type-Options': "string",
    'X-Frame-Options': "string"
    }

conn.request("GET", "/open-insurance/products-services/v1/home-insurance/commercializationArea/0", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/products-services/v1/home-insurance/commercializationArea/0")
  .header("Accept", "application/json")
  .header("cache-control", "string")
  .header("Content-Security-Policy", "string")
  .header("content-Type", "string")
  .header("Strict-Transport-Security", "string")
  .header("X-Content-Type-Options", "string")
  .header("X-Frame-Options", "string")
  .asString();
```

`GET /home-insurance/commercializationArea/{commercializationArea}`

Obtém informações de seguros redidenciais

<h3 id="obtém-informações-de-seguros-residenciais-parameters">Parameters</h3>

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
|commercializationArea|path|integer|true|Area de comercialização.|

> Example responses

> 200 Response

```json
{
  "data": {
    "brand": {
      "name": "EMPRESA A seguros",
      "company": [
        {
          "name": "ABCDE SEGUROS",
          "cnpjNumber": 12345678901234,
          "products": [
            {
              "name": "RESIDENCIAL XPTO",
              "code": "0000-0",
              "coverages": [
                {
                  "coverageType": "Escritório em Residência",
                  "coverageDetail": "Cobertura especial para escritório residenciais",
                  "coveragePermissionSeparteAquisition": false,
                  "coverageAttributes": {
                    "minLMI": {},
                    "maxLMI": {},
                    "minDeductibleAmount": {},
                    "insuredMandatoryParticipationPercentage": 0
                  }
                }
              ],
              "propertyCharacteristics": [
                {
                  "propertyType": "CASA",
                  "propertyBuildType": "ALVENARIA",
                  "propertyUsageType": "HABITUAL",
                  "destinationInsuredImportance": "PRÉDIO"
                }
              ],
              "propertyZipCode": "1311000",
              "protective": true,
              "additional": [
                "SORTEIO_GRATUITO"
              ],
              "additionalOthers": "string",
              "assistanceServices": [
                {
                  "assistanceServicesPackage": "ATE_10_SERVICOS",
                  "complementaryAssistanceServicesDetail": "reboque pane seca",
                  "chargeTypeSignaling": "GRATUITA"
                }
              ],
              "termsAndConditions": [
                {
                  "susepProcessNumber": "XXXXX.XXXXXX/XXXX-XX",
                  "definition": "https://openinsurance.com.br/aaa"
                }
              ],
              "validity": [
                {
                  "term": "ANUAL",
                  "termOthers": "string"
                }
              ],
              "customerServices": [
                "LIVRE ESCOLHA"
              ],
              "premiumRates": [
                "string"
              ],
              "premiumPayments": [
                {
                  "paymentMethod": "CARTÃO DE CRÉDITO",
                  "paymentMethodDetail": "string",
                  "paymentType": "PAGAMENTO_UNICO"
                }
              ],
              "minimumRequirements": [
                {
                  "contractingType": "COLETIVO",
                  "contractingMinRequirement": "https://openinsurance.com.br/aaa"
                }
              ],
              "targetAudiences": [
                "PESSOA_NATURAL"
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}
```

<h3 id="obtém-informações-de-seguros-residenciais-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dados dos Seguros Residenciais|[ResponseHomeInsuranceList](#schemaresponsehomeinsurancelist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|none|None|

<aside class="success">
This operation does not require authentication
</aside>

## capitalization-title

### Obtém a lista dos produtos do tipo título de capitalização

<a id="opIdcapitalizationTitle"></a>

<a href="files/swagger/capitalization-title.yaml">Especificação em OAS</a> <br>


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

xhr.open("GET", "https://api.organizacao.com.br/open-insurance/products-services/v1/capitalization-title");
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

conn = http.client.HTTPSConnection("api.organizacao.com.br")

headers = {
    'Accept': "application/json",
    'cache-control': "string",
    'Content-Security-Policy': "string",
    'content-Type': "string",
    'Strict-Transport-Security': "string",
    'X-Content-Type-Options': "string",
    'X-Frame-Options': "string"
    }

conn.request("GET", "/open-insurance/products-services/v1/capitalization-title", headers=headers)

res = conn.getresponse()
data = res.read()

print(data.decode("utf-8"))
```

```java
HttpResponse<String> response = Unirest.get("https://api.organizacao.com.br/open-insurance/products-services/v1/capitalization-title")
  .header("Accept", "application/json")
  .header("cache-control", "string")
  .header("Content-Security-Policy", "string")
  .header("content-Type", "string")
  .header("Strict-Transport-Security", "string")
  .header("X-Content-Type-Options", "string")
  .header("X-Frame-Options", "string")
  .asString();
```

`GET /capitalization-title`

Obtém a lista dos produtos do tipo título de capitalização

<h3 id="obtém-a-lista-dos-produtos-do-tipo-título-de-capitalização-parameters">Parameters</h3>

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

> Example responses

> 200 Response

```json
{
  "requestTime": "2021-08-20T08:30:00Z",
  "brand": {
    "name": "ACME seguros",
    "companies": [
      {
        "name": "ACME cap da ACME seguros",
        "cnpjNumber": "12345678901234",
        "product": [
          {
            "name": "ACMEcap",
            "code": "01234589_cap",
            "modality": [
              "TRADICIONAL"
            ],
            "costType": [
              "PAGAMENTO_UNICO"
            ],
            "termsAndConditions": {
              "susepProcessNumber": 15414622222222222,
              "termsRegulations": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
            },
            "quotas": [
              {
                "quota": 10,
                "capitalizationQuota": [
                  10
                ],
                "raffleQuota": [
                  10
                ],
                "chargingQuota": [
                  10
                ]
              }
            ],
            "validity": 48,
            "serieSize": 5000000,
            "capitalizationPeriod": {
              "interestRate": 0.25123,
              "updateIndex": [
                "IPCA"
              ],
              "others": [
                "Índice de atualização"
              ],
              "contributionAmount": {
                "minValue": 500,
                "maxValue": 5000,
                "frequency": "MENSAL",
                "value": 0
              },
              "earlyRedemption": [
                10
              ],
              "redemptionPercentageEndTerm": 100.002,
              "gracePeriodRedemption": 48
            },
            "latePayment": {
              "suspensionPeriod": 10,
              "termExtensionOption": true
            },
            "contributionPayment": {
              "paymentMethod": [
                "CARTAO_CREDITO"
              ],
              "updateIndex": [
                "IPCA"
              ],
              "others": [
                "Índice de atualização"
              ]
            },
            "redemption": {
              "redemption": 151.23
            },
            "raffle": {
              "raffleQty": 10000,
              "timeInterval": [
                "QUINZENAL"
              ],
              "raffleValue": 5,
              "earlySettlementRaffle": true,
              "mandatoryContemplation": true,
              "ruleDescription": "Sorteio às quartas-feiras",
              "minimumContemplationProbability": 0.000001
            },
            "additionalDetails": {
              "additionalDetails": "https://example.com/openinsurance"
            },
            "minimumRequirements": {
              "minimumRequirementDetails": "https://ey.exemplo/capitalizacao/tradicional/PU/requisitos_min",
              "targetAudiences": [
                "PESSOAL_NATURAL"
              ]
            }
          }
        ]
      }
    ]
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}
```

<h3 id="obtém-a-lista-dos-produtos-do-tipo-título-de-capitalização-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Dados dos produtos de Título de Capitalização|[ResponseCapitalizationTitleList](#schemaresponsecapitalizationtitlelist)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|A requisição foi malformada, omitindo atributos obrigatórios, seja no payload ou através de atributos na URL.|[ResponseError](#schemaresponseerror)|
|401|[Unauthorized](https://tools.ietf.org/html/rfc7235#section-3.1)|Cabeçalho de autenticação ausente/inválido ou token inválido|[ResponseError](#schemaresponseerror)|
|403|[Forbidden](https://tools.ietf.org/html/rfc7231#section-6.5.3)|O token tem escopo incorreto ou uma política de segurança foi violada|[ResponseError](#schemaresponseerror)|
|404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|O recurso solicitado não existe ou não foi implementado|[ResponseError](#schemaresponseerror)|
|405|[Method Not Allowed](https://tools.ietf.org/html/rfc7231#section-6.5.5)|O consumidor tentou acessar o recurso com um método não suportado|[ResponseError](#schemaresponseerror)|
|406|[Not Acceptable](https://tools.ietf.org/html/rfc7231#section-6.5.6)|A solicitação continha um cabeçalho Accept diferente dos tipos de mídia permitidos ou um conjunto de caracteres diferente de UTF-8|[ResponseError](#schemaresponseerror)|
|429|[Too Many Requests](https://tools.ietf.org/html/rfc6585#section-4)|A operação foi recusada, pois muitas solicitações foram feitas dentro de um determinado período ou o limite global de requisições concorrentes foi atingido|[ResponseError](#schemaresponseerror)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Ocorreu um erro no gateway da API ou no microsserviço|[ResponseError](#schemaresponseerror)|
|default|Default|Dados dos produtos de Título de Capitalização|[ResponseCapitalizationTitleList](#schemaresponsecapitalizationtitlelist)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_ResponseLifePensionList">ResponseLifePensionList</h2>
<!-- backwards compatibility -->
<a id="schemaresponselifepensionlist"></a>
<a id="schema_ResponseLifePensionList"></a>
<a id="tocSresponselifepensionlist"></a>
<a id="tocsresponselifepensionlist"></a>

```json
[
  {
    "identification": {
      "brand": "Brasilprev",
      "societyName": "Brasilprev Seguros e Previdência S.A",
      "cnpjNumber": "27665207000131"
    },
    "products": [
      {
        "name": "Brasilprev Private Multimercado 2020",
        "code": "1234",
        "segment": "PREVIDENCIA",
        "type": "PGBL",
        "modality": "CONTRIBUICAO_VARIAVEL",
        "optionalCoverage": "string",
        "productDetails": [
          {
            "susepProcessNumber": "15414.614141/2020-71",
            "contractTermsConditions": "https://example.com/mobilebanking",
            "defferalPeriod": {
              "interestRate": 0.25123,
              "updateIndex": "IPCA",
              "otherMinimumPerformanceGarantees": "SELIC",
              "reversalFinancialResults": 5.123,
              "minimumPremiumAmount": [
                {
                  "minimumPremiumAmountValue": 250,
                  "minimumPremiumAmountDescription": ""
                }
              ],
              "premiumPaymentMethod": [
                "CARTAO_CREDITO"
              ],
              "permissionExtraordinaryContributions": true,
              "permissonScheduledFinancialPayments": true,
              "gracePeriodRedemption": 100,
              "gracePeriodBetweenRedemptionRequests": 30,
              "redemptionPaymentTerm": 10,
              "gracePeriodPortability": 12,
              "gracePeriodBetweenPortabilityRequests": 15,
              "portabilityPaymentTerm": 20,
              "investimentFunds": [
                {
                  "cnpjNumber": "13.456.789/0001-12",
                  "companyName": "EYPREV",
                  "maximumAdministrationFee": 20.1,
                  "typePerformanceFee": [
                    "DIRETAMENTE"
                  ],
                  "maximumPerformanceFee": 20,
                  "eligibilityRule": true,
                  "minimumContributionAmount": 1000,
                  "minimumMathematicalProvisionAmount": 1000
                }
              ]
            },
            "grantPeriodBenefit": {
              "incomeModality": [
                "RENDA_VITALICIA"
              ],
              "biometricTable": [
                "AT_2000_FEMALE_SUAVIZADA_15"
              ],
              "interestRate": 3.225,
              "updateIndex": "IPCA",
              "reversalResultsFinancial": 13.252,
              "investimentFunds": [
                {
                  "cnpjNumber": "13.456.789/0001-12",
                  "companyName": "EYPREV",
                  "maximumAdministrationFee": 20.1,
                  "typePerformanceFee": [
                    "DIRETAMENTE"
                  ],
                  "maximumPerformanceFee": 20,
                  "eligibilityRule": true,
                  "minimumContributionAmount": 1000,
                  "minimumMathematicalProvisionAmount": 1000
                }
              ]
            },
            "costs": {
              "loadingAntecipated": {
                "minValue": 4.122,
                "maxValue": 10
              },
              "loadingLate": {
                "minValue": 4.122,
                "maxValue": 10
              }
            }
          }
        ],
        "minimumRequirements": {
          "contractType": "INDIVIDUAL",
          "participantQualified": true,
          "minRequirementsContract": "https://example.com/mobile-banking"
        },
        "targetAudience": "PESSOA_NATURAL"
      }
    ],
    "links": {
      "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
      "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
      "prev": "string",
      "next": "string",
      "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
    },
    "meta": {
      "totalRecords": 10,
      "totalPages": 1
    }
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|identification|[LifePensionIdentification](#schemalifepensionidentification)|true|none|Organização controladora do grupo.|
|products|[LifePensionProduct](#schemalifepensionproduct)|true|none|none|
|links|[LinksPaginated](#schemalinkspaginated)|true|none|none|
|meta|[MetaPaginated](#schemametapaginated)|true|none|none|

<h2 id="tocS_LifePensionIdentification">LifePensionIdentification</h2>
<!-- backwards compatibility -->
<a id="schemalifepensionidentification"></a>
<a id="schema_LifePensionIdentification"></a>
<a id="tocSlifepensionidentification"></a>
<a id="tocslifepensionidentification"></a>

```json
{
  "brand": "Brasilprev",
  "societyName": "Brasilprev Seguros e Previdência S.A",
  "cnpjNumber": "27665207000131"
}

```

Organização controladora do grupo.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|brand|string|true|none|Nome da marca reportada pelo participante do Open Insurance. O conceito a que se refere a marca é em essência uma promessa das sociedades sob ela em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes.|
|societyName|string|true|none|Nome da sociedade pertencente à marca.|
|cnpjNumber|string|true|none|CNPJ da sociedade pertencente à marca.|

<h2 id="tocS_LifePensionProduct">LifePensionProduct</h2>
<!-- backwards compatibility -->
<a id="schemalifepensionproduct"></a>
<a id="schema_LifePensionProduct"></a>
<a id="tocSlifepensionproduct"></a>
<a id="tocslifepensionproduct"></a>

```json
[
  {
    "name": "Brasilprev Private Multimercado 2020",
    "code": "1234",
    "segment": "PREVIDENCIA",
    "type": "PGBL",
    "modality": "CONTRIBUICAO_VARIAVEL",
    "optionalCoverage": "string",
    "productDetails": [
      {
        "susepProcessNumber": "15414.614141/2020-71",
        "contractTermsConditions": "https://example.com/mobilebanking",
        "defferalPeriod": {
          "interestRate": 0.25123,
          "updateIndex": "IPCA",
          "otherMinimumPerformanceGarantees": "SELIC",
          "reversalFinancialResults": 5.123,
          "minimumPremiumAmount": [
            {
              "minimumPremiumAmountValue": 250,
              "minimumPremiumAmountDescription": ""
            }
          ],
          "premiumPaymentMethod": [
            "CARTAO_CREDITO"
          ],
          "permissionExtraordinaryContributions": true,
          "permissonScheduledFinancialPayments": true,
          "gracePeriodRedemption": 100,
          "gracePeriodBetweenRedemptionRequests": 30,
          "redemptionPaymentTerm": 10,
          "gracePeriodPortability": 12,
          "gracePeriodBetweenPortabilityRequests": 15,
          "portabilityPaymentTerm": 20,
          "investimentFunds": [
            {
              "cnpjNumber": "13.456.789/0001-12",
              "companyName": "EYPREV",
              "maximumAdministrationFee": 20.1,
              "typePerformanceFee": [
                "DIRETAMENTE"
              ],
              "maximumPerformanceFee": 20,
              "eligibilityRule": true,
              "minimumContributionAmount": 1000,
              "minimumMathematicalProvisionAmount": 1000
            }
          ]
        },
        "grantPeriodBenefit": {
          "incomeModality": [
            "RENDA_VITALICIA"
          ],
          "biometricTable": [
            "AT_2000_FEMALE_SUAVIZADA_15"
          ],
          "interestRate": 3.225,
          "updateIndex": "IPCA",
          "reversalResultsFinancial": 13.252,
          "investimentFunds": [
            {
              "cnpjNumber": "13.456.789/0001-12",
              "companyName": "EYPREV",
              "maximumAdministrationFee": 20.1,
              "typePerformanceFee": [
                "DIRETAMENTE"
              ],
              "maximumPerformanceFee": 20,
              "eligibilityRule": true,
              "minimumContributionAmount": 1000,
              "minimumMathematicalProvisionAmount": 1000
            }
          ]
        },
        "costs": {
          "loadingAntecipated": {
            "minValue": 4.122,
            "maxValue": 10
          },
          "loadingLate": {
            "minValue": 4.122,
            "maxValue": 10
          }
        }
      }
    ],
    "minimumRequirements": {
      "contractType": "INDIVIDUAL",
      "participantQualified": true,
      "minRequirementsContract": "https://example.com/mobile-banking"
    },
    "targetAudience": "PESSOA_NATURAL"
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome comercial do produto, pelo qual é identificado nos canais de distribuição e atendimento da sociedade.|
|code|string|true|none|Código único a ser definido pela sociedade.|
|segment|string|true|none|Segmento do qual se trata o produto contratado.|
|type|string|false|none|Tipo do produto contratado.|
|modality|string|true|none|Modalidade do produto contratado.|
|optionalCoverage|string|false|none|Campo aberto (possibilidade de incluir URL).|
|productDetails|[LifePensionProductDetails](#schemalifepensionproductdetails)|false|none|none|
|minimumRequirements|[LifePensionMinimumRequirements](#schemalifepensionminimumrequirements)|true|none|none|
|targetAudience|string|true|none|Público-alvo.|

#### Enumerated Values

|Property|Value|
|---|---|
|segment|SEGURO_PESSOAS|
|segment|PREVIDENCIA|
|type|PGBL|
|type|PRGP|
|type|PAGP|
|type|PRSA|
|type|PRI|
|type|PDR|
|type|VGBL|
|type|VRGP|
|type|VAGP|
|type|VRSA|
|type|VRI|
|type|VDR|
|type|DEMAIS_PRODUTOS_PREVIDENCIA|
|modality|CONTRIBUICAO_VARIAVEL|
|modality|BENEFICIO_DEFINIDO|
|targetAudience|PESSOA_NATURAL|
|targetAudience|PESSOA_JURIDICA|

<h2 id="tocS_LifePensionProductDetails">LifePensionProductDetails</h2>
<!-- backwards compatibility -->
<a id="schemalifepensionproductdetails"></a>
<a id="schema_LifePensionProductDetails"></a>
<a id="tocSlifepensionproductdetails"></a>
<a id="tocslifepensionproductdetails"></a>

```json
[
  {
    "susepProcessNumber": "15414.614141/2020-71",
    "contractTermsConditions": "https://example.com/mobilebanking",
    "defferalPeriod": {
      "interestRate": 0.25123,
      "updateIndex": "IPCA",
      "otherMinimumPerformanceGarantees": "SELIC",
      "reversalFinancialResults": 5.123,
      "minimumPremiumAmount": [
        {
          "minimumPremiumAmountValue": 250,
          "minimumPremiumAmountDescription": ""
        }
      ],
      "premiumPaymentMethod": [
        "CARTAO_CREDITO"
      ],
      "permissionExtraordinaryContributions": true,
      "permissonScheduledFinancialPayments": true,
      "gracePeriodRedemption": 100,
      "gracePeriodBetweenRedemptionRequests": 30,
      "redemptionPaymentTerm": 10,
      "gracePeriodPortability": 12,
      "gracePeriodBetweenPortabilityRequests": 15,
      "portabilityPaymentTerm": 20,
      "investimentFunds": [
        {
          "cnpjNumber": "13.456.789/0001-12",
          "companyName": "EYPREV",
          "maximumAdministrationFee": 20.1,
          "typePerformanceFee": [
            "DIRETAMENTE"
          ],
          "maximumPerformanceFee": 20,
          "eligibilityRule": true,
          "minimumContributionAmount": 1000,
          "minimumMathematicalProvisionAmount": 1000
        }
      ]
    },
    "grantPeriodBenefit": {
      "incomeModality": [
        "RENDA_VITALICIA"
      ],
      "biometricTable": [
        "AT_2000_FEMALE_SUAVIZADA_15"
      ],
      "interestRate": 3.225,
      "updateIndex": "IPCA",
      "reversalResultsFinancial": 13.252,
      "investimentFunds": [
        {
          "cnpjNumber": "13.456.789/0001-12",
          "companyName": "EYPREV",
          "maximumAdministrationFee": 20.1,
          "typePerformanceFee": [
            "DIRETAMENTE"
          ],
          "maximumPerformanceFee": 20,
          "eligibilityRule": true,
          "minimumContributionAmount": 1000,
          "minimumMathematicalProvisionAmount": 1000
        }
      ]
    },
    "costs": {
      "loadingAntecipated": {
        "minValue": 4.122,
        "maxValue": 10
      },
      "loadingLate": {
        "minValue": 4.122,
        "maxValue": 10
      }
    }
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|susepProcessNumber|string|true|none|Sequência numérica utilizada para consulta dos processos eletrônicos na SUSEP, com caracteres especiais.|
|contractTermsConditions|string|true|none|Campo aberto (possibilidade de incluir URL).|
|defferalPeriod|[LifePensionDefferalPeriod](#schemalifepensiondefferalperiod)|true|none|none|
|grantPeriodBenefit|[LifePensionPeriodGrantBenefit](#schemalifepensionperiodgrantbenefit)|true|none|none|
|costs|[LifePensionCosts](#schemalifepensioncosts)|true|none|none|

<h2 id="tocS_LifePensionDefferalPeriod">LifePensionDefferalPeriod</h2>
<!-- backwards compatibility -->
<a id="schemalifepensiondefferalperiod"></a>
<a id="schema_LifePensionDefferalPeriod"></a>
<a id="tocSlifepensiondefferalperiod"></a>
<a id="tocslifepensiondefferalperiod"></a>

```json
{
  "interestRate": 0.25123,
  "updateIndex": "IPCA",
  "otherMinimumPerformanceGarantees": "SELIC",
  "reversalFinancialResults": 5.123,
  "minimumPremiumAmount": [
    {
      "minimumPremiumAmountValue": 250,
      "minimumPremiumAmountDescription": ""
    }
  ],
  "premiumPaymentMethod": [
    "CARTAO_CREDITO"
  ],
  "permissionExtraordinaryContributions": true,
  "permissonScheduledFinancialPayments": true,
  "gracePeriodRedemption": 100,
  "gracePeriodBetweenRedemptionRequests": 30,
  "redemptionPaymentTerm": 10,
  "gracePeriodPortability": 12,
  "gracePeriodBetweenPortabilityRequests": 15,
  "portabilityPaymentTerm": 20,
  "investimentFunds": [
    {
      "cnpjNumber": "13.456.789/0001-12",
      "companyName": "EYPREV",
      "maximumAdministrationFee": 20.1,
      "typePerformanceFee": [
        "DIRETAMENTE"
      ],
      "maximumPerformanceFee": 20,
      "eligibilityRule": true,
      "minimumContributionAmount": 1000,
      "minimumMathematicalProvisionAmount": 1000
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|interestRate|number|true|none|Taxa de juros garantida que remunera o plano durante a fase de diferimento/acumulação.|
|updateIndex|string|true|none|Indice garantido que remunera o plano durante a fase de diferimento/ acumulação.|
|otherMinimumPerformanceGarantees|string|true|none|Para produtos do tipo PDR e VDR, indicação do percentual e do índice de ampla divulgação utilizados como garantia mínima de desempenho. Em %.|
|reversalFinancialResults|number|true|none|Percentual de reversão de excedente financeiro no período de diferimento.|
|minimumPremiumAmount|[object]|true|none|none|
|» minimumPremiumAmountValue|number|false|none|Valor|
|» minimumPremiumAmountDescription|string|false|none|Descrição Período.|
|premiumPaymentMethod|[string]|false|none|none|
|permissionExtraordinaryContributions|boolean|false|none|Se ficam permitidos aportes extraordinários.|
|permissonScheduledFinancialPayments|boolean|true|none|Se ficam permitidos pagamentos financeiros programados.|
|gracePeriodRedemption|integer|true|none|Prazo em dias de carência para resgate.|
|gracePeriodBetweenRedemptionRequests|integer|true|none|Prazo em dias de carência entre pedidos de resgate.|
|redemptionPaymentTerm|integer|true|none|Prazo em dias para pagamento do resgate.|
|gracePeriodPortability|integer|true|none|Prazo em dias de carência para portabilidade.|
|gracePeriodBetweenPortabilityRequests|integer|true|none|Prazo em dias de carência entre pedidos de portabilidade.|
|portabilityPaymentTerm|integer|true|none|Prazo em dias para pagamento da portabilidade.|
|investimentFunds|[LifePensionInvestmentFunds](#schemalifepensioninvestmentfunds)|true|none|Lista com as informações do(s) Fundo(s) de Investimento(s) disponíveis para o período de diferimento/acumulação.|

#### Enumerated Values

|Property|Value|
|---|---|
|updateIndex|IPCA|
|updateIndex|IGP-M|
|updateIndex|INPC|

<h2 id="tocS_LifePensionInvestmentFunds">LifePensionInvestmentFunds</h2>
<!-- backwards compatibility -->
<a id="schemalifepensioninvestmentfunds"></a>
<a id="schema_LifePensionInvestmentFunds"></a>
<a id="tocSlifepensioninvestmentfunds"></a>
<a id="tocslifepensioninvestmentfunds"></a>

```json
[
  {
    "cnpjNumber": "13.456.789/0001-12",
    "companyName": "EYPREV",
    "maximumAdministrationFee": 20.1,
    "typePerformanceFee": [
      "DIRETAMENTE"
    ],
    "maximumPerformanceFee": 20,
    "eligibilityRule": true,
    "minimumContributionAmount": 1000,
    "minimumMathematicalProvisionAmount": 1000
  }
]

```

Lista com as informações do(s) Fundo(s) de Investimento(s) disponíveis para o período de diferimento/acumulação.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|cnpjNumber|string|true|none|Número de CNPJ.|
|companyName|string|true|none|Nome Fantasia.|
|maximumAdministrationFee|number|true|none|Taxa Máxima de Administração – em %.|
|typePerformanceFee|[string]|true|none|none|
|maximumPerformanceFee|number|false|none|Taxa Máxima de Performance. Caso o Tipo de Taxa de Performance seja ‘Diretamente’.|
|eligibilityRule|boolean|true|none|Regra de Eligibilidade.|
|minimumContributionAmount|number|true|none|Valor Mínimo de Contribuição. Regra de Elegibilidade. Caso a Regra de Elegibilidade SIM.|
|minimumMathematicalProvisionAmount|number|true|none|Valor Mínimo Provisão Matemática. Caso a Regra de Elegibilidade SIM.|

<h2 id="tocS_LifePensionPeriodGrantBenefit">LifePensionPeriodGrantBenefit</h2>
<!-- backwards compatibility -->
<a id="schemalifepensionperiodgrantbenefit"></a>
<a id="schema_LifePensionPeriodGrantBenefit"></a>
<a id="tocSlifepensionperiodgrantbenefit"></a>
<a id="tocslifepensionperiodgrantbenefit"></a>

```json
{
  "incomeModality": [
    "RENDA_VITALICIA"
  ],
  "biometricTable": [
    "AT_2000_FEMALE_SUAVIZADA_15"
  ],
  "interestRate": 3.225,
  "updateIndex": "IPCA",
  "reversalResultsFinancial": 13.252,
  "investimentFunds": [
    {
      "cnpjNumber": "13.456.789/0001-12",
      "companyName": "EYPREV",
      "maximumAdministrationFee": 20.1,
      "typePerformanceFee": [
        "DIRETAMENTE"
      ],
      "maximumPerformanceFee": 20,
      "eligibilityRule": true,
      "minimumContributionAmount": 1000,
      "minimumMathematicalProvisionAmount": 1000
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|incomeModality|[string]|true|none|none|
|biometricTable|[string]|true|none|none|
|interestRate|number|true|none|Taxa de juros garantida utilizada para conversão em renda. Em %.|
|updateIndex|string|true|none|É o índice contratado para atualização monetária dos valores relativos ao plano, na forma estabelecida por este regulamento.|
|reversalResultsFinancial|number|true|none|Percentual de reversão de excedente financeiro na concessão. Em %.|
|investimentFunds|[LifePensionInvestmentFunds](#schemalifepensioninvestmentfunds)|true|none|Lista com as informações do(s) Fundo(s) de Investimento(s) disponíveis para o período de diferimento/acumulação.|

#### Enumerated Values

|Property|Value|
|---|---|
|updateIndex|IPCA|
|updateIndex|IGP-M|
|updateIndex|INPC|

<h2 id="tocS_LifePensionCosts">LifePensionCosts</h2>
<!-- backwards compatibility -->
<a id="schemalifepensioncosts"></a>
<a id="schema_LifePensionCosts"></a>
<a id="tocSlifepensioncosts"></a>
<a id="tocslifepensioncosts"></a>

```json
{
  "loadingAntecipated": {
    "minValue": 4.122,
    "maxValue": 10
  },
  "loadingLate": {
    "minValue": 4.122,
    "maxValue": 10
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|loadingAntecipated|[LifePensionLoading](#schemalifepensionloading)|true|none|none|
|loadingLate|[LifePensionLoading](#schemalifepensionloading)|true|none|none|

<h2 id="tocS_LifePensionLoading">LifePensionLoading</h2>
<!-- backwards compatibility -->
<a id="schemalifepensionloading"></a>
<a id="schema_LifePensionLoading"></a>
<a id="tocSlifepensionloading"></a>
<a id="tocslifepensionloading"></a>

```json
{
  "minValue": 4.122,
  "maxValue": 10
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|minValue|number|true|none|Valor mínimo em %.|
|maxValue|number|true|none|alor máximo em %.|

<h2 id="tocS_LifePensionMinimumRequirements">LifePensionMinimumRequirements</h2>
<!-- backwards compatibility -->
<a id="schemalifepensionminimumrequirements"></a>
<a id="schema_LifePensionMinimumRequirements"></a>
<a id="tocSlifepensionminimumrequirements"></a>
<a id="tocslifepensionminimumrequirements"></a>

```json
{
  "contractType": "INDIVIDUAL",
  "participantQualified": true,
  "minRequirementsContract": "https://example.com/mobile-banking"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contractType|string|true|none|O tipo de serviço contratado.|
|participantQualified|boolean|true|none|Indicação se o plano é destinado para participante qualificado.|
|minRequirementsContract|string|true|none|Campo aberto contendo todos os requisitos mínimos para contratação (possibilidade de incluir URL).|

#### Enumerated Values

|Property|Value|
|---|---|
|contractType|COLETIVO_AVERBADO|
|contractType|COLETIVO_INSTITUIDO|
|contractType|INDIVIDUAL|

<h2 id="tocS_LinksPaginated">LinksPaginated</h2>
<!-- backwards compatibility -->
<a id="schemalinkspaginated"></a>
<a id="schema_LinksPaginated"></a>
<a id="tocSlinkspaginated"></a>
<a id="tocslinkspaginated"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
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
  "totalRecords": 10,
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
    "totalRecords": 10,
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

<h2 id="tocS_ResponsePersonList">ResponsePersonList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsepersonlist"></a>
<a id="schema_ResponsePersonList"></a>
<a id="tocSresponsepersonlist"></a>
<a id="tocsresponsepersonlist"></a>

```json
{
  "data": {
    "brand": {
      "name": "Marca",
      "companies": [
        {
          "name": "Seguradora",
          "cnpjNumber": 45086338000178,
          "products": [
            {
              "name": "Seguro Pessoal",
              "code": "123456789_cap",
              "category": "TRADICIONAL",
              "insuranceModality": "FUNERAL",
              "coverages": [
                {
                  "coverage": "AUXILIO_CESTA_BASICA",
                  "coverageOthers": [
                    "string"
                  ],
                  "coverageAttributes": {
                    "indemnityPaymentMethod": [],
                    "indemnityPaymentFrequency": [],
                    "minValue": {},
                    "maxValue": {},
                    "indemnifiablePeriod": [],
                    "maximumQtyIndemnifiableInstallments": 0,
                    "currency": "BRL",
                    "gracePeriod": {},
                    "differentiatedGracePeriod": {},
                    "deductibleDays": 0,
                    "differentiatedDeductibleDays": 0,
                    "deductibleBRL": 0,
                    "differentiatedDeductibleBRL": "string",
                    "excludedRisks": [],
                    "excludedRisksURL": "string",
                    "allowApartPurchase": true
                  }
                }
              ],
              "assistanceType": [
                "ACOMPANHANTE_CASO_HOSPITALIZACAO_PROLONGADA"
              ],
              "additional": [
                "SORTEIO"
              ],
              "assistanceTypeOthers": [
                "string"
              ],
              "termsAndConditions": [
                {
                  "susepProcessNumber": "string",
                  "definition": "string"
                }
              ],
              "globalCapital": true,
              "validity": [
                "VITALICIA"
              ],
              "pmbacRemuneration": {
                "interestRate": 0,
                "pmbacUpdateIndex": "IPCA"
              },
              "benefitRecalculation": {
                "benefitRecalculationCriteria": "INDICE",
                "benefitUpdateIndex": "IPCA"
              },
              "ageAdjustment": {
                "criterion": "APOS_PERIODO_EM_ANOS",
                "frequency": 0
              },
              "contractType": "REPARTICAO_SIMPLES",
              "reclaim": {
                "reclaimTable": [
                  {
                    "initialMonthRange": 1,
                    "finalMonthRange": 12,
                    "percentage": 0
                  }
                ],
                "differentiatedPercentage": "string",
                "gracePeriod": {
                  "amount": 60,
                  "unit": "DIAS"
                }
              },
              "otherGuaranteedValues": "SALDAMENTO",
              "allowPortability": true,
              "portabilityGraceTime": 0,
              "indemnityPaymentMethod": [
                "UNICO"
              ],
              "indemnityPaymentIncome": [
                "CERTA"
              ],
              "premiumPayment": {
                "paymentMethod": [
                  "CARTAO_CREDITO"
                ],
                "frequency": [
                  "DIARIA"
                ],
                "premiumTax": "string"
              },
              "minimunRequirements": {
                "contractingType": "COLETIVO",
                "contractingMinRequirement": "string"
              },
              "targetAudience": "PESSOA_NATURAL"
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|true|none|none|
|» brand|[PersonBrand](#schemapersonbrand)|true|none|Organização controladora do grupo.|
|links|[LinksPaginated](#schemalinkspaginated)|true|none|none|
|meta|[MetaPaginated](#schemametapaginated)|true|none|none|

<h2 id="tocS_PersonBrand">PersonBrand</h2>
<!-- backwards compatibility -->
<a id="schemapersonbrand"></a>
<a id="schema_PersonBrand"></a>
<a id="tocSpersonbrand"></a>
<a id="tocspersonbrand"></a>

```json
{
  "name": "Marca",
  "companies": [
    {
      "name": "Seguradora",
      "cnpjNumber": 45086338000178,
      "products": [
        {
          "name": "Seguro Pessoal",
          "code": "123456789_cap",
          "category": "TRADICIONAL",
          "insuranceModality": "FUNERAL",
          "coverages": [
            {
              "coverage": "AUXILIO_CESTA_BASICA",
              "coverageOthers": [
                "string"
              ],
              "coverageAttributes": {
                "indemnityPaymentMethod": [
                  "PAGAMENTO_CAPITAL_SEGURADO_VALOR_MONETARIO"
                ],
                "indemnityPaymentFrequency": [
                  "INDENIZACAO_UNICA"
                ],
                "minValue": {},
                "maxValue": {},
                "indemnifiablePeriod": [
                  "ATE_FIM_CICLO_DETERMINADO"
                ],
                "maximumQtyIndemnifiableInstallments": 0,
                "currency": "BRL",
                "gracePeriod": {
                  "amount": 60,
                  "unit": "DIAS"
                },
                "differentiatedGracePeriod": {
                  "amount": 60,
                  "unit": "DIAS"
                },
                "deductibleDays": 0,
                "differentiatedDeductibleDays": 0,
                "deductibleBRL": 0,
                "differentiatedDeductibleBRL": "string",
                "excludedRisks": [
                  "ATO_RECONHECIMENTO_PERIGOSO"
                ],
                "excludedRisksURL": "string",
                "allowApartPurchase": true
              }
            }
          ],
          "assistanceType": [
            "ACOMPANHANTE_CASO_HOSPITALIZACAO_PROLONGADA"
          ],
          "additional": [
            "SORTEIO"
          ],
          "assistanceTypeOthers": [
            "string"
          ],
          "termsAndConditions": [
            {
              "susepProcessNumber": "string",
              "definition": "string"
            }
          ],
          "globalCapital": true,
          "validity": [
            "VITALICIA"
          ],
          "pmbacRemuneration": {
            "interestRate": 0,
            "pmbacUpdateIndex": "IPCA"
          },
          "benefitRecalculation": {
            "benefitRecalculationCriteria": "INDICE",
            "benefitUpdateIndex": "IPCA"
          },
          "ageAdjustment": {
            "criterion": "APOS_PERIODO_EM_ANOS",
            "frequency": 0
          },
          "contractType": "REPARTICAO_SIMPLES",
          "reclaim": {
            "reclaimTable": [
              {
                "initialMonthRange": 1,
                "finalMonthRange": 12,
                "percentage": 0
              }
            ],
            "differentiatedPercentage": "string",
            "gracePeriod": {
              "amount": 60,
              "unit": "DIAS"
            }
          },
          "otherGuaranteedValues": "SALDAMENTO",
          "allowPortability": true,
          "portabilityGraceTime": 0,
          "indemnityPaymentMethod": [
            "UNICO"
          ],
          "indemnityPaymentIncome": [
            "CERTA"
          ],
          "premiumPayment": {
            "paymentMethod": [
              "CARTAO_CREDITO"
            ],
            "frequency": [
              "DIARIA"
            ],
            "premiumTax": "string"
          },
          "minimunRequirements": {
            "contractingType": "COLETIVO",
            "contractingMinRequirement": "string"
          },
          "targetAudience": "PESSOA_NATURAL"
        }
      ]
    }
  ]
}

```

Organização controladora do grupo.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da marca reportada pelo participante do Open Insurance. O conceito a que se refere a marca é em essência uma promessa das sociedades sob ela em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes.|
|companies|[PersonCompany](#schemapersoncompany)|true|none|none|

<h2 id="tocS_PersonCompany">PersonCompany</h2>
<!-- backwards compatibility -->
<a id="schemapersoncompany"></a>
<a id="schema_PersonCompany"></a>
<a id="tocSpersoncompany"></a>
<a id="tocspersoncompany"></a>

```json
[
  {
    "name": "Seguradora",
    "cnpjNumber": 45086338000178,
    "products": [
      {
        "name": "Seguro Pessoal",
        "code": "123456789_cap",
        "category": "TRADICIONAL",
        "insuranceModality": "FUNERAL",
        "coverages": [
          {
            "coverage": "AUXILIO_CESTA_BASICA",
            "coverageOthers": [
              "string"
            ],
            "coverageAttributes": {
              "indemnityPaymentMethod": [
                "PAGAMENTO_CAPITAL_SEGURADO_VALOR_MONETARIO"
              ],
              "indemnityPaymentFrequency": [
                "INDENIZACAO_UNICA"
              ],
              "minValue": {},
              "maxValue": {},
              "indemnifiablePeriod": [
                "ATE_FIM_CICLO_DETERMINADO"
              ],
              "maximumQtyIndemnifiableInstallments": 0,
              "currency": "BRL",
              "gracePeriod": {
                "amount": 60,
                "unit": "DIAS"
              },
              "differentiatedGracePeriod": {
                "amount": 60,
                "unit": "DIAS"
              },
              "deductibleDays": 0,
              "differentiatedDeductibleDays": 0,
              "deductibleBRL": 0,
              "differentiatedDeductibleBRL": "string",
              "excludedRisks": [
                "ATO_RECONHECIMENTO_PERIGOSO"
              ],
              "excludedRisksURL": "string",
              "allowApartPurchase": true
            }
          }
        ],
        "assistanceType": [
          "ACOMPANHANTE_CASO_HOSPITALIZACAO_PROLONGADA"
        ],
        "additional": [
          "SORTEIO"
        ],
        "assistanceTypeOthers": [
          "string"
        ],
        "termsAndConditions": [
          {
            "susepProcessNumber": "string",
            "definition": "string"
          }
        ],
        "globalCapital": true,
        "validity": [
          "VITALICIA"
        ],
        "pmbacRemuneration": {
          "interestRate": 0,
          "pmbacUpdateIndex": "IPCA"
        },
        "benefitRecalculation": {
          "benefitRecalculationCriteria": "INDICE",
          "benefitUpdateIndex": "IPCA"
        },
        "ageAdjustment": {
          "criterion": "APOS_PERIODO_EM_ANOS",
          "frequency": 0
        },
        "contractType": "REPARTICAO_SIMPLES",
        "reclaim": {
          "reclaimTable": [
            {
              "initialMonthRange": 1,
              "finalMonthRange": 12,
              "percentage": 0
            }
          ],
          "differentiatedPercentage": "string",
          "gracePeriod": {
            "amount": 60,
            "unit": "DIAS"
          }
        },
        "otherGuaranteedValues": "SALDAMENTO",
        "allowPortability": true,
        "portabilityGraceTime": 0,
        "indemnityPaymentMethod": [
          "UNICO"
        ],
        "indemnityPaymentIncome": [
          "CERTA"
        ],
        "premiumPayment": {
          "paymentMethod": [
            "CARTAO_CREDITO"
          ],
          "frequency": [
            "DIARIA"
          ],
          "premiumTax": "string"
        },
        "minimunRequirements": {
          "contractingType": "COLETIVO",
          "contractingMinRequirement": "string"
        },
        "targetAudience": "PESSOA_NATURAL"
      }
    ]
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da sociedade pertencente à marca.|
|cnpjNumber|string|true|none|CNPJ da sociedade pertencente à marca.|
|products|[PersonProducts](#schemapersonproducts)|false|none|Lista de Dependências de uma Instituição.|

<h2 id="tocS_PersonProducts">PersonProducts</h2>
<!-- backwards compatibility -->
<a id="schemapersonproducts"></a>
<a id="schema_PersonProducts"></a>
<a id="tocSpersonproducts"></a>
<a id="tocspersonproducts"></a>

```json
[
  {
    "name": "Seguro Pessoal",
    "code": "123456789_cap",
    "category": "TRADICIONAL",
    "insuranceModality": "FUNERAL",
    "coverages": [
      {
        "coverage": "AUXILIO_CESTA_BASICA",
        "coverageOthers": [
          "string"
        ],
        "coverageAttributes": {
          "indemnityPaymentMethod": [
            "PAGAMENTO_CAPITAL_SEGURADO_VALOR_MONETARIO"
          ],
          "indemnityPaymentFrequency": [
            "INDENIZACAO_UNICA"
          ],
          "minValue": {},
          "maxValue": {},
          "indemnifiablePeriod": [
            "ATE_FIM_CICLO_DETERMINADO"
          ],
          "maximumQtyIndemnifiableInstallments": 0,
          "currency": "BRL",
          "gracePeriod": {
            "amount": 60,
            "unit": "DIAS"
          },
          "differentiatedGracePeriod": {
            "amount": 60,
            "unit": "DIAS"
          },
          "deductibleDays": 0,
          "differentiatedDeductibleDays": 0,
          "deductibleBRL": 0,
          "differentiatedDeductibleBRL": "string",
          "excludedRisks": [
            "ATO_RECONHECIMENTO_PERIGOSO"
          ],
          "excludedRisksURL": "string",
          "allowApartPurchase": true
        }
      }
    ],
    "assistanceType": [
      "ACOMPANHANTE_CASO_HOSPITALIZACAO_PROLONGADA"
    ],
    "additional": [
      "SORTEIO"
    ],
    "assistanceTypeOthers": [
      "string"
    ],
    "termsAndConditions": [
      {
        "susepProcessNumber": "string",
        "definition": "string"
      }
    ],
    "globalCapital": true,
    "validity": [
      "VITALICIA"
    ],
    "pmbacRemuneration": {
      "interestRate": 0,
      "pmbacUpdateIndex": "IPCA"
    },
    "benefitRecalculation": {
      "benefitRecalculationCriteria": "INDICE",
      "benefitUpdateIndex": "IPCA"
    },
    "ageAdjustment": {
      "criterion": "APOS_PERIODO_EM_ANOS",
      "frequency": 0
    },
    "contractType": "REPARTICAO_SIMPLES",
    "reclaim": {
      "reclaimTable": [
        {
          "initialMonthRange": 1,
          "finalMonthRange": 12,
          "percentage": 0
        }
      ],
      "differentiatedPercentage": "string",
      "gracePeriod": {
        "amount": 60,
        "unit": "DIAS"
      }
    },
    "otherGuaranteedValues": "SALDAMENTO",
    "allowPortability": true,
    "portabilityGraceTime": 0,
    "indemnityPaymentMethod": [
      "UNICO"
    ],
    "indemnityPaymentIncome": [
      "CERTA"
    ],
    "premiumPayment": {
      "paymentMethod": [
        "CARTAO_CREDITO"
      ],
      "frequency": [
        "DIARIA"
      ],
      "premiumTax": "string"
    },
    "minimunRequirements": {
      "contractingType": "COLETIVO",
      "contractingMinRequirement": "string"
    },
    "targetAudience": "PESSOA_NATURAL"
  }
]

```

Lista de Dependências de uma Instituição.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome comercial do produto, pelo qual é identificado nos canais de distribuição e atendimento da sociedade.|
|code|string|true|none|Código único a ser definido pela sociedade (código interno do produto) a critério da participante.|
|category|string|true|none|Indica a categoria do Produto|
|insuranceModality|string|true|none|none|
|coverages|[object]|true|none|none|
|» coverage|string|false|none|none|
|» coverageOthers|[string]|false|none|none|
|» coverageAttributes|[PersonCoverageAttributes](#schemapersoncoverageattributes)|false|none|none|
|assistanceType|[string]|false|none|Listagem dos serviços de assistências complementares disponíveis vinculados ao produto. Deve ser padronizada na proposta técnica submetida pela Estrutura Inicial de  Governança para observância comum por todas as sociedades participantes|
|additional|[string]|true|none|none|
|assistanceTypeOthers|[string]|false|none|none|
|termsAndConditions|[[PersonTermsAndCondition](#schemapersontermsandcondition)]|true|none|none|
|globalCapital|boolean|true|none|Seguro de pessoas com capital global modalidade de contratação coletiva da cobertura de risco, respeitados os critérios técnico-operacionais, forma e limites fixados pela SUSEP, segundo a qual o valor do capital segurado referente a cada componente sofrerá variações decorrentes de mudanças na composição do grupo segurado|
|validity|[string]|true|none|none|
|pmbacRemuneration|[PersonPmbacRemuneration](#schemapersonpmbacremuneration)|false|none|none|
|benefitRecalculation|[PersonBenefitRecalculation](#schemapersonbenefitrecalculation)|false|none|none|
|ageAdjustment|[PersonAgeAdjustment](#schemapersonageadjustment)|false|none|none|
|contractType|string|true|none|Regime Financeiro|
|reclaim|[PersonReclaim](#schemapersonreclaim)|false|none|none|
|otherGuaranteedValues|string|true|none|none|
|allowPortability|boolean|true|none|Permite Portabilidade|
|portabilityGraceTime|integer|true|none|Prazo de carência em dias para Portabilidade|
|indemnityPaymentMethod|[string]|true|none|none|
|indemnityPaymentIncome|[string]|true|none|none|
|premiumPayment|[PersonPremiumPayment](#schemapersonpremiumpayment)|false|none|none|
|minimunRequirements|[PersonMinimumRequirements](#schemapersonminimumrequirements)|false|none|none|
|targetAudience|string|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|category|TRADICIONAL|
|category|MICROSEGURO|
|insuranceModality|FUNERAL|
|insuranceModality|PRESTAMISTA|
|insuranceModality|VIAGEM|
|insuranceModality|EDUCACIONAL|
|insuranceModality|DOTAL|
|insuranceModality|ACIDENTES_PESSOAIS|
|insuranceModality|VIDA|
|insuranceModality|PERDA_CERTIFICADO_HABILITACAOO_VOO|
|insuranceModality|DOENCAS_GRAVES_DOENCA_TERMINAL|
|insuranceModality|DESEMPREGO_PERDA_RENDA|
|insuranceModality|EVENTOS_ALEATORIOS|
|coverage|ADIANTAMENTO_DOENCA_ESTAGIO_TERMINAL|
|coverage|AUXILIO_CESTA_BASICA|
|coverage|AUXILIO_FINANCEIRO_IMEDIATO|
|coverage|CANCELAMENTO_DE_VIAGEM|
|coverage|CIRURGIA|
|coverage|COBERTURA_PARA_HERNIA|
|coverage|COBERTURA_PARA_LER_DORT|
|coverage|CUIDADOS_PROLONGADOS_ACIDENTE|
|coverage|DESEMPREGO_PERDA_DE_RENDA|
|coverage|DESPESAS_EXTRA_INVALIDEZ_PERMANENTE_TOTAL_PARCIAL_ACIDENTE_DEI|
|coverage|DESPESAS_EXTRA_MORTE_DEM|
|coverage|DESPESAS_MEDICAS_HOSPITALARES_ODONTOLOGICAS|
|coverage|DESPESAS_MEDICAS_HOSPITALARES_ODONTOLOGICAS_BRASIL|
|coverage|DESPESAS_MEDICAS_HOSPITALARES_ODONTOLOGICAS_EXTERIOR|
|coverage|DIARIA_INCAPACIDADE_TOTAL_TEMPORARIA|
|coverage|DIARIA_INTERNACAO_HOSPITALAR|
|coverage|INTERNACAO_HOSPITALAR|
|coverage|DIARIAS_INCAPACIDADE_PECUNIARIA_DIP|
|coverage|DOENCA_GRAVE|
|coverage|DOENCA_CONGENITA_FILHOS_DCF|
|coverage|FRATURA_OSSEA|
|coverage|DOENCAS_TROPICAIS|
|coverage|INCAPACIDADE_TOTAL_OU_TEMPORARIA|
|coverage|INVALIDEZ_PERMANENTE_TOTAL_PARCIAL|
|coverage|INVALIDEZ_TOTAL_ACIDENTE|
|coverage|INVALIDEZ_PARCIAL_ACIDENTE|
|coverage|INVALIDEZ_FUNCIONAL_PERMANENTE_DOENCA|
|coverage|INVALIDEZ_LABORATIVA_DOENCA|
|coverage|MORTE|
|coverage|MORTE_ACIDENTAL|
|coverage|MORTE_CONJUGE|
|coverage|MORTE_FILHOS|
|coverage|MORTE_ADIATAMENTO_DOENCA_ESTAGIO_TERMINAL|
|coverage|PAGAMENTO_ANTECIPADO_ESPECIAL_DOENCA_PROFISSIONAL_PAED|
|coverage|PERDA_DA_AUTONOMIA_PESSOAL|
|coverage|PERDA_INVOLUNTARIA_EMPREGO|
|coverage|QUEIMADURA_GRAVE|
|coverage|REGRESSO_ANTECIPADO_SANITARIO|
|coverage|RENDA_INCAPACIDADE_TEMPORARIA|
|coverage|RESCISAO_CONTRATUAL_CASO_MORTE_RCM|
|coverage|RESCISAO_TRABALHISTA|
|coverage|SERVICO_AUXILIO_FUNERAL|
|coverage|SOBREVIVENCIA|
|coverage|TRANSPLANTE_ORGAOS|
|coverage|TRANSLADO|
|coverage|TRANSLADO_MEDICO|
|coverage|TRANSLADO_CORPO|
|coverage|VERBA_RESCISORIA|
|coverage|OUTRAS|
|contractType|REPARTICAO_SIMPLES|
|contractType|REPARTICAO_CAPITAIS|
|contractType|CAPITALIZACAO|
|otherGuaranteedValues|SALDAMENTO|
|otherGuaranteedValues|BENEFICIO_PROLONGADO|
|otherGuaranteedValues|NAO_SE_APLICA|
|targetAudience|PESSOA_NATURAL|
|targetAudience|PESSOA_JURIDICA|

<h2 id="tocS_PersonTermsAndCondition">PersonTermsAndCondition</h2>
<!-- backwards compatibility -->
<a id="schemapersontermsandcondition"></a>
<a id="schema_PersonTermsAndCondition"></a>
<a id="tocSpersontermsandcondition"></a>
<a id="tocspersontermsandcondition"></a>

```json
{
  "susepProcessNumber": "string",
  "definition": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|susepProcessNumber|string|true|none|Número do processo Susep.|
|definition|string|true|none|Campo aberto (possibilidade de incluir URL).|

<h2 id="tocS_PersonCoverageAttibutesDetailsUnit">PersonCoverageAttibutesDetailsUnit</h2>
<!-- backwards compatibility -->
<a id="schemapersoncoverageattibutesdetailsunit"></a>
<a id="schema_PersonCoverageAttibutesDetailsUnit"></a>
<a id="tocSpersoncoverageattibutesdetailsunit"></a>
<a id="tocspersoncoverageattibutesdetailsunit"></a>

```json
{
  "code": "R$",
  "description": "description"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|true|none|Tipo unidade de medida.|
|description|string|true|none|Descrição da unidade de medida|

<h2 id="tocS_PersonCoverageAttibutesDetails">PersonCoverageAttibutesDetails</h2>
<!-- backwards compatibility -->
<a id="schemapersoncoverageattibutesdetails"></a>
<a id="schema_PersonCoverageAttibutesDetails"></a>
<a id="tocSpersoncoverageattibutesdetails"></a>
<a id="tocspersoncoverageattibutesdetails"></a>

```json
{
  "amount": 60,
  "unit": {
    "code": "R$",
    "description": "description"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number|true|none|Valor.|
|unit|[PersonCoverageAttibutesDetailsUnit](#schemapersoncoverageattibutesdetailsunit)|true|none|none|

<h2 id="tocS_PersonGracePeriodUnit">PersonGracePeriodUnit</h2>
<!-- backwards compatibility -->
<a id="schemapersongraceperiodunit"></a>
<a id="schema_PersonGracePeriodUnit"></a>
<a id="tocSpersongraceperiodunit"></a>
<a id="tocspersongraceperiodunit"></a>

```json
{
  "amount": 60,
  "unit": "DIAS"
}

```

Período de carência

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number|false|none|Prazo de Carência|
|unit|string|false|none|Unidade do prazo (dias ou meses).|

#### Enumerated Values

|Property|Value|
|---|---|
|unit|DIAS|
|unit|MESES|
|unit|NAO_SE_APLICA|

<h2 id="tocS_personPortabilityGraceTime">personPortabilityGraceTime</h2>
<!-- backwards compatibility -->
<a id="schemapersonportabilitygracetime"></a>
<a id="schema_personPortabilityGraceTime"></a>
<a id="tocSpersonportabilitygracetime"></a>
<a id="tocspersonportabilitygracetime"></a>

```json
{
  "amount": 60,
  "unit": "DIAS"
}

```

Prazo de carência em dias para Portabilidade

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number|false|none|Prazo de Carência|
|unit|string|false|none|Unidade do prazo (dias ou meses).|

#### Enumerated Values

|Property|Value|
|---|---|
|unit|DIAS|
|unit|MESES|
|unit|NAO_SE_APLICA|

<h2 id="tocS_PersonCoverageAttributes">PersonCoverageAttributes</h2>
<!-- backwards compatibility -->
<a id="schemapersoncoverageattributes"></a>
<a id="schema_PersonCoverageAttributes"></a>
<a id="tocSpersoncoverageattributes"></a>
<a id="tocspersoncoverageattributes"></a>

```json
{
  "indemnityPaymentMethod": [
    "PAGAMENTO_CAPITAL_SEGURADO_VALOR_MONETARIO"
  ],
  "indemnityPaymentFrequency": [
    "INDENIZACAO_UNICA"
  ],
  "minValue": {},
  "maxValue": {},
  "indemnifiablePeriod": [
    "ATE_FIM_CICLO_DETERMINADO"
  ],
  "maximumQtyIndemnifiableInstallments": 0,
  "currency": "BRL",
  "gracePeriod": {
    "amount": 60,
    "unit": "DIAS"
  },
  "differentiatedGracePeriod": {
    "amount": 60,
    "unit": "DIAS"
  },
  "deductibleDays": 0,
  "differentiatedDeductibleDays": 0,
  "deductibleBRL": 0,
  "differentiatedDeductibleBRL": "string",
  "excludedRisks": [
    "ATO_RECONHECIMENTO_PERIGOSO"
  ],
  "excludedRisksURL": "string",
  "allowApartPurchase": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|indemnityPaymentMethod|[string]|true|none|Listagem da forma de pagamento da indenização para cada combinação de  modalidade/cobertura do produto|
|indemnityPaymentFrequency|[string]|true|none|Listagem de tipos de frequência de pagamento de indenização para cada combinação de modalidade/cobertura do produto|
|minValue|object|true|none|Listagem do valor mínimo de cobertura (Capital Segurado), diária ou parcela aceito pela  sociedade para cada  combinação de modalidade/cobertura do produto. Em reais|
|maxValue|object|true|none|Listagem do valor máximo de cobertura (Capital Segurado), diária ou parcela aceito  pela sociedade para cada  combinação de modalidade/cobertura do produto. Em reais|
|indemnifiablePeriod|[string]|true|none|Listagem de período indenizável para cada combinação de modalidade/cobertura do produto|
|maximumQtyIndemnifiableInstallments|integer|true|none|Caso o período indenizável seja relacionado a parcelas, listagem de número máximo de  parcelas indenizáveis para cada combinação de modalidade/ cobertura do produto|
|currency|string|true|none|Moeda sobre a qual a cobertura se refere. De acordo com ISO-4217.|
|gracePeriod|[PersonGracePeriodUnit](#schemapersongraceperiodunit)|true|none|Período de carência|
|differentiatedGracePeriod|[PersonGracePeriodUnit](#schemapersongraceperiodunit)|false|none|Detalhamento do período de carência diferentes para cada cobertura que exista alguma especificidade. Caso a seguradora não tenha essa diferenciação, não retornará nada no campo|
|deductibleDays|integer|true|none|Listagem de franquia em dias para cada combinação de modalidade/cobertura do produto.|
|differentiatedDeductibleDays|number|false|none|Detalhamento da franquia em dias diferentes para cada cobertura que exista alguma especificidade. Caso a seguradora não tenha essa diferenciação, não retornará nada no campo.|
|deductibleBRL|number|true|none|Listagem de franquia em reais para cada combinação de modalidade/cobertura do produto.|
|differentiatedDeductibleBRL|string|false|none|Detalhamento da franquia em reais diferentes para cada cobertura que exista alguma especificidade. Caso a seguradora não tenha essa diferenciação, não retornará nada no campo.|
|excludedRisks|[string]|true|none|Listagem dos tipos de riscos excluídos para cada combinação de modalidade/cobertura do produto. Deve ser padronizada na proposta técnica submetida pela Estrutura Inicial de Governança para observância comum por todas as sociedades participantes|
|excludedRisksURL|string|false|none|Campo aberto (possibilidade de incluir URL).|
|allowApartPurchase|boolean|true|none|Indicar se a cobertura pode ser contratada isoladamente ou não.|

#### Enumerated Values

|Property|Value|
|---|---|
|currency|AFN|
|currency|ALL|
|currency|DZD|
|currency|USD|
|currency|EUR|
|currency|AOA|
|currency|XCD|
|currency|XCD|
|currency|ARS|
|currency|AMD|
|currency|AWG|
|currency|AUD|
|currency|EUR|
|currency|AZN|
|currency|BSD|
|currency|BHD|
|currency|BDT|
|currency|BBD|
|currency|BYN|
|currency|EUR|
|currency|BZD|
|currency|XOF|
|currency|BMD|
|currency|BTN|
|currency|BOB|
|currency|BOV|
|currency|USD|
|currency|BAM|
|currency|BWP|
|currency|NOK|
|currency|BRL|
|currency|USD|
|currency|BND|
|currency|BGN|
|currency|XOF|
|currency|BIF|
|currency|CVE|
|currency|KHR|
|currency|XAF|
|currency|CAD|
|currency|KYD|
|currency|XAF|
|currency|XAF|
|currency|CLF|
|currency|CLP|
|currency|CNY|
|currency|AUD|
|currency|AUD|
|currency|COP|
|currency|COU|
|currency|KMF|
|currency|CDF|
|currency|XAF|
|currency|NZD|
|currency|CRC|
|currency|HRK|
|currency|CUC|
|currency|CUP|
|currency|ANG|
|currency|EUR|
|currency|CZK|
|currency|XOF|
|currency|DKK|
|currency|DJF|
|currency|XCD|
|currency|DOP|
|currency|USD|
|currency|EGP|
|currency|SVC|
|currency|USD|
|currency|XAF|
|currency|ERN|
|currency|EUR|
|currency|ETB|
|currency|EUR|
|currency|FKP|
|currency|DKK|
|currency|FJD|
|currency|EUR|
|currency|EUR|
|currency|EUR|
|currency|XPF|
|currency|EUR|
|currency|XAF|
|currency|GMD|
|currency|GEL|
|currency|EUR|
|currency|GHS|
|currency|GIP|
|currency|EUR|
|currency|DKK|
|currency|XCD|
|currency|EUR|
|currency|USD|
|currency|GTQ|
|currency|GBP|
|currency|GNF|
|currency|XOF|
|currency|GYD|
|currency|HTG|
|currency|USD|
|currency|AUD|
|currency|EUR|
|currency|HNL|
|currency|HKD|
|currency|HUF|
|currency|ISK|
|currency|INR|
|currency|IDR|
|currency|XDR|
|currency|IRR|
|currency|IQD|
|currency|EUR|
|currency|GBP|
|currency|ILS|
|currency|EUR|
|currency|JMD|
|currency|JPY|
|currency|GBP|
|currency|JOD|
|currency|KZT|
|currency|KES|
|currency|AUD|
|currency|KPW|
|currency|KRW|
|currency|KWD|
|currency|KGS|
|currency|LAK|
|currency|EUR|
|currency|LBP|
|currency|LSL|
|currency|ZAR|
|currency|LRD|
|currency|LYD|
|currency|CHF|
|currency|EUR|
|currency|EUR|
|currency|MOP|
|currency|MGA|
|currency|MWK|
|currency|MYR|
|currency|MVR|
|currency|XOF|
|currency|EUR|
|currency|USD|
|currency|EUR|
|currency|MRU|
|currency|MUR|
|currency|EUR|
|currency|XUA|
|currency|MXN|
|currency|MXV|
|currency|USD|
|currency|MDL|
|currency|EUR|
|currency|MNT|
|currency|EUR|
|currency|XCD|
|currency|MAD|
|currency|MZN|
|currency|MMK|
|currency|NAD|
|currency|ZAR|
|currency|AUD|
|currency|NPR|
|currency|EUR|
|currency|XPF|
|currency|NZD|
|currency|NIO|
|currency|XOF|
|currency|NGN|
|currency|NZD|
|currency|AUD|
|currency|USD|
|currency|NOK|
|currency|OMR|
|currency|PKR|
|currency|USD|
|currency|PAB|
|currency|USD|
|currency|PGK|
|currency|PYG|
|currency|PEN|
|currency|PHP|
|currency|NZD|
|currency|PLN|
|currency|EUR|
|currency|USD|
|currency|QAR|
|currency|MKD|
|currency|RON|
|currency|RUB|
|currency|RWF|
|currency|EUR|
|currency|EUR|
|currency|SHP|
|currency|XCD|
|currency|XCD|
|currency|EUR|
|currency|EUR|
|currency|XCD|
|currency|WST|
|currency|EUR|
|currency|STN|
|currency|SAR|
|currency|XOF|
|currency|RSD|
|currency|SCR|
|currency|SLL|
|currency|SGD|
|currency|ANG|
|currency|XSU|
|currency|EUR|
|currency|EUR|
|currency|SBD|
|currency|SOS|
|currency|ZAR|
|currency|SSP|
|currency|EUR|
|currency|LKR|
|currency|SDG|
|currency|SRD|
|currency|NOK|
|currency|SZL|
|currency|SEK|
|currency|CHE|
|currency|CHF|
|currency|CHW|
|currency|SYP|
|currency|TWD|
|currency|TJS|
|currency|TZS|
|currency|THB|
|currency|USD|
|currency|XOF|
|currency|NZD|
|currency|TOP|
|currency|TTD|
|currency|TND|
|currency|TRY|
|currency|TMT|
|currency|USD|
|currency|AUD|
|currency|UGX|
|currency|UAH|
|currency|AED|
|currency|GBP|
|currency|USD|
|currency|USD|
|currency|USN|
|currency|UYI|
|currency|UYU|
|currency|UZS|
|currency|VUV|
|currency|VEF|
|currency|VND|
|currency|USD|
|currency|USD|
|currency|XPF|
|currency|MAD|
|currency|YER|
|currency|ZMW|
|currency|ZWL|

<h2 id="tocS_PersonPmbacRemuneration">PersonPmbacRemuneration</h2>
<!-- backwards compatibility -->
<a id="schemapersonpmbacremuneration"></a>
<a id="schema_PersonPmbacRemuneration"></a>
<a id="tocSpersonpmbacremuneration"></a>
<a id="tocspersonpmbacremuneration"></a>

```json
{
  "interestRate": 0,
  "pmbacUpdateIndex": "IPCA"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|interestRate|number|false|none|Taxa de juros para capitalização da PMBaC.|
|pmbacUpdateIndex|string|true|none|Índice utilizado na atualização da PMBaC.|

#### Enumerated Values

|Property|Value|
|---|---|
|pmbacUpdateIndex|IPCA|
|pmbacUpdateIndex|IGP-M|
|pmbacUpdateIndex|INPC|

<h2 id="tocS_PersonBenefitRecalculation">PersonBenefitRecalculation</h2>
<!-- backwards compatibility -->
<a id="schemapersonbenefitrecalculation"></a>
<a id="schema_PersonBenefitRecalculation"></a>
<a id="tocSpersonbenefitrecalculation"></a>
<a id="tocspersonbenefitrecalculation"></a>

```json
{
  "benefitRecalculationCriteria": "INDICE",
  "benefitUpdateIndex": "IPCA"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|benefitRecalculationCriteria|string|true|none|none|
|benefitUpdateIndex|string|true|none|Índice utilizado na atualização do prêmio/contribuição e do capital segurado/ benefício,  caso critério de atualização por meio de índice|

#### Enumerated Values

|Property|Value|
|---|---|
|benefitRecalculationCriteria|INDICE|
|benefitRecalculationCriteria|VINCULADO_SALDO_DEVEDOR|
|benefitRecalculationCriteria|VARIAVEL_ACORDO_CRITERIO_ESPECIFICO|
|benefitUpdateIndex|IPCA|
|benefitUpdateIndex|IGP-M|
|benefitUpdateIndex|INPC|

<h2 id="tocS_PersonAgeAdjustment">PersonAgeAdjustment</h2>
<!-- backwards compatibility -->
<a id="schemapersonageadjustment"></a>
<a id="schema_PersonAgeAdjustment"></a>
<a id="tocSpersonageadjustment"></a>
<a id="tocspersonageadjustment"></a>

```json
{
  "criterion": "APOS_PERIODO_EM_ANOS",
  "frequency": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|criterion|string|true|none|Critério escolhido para reenquadramento etário|
|frequency|integer|true|none|Período em anos, caso critério de reenquadramento após ou a cada período em anos.|

#### Enumerated Values

|Property|Value|
|---|---|
|criterion|APOS_PERIODO_EM_ANOS|
|criterion|A_CADA_PERIODO_EM_ANOS|
|criterion|POR_MUDANCA_DE_FAIXA_ETARIA|
|criterion|NAO_APLICAVEL|

<h2 id="tocS_personReclaimTable">personReclaimTable</h2>
<!-- backwards compatibility -->
<a id="schemapersonreclaimtable"></a>
<a id="schema_personReclaimTable"></a>
<a id="tocSpersonreclaimtable"></a>
<a id="tocspersonreclaimtable"></a>

```json
{
  "initialMonthRange": 1,
  "finalMonthRange": 12,
  "percentage": 0
}

```

Tabela Percentuais de resgate

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|initialMonthRange|integer|true|none|Mês inicial do range|
|finalMonthRange|integer|true|none|Mês final do range|
|percentage|number|true|none|Percentual da faixa de resgate|

<h2 id="tocS_PersonReclaim">PersonReclaim</h2>
<!-- backwards compatibility -->
<a id="schemapersonreclaim"></a>
<a id="schema_PersonReclaim"></a>
<a id="tocSpersonreclaim"></a>
<a id="tocspersonreclaim"></a>

```json
{
  "reclaimTable": [
    {
      "initialMonthRange": 1,
      "finalMonthRange": 12,
      "percentage": 0
    }
  ],
  "differentiatedPercentage": "string",
  "gracePeriod": {
    "amount": 60,
    "unit": "DIAS"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|reclaimTable|[[personReclaimTable](#schemapersonreclaimtable)]|true|none|Listagem de percentuais de resgate da PMBaC para cada conjunto de prazo aplicável e para cada combinação de modalidade/cobertura estruturados em regime de capitalização|
|differentiatedPercentage|string|false|none|Campo aberto (possibilidade de incluir URL).|
|gracePeriod|[PersonGracePeriodUnit](#schemapersongraceperiodunit)|true|none|Período de carência|

<h2 id="tocS_PersonPremiumPayment">PersonPremiumPayment</h2>
<!-- backwards compatibility -->
<a id="schemapersonpremiumpayment"></a>
<a id="schema_PersonPremiumPayment"></a>
<a id="tocSpersonpremiumpayment"></a>
<a id="tocspersonpremiumpayment"></a>

```json
{
  "paymentMethod": [
    "CARTAO_CREDITO"
  ],
  "frequency": [
    "DIARIA"
  ],
  "premiumTax": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|paymentMethod|[string]|true|none|none|
|frequency|[string]|true|none|none|
|premiumTax|string|false|none|Distribuição de frequência relativa aos valores referentes às taxas cobradas.|

<h2 id="tocS_PersonMinimumRequirements">PersonMinimumRequirements</h2>
<!-- backwards compatibility -->
<a id="schemapersonminimumrequirements"></a>
<a id="schema_PersonMinimumRequirements"></a>
<a id="tocSpersonminimumrequirements"></a>
<a id="tocspersonminimumrequirements"></a>

```json
{
  "contractingType": "COLETIVO",
  "contractingMinRequirement": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contractingType|string|true|none|none|
|contractingMinRequirement|string|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|contractingType|COLETIVO|
|contractingType|INDIVIDUAL|

<h2 id="tocS_LinksPaginated">LinksPaginated</h2>
<!-- backwards compatibility -->
<a id="schemalinkspaginated"></a>
<a id="schema_LinksPaginated"></a>
<a id="tocSlinkspaginated"></a>
<a id="tocslinkspaginated"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
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
  "totalRecords": 10,
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
    "totalRecords": 10,
    "totalPages": 1
  }
}

```

<h2 id="tocS_ResponsePensionPlanList">ResponsePensionPlanList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsepensionplanlist"></a>
<a id="schema_ResponsePensionPlanList"></a>
<a id="tocSresponsepensionplanlist"></a>
<a id="tocsresponsepensionplanlist"></a>

```json
{
  "requestTime": "2021-08-20T08:30:00Z",
  "data": {},
  "brand": {
    "name": "EMPRESA",
    "companies": {
      "name": "EMPRESA Seguros",
      "cnpjNumber": 45086338000178,
      "products": [
        {
          "name": "Nome comercial do Produto",
          "code": "123456789_cap",
          "modality": "PENSAO",
          "coverages": [
            {
              "coverage": "INVALIDEZ",
              "coveragesAttributes": {
                "indenizationPaymentMethod": "Pagamento Único",
                "minValue": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "maxValue": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "indemnifiablePeriod": "Prazo",
                "indemnifiableDeadline": 48,
                "currency": "BRL",
                "gracePeriod": {
                  "amount": 0,
                  "unit": "DIAS"
                },
                "excludedRisk": [
                  "ATO_RECONHECIMENTO_PERIGOSO"
                ],
                "excludedRiskURL": "string"
              },
              "coveragePeriod": "Vitalícia"
            }
          ],
          "additional": "SORTEIO",
          "additionalOthers": "string",
          "assistanceType": [
            "Funeral"
          ],
          "assistanceTypeOthers": [
            "string"
          ],
          "termAndCondition": [
            {
              "susepProcessNumber": "15414.622222/2222-22",
              "definition": "wwww.seguradora.com.br/termos"
            }
          ],
          "updatePMBaC": {
            "interestRate": 14,
            "updateIndex": "IPCA(IBGE)"
          },
          "premiumUpdateIndex": "IPCA",
          "ageReframing": {
            "reframingCriterion": "Após período em anos",
            "reframingPeriodicity": 10
          },
          "financialRegimeContractType": "Repartição Simples",
          "reclaim": {
            "reclaimTable": [
              {
                "initialMonthRange": 0,
                "finalMonthRange": 0,
                "percentage": "string"
              }
            ],
            "differentiatedPercentage": "string",
            "gracePeriod": "20/Não se aplica"
          },
          "otherGuarateedValues": "Saldamento",
          "profitModality": "PAGAMENTO_UNICO",
          "contributionPayment": {
            "contributionPaymentMethod": [
              "Cartão de crédito"
            ],
            "contributionPeriodicity": [
              "Mensal"
            ]
          },
          "contributionTax": "string",
          "minimumRequirements": {
            "minRequirementsContractType": "Individual",
            "minRequirementsContract": "wwww.seguradora.com.br/termos"
          },
          "targetAudience": "Pessoa Natural"
        }
      ]
    }
  },
  "linksPaginated": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "metaPaginated": {
    "totalRecords": 10,
    "totalPages": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|requestTime|string(date-time)|false|none|Data e hora da consulta, conforme especificação RFC-3339, formato UTC.|
|data|object|true|none|none|
|brand|[PensionPlanBrand](#schemapensionplanbrand)|true|none|Organização controladora do grupo.|
|linksPaginated|[LinksPaginated](#schemalinkspaginated)|true|none|none|
|metaPaginated|[MetaPaginated](#schemametapaginated)|true|none|none|

<h2 id="tocS_PensionPlanBrand">PensionPlanBrand</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanbrand"></a>
<a id="schema_PensionPlanBrand"></a>
<a id="tocSpensionplanbrand"></a>
<a id="tocspensionplanbrand"></a>

```json
{
  "name": "EMPRESA",
  "companies": {
    "name": "EMPRESA Seguros",
    "cnpjNumber": 45086338000178,
    "products": [
      {
        "name": "Nome comercial do Produto",
        "code": "123456789_cap",
        "modality": "PENSAO",
        "coverages": [
          {
            "coverage": "INVALIDEZ",
            "coveragesAttributes": {
              "indenizationPaymentMethod": "Pagamento Único",
              "minValue": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "maxValue": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "indemnifiablePeriod": "Prazo",
              "indemnifiableDeadline": 48,
              "currency": "BRL",
              "gracePeriod": {
                "amount": 0,
                "unit": "DIAS"
              },
              "excludedRisk": [
                "ATO_RECONHECIMENTO_PERIGOSO"
              ],
              "excludedRiskURL": "string"
            },
            "coveragePeriod": "Vitalícia"
          }
        ],
        "additional": "SORTEIO",
        "additionalOthers": "string",
        "assistanceType": [
          "Funeral"
        ],
        "assistanceTypeOthers": [
          "string"
        ],
        "termAndCondition": [
          {
            "susepProcessNumber": "15414.622222/2222-22",
            "definition": "wwww.seguradora.com.br/termos"
          }
        ],
        "updatePMBaC": {
          "interestRate": 14,
          "updateIndex": "IPCA(IBGE)"
        },
        "premiumUpdateIndex": "IPCA",
        "ageReframing": {
          "reframingCriterion": "Após período em anos",
          "reframingPeriodicity": 10
        },
        "financialRegimeContractType": "Repartição Simples",
        "reclaim": {
          "reclaimTable": [
            {
              "initialMonthRange": 0,
              "finalMonthRange": 0,
              "percentage": "string"
            }
          ],
          "differentiatedPercentage": "string",
          "gracePeriod": "20/Não se aplica"
        },
        "otherGuarateedValues": "Saldamento",
        "profitModality": "PAGAMENTO_UNICO",
        "contributionPayment": {
          "contributionPaymentMethod": [
            "Cartão de crédito"
          ],
          "contributionPeriodicity": [
            "Mensal"
          ]
        },
        "contributionTax": "string",
        "minimumRequirements": {
          "minRequirementsContractType": "Individual",
          "minRequirementsContract": "wwww.seguradora.com.br/termos"
        },
        "targetAudience": "Pessoa Natural"
      }
    ]
  }
}

```

Organização controladora do grupo.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da marca reportada pelo participante do Open Insurance. O conceito a que se refere a marca é em essência uma promessa das sociedades sob ela em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes.|
|companies|[PensionPlanCompany](#schemapensionplancompany)|true|none|Informações referente a sociedade a qual a marca pertence.|

<h2 id="tocS_PensionPlanCompany">PensionPlanCompany</h2>
<!-- backwards compatibility -->
<a id="schemapensionplancompany"></a>
<a id="schema_PensionPlanCompany"></a>
<a id="tocSpensionplancompany"></a>
<a id="tocspensionplancompany"></a>

```json
{
  "name": "EMPRESA Seguros",
  "cnpjNumber": 45086338000178,
  "products": [
    {
      "name": "Nome comercial do Produto",
      "code": "123456789_cap",
      "modality": "PENSAO",
      "coverages": [
        {
          "coverage": "INVALIDEZ",
          "coveragesAttributes": {
            "indenizationPaymentMethod": "Pagamento Único",
            "minValue": {
              "amount": 0,
              "unit": {
                "code": "string",
                "description": "string"
              }
            },
            "maxValue": {
              "amount": 0,
              "unit": {
                "code": "string",
                "description": "string"
              }
            },
            "indemnifiablePeriod": "Prazo",
            "indemnifiableDeadline": 48,
            "currency": "BRL",
            "gracePeriod": {
              "amount": 0,
              "unit": "DIAS"
            },
            "excludedRisk": [
              "ATO_RECONHECIMENTO_PERIGOSO"
            ],
            "excludedRiskURL": "string"
          },
          "coveragePeriod": "Vitalícia"
        }
      ],
      "additional": "SORTEIO",
      "additionalOthers": "string",
      "assistanceType": [
        "Funeral"
      ],
      "assistanceTypeOthers": [
        "string"
      ],
      "termAndCondition": [
        {
          "susepProcessNumber": "15414.622222/2222-22",
          "definition": "wwww.seguradora.com.br/termos"
        }
      ],
      "updatePMBaC": {
        "interestRate": 14,
        "updateIndex": "IPCA(IBGE)"
      },
      "premiumUpdateIndex": "IPCA",
      "ageReframing": {
        "reframingCriterion": "Após período em anos",
        "reframingPeriodicity": 10
      },
      "financialRegimeContractType": "Repartição Simples",
      "reclaim": {
        "reclaimTable": [
          {
            "initialMonthRange": 0,
            "finalMonthRange": 0,
            "percentage": "string"
          }
        ],
        "differentiatedPercentage": "string",
        "gracePeriod": "20/Não se aplica"
      },
      "otherGuarateedValues": "Saldamento",
      "profitModality": "PAGAMENTO_UNICO",
      "contributionPayment": {
        "contributionPaymentMethod": [
          "Cartão de crédito"
        ],
        "contributionPeriodicity": [
          "Mensal"
        ]
      },
      "contributionTax": "string",
      "minimumRequirements": {
        "minRequirementsContractType": "Individual",
        "minRequirementsContract": "wwww.seguradora.com.br/termos"
      },
      "targetAudience": "Pessoa Natural"
    }
  ]
}

```

Informações referente a sociedade a qual a marca pertence.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da sociedade pertencente à marca.|
|cnpjNumber|string|true|none|CNPJ da sociedade pertencente à marca.|
|products|[PensionPlanProduct](#schemapensionplanproduct)|false|none|Produtos de Seguro de Automóveis.|

<h2 id="tocS_PensionPlanProduct">PensionPlanProduct</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanproduct"></a>
<a id="schema_PensionPlanProduct"></a>
<a id="tocSpensionplanproduct"></a>
<a id="tocspensionplanproduct"></a>

```json
[
  {
    "name": "Nome comercial do Produto",
    "code": "123456789_cap",
    "modality": "PENSAO",
    "coverages": [
      {
        "coverage": "INVALIDEZ",
        "coveragesAttributes": {
          "indenizationPaymentMethod": "Pagamento Único",
          "minValue": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "maxValue": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "indemnifiablePeriod": "Prazo",
          "indemnifiableDeadline": 48,
          "currency": "BRL",
          "gracePeriod": {
            "amount": 0,
            "unit": "DIAS"
          },
          "excludedRisk": [
            "ATO_RECONHECIMENTO_PERIGOSO"
          ],
          "excludedRiskURL": "string"
        },
        "coveragePeriod": "Vitalícia"
      }
    ],
    "additional": "SORTEIO",
    "additionalOthers": "string",
    "assistanceType": [
      "Funeral"
    ],
    "assistanceTypeOthers": [
      "string"
    ],
    "termAndCondition": [
      {
        "susepProcessNumber": "15414.622222/2222-22",
        "definition": "wwww.seguradora.com.br/termos"
      }
    ],
    "updatePMBaC": {
      "interestRate": 14,
      "updateIndex": "IPCA(IBGE)"
    },
    "premiumUpdateIndex": "IPCA",
    "ageReframing": {
      "reframingCriterion": "Após período em anos",
      "reframingPeriodicity": 10
    },
    "financialRegimeContractType": "Repartição Simples",
    "reclaim": {
      "reclaimTable": [
        {
          "initialMonthRange": 0,
          "finalMonthRange": 0,
          "percentage": "string"
        }
      ],
      "differentiatedPercentage": "string",
      "gracePeriod": "20/Não se aplica"
    },
    "otherGuarateedValues": "Saldamento",
    "profitModality": "PAGAMENTO_UNICO",
    "contributionPayment": {
      "contributionPaymentMethod": [
        "Cartão de crédito"
      ],
      "contributionPeriodicity": [
        "Mensal"
      ]
    },
    "contributionTax": "string",
    "minimumRequirements": {
      "minRequirementsContractType": "Individual",
      "minRequirementsContract": "wwww.seguradora.com.br/termos"
    },
    "targetAudience": "Pessoa Natural"
  }
]

```

Produtos de Seguro de Automóveis.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome comercial do produto, pelo qual é identificado nos canais de distribuição e atendimento da sociedade.|
|code|string|true|none|Código único a ser definido pela sociedade.|
|modality|string|true|none|Lista padronizada de modalidades de coberturas  incluídas no produto.|
|coverages|[object]|true|none|none|
|» coverage|string|false|none|Formas de coberturas.|
|» coveragesAttributes|[PensionPlanCoverageAttributes](#schemapensionplancoverageattributes)|false|none|Atributos da cobertura.|
|» coveragePeriod|string|false|none|Formas de coberturas.|
|additional|string|false|none|Adicional ao plano.|
|additionalOthers|string|false|none|Lista a ser preenchida pelas participantes quando houver ‘Outros’ no campo ‘additional’|
|assistanceType|[string]|false|none|Tipos de assistências.|
|assistanceTypeOthers|[string]|false|none|Outros tipos de assistências.|
|termAndCondition|[[PensionPlanTerms](#schemapensionplanterms)]|false|none|[Informações dos termos e condições conforme número do processo SUSEP.]|
|updatePMBaC|[PensionPlanUpdatePMBaC](#schemapensionplanupdatepmbac)|false|none|Atualização/ Remuneração da PMaC.|
|premiumUpdateIndex|string|true|none|Índice utilizado na atualização do prêmio/contribuição e do capital segurado/benefício|
|ageReframing|[PensionPlanAgeReframing](#schemapensionplanagereframing)|false|none|Reenquadramento etário.|
|financialRegimeContractType|string|true|none|Tipo de contratação de regime financeiro.|
|reclaim|[PensionPlanReclaim](#schemapensionplanreclaim)|false|none|Resgate.|
|otherGuarateedValues|string|true|none|Outros valores garantidos.|
|profitModality|string|true|none|Modalidade de pagamento da indenização.|
|contributionPayment|[PensionPlanContributionPayment](#schemapensionplancontributionpayment)|true|none|Pagamento da contribuição.|
|contributionTax|string|false|none|Distribuição de frequência relativa aos valores referentes às taxas cobradas|
|minimumRequirements|[PensionPlanMinimumRequirements](#schemapensionplanminimumrequirements)|true|none|Requisitos mínimos.|
|targetAudience|string|true|none|none|

#### Enumerated Values

|Property|Value|
|---|---|
|modality|PECULIO|
|modality|RENDA|
|modality|PENSAO_PRAZO_CERTO|
|modality|PENSAO_MENORES_21|
|modality|PENSAO_MENORES_24|
|modality|PENSAO_CONJUGE_VITALICIA|
|modality|PENSAO_CONJUGE_TEMPORARIA|
|coverage|MORTE|
|coverage|INVALIDEZ|
|coveragePeriod|VITALICIA|
|coveragePeriod|TEMPORARIA|
|additional|SORTEIO|
|additional|OUTROS|
|premiumUpdateIndex|IPCA|
|premiumUpdateIndex|IGPM|
|premiumUpdateIndex|INPC|
|financialRegimeContractType|REPARTICAO_SIMPLES|
|financialRegimeContractType|REPARTICAO_CAPITAIS_COBERTURA|
|financialRegimeContractType|CAPITALIZACAO|
|otherGuarateedValues|SALDAMENTO|
|otherGuarateedValues|BENEFICIO_PROLOGANDO|
|otherGuarateedValues|NAO_APLICA|
|profitModality|PAGAMENTO_UNICO|
|profitModality|FORMA_RENDA|
|targetAudience|PESSOA_NATURAL|
|targetAudience|PESSOA_JURIDICA|

<h2 id="tocS_PensionPlanTerms">PensionPlanTerms</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanterms"></a>
<a id="schema_PensionPlanTerms"></a>
<a id="tocSpensionplanterms"></a>
<a id="tocspensionplanterms"></a>

```json
{
  "susepProcessNumber": "15414.622222/2222-22",
  "definition": "wwww.seguradora.com.br/termos"
}

```

Informações dos termos e condições conforme número do processo SUSEP.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|susepProcessNumber|string|true|none|Número do processo SUSEP.|
|definition|string|true|none|Campo aberto (possibilidade de incluir uma url).|

<h2 id="tocS_PensionPlanCovaregeAttibutesDetailsUnit">PensionPlanCovaregeAttibutesDetailsUnit</h2>
<!-- backwards compatibility -->
<a id="schemapensionplancovaregeattibutesdetailsunit"></a>
<a id="schema_PensionPlanCovaregeAttibutesDetailsUnit"></a>
<a id="tocSpensionplancovaregeattibutesdetailsunit"></a>
<a id="tocspensionplancovaregeattibutesdetailsunit"></a>

```json
{
  "code": "string",
  "description": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|true|none|Tipo unidade de medida|
|description|string|true|none|Descrição da unidade de medida|

<h2 id="tocS_PensionPlanCovaregeAttibutesDetails">PensionPlanCovaregeAttibutesDetails</h2>
<!-- backwards compatibility -->
<a id="schemapensionplancovaregeattibutesdetails"></a>
<a id="schema_PensionPlanCovaregeAttibutesDetails"></a>
<a id="tocSpensionplancovaregeattibutesdetails"></a>
<a id="tocspensionplancovaregeattibutesdetails"></a>

```json
{
  "amount": 0,
  "unit": {
    "code": "string",
    "description": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number|true|none|none|
|unit|[PensionPlanCovaregeAttibutesDetailsUnit](#schemapensionplancovaregeattibutesdetailsunit)|true|none|none|

<h2 id="tocS_PensionPlanCoverageAttributes">PensionPlanCoverageAttributes</h2>
<!-- backwards compatibility -->
<a id="schemapensionplancoverageattributes"></a>
<a id="schema_PensionPlanCoverageAttributes"></a>
<a id="tocSpensionplancoverageattributes"></a>
<a id="tocspensionplancoverageattributes"></a>

```json
{
  "indenizationPaymentMethod": "Pagamento Único",
  "minValue": {
    "amount": 0,
    "unit": {
      "code": "string",
      "description": "string"
    }
  },
  "maxValue": {
    "amount": 0,
    "unit": {
      "code": "string",
      "description": "string"
    }
  },
  "indemnifiablePeriod": "Prazo",
  "indemnifiableDeadline": 48,
  "currency": "BRL",
  "gracePeriod": {
    "amount": 0,
    "unit": "DIAS"
  },
  "excludedRisk": [
    "ATO_RECONHECIMENTO_PERIGOSO"
  ],
  "excludedRiskURL": "string"
}

```

Atributos da cobertura.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|indenizationPaymentMethod|string|true|none|Forma de pagamento da indenização.|
|minValue|[PensionPlanCovaregeAttibutesDetails](#schemapensionplancovaregeattibutesdetails)|true|none|Valor mínimo de cobertura diária ou parcelada. Em reais.|
|maxValue|[PensionPlanCovaregeAttibutesDetails](#schemapensionplancovaregeattibutesdetails)|true|none|Valor máxima de cobertura diária ou parcelada. Em reais.|
|indemnifiablePeriod|string|true|none|Período indenizável. Se for indenização única, esse campo não se aplica.|
|indemnifiableDeadline|integer|true|none|Número máximo de parcelas indenizáveis. Caso seja relacionado a parcelas.|
|currency|string|true|none|Moeda utilizada.|
|gracePeriod|[PensionPlanGracePeriod](#schemapensionplangraceperiod)|true|none|Período de carência.|
|excludedRisk|[string]|true|none|Riscos excluídos.|
|excludedRiskURL|string|true|none|Campo aberto (possibilidade de incluir URL)|

#### Enumerated Values

|Property|Value|
|---|---|
|indenizationPaymentMethod|PAGAMENTO_UNICO|
|indenizationPaymentMethod|FORMA_RENDA|
|indemnifiablePeriod|PRAZO|
|indemnifiablePeriod|ATE_FIM_CICLO_DETERMINADO|
|currency|AFN|
|currency|ALL|
|currency|DZD|
|currency|USD|
|currency|EUR|
|currency|AOA|
|currency|XCD|
|currency|XCD|
|currency|ARS|
|currency|AMD|
|currency|AWG|
|currency|AUD|
|currency|EUR|
|currency|AZN|
|currency|BSD|
|currency|BHD|
|currency|BDT|
|currency|BBD|
|currency|BYN|
|currency|EUR|
|currency|BZD|
|currency|XOF|
|currency|BMD|
|currency|BTN|
|currency|BOB|
|currency|BOV|
|currency|USD|
|currency|BAM|
|currency|BWP|
|currency|NOK|
|currency|BRL|
|currency|USD|
|currency|BND|
|currency|BGN|
|currency|XOF|
|currency|BIF|
|currency|CVE|
|currency|KHR|
|currency|XAF|
|currency|CAD|
|currency|KYD|
|currency|XAF|
|currency|XAF|
|currency|CLF|
|currency|CLP|
|currency|CNY|
|currency|AUD|
|currency|AUD|
|currency|COP|
|currency|COU|
|currency|KMF|
|currency|CDF|
|currency|XAF|
|currency|NZD|
|currency|CRC|
|currency|HRK|
|currency|CUC|
|currency|CUP|
|currency|ANG|
|currency|EUR|
|currency|CZK|
|currency|XOF|
|currency|DKK|
|currency|DJF|
|currency|XCD|
|currency|DOP|
|currency|USD|
|currency|EGP|
|currency|SVC|
|currency|USD|
|currency|XAF|
|currency|ERN|
|currency|EUR|
|currency|ETB|
|currency|EUR|
|currency|FKP|
|currency|DKK|
|currency|FJD|
|currency|EUR|
|currency|EUR|
|currency|EUR|
|currency|XPF|
|currency|EUR|
|currency|XAF|
|currency|GMD|
|currency|GEL|
|currency|EUR|
|currency|GHS|
|currency|GIP|
|currency|EUR|
|currency|DKK|
|currency|XCD|
|currency|EUR|
|currency|USD|
|currency|GTQ|
|currency|GBP|
|currency|GNF|
|currency|XOF|
|currency|GYD|
|currency|HTG|
|currency|USD|
|currency|AUD|
|currency|EUR|
|currency|HNL|
|currency|HKD|
|currency|HUF|
|currency|ISK|
|currency|INR|
|currency|IDR|
|currency|XDR|
|currency|IRR|
|currency|IQD|
|currency|EUR|
|currency|GBP|
|currency|ILS|
|currency|EUR|
|currency|JMD|
|currency|JPY|
|currency|GBP|
|currency|JOD|
|currency|KZT|
|currency|KES|
|currency|AUD|
|currency|KPW|
|currency|KRW|
|currency|KWD|
|currency|KGS|
|currency|LAK|
|currency|EUR|
|currency|LBP|
|currency|LSL|
|currency|ZAR|
|currency|LRD|
|currency|LYD|
|currency|CHF|
|currency|EUR|
|currency|EUR|
|currency|MOP|
|currency|MGA|
|currency|MWK|
|currency|MYR|
|currency|MVR|
|currency|XOF|
|currency|EUR|
|currency|USD|
|currency|EUR|
|currency|MRU|
|currency|MUR|
|currency|EUR|
|currency|XUA|
|currency|MXN|
|currency|MXV|
|currency|USD|
|currency|MDL|
|currency|EUR|
|currency|MNT|
|currency|EUR|
|currency|XCD|
|currency|MAD|
|currency|MZN|
|currency|MMK|
|currency|NAD|
|currency|ZAR|
|currency|AUD|
|currency|NPR|
|currency|EUR|
|currency|XPF|
|currency|NZD|
|currency|NIO|
|currency|XOF|
|currency|NGN|
|currency|NZD|
|currency|AUD|
|currency|USD|
|currency|NOK|
|currency|OMR|
|currency|PKR|
|currency|USD|
|currency|PAB|
|currency|USD|
|currency|PGK|
|currency|PYG|
|currency|PEN|
|currency|PHP|
|currency|NZD|
|currency|PLN|
|currency|EUR|
|currency|USD|
|currency|QAR|
|currency|MKD|
|currency|RON|
|currency|RUB|
|currency|RWF|
|currency|EUR|
|currency|EUR|
|currency|SHP|
|currency|XCD|
|currency|XCD|
|currency|EUR|
|currency|EUR|
|currency|XCD|
|currency|WST|
|currency|EUR|
|currency|STN|
|currency|SAR|
|currency|XOF|
|currency|RSD|
|currency|SCR|
|currency|SLL|
|currency|SGD|
|currency|ANG|
|currency|XSU|
|currency|EUR|
|currency|EUR|
|currency|SBD|
|currency|SOS|
|currency|ZAR|
|currency|SSP|
|currency|EUR|
|currency|LKR|
|currency|SDG|
|currency|SRD|
|currency|NOK|
|currency|SZL|
|currency|SEK|
|currency|CHE|
|currency|CHF|
|currency|CHW|
|currency|SYP|
|currency|TWD|
|currency|TJS|
|currency|TZS|
|currency|THB|
|currency|USD|
|currency|XOF|
|currency|NZD|
|currency|TOP|
|currency|TTD|
|currency|TND|
|currency|TRY|
|currency|TMT|
|currency|USD|
|currency|AUD|
|currency|UGX|
|currency|UAH|
|currency|AED|
|currency|GBP|
|currency|USD|
|currency|USD|
|currency|USN|
|currency|UYI|
|currency|UYU|
|currency|UZS|
|currency|VUV|
|currency|VEF|
|currency|VND|
|currency|USD|
|currency|USD|
|currency|XPF|
|currency|MAD|
|currency|YER|
|currency|ZMW|
|currency|ZWL|
|currency|EUR|

<h2 id="tocS_PensionPlanUpdatePMBaC">PensionPlanUpdatePMBaC</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanupdatepmbac"></a>
<a id="schema_PensionPlanUpdatePMBaC"></a>
<a id="tocSpensionplanupdatepmbac"></a>
<a id="tocspensionplanupdatepmbac"></a>

```json
{
  "interestRate": 14,
  "updateIndex": "IPCA(IBGE)"
}

```

Atualização/ Remuneração da PMaC.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|interestRate|number|true|none|Taxa de juros para capitalização da PMBaC PMBC.|
|updateIndex|string|true|none|Índice utilizado na atualização da PMBaC.|

#### Enumerated Values

|Property|Value|
|---|---|
|updateIndex|FINANCEIRA|
|updateIndex|IGPM|
|updateIndex|INPC|

<h2 id="tocS_PensionPlanAgeReframing">PensionPlanAgeReframing</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanagereframing"></a>
<a id="schema_PensionPlanAgeReframing"></a>
<a id="tocSpensionplanagereframing"></a>
<a id="tocspensionplanagereframing"></a>

```json
{
  "reframingCriterion": "Após período em anos",
  "reframingPeriodicity": 10
}

```

Reenquadramento etário.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|reframingCriterion|string|true|none|Critério para reenquadramento etário.|
|reframingPeriodicity|integer|true|none|Período em anos para reenquadramento etário.|

#### Enumerated Values

|Property|Value|
|---|---|
|reframingCriterion|APOS_PERIODO_ANOS|
|reframingCriterion|CADA_PERIODO_ANOS|
|reframingCriterion|MUDANCA_FAIXA_ETARIA|
|reframingCriterion|NAO_APLICAVEL|

<h2 id="tocS_PensionPlanReclaim">PensionPlanReclaim</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanreclaim"></a>
<a id="schema_PensionPlanReclaim"></a>
<a id="tocSpensionplanreclaim"></a>
<a id="tocspensionplanreclaim"></a>

```json
{
  "reclaimTable": [
    {
      "initialMonthRange": 0,
      "finalMonthRange": 0,
      "percentage": "string"
    }
  ],
  "differentiatedPercentage": "string",
  "gracePeriod": "20/Não se aplica"
}

```

Resgate.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|reclaimTable|[[PensionPlanReclaimTable](#schemapensionplanreclaimtable)]|true|none|Percentual de resgate para PMBaC para cada conjunto aplicável.|
|differentiatedPercentage|string|false|none|Campo aberto (possibilidade de incluir URL)|
|gracePeriod|string|true|none|Prazo de carência em dias para resgate.|

<h2 id="tocS_PensionPlanReclaimTable">PensionPlanReclaimTable</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanreclaimtable"></a>
<a id="schema_PensionPlanReclaimTable"></a>
<a id="tocSpensionplanreclaimtable"></a>
<a id="tocspensionplanreclaimtable"></a>

```json
{
  "initialMonthRange": 0,
  "finalMonthRange": 0,
  "percentage": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|initialMonthRange|number|true|none|Mês inicial do range|
|finalMonthRange|number|true|none|Mês final do range|
|percentage|string|true|none|Percentual da faixa de resgate|

<h2 id="tocS_PensionPlanContributionPayment">PensionPlanContributionPayment</h2>
<!-- backwards compatibility -->
<a id="schemapensionplancontributionpayment"></a>
<a id="schema_PensionPlanContributionPayment"></a>
<a id="tocSpensionplancontributionpayment"></a>
<a id="tocspensionplancontributionpayment"></a>

```json
{
  "contributionPaymentMethod": [
    "Cartão de crédito"
  ],
  "contributionPeriodicity": [
    "Mensal"
  ]
}

```

Pagamento da contribuição.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contributionPaymentMethod|[string]|true|none|Forma de pagamento da contribuição.|
|contributionPeriodicity|[string]|true|none|Periodicidade de pagamento da contribuição.|

<h2 id="tocS_PensionPlanMinimumRequirements">PensionPlanMinimumRequirements</h2>
<!-- backwards compatibility -->
<a id="schemapensionplanminimumrequirements"></a>
<a id="schema_PensionPlanMinimumRequirements"></a>
<a id="tocSpensionplanminimumrequirements"></a>
<a id="tocspensionplanminimumrequirements"></a>

```json
{
  "minRequirementsContractType": "Individual",
  "minRequirementsContract": "wwww.seguradora.com.br/termos"
}

```

Requisitos mínimos.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|minRequirementsContractType|string|true|none|Tipo de contratação.|
|minRequirementsContract|string|true|none|Campo aberto contendo todos os requisitos mínimos para contratação.|

#### Enumerated Values

|Property|Value|
|---|---|
|minRequirementsContractType|COLETIVO|
|minRequirementsContractType|INDIVIDUAL|

<h2 id="tocS_PensionPlanGracePeriod">PensionPlanGracePeriod</h2>
<!-- backwards compatibility -->
<a id="schemapensionplangraceperiod"></a>
<a id="schema_PensionPlanGracePeriod"></a>
<a id="tocSpensionplangraceperiod"></a>
<a id="tocspensionplangraceperiod"></a>

```json
{
  "amount": 0,
  "unit": "DIAS"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number|false|none|Prazo de Carência|
|unit|string|false|none|Unidade do prazo (dias ou meses)|

#### Enumerated Values

|Property|Value|
|---|---|
|unit|DIAS|
|unit|MESES|
|unit|NAO_SE_APLICA|

<h2 id="tocS_LinksPaginated">LinksPaginated</h2>
<!-- backwards compatibility -->
<a id="schemalinkspaginated"></a>
<a id="schema_LinksPaginated"></a>
<a id="tocSlinkspaginated"></a>
<a id="tocslinkspaginated"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|self|string|true|none|URI completo que gerou a resposta atual.|
|first|string|false|none|URI da primeira página que originou essa lista de resultados. Restrição - Obrigatório quando não for a primeira página da resposta|
|prev|string|false|none|URI da página anterior dessa lista de resultados. Restrição - Obrigatório quando não for a primeira página da resposta|
|next|string|false|none|URI da próxima página dessa lista de resultados. Restrição - Obrigatório quando não for a última página da resposta|
|last|string|false|none|URI da última página dessa lista de resultados. Restrição - Obrigatório quando não for a última página da resposta|

<h2 id="tocS_MetaPaginated">MetaPaginated</h2>
<!-- backwards compatibility -->
<a id="schemametapaginated"></a>
<a id="schema_MetaPaginated"></a>
<a id="tocSmetapaginated"></a>
<a id="tocsmetapaginated"></a>

```json
{
  "totalRecords": 10,
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
    "totalRecords": 10,
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

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|errors|[object]|true|none|none|
|» code|string|true|none|Código de erro específico do endpoint|
|» title|string|true|none|Título legível por humanos deste erro específico|
|» detail|string|true|none|Descrição legível por humanos deste erro específico|
|» requestDateTime|string(date-time)|true|none|Data e hora da consulta, conforme especificação RFC-3339, formato UTC.|
|meta|[MetaPaginated](#schemametapaginated)|false|none|none|

<h2 id="tocS_ResponseAutoInsuranceList">ResponseAutoInsuranceList</h2>
<!-- backwards compatibility -->
<a id="schemaresponseautoinsurancelist"></a>
<a id="schema_ResponseAutoInsuranceList"></a>
<a id="tocSresponseautoinsurancelist"></a>
<a id="tocsresponseautoinsurancelist"></a>

```json
{
  "data": {
    "brand": {
      "name": "string",
      "company": [
        {
          "name": "string",
          "cnpjNumber": "string",
          "products": [
            {
              "name": "string",
              "code": "string",
              "coverages": [
                {
                  "coverage": "VIDROS",
                  "coverageDetail": "Roubo total",
                  "coveragePermissionSeparteAcquisition": true,
                  "coverageAttributes": {
                    "minLMI": {},
                    "maxLMI": {},
                    "contractBase": [],
                    "newCarMaximumCalculatingPeriod": 12,
                    "newCarContractBase": [],
                    "fullIndemnityPercentage": {},
                    "deductibleType": [],
                    "fullIndemnityDeductible": true,
                    "deductiblePaymentByCoverage": true,
                    "deductiblePercentage": {},
                    "mandatoryParticipation": "Casco - RCF-V Danos",
                    "geographicScopeCoverage": [],
                    "geographicScopeCoverageOthers": "string"
                  }
                }
              ],
              "carParts": [
                {
                  "carPartCondition": "NOVAS",
                  "carPartType": "ORIGINAIS"
                }
              ],
              "carModels": [
                {
                  "manufacturer": "FORD",
                  "model": "KA",
                  "year": 2018,
                  "fipeCode": "string"
                }
              ],
              "vehicleOvernightZipCode": 1311000,
              "additional": [
                "SORTEIO GRATUITO"
              ],
              "additionalOthers": "string",
              "assistanceServices": [
                {
                  "assistanceServicesPackage": [
                    "ATE_10_SERVICOS"
                  ],
                  "assistanceServicesDetail": "Perda Parcial - Colisão",
                  "chargeTypeSignaling": "GRATUITA"
                }
              ],
              "termsAndConditions": [
                {
                  "susepProcessNumber": "15414.622222/2222-22",
                  "definition": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
                }
              ],
              "terms": [
                "ANUAL"
              ],
              "customerService": [
                "REDE REFERECIADA"
              ],
              "premiumPayment": {
                "paymentMethod": [
                  "CARTÃO DE CRÉDITO"
                ],
                "paymentType": [
                  "PARCELADO"
                ],
                "paymentDetail": "string"
              },
              "minimumRequirements": {
                "contractingType": [
                  "COLETIVO"
                ],
                "contractingMinRequirement": "https://example.com/mobile-banking"
              },
              "targetAudiences": [
                "PESSOA_NATURAL"
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|true|none|none|
|» brand|[AutoInsuranceBrand](#schemaautoinsurancebrand)|false|none|none|
|links|[Links](#schemalinks)|true|none|none|
|meta|[Meta](#schemameta)|true|none|none|

<h2 id="tocS_AutoInsuranceBrand">AutoInsuranceBrand</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancebrand"></a>
<a id="schema_AutoInsuranceBrand"></a>
<a id="tocSautoinsurancebrand"></a>
<a id="tocsautoinsurancebrand"></a>

```json
{
  "name": "string",
  "company": [
    {
      "name": "string",
      "cnpjNumber": "string",
      "products": [
        {
          "name": "string",
          "code": "string",
          "coverages": [
            {
              "coverage": "VIDROS",
              "coverageDetail": "Roubo total",
              "coveragePermissionSeparteAcquisition": true,
              "coverageAttributes": {
                "minLMI": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "maxLMI": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "contractBase": [
                  {
                    "contractBaseType": "VALOR DETERMINADO",
                    "contractBaseMinValue": {},
                    "contractBaseMaxValue": {}
                  }
                ],
                "newCarMaximumCalculatingPeriod": 12,
                "newCarContractBase": [
                  {
                    "contractBaseType": "VALOR DETERMINADO",
                    "contractBaseMinValue": {},
                    "contractBaseMaxValue": {}
                  }
                ],
                "fullIndemnityPercentage": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "deductibleType": [
                  "NORMAL"
                ],
                "fullIndemnityDeductible": true,
                "deductiblePaymentByCoverage": true,
                "deductiblePercentage": {
                  "amount": 0,
                  "unit": {
                    "code": "string",
                    "description": "string"
                  }
                },
                "mandatoryParticipation": "Casco - RCF-V Danos",
                "geographicScopeCoverage": [
                  "NACIONAL"
                ],
                "geographicScopeCoverageOthers": "string"
              }
            }
          ],
          "carParts": [
            {
              "carPartCondition": "NOVAS",
              "carPartType": "ORIGINAIS"
            }
          ],
          "carModels": [
            {
              "manufacturer": "FORD",
              "model": "KA",
              "year": 2018,
              "fipeCode": "string"
            }
          ],
          "vehicleOvernightZipCode": 1311000,
          "additional": [
            "SORTEIO GRATUITO"
          ],
          "additionalOthers": "string",
          "assistanceServices": [
            {
              "assistanceServicesPackage": [
                "ATE_10_SERVICOS"
              ],
              "assistanceServicesDetail": "Perda Parcial - Colisão",
              "chargeTypeSignaling": "GRATUITA"
            }
          ],
          "termsAndConditions": [
            {
              "susepProcessNumber": "15414.622222/2222-22",
              "definition": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
            }
          ],
          "terms": [
            "ANUAL"
          ],
          "customerService": [
            "REDE REFERECIADA"
          ],
          "premiumPayment": {
            "paymentMethod": [
              "CARTÃO DE CRÉDITO"
            ],
            "paymentType": [
              "PARCELADO"
            ],
            "paymentDetail": "string"
          },
          "minimumRequirements": {
            "contractingType": [
              "COLETIVO"
            ],
            "contractingMinRequirement": "https://example.com/mobile-banking"
          },
          "targetAudiences": [
            "PESSOA_NATURAL"
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
|name|string|true|none|Nome da marca reportada pelo participante do Open Insurance. O conceito a que se refere a marca é em essência uma promessa das sociedades sob ela em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes.|
|company|[AutoInsuranceCompany](#schemaautoinsurancecompany)|true|none|none|

<h2 id="tocS_AutoInsuranceCompany">AutoInsuranceCompany</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecompany"></a>
<a id="schema_AutoInsuranceCompany"></a>
<a id="tocSautoinsurancecompany"></a>
<a id="tocsautoinsurancecompany"></a>

```json
[
  {
    "name": "string",
    "cnpjNumber": "string",
    "products": [
      {
        "name": "string",
        "code": "string",
        "coverages": [
          {
            "coverage": "VIDROS",
            "coverageDetail": "Roubo total",
            "coveragePermissionSeparteAcquisition": true,
            "coverageAttributes": {
              "minLMI": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "maxLMI": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "contractBase": [
                {
                  "contractBaseType": "VALOR DETERMINADO",
                  "contractBaseMinValue": {
                    "amount": 0,
                    "unit": {}
                  },
                  "contractBaseMaxValue": {
                    "amount": 0,
                    "unit": {}
                  }
                }
              ],
              "newCarMaximumCalculatingPeriod": 12,
              "newCarContractBase": [
                {
                  "contractBaseType": "VALOR DETERMINADO",
                  "contractBaseMinValue": {
                    "amount": 0,
                    "unit": {}
                  },
                  "contractBaseMaxValue": {
                    "amount": 0,
                    "unit": {}
                  }
                }
              ],
              "fullIndemnityPercentage": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "deductibleType": [
                "NORMAL"
              ],
              "fullIndemnityDeductible": true,
              "deductiblePaymentByCoverage": true,
              "deductiblePercentage": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "mandatoryParticipation": "Casco - RCF-V Danos",
              "geographicScopeCoverage": [
                "NACIONAL"
              ],
              "geographicScopeCoverageOthers": "string"
            }
          }
        ],
        "carParts": [
          {
            "carPartCondition": "NOVAS",
            "carPartType": "ORIGINAIS"
          }
        ],
        "carModels": [
          {
            "manufacturer": "FORD",
            "model": "KA",
            "year": 2018,
            "fipeCode": "string"
          }
        ],
        "vehicleOvernightZipCode": 1311000,
        "additional": [
          "SORTEIO GRATUITO"
        ],
        "additionalOthers": "string",
        "assistanceServices": [
          {
            "assistanceServicesPackage": [
              "ATE_10_SERVICOS"
            ],
            "assistanceServicesDetail": "Perda Parcial - Colisão",
            "chargeTypeSignaling": "GRATUITA"
          }
        ],
        "termsAndConditions": [
          {
            "susepProcessNumber": "15414.622222/2222-22",
            "definition": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
          }
        ],
        "terms": [
          "ANUAL"
        ],
        "customerService": [
          "REDE REFERECIADA"
        ],
        "premiumPayment": {
          "paymentMethod": [
            "CARTÃO DE CRÉDITO"
          ],
          "paymentType": [
            "PARCELADO"
          ],
          "paymentDetail": "string"
        },
        "minimumRequirements": {
          "contractingType": [
            "COLETIVO"
          ],
          "contractingMinRequirement": "https://example.com/mobile-banking"
        },
        "targetAudiences": [
          "PESSOA_NATURAL"
        ]
      }
    ]
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da sociedade pertencente à marca.|
|cnpjNumber|string|true|none|CNPJ da sociedade pertencente à marca.|
|products|[AutoInsuranceProduct](#schemaautoinsuranceproduct)|true|none|Lista de Dependências de uma Instituição.|

<h2 id="tocS_AutoInsuranceProduct">AutoInsuranceProduct</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsuranceproduct"></a>
<a id="schema_AutoInsuranceProduct"></a>
<a id="tocSautoinsuranceproduct"></a>
<a id="tocsautoinsuranceproduct"></a>

```json
[
  {
    "name": "string",
    "code": "string",
    "coverages": [
      {
        "coverage": "VIDROS",
        "coverageDetail": "Roubo total",
        "coveragePermissionSeparteAcquisition": true,
        "coverageAttributes": {
          "minLMI": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "maxLMI": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "contractBase": [
            {
              "contractBaseType": "VALOR DETERMINADO",
              "contractBaseMinValue": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "contractBaseMaxValue": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              }
            }
          ],
          "newCarMaximumCalculatingPeriod": 12,
          "newCarContractBase": [
            {
              "contractBaseType": "VALOR DETERMINADO",
              "contractBaseMinValue": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              },
              "contractBaseMaxValue": {
                "amount": 0,
                "unit": {
                  "code": "string",
                  "description": "string"
                }
              }
            }
          ],
          "fullIndemnityPercentage": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "deductibleType": [
            "NORMAL"
          ],
          "fullIndemnityDeductible": true,
          "deductiblePaymentByCoverage": true,
          "deductiblePercentage": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "mandatoryParticipation": "Casco - RCF-V Danos",
          "geographicScopeCoverage": [
            "NACIONAL"
          ],
          "geographicScopeCoverageOthers": "string"
        }
      }
    ],
    "carParts": [
      {
        "carPartCondition": "NOVAS",
        "carPartType": "ORIGINAIS"
      }
    ],
    "carModels": [
      {
        "manufacturer": "FORD",
        "model": "KA",
        "year": 2018,
        "fipeCode": "string"
      }
    ],
    "vehicleOvernightZipCode": 1311000,
    "additional": [
      "SORTEIO GRATUITO"
    ],
    "additionalOthers": "string",
    "assistanceServices": [
      {
        "assistanceServicesPackage": [
          "ATE_10_SERVICOS"
        ],
        "assistanceServicesDetail": "Perda Parcial - Colisão",
        "chargeTypeSignaling": "GRATUITA"
      }
    ],
    "termsAndConditions": [
      {
        "susepProcessNumber": "15414.622222/2222-22",
        "definition": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
      }
    ],
    "terms": [
      "ANUAL"
    ],
    "customerService": [
      "REDE REFERECIADA"
    ],
    "premiumPayment": {
      "paymentMethod": [
        "CARTÃO DE CRÉDITO"
      ],
      "paymentType": [
        "PARCELADO"
      ],
      "paymentDetail": "string"
    },
    "minimumRequirements": {
      "contractingType": [
        "COLETIVO"
      ],
      "contractingMinRequirement": "https://example.com/mobile-banking"
    },
    "targetAudiences": [
      "PESSOA_NATURAL"
    ]
  }
]

```

Produtos de Seguro de Automóveis.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome comercial do produto, pelo qual é identificado nos canais de distribuição e atendimento da sociedade.|
|code|string|true|none|Código único a ser definido pela sociedade.|
|coverages|[AutoInsuranceCoverage](#schemaautoinsurancecoverage)|true|none|Listagem de coberturas incluídas no produto que deve observar a relação discriminada de coberturas, conforme Tabela II.5 do Anexo II|
|carParts|[AutoInsuranceCarPart](#schemaautoinsurancecarpart)|true|none|Tipo de peça utilizada para reparação.|
|carModels|[AutoInsuranceCarModel](#schemaautoinsurancecarmodel)|true|none|Listagem de modelos / ano de veículos. Deve ser padronizada na proposta técnica submetida pela Estrutura Inicial de Governança para observância comum por todas as sociedades participantes.|
|vehicleOvernightZipCode|string|true|none|Área de comercialização do seguro do automóvel.|
|additional|[string]|true|none|none|
|additionalOthers|string|false|none|Campo aberto para descrição de cada participante ao selecionar o domínio ‘Outros’ no campo acima ‘Adicionais’|
|assistanceServices|[[AutoInsuranceAssistanceServices](#schemaautoinsuranceassistanceservices)]|true|none|[Serviços de Assistência.]|
|termsAndConditions|[AutoInsuranceTermsAndConditions](#schemaautoinsurancetermsandconditions)|true|none|none|
|terms|[string]|true|none|Prazo.|
|customerService|[string]|true|none|Rede de atendimento do seguro contratado.|
|premiumPayment|[AutoInsurancePremiumPayment](#schemaautoinsurancepremiumpayment)|true|none|Informações de pagamento de prêmio.|
|minimumRequirements|[AutoInsuranceMinimumRequirements](#schemaautoinsuranceminimumrequirements)|true|none|Produtos de Seguro de Automóvel.|
|targetAudiences|[string]|true|none|Público-alvo.|

<h2 id="tocS_AutoInsuranceCoverage">AutoInsuranceCoverage</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecoverage"></a>
<a id="schema_AutoInsuranceCoverage"></a>
<a id="tocSautoinsurancecoverage"></a>
<a id="tocsautoinsurancecoverage"></a>

```json
[
  {
    "coverage": "VIDROS",
    "coverageDetail": "Roubo total",
    "coveragePermissionSeparteAcquisition": true,
    "coverageAttributes": {
      "minLMI": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      },
      "maxLMI": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      },
      "contractBase": [
        {
          "contractBaseType": "VALOR DETERMINADO",
          "contractBaseMinValue": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "contractBaseMaxValue": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          }
        }
      ],
      "newCarMaximumCalculatingPeriod": 12,
      "newCarContractBase": [
        {
          "contractBaseType": "VALOR DETERMINADO",
          "contractBaseMinValue": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          },
          "contractBaseMaxValue": {
            "amount": 0,
            "unit": {
              "code": "string",
              "description": "string"
            }
          }
        }
      ],
      "fullIndemnityPercentage": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      },
      "deductibleType": [
        "NORMAL"
      ],
      "fullIndemnityDeductible": true,
      "deductiblePaymentByCoverage": true,
      "deductiblePercentage": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      },
      "mandatoryParticipation": "Casco - RCF-V Danos",
      "geographicScopeCoverage": [
        "NACIONAL"
      ],
      "geographicScopeCoverageOthers": "string"
    }
  }
]

```

Listagem de coberturas incluídas no produto que deve observar a relação discriminada de coberturas, conforme Tabela II.5 do Anexo II

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|coverage|string|true|none|Conjunto de riscos elencados na apólice.|
|coverageDetail|string|true|none|Campo aberto para detalhamento de riscos possíveis dos produtos a ser feito para cada participante.|
|coveragePermissionSeparteAcquisition|boolean|false|none|Indicação se a cobertura permite contratação separada (por cobertura selecionada).|
|coverageAttributes|[AutoInsuranceCoverageAttributes](#schemaautoinsurancecoverageattributes)|false|none|Atributos da cobertura.|

#### Enumerated Values

|Property|Value|
|---|---|
|coverage|CASCO_COMPREENSIVA_COLISAO_INCENDIO_ROUBO_FURTO|
|coverage|CASCO_INCENDIO_ROUBO_FURTO|
|coverage|CASCO_ROUBO_FURTO|
|coverage|CASCO_INCENDIO|
|coverage|CASCO_ALAGAMENTO|
|coverage|CASCO_COLISAO_INDENIZACAO_PARCIAL|
|coverage|CASCO_COLISAO_INDENIZACAO_INTEGRAL|
|coverage|RESPONSABILIDADE_CIVIL_FACULTATIVA_VEICULOS_RCFV|
|coverage|RESPONSABILIDADE_CIVIL_FACULTATIVA_CONDUTOR_RCFC|
|coverage|ACIDENTE_PESSOAIS_PASSAGEIROS_VEICULO|
|coverage|ACIDENTE_PESSOAIS_PASSAGEIROS_CONDUTOR|
|coverage|VIDROS|
|coverage|DIARIA_INDISPONIBILIDADE|
|coverage|LFR_LANTERNAS_FAROIS_RETROVISORES|
|coverage|ACESSORIOS_EQUIPAMENTOS|
|coverage|CARRO_RESERVA|
|coverage|PEQUENOS_REPAROS|
|coverage|RESPONSABILIDADE_CIVIL_CARTA_VERDE|
|coverage|VOUCHER_MOBILIDADE|
|coverage|DESPESAS_EXTRAORDINARIAS|
|coverage|PEQUENOS_REPAROS|
|coverage|GARANTIA_MECANICA|
|coverage|OUTRAS|

<h2 id="tocS_AutoInsuranceCovaregeAttibutesDetailsUnit">AutoInsuranceCovaregeAttibutesDetailsUnit</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecovaregeattibutesdetailsunit"></a>
<a id="schema_AutoInsuranceCovaregeAttibutesDetailsUnit"></a>
<a id="tocSautoinsurancecovaregeattibutesdetailsunit"></a>
<a id="tocsautoinsurancecovaregeattibutesdetailsunit"></a>

```json
{
  "code": "string",
  "description": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|true|none|none|
|description|string|true|none|none|

<h2 id="tocS_AutoInsuranceCovaregeAttibutesDetails">AutoInsuranceCovaregeAttibutesDetails</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecovaregeattibutesdetails"></a>
<a id="schema_AutoInsuranceCovaregeAttibutesDetails"></a>
<a id="tocSautoinsurancecovaregeattibutesdetails"></a>
<a id="tocsautoinsurancecovaregeattibutesdetails"></a>

```json
{
  "amount": 0,
  "unit": {
    "code": "string",
    "description": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number|true|none|none|
|unit|[AutoInsuranceCovaregeAttibutesDetailsUnit](#schemaautoinsurancecovaregeattibutesdetailsunit)|true|none|none|

<h2 id="tocS_AutoInsuranceContractBase">AutoInsuranceContractBase</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecontractbase"></a>
<a id="schema_AutoInsuranceContractBase"></a>
<a id="tocSautoinsurancecontractbase"></a>
<a id="tocsautoinsurancecontractbase"></a>

```json
[
  {
    "contractBaseType": "VALOR DETERMINADO",
    "contractBaseMinValue": {
      "amount": 0,
      "unit": {
        "code": "string",
        "description": "string"
      }
    },
    "contractBaseMaxValue": {
      "amount": 0,
      "unit": {
        "code": "string",
        "description": "string"
      }
    }
  }
]

```

Base de contratação.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contractBaseType|string|true|none|Incidência ao capital segurado da cobertura de casco.|
|contractBaseMinValue|[AutoInsuranceCovaregeAttibutesDetails](#schemaautoinsurancecovaregeattibutesdetails)|false|none|Valor Base de Contratação Mínimo.|
|contractBaseMaxValue|[AutoInsuranceCovaregeAttibutesDetails](#schemaautoinsurancecovaregeattibutesdetails)|false|none|Valor Base de Contratação Máximo.|

#### Enumerated Values

|Property|Value|
|---|---|
|contractBaseType|VALOR_DETERMINADO|
|contractBaseType|VALOR_MERCADO|
|contractBaseType|AMBOS|

<h2 id="tocS_AutoInsuranceCoverageAttributes">AutoInsuranceCoverageAttributes</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecoverageattributes"></a>
<a id="schema_AutoInsuranceCoverageAttributes"></a>
<a id="tocSautoinsurancecoverageattributes"></a>
<a id="tocsautoinsurancecoverageattributes"></a>

```json
{
  "minLMI": {
    "amount": 0,
    "unit": {
      "code": "string",
      "description": "string"
    }
  },
  "maxLMI": {
    "amount": 0,
    "unit": {
      "code": "string",
      "description": "string"
    }
  },
  "contractBase": [
    {
      "contractBaseType": "VALOR DETERMINADO",
      "contractBaseMinValue": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      },
      "contractBaseMaxValue": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      }
    }
  ],
  "newCarMaximumCalculatingPeriod": 12,
  "newCarContractBase": [
    {
      "contractBaseType": "VALOR DETERMINADO",
      "contractBaseMinValue": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      },
      "contractBaseMaxValue": {
        "amount": 0,
        "unit": {
          "code": "string",
          "description": "string"
        }
      }
    }
  ],
  "fullIndemnityPercentage": {
    "amount": 0,
    "unit": {
      "code": "string",
      "description": "string"
    }
  },
  "deductibleType": [
    "NORMAL"
  ],
  "fullIndemnityDeductible": true,
  "deductiblePaymentByCoverage": true,
  "deductiblePercentage": {
    "amount": 0,
    "unit": {
      "code": "string",
      "description": "string"
    }
  },
  "mandatoryParticipation": "Casco - RCF-V Danos",
  "geographicScopeCoverage": [
    "NACIONAL"
  ],
  "geographicScopeCoverageOthers": "string"
}

```

Atributos da cobertura.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|minLMI|[AutoInsuranceCovaregeAttibutesDetails](#schemaautoinsurancecovaregeattibutesdetails)|true|none|Lista com valor mínimo de LMI aceito pela sociedade para cada cobertura.|
|maxLMI|[AutoInsuranceCovaregeAttibutesDetails](#schemaautoinsurancecovaregeattibutesdetails)|true|none|Lista com valor máximo de LMI aceito pela sociedade para cada cobertura.|
|contractBase|[AutoInsuranceContractBase](#schemaautoinsurancecontractbase)|true|none|Veículo Zero Km Base de Contratação|
|newCarMaximumCalculatingPeriod|integer|true|none|Prazo máximo para apuração do valor a ser indenizado para veículo zero quilômetro. Em meses.|
|newCarContractBase|[AutoInsuranceContractBase](#schemaautoinsurancecontractbase)|false|none|Semelhante ao campo “Atributos cobertura - base de contratação” aplicada ao veículo Zero Km.|
|fullIndemnityPercentage|[AutoInsuranceCovaregeAttibutesDetails](#schemaautoinsurancecovaregeattibutesdetails)|true|none|Percentual do Limite Máximo de Indenização para caracterização de indenização integral.|
|deductibleType|[string]|true|none|Listagem de tipo de franquia para cada tipo de cobertura do produto.|
|fullIndemnityDeductible|boolean|true|none|Franquia para Indenização Integral.|
|deductiblePaymentByCoverage|boolean|true|none|Sinalização para cada cobertura se a seguradora exige pagamento de franquia.|
|deductiblePercentage|[AutoInsuranceCovaregeAttibutesDetails](#schemaautoinsurancecovaregeattibutesdetails)|true|none|Listagem percentual de franquia e/ou percentual de participação obrigatória do segurado estabelecida pela sociedade para cada tipo de cobertura de produto.|
|mandatoryParticipation|string|true|none|Participação Obrigatória do Segurado.|
|geographicScopeCoverage|[string]|true|none|Listagem de abrangência geográfica do produto para fins de cada cobertura.|
|geographicScopeCoverageOthers|string|false|none|Âmbito geográficoda cobertura - Outros|

<h2 id="tocS_AutoInsuranceMinimumRequirements">AutoInsuranceMinimumRequirements</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsuranceminimumrequirements"></a>
<a id="schema_AutoInsuranceMinimumRequirements"></a>
<a id="tocSautoinsuranceminimumrequirements"></a>
<a id="tocsautoinsuranceminimumrequirements"></a>

```json
{
  "contractingType": [
    "COLETIVO"
  ],
  "contractingMinRequirement": "https://example.com/mobile-banking"
}

```

Produtos de Seguro de Automóvel.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contractingType|[string]|true|none|Informações sobre todos os requisitos mínimos para contratação.|
|contractingMinRequirement|string|true|none|Campo aberto contendo todos os requisitos mínimos para contratação (possibilidade de incluir URL).|

<h2 id="tocS_AutoInsuranceTermsAndConditions">AutoInsuranceTermsAndConditions</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancetermsandconditions"></a>
<a id="schema_AutoInsuranceTermsAndConditions"></a>
<a id="tocSautoinsurancetermsandconditions"></a>
<a id="tocsautoinsurancetermsandconditions"></a>

```json
[
  {
    "susepProcessNumber": "15414.622222/2222-22",
    "definition": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|susepProcessNumber|string|true|none|Número do processo SUSEP.|
|definition|string|true|none|Campo aberto (possibilidade de incluir uma url).|

<h2 id="tocS_AutoInsurancePremiumPayment">AutoInsurancePremiumPayment</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancepremiumpayment"></a>
<a id="schema_AutoInsurancePremiumPayment"></a>
<a id="tocSautoinsurancepremiumpayment"></a>
<a id="tocsautoinsurancepremiumpayment"></a>

```json
{
  "paymentMethod": [
    "CARTÃO DE CRÉDITO"
  ],
  "paymentType": [
    "PARCELADO"
  ],
  "paymentDetail": "string"
}

```

Informações de pagamento de prêmio.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|paymentMethod|[string]|true|none|Meio de pagamento escolhido pelo segurado.|
|paymentType|[string]|false|none|Forma de pagamento.|
|paymentDetail|string|false|none|Campo aberto para detalhamento do campo ‘Outros’ por cada participante.|

<h2 id="tocS_AutoInsuranceAssistanceServices">AutoInsuranceAssistanceServices</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsuranceassistanceservices"></a>
<a id="schema_AutoInsuranceAssistanceServices"></a>
<a id="tocSautoinsuranceassistanceservices"></a>
<a id="tocsautoinsuranceassistanceservices"></a>

```json
{
  "assistanceServicesPackage": [
    "ATE_10_SERVICOS"
  ],
  "assistanceServicesDetail": "Perda Parcial - Colisão",
  "chargeTypeSignaling": "GRATUITA"
}

```

Serviços de Assistência.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|assistanceServicesPackage|[string]|true|none|Pacotes de Assistência - Agrupamento.|
|assistanceServicesDetail|string|true|none|Serviços de assistência - Detalhamento.|
|chargeTypeSignaling|string|false|none|Sinalização em campo exclusivo se o pacote de Assistência é gratuita ou contratada/paga.|

#### Enumerated Values

|Property|Value|
|---|---|
|chargeTypeSignaling|GRATUITA|
|chargeTypeSignaling|PAGA|

<h2 id="tocS_AutoInsuranceCarPart">AutoInsuranceCarPart</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecarpart"></a>
<a id="schema_AutoInsuranceCarPart"></a>
<a id="tocSautoinsurancecarpart"></a>
<a id="tocsautoinsurancecarpart"></a>

```json
[
  {
    "carPartCondition": "NOVAS",
    "carPartType": "ORIGINAIS"
  }
]

```

Tipo de peça utilizada para reparação.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|carPartCondition|string|true|none|Nova ou usada|
|carPartType|string|true|none|Originais e não originais|

#### Enumerated Values

|Property|Value|
|---|---|
|carPartCondition|NOVAS|
|carPartCondition|USADAS|
|carPartCondition|AMBAS|
|carPartType|ORIGINAIS|
|carPartType|COMPATIVEIS|
|carPartType|AMBAS|

<h2 id="tocS_AutoInsuranceCarModel">AutoInsuranceCarModel</h2>
<!-- backwards compatibility -->
<a id="schemaautoinsurancecarmodel"></a>
<a id="schema_AutoInsuranceCarModel"></a>
<a id="tocSautoinsurancecarmodel"></a>
<a id="tocsautoinsurancecarmodel"></a>

```json
[
  {
    "manufacturer": "FORD",
    "model": "KA",
    "year": 2018,
    "fipeCode": "string"
  }
]

```

Listagem de modelos / ano de veículos. Deve ser padronizada na proposta técnica submetida pela Estrutura Inicial de Governança para observância comum por todas as sociedades participantes.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|manufacturer|string|true|none|Fabricante|
|model|string|true|none|Modelo|
|year|integer|true|none|Ano de fabricação.|
|fipeCode|string|true|none|Código FIPE do veículo.|

<h2 id="tocS_Links">Links</h2>
<!-- backwards compatibility -->
<a id="schemalinks"></a>
<a id="schema_Links"></a>
<a id="tocSlinks"></a>
<a id="tocslinks"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
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
  "totalRecords": 10,
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
    "totalRecords": 10,
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
|meta|[Meta](#schemameta)|false|none|none|

<h2 id="tocS_ResponseHomeInsuranceList">ResponseHomeInsuranceList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsehomeinsurancelist"></a>
<a id="schema_ResponseHomeInsuranceList"></a>
<a id="tocSresponsehomeinsurancelist"></a>
<a id="tocsresponsehomeinsurancelist"></a>

```json
{
  "data": {
    "brand": {
      "name": "EMPRESA A seguros",
      "company": [
        {
          "name": "ABCDE SEGUROS",
          "cnpjNumber": 12345678901234,
          "products": [
            {
              "name": "RESIDENCIAL XPTO",
              "code": "0000-0",
              "coverages": [
                {
                  "coverageType": "Escritório em Residência",
                  "coverageDetail": "Cobertura especial para escritório residenciais",
                  "coveragePermissionSeparteAquisition": false,
                  "coverageAttributes": {
                    "minLMI": {},
                    "maxLMI": {},
                    "minDeductibleAmount": {},
                    "insuredMandatoryParticipationPercentage": 0
                  }
                }
              ],
              "propertyCharacteristics": [
                {
                  "propertyType": "CASA",
                  "propertyBuildType": "ALVENARIA",
                  "propertyUsageType": "HABITUAL",
                  "destinationInsuredImportance": "PRÉDIO"
                }
              ],
              "propertyZipCode": "1311000",
              "protective": true,
              "additional": [
                "SORTEIO_GRATUITO"
              ],
              "additionalOthers": "string",
              "assistanceServices": [
                {
                  "assistanceServicesPackage": "ATE_10_SERVICOS",
                  "complementaryAssistanceServicesDetail": "reboque pane seca",
                  "chargeTypeSignaling": "GRATUITA"
                }
              ],
              "termsAndConditions": [
                {
                  "susepProcessNumber": "XXXXX.XXXXXX/XXXX-XX",
                  "definition": "https://openinsurance.com.br/aaa"
                }
              ],
              "validity": [
                {
                  "term": "ANUAL",
                  "termOthers": "string"
                }
              ],
              "customerServices": [
                "LIVRE ESCOLHA"
              ],
              "premiumRates": [
                "string"
              ],
              "premiumPayments": [
                {
                  "paymentMethod": "CARTÃO DE CRÉDITO",
                  "paymentMethodDetail": "string",
                  "paymentType": "PAGAMENTO_UNICO"
                }
              ],
              "minimumRequirements": [
                {
                  "contractingType": "COLETIVO",
                  "contractingMinRequirement": "https://openinsurance.com.br/aaa"
                }
              ],
              "targetAudiences": [
                "PESSOA_NATURAL"
              ]
            }
          ]
        }
      ]
    }
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|data|object|true|none|none|
|» brand|[HomeInsuranceBrand](#schemahomeinsurancebrand)|false|none|none|
|links|[Links](#schemalinks)|true|none|none|
|meta|[Meta](#schemameta)|true|none|none|

<h2 id="tocS_HomeInsuranceBrand">HomeInsuranceBrand</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancebrand"></a>
<a id="schema_HomeInsuranceBrand"></a>
<a id="tocShomeinsurancebrand"></a>
<a id="tocshomeinsurancebrand"></a>

```json
{
  "name": "EMPRESA A seguros",
  "company": [
    {
      "name": "ABCDE SEGUROS",
      "cnpjNumber": 12345678901234,
      "products": [
        {
          "name": "RESIDENCIAL XPTO",
          "code": "0000-0",
          "coverages": [
            {
              "coverageType": "Escritório em Residência",
              "coverageDetail": "Cobertura especial para escritório residenciais",
              "coveragePermissionSeparteAquisition": false,
              "coverageAttributes": {
                "minLMI": {
                  "amount": 0,
                  "unit": {
                    "code": "R$",
                    "description": "REAL"
                  }
                },
                "maxLMI": {
                  "amount": 0,
                  "unit": {
                    "code": "R$",
                    "description": "REAL"
                  }
                },
                "minDeductibleAmount": {
                  "amount": 0,
                  "unit": {
                    "code": "R$",
                    "description": "REAL"
                  }
                },
                "insuredMandatoryParticipationPercentage": 0
              }
            }
          ],
          "propertyCharacteristics": [
            {
              "propertyType": "CASA",
              "propertyBuildType": "ALVENARIA",
              "propertyUsageType": "HABITUAL",
              "destinationInsuredImportance": "PRÉDIO"
            }
          ],
          "propertyZipCode": "1311000",
          "protective": true,
          "additional": [
            "SORTEIO_GRATUITO"
          ],
          "additionalOthers": "string",
          "assistanceServices": [
            {
              "assistanceServicesPackage": "ATE_10_SERVICOS",
              "complementaryAssistanceServicesDetail": "reboque pane seca",
              "chargeTypeSignaling": "GRATUITA"
            }
          ],
          "termsAndConditions": [
            {
              "susepProcessNumber": "XXXXX.XXXXXX/XXXX-XX",
              "definition": "https://openinsurance.com.br/aaa"
            }
          ],
          "validity": [
            {
              "term": "ANUAL",
              "termOthers": "string"
            }
          ],
          "customerServices": [
            "LIVRE ESCOLHA"
          ],
          "premiumRates": [
            "string"
          ],
          "premiumPayments": [
            {
              "paymentMethod": "CARTÃO DE CRÉDITO",
              "paymentMethodDetail": "string",
              "paymentType": "PAGAMENTO_UNICO"
            }
          ],
          "minimumRequirements": [
            {
              "contractingType": "COLETIVO",
              "contractingMinRequirement": "https://openinsurance.com.br/aaa"
            }
          ],
          "targetAudiences": [
            "PESSOA_NATURAL"
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
|name|string|true|none|Nome da marca reportada pelo participante do Open Insurance. O conceito a que se refere a marca é em essência uma promessa das sociedades sob ela em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes.|
|company|[HomeInsuranceCompany](#schemahomeinsurancecompany)|false|none|none|

<h2 id="tocS_HomeInsuranceCompany">HomeInsuranceCompany</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancecompany"></a>
<a id="schema_HomeInsuranceCompany"></a>
<a id="tocShomeinsurancecompany"></a>
<a id="tocshomeinsurancecompany"></a>

```json
[
  {
    "name": "ABCDE SEGUROS",
    "cnpjNumber": 12345678901234,
    "products": [
      {
        "name": "RESIDENCIAL XPTO",
        "code": "0000-0",
        "coverages": [
          {
            "coverageType": "Escritório em Residência",
            "coverageDetail": "Cobertura especial para escritório residenciais",
            "coveragePermissionSeparteAquisition": false,
            "coverageAttributes": {
              "minLMI": {
                "amount": 0,
                "unit": {
                  "code": "R$",
                  "description": "REAL"
                }
              },
              "maxLMI": {
                "amount": 0,
                "unit": {
                  "code": "R$",
                  "description": "REAL"
                }
              },
              "minDeductibleAmount": {
                "amount": 0,
                "unit": {
                  "code": "R$",
                  "description": "REAL"
                }
              },
              "insuredMandatoryParticipationPercentage": 0
            }
          }
        ],
        "propertyCharacteristics": [
          {
            "propertyType": "CASA",
            "propertyBuildType": "ALVENARIA",
            "propertyUsageType": "HABITUAL",
            "destinationInsuredImportance": "PRÉDIO"
          }
        ],
        "propertyZipCode": "1311000",
        "protective": true,
        "additional": [
          "SORTEIO_GRATUITO"
        ],
        "additionalOthers": "string",
        "assistanceServices": [
          {
            "assistanceServicesPackage": "ATE_10_SERVICOS",
            "complementaryAssistanceServicesDetail": "reboque pane seca",
            "chargeTypeSignaling": "GRATUITA"
          }
        ],
        "termsAndConditions": [
          {
            "susepProcessNumber": "XXXXX.XXXXXX/XXXX-XX",
            "definition": "https://openinsurance.com.br/aaa"
          }
        ],
        "validity": [
          {
            "term": "ANUAL",
            "termOthers": "string"
          }
        ],
        "customerServices": [
          "LIVRE ESCOLHA"
        ],
        "premiumRates": [
          "string"
        ],
        "premiumPayments": [
          {
            "paymentMethod": "CARTÃO DE CRÉDITO",
            "paymentMethodDetail": "string",
            "paymentType": "PAGAMENTO_UNICO"
          }
        ],
        "minimumRequirements": [
          {
            "contractingType": "COLETIVO",
            "contractingMinRequirement": "https://openinsurance.com.br/aaa"
          }
        ],
        "targetAudiences": [
          "PESSOA_NATURAL"
        ]
      }
    ]
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da sociedade pertencente à marca.|
|cnpjNumber|string|true|none|CNPJ da sociedade pertencente à marca.|
|products|[HomeInsuranceProduct](#schemahomeinsuranceproduct)|false|none|Produtos de Seguro Residencial.|

<h2 id="tocS_HomeInsuranceProduct">HomeInsuranceProduct</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsuranceproduct"></a>
<a id="schema_HomeInsuranceProduct"></a>
<a id="tocShomeinsuranceproduct"></a>
<a id="tocshomeinsuranceproduct"></a>

```json
[
  {
    "name": "RESIDENCIAL XPTO",
    "code": "0000-0",
    "coverages": [
      {
        "coverageType": "Escritório em Residência",
        "coverageDetail": "Cobertura especial para escritório residenciais",
        "coveragePermissionSeparteAquisition": false,
        "coverageAttributes": {
          "minLMI": {
            "amount": 0,
            "unit": {
              "code": "R$",
              "description": "REAL"
            }
          },
          "maxLMI": {
            "amount": 0,
            "unit": {
              "code": "R$",
              "description": "REAL"
            }
          },
          "minDeductibleAmount": {
            "amount": 0,
            "unit": {
              "code": "R$",
              "description": "REAL"
            }
          },
          "insuredMandatoryParticipationPercentage": 0
        }
      }
    ],
    "propertyCharacteristics": [
      {
        "propertyType": "CASA",
        "propertyBuildType": "ALVENARIA",
        "propertyUsageType": "HABITUAL",
        "destinationInsuredImportance": "PRÉDIO"
      }
    ],
    "propertyZipCode": "1311000",
    "protective": true,
    "additional": [
      "SORTEIO_GRATUITO"
    ],
    "additionalOthers": "string",
    "assistanceServices": [
      {
        "assistanceServicesPackage": "ATE_10_SERVICOS",
        "complementaryAssistanceServicesDetail": "reboque pane seca",
        "chargeTypeSignaling": "GRATUITA"
      }
    ],
    "termsAndConditions": [
      {
        "susepProcessNumber": "XXXXX.XXXXXX/XXXX-XX",
        "definition": "https://openinsurance.com.br/aaa"
      }
    ],
    "validity": [
      {
        "term": "ANUAL",
        "termOthers": "string"
      }
    ],
    "customerServices": [
      "LIVRE ESCOLHA"
    ],
    "premiumRates": [
      "string"
    ],
    "premiumPayments": [
      {
        "paymentMethod": "CARTÃO DE CRÉDITO",
        "paymentMethodDetail": "string",
        "paymentType": "PAGAMENTO_UNICO"
      }
    ],
    "minimumRequirements": [
      {
        "contractingType": "COLETIVO",
        "contractingMinRequirement": "https://openinsurance.com.br/aaa"
      }
    ],
    "targetAudiences": [
      "PESSOA_NATURAL"
    ]
  }
]

```

Produtos de Seguro Residencial.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome comercial do produto, pelo qual é identificado nos canais de distribuição e atendimento da sociedade.|
|code|string|true|none|Código único a ser definido pela sociedade.|
|coverages|[HomeInsuranceCoverages](#schemahomeinsurancecoverages)|true|none|Listagem de coberturas incluídas no produto.|
|propertyCharacteristics|[HomeInsurancePropertyCharacteristics](#schemahomeinsurancepropertycharacteristics)|true|none|Caracteristicas do imóvel.|
|propertyZipCode|string|true|none|Código de Endereçamento Postal do Imóvel|
|protective|boolean|true|none|Protecionais - Indicativo de exigência de itens protecionais.|
|additional|[string]|true|none|none|
|additionalOthers|string|false|none|Campo aberto para descrição de cada participante ao selecionar o domínio ‘Outros’ no campo acima ‘Adicionais’.|
|assistanceServices|[HomeInsuranceAssistanceServices](#schemahomeinsuranceassistanceservices)|true|none|Agrupamento dos serviços de assistências disponíveis vinculado ao produto.|
|termsAndConditions|[HomeInsuranceTermsAndConditions](#schemahomeinsurancetermsandconditions)|true|none|Informações dos termos e condições conforme número do processo SUSEP.|
|validity|[HomeInsuranceValidity](#schemahomeinsurancevalidity)|true|none|Vigência|
|customerServices|[string]|false|none|Informações de pagamento de prêmio.|
|premiumRates|[string]|false|none|Distribuição de frequência relativa aos valores referentes às taxas cobradas.|
|premiumPayments|[HomeInsurancePremiumPayment](#schemahomeinsurancepremiumpayment)|true|none|Informações de pagamento de prêmio.|
|minimumRequirements|[[HomeInsuranceMinimumRequirements](#schemahomeinsuranceminimumrequirements)]|false|none|[Produtos de Seguro Residencial.]|
|targetAudiences|[string]|true|none|none|

<h2 id="tocS_HomeInsuranceMinimumRequirements">HomeInsuranceMinimumRequirements</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsuranceminimumrequirements"></a>
<a id="schema_HomeInsuranceMinimumRequirements"></a>
<a id="tocShomeinsuranceminimumrequirements"></a>
<a id="tocshomeinsuranceminimumrequirements"></a>

```json
{
  "contractingType": "COLETIVO",
  "contractingMinRequirement": "https://openinsurance.com.br/aaa"
}

```

Produtos de Seguro Residencial.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|contractingType|string|true|none|Tipo de contratação.|
|contractingMinRequirement|string|true|none|Campo aberto contendo todos os requisitos mínimos para contratação (possibilidade de incluir URL).|

#### Enumerated Values

|Property|Value|
|---|---|
|contractingType|COLETIVO|
|contractingType|INDIVIDUAL|
|contractingType|AMBAS|

<h2 id="tocS_HomeInsuranceCoverageAttributes">HomeInsuranceCoverageAttributes</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancecoverageattributes"></a>
<a id="schema_HomeInsuranceCoverageAttributes"></a>
<a id="tocShomeinsurancecoverageattributes"></a>
<a id="tocshomeinsurancecoverageattributes"></a>

```json
{
  "minLMI": {
    "amount": 0,
    "unit": {
      "code": "R$",
      "description": "REAL"
    }
  },
  "maxLMI": {
    "amount": 0,
    "unit": {
      "code": "R$",
      "description": "REAL"
    }
  },
  "minDeductibleAmount": {
    "amount": 0,
    "unit": {
      "code": "R$",
      "description": "REAL"
    }
  },
  "insuredMandatoryParticipationPercentage": 0
}

```

Informações de cobertura do Seguro Residencial.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|minLMI|[HomeInsuranceCovaregeAttibutesDetails](#schemahomeinsurancecovaregeattibutesdetails)|true|none|Lista com valor mínimo de LMI aceito pela sociedade para cada cobertura.|
|maxLMI|[HomeInsuranceCovaregeAttibutesDetails](#schemahomeinsurancecovaregeattibutesdetails)|true|none|Lista com valor máximo de LMI aceito pela sociedade para cada cobertura.|
|minDeductibleAmount|[HomeInsuranceCovaregeAttibutesDetails](#schemahomeinsurancecovaregeattibutesdetails)|true|none|Valor mínimo de franquia e participação obrigatória do segurado - Listagem de valor mínimo da franquia (Reais) e/ou Participação Obrigatória do Segurado (Percentual) estabelecida pela sociedade para cada tipo de cobertura do produto.|
|insuredMandatoryParticipationPercentage|number|true|none|Listagem percentual de franquia e/ou percentual de participação obrigatória do segurado estabelecida pela sociedade para cada tipo de cobertura de produto.|

<h2 id="tocS_HomeInsuranceCovaregeAttibutesDetailsUnit">HomeInsuranceCovaregeAttibutesDetailsUnit</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancecovaregeattibutesdetailsunit"></a>
<a id="schema_HomeInsuranceCovaregeAttibutesDetailsUnit"></a>
<a id="tocShomeinsurancecovaregeattibutesdetailsunit"></a>
<a id="tocshomeinsurancecovaregeattibutesdetailsunit"></a>

```json
{
  "code": "R$",
  "description": "REAL"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|true|none|none|
|description|string|true|none|none|

<h2 id="tocS_HomeInsuranceCovaregeAttibutesDetails">HomeInsuranceCovaregeAttibutesDetails</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancecovaregeattibutesdetails"></a>
<a id="schema_HomeInsuranceCovaregeAttibutesDetails"></a>
<a id="tocShomeinsurancecovaregeattibutesdetails"></a>
<a id="tocshomeinsurancecovaregeattibutesdetails"></a>

```json
{
  "amount": 0,
  "unit": {
    "code": "R$",
    "description": "REAL"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|number|true|none|none|
|unit|[HomeInsuranceCovaregeAttibutesDetailsUnit](#schemahomeinsurancecovaregeattibutesdetailsunit)|true|none|none|

<h2 id="tocS_HomeInsuranceTermsAndConditions">HomeInsuranceTermsAndConditions</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancetermsandconditions"></a>
<a id="schema_HomeInsuranceTermsAndConditions"></a>
<a id="tocShomeinsurancetermsandconditions"></a>
<a id="tocshomeinsurancetermsandconditions"></a>

```json
[
  {
    "susepProcessNumber": "XXXXX.XXXXXX/XXXX-XX",
    "definition": "https://openinsurance.com.br/aaa"
  }
]

```

Informações dos termos e condições conforme número do processo SUSEP.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|susepProcessNumber|string|true|none|Número do processo SUSEP.|
|definition|string|true|none|Campo aberto (possibilidade de incluir uma url).|

<h2 id="tocS_HomeInsuranceValidity">HomeInsuranceValidity</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancevalidity"></a>
<a id="schema_HomeInsuranceValidity"></a>
<a id="tocShomeinsurancevalidity"></a>
<a id="tocshomeinsurancevalidity"></a>

```json
[
  {
    "term": "ANUAL",
    "termOthers": "string"
  }
]

```

Vigência

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|term|string|true|none|Prazo de vigência do seguro contratado Intervalo contínuo de tempo durante o qual está em vigor o contrato de seguro. (RESOLUÇÃO CNSP Nº 341/2016).|
|termOthers|string|false|none|Campo livre para descrição por cada participante ao selecionar o domínio “Outros” no campo Prazo (acima).|

#### Enumerated Values

|Property|Value|
|---|---|
|term|ANUAL|
|term|ANUAL_INTERMITENTE|
|term|PLURIANUAL|
|term|PLURIANUAL_INTERMITENTE|
|term|MENSAL|
|term|MENSAL_INTERMITENTE|
|term|DIARIO|
|term|DIARIO_INTERMITENTE|
|term|OUTROS|

<h2 id="tocS_HomeInsurancePremiumPayment">HomeInsurancePremiumPayment</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancepremiumpayment"></a>
<a id="schema_HomeInsurancePremiumPayment"></a>
<a id="tocShomeinsurancepremiumpayment"></a>
<a id="tocshomeinsurancepremiumpayment"></a>

```json
[
  {
    "paymentMethod": "CARTÃO DE CRÉDITO",
    "paymentMethodDetail": "string",
    "paymentType": "PAGAMENTO_UNICO"
  }
]

```

Informações de pagamento de prêmio.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|paymentMethod|string|true|none|Meio de pagamento escolhido pelo segurado.|
|paymentMethodDetail|string|false|none|Campo aberto para detalhamento do campo ‘Outros’ por cada participante.|
|paymentType|string|true|none|Forma de pagamento|

#### Enumerated Values

|Property|Value|
|---|---|
|paymentMethod|CARTAO_CREDITO|
|paymentMethod|CARTAO_DEBITO|
|paymentMethod|DEBITO_CONTA_CORRENTE|
|paymentMethod|DEBITO_CONTA_POUPANCA|
|paymentMethod|BOLETO_BANCARIO|
|paymentMethod|PIX|
|paymentMethod|CONSIGINACAO_FOLHA_PAGAMENTO|
|paymentMethod|PONTOS_PROGRAMAS_BENEFICIO|
|paymentMethod|OUTROS|
|paymentType|PAGAMENTO_UNICO|
|paymentType|PARCELADO|
|paymentType|AMBOS|

<h2 id="tocS_HomeInsuranceAssistanceServices">HomeInsuranceAssistanceServices</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsuranceassistanceservices"></a>
<a id="schema_HomeInsuranceAssistanceServices"></a>
<a id="tocShomeinsuranceassistanceservices"></a>
<a id="tocshomeinsuranceassistanceservices"></a>

```json
[
  {
    "assistanceServicesPackage": "ATE_10_SERVICOS",
    "complementaryAssistanceServicesDetail": "reboque pane seca",
    "chargeTypeSignaling": "GRATUITA"
  }
]

```

Agrupamento dos serviços de assistências disponíveis vinculado ao produto.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|assistanceServicesPackage|string|true|none|Pacotes de Assistência.|
|complementaryAssistanceServicesDetail|string|true|none|Campo livre para descrição dos serviços ofertados por cada sociedade participante.|
|chargeTypeSignaling|string|true|none|Sinalização em campo exclusivo se o pacote de Assistência é gratuita ou contratada/paga.|

#### Enumerated Values

|Property|Value|
|---|---|
|assistanceServicesPackage|ATE_10_SERVICOS|
|assistanceServicesPackage|ATE_20_SERVICOS|
|assistanceServicesPackage|ACIMA_20_SERVICOS|
|assistanceServicesPackage|CUSTOMIZAVEL|
|chargeTypeSignaling|GRATUITA|
|chargeTypeSignaling|PAGO|

<h2 id="tocS_HomeInsuranceCoverages">HomeInsuranceCoverages</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancecoverages"></a>
<a id="schema_HomeInsuranceCoverages"></a>
<a id="tocShomeinsurancecoverages"></a>
<a id="tocshomeinsurancecoverages"></a>

```json
[
  {
    "coverageType": "Escritório em Residência",
    "coverageDetail": "Cobertura especial para escritório residenciais",
    "coveragePermissionSeparteAquisition": false,
    "coverageAttributes": {
      "minLMI": {
        "amount": 0,
        "unit": {
          "code": "R$",
          "description": "REAL"
        }
      },
      "maxLMI": {
        "amount": 0,
        "unit": {
          "code": "R$",
          "description": "REAL"
        }
      },
      "minDeductibleAmount": {
        "amount": 0,
        "unit": {
          "code": "R$",
          "description": "REAL"
        }
      },
      "insuredMandatoryParticipationPercentage": 0
    }
  }
]

```

Listagem de coberturas incluídas no produto.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|coverageType|string|true|none|Nome do tipo da cobertura.|
|coverageDetail|string|true|none|Campo aberto para detalhamento por coberturas possíveis dos produtos a ser feito por cada participante.|
|coveragePermissionSeparteAquisition|boolean|true|none|Indicação se a cobertura permite contratação separada (por cobertura selecionada).|
|coverageAttributes|[HomeInsuranceCoverageAttributes](#schemahomeinsurancecoverageattributes)|true|none|Informações de cobertura do Seguro Residencial.|

#### Enumerated Values

|Property|Value|
|---|---|
|coverageType|IMOVEL_BASICA|
|coverageType|IMOVEL_AMPLA|
|coverageType|DANOS_ELETRICOS|
|coverageType|DANOS_POR_AGUA|
|coverageType|ALAGAMENTO|
|coverageType|RESPONSABILIDADE_CIVIL_FAMILIAR|
|coverageType|RESPONSABILIDADE_CIVIL_DANOS_MORAIS|
|coverageType|ROUBO_SUBTRACAO_BENS|
|coverageType|ROUBO_SUBTRACAO_BENS_FORA_LOCAL_SEGURADO|
|coverageType|TACOS_GOLFE_HOLE_ONE|
|coverageType|PEQUENAS_REFORMAS_OBRAS|
|coverageType|GREVES_TUMULTOS_LOCKOUT|
|coverageType|MICROEMPREENDEDOR|
|coverageType|ESCRITORIO_RESIDENCIA|
|coverageType|DANOS_EQUIPAMENTOS_ELETRONICOS|
|coverageType|QUEBRA_VIDROS|
|coverageType|IMPACTO_VEICULOS|
|coverageType|VENDAVAL|
|coverageType|PERDA_PAGAMENTO_ALUGUEL|
|coverageType|BICICLETA|
|coverageType|RESPONSABILIDADE_CIVIL_BICICLETA|
|coverageType|RC_EMPREGADOR|
|coverageType|DESMORONAMENTO|
|coverageType|DESPESAS_EXTRAORDINARIAS|
|coverageType|JOIAS_OBRAS_ARTE|
|coverageType|TERREMOTO|
|coverageType|IMPACTO_AERONAVES|
|coverageType|PAISAGISMO|
|coverageType|INCENDIO|
|coverageType|QUEDA_RAIO|
|coverageType|EXPLOSAO|
|coverageType|OUTRAS|

<h2 id="tocS_HomeInsurancePropertyCharacteristics">HomeInsurancePropertyCharacteristics</h2>
<!-- backwards compatibility -->
<a id="schemahomeinsurancepropertycharacteristics"></a>
<a id="schema_HomeInsurancePropertyCharacteristics"></a>
<a id="tocShomeinsurancepropertycharacteristics"></a>
<a id="tocshomeinsurancepropertycharacteristics"></a>

```json
[
  {
    "propertyType": "CASA",
    "propertyBuildType": "ALVENARIA",
    "propertyUsageType": "HABITUAL",
    "destinationInsuredImportance": "PRÉDIO"
  }
]

```

Caracteristicas do imóvel.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|propertyType|string|true|none|Tipo de imóvel.|
|propertyBuildType|string|true|none|Descrição do tipo de construção da propriedade.|
|propertyUsageType|string|true|none|Descrição do tipo de uso da propriedade.|
|destinationInsuredImportance|string|true|none|Destinação da Importância Segurada.|

#### Enumerated Values

|Property|Value|
|---|---|
|propertyType|CASA|
|propertyType|APARTAMENTO|
|propertyBuildType|ALVENARIA|
|propertyBuildType|MADEIRA|
|propertyBuildType|METALICA|
|propertyBuildType|MISTA|
|propertyUsageType|HABITUAL|
|propertyUsageType|VERANEIO|
|propertyUsageType|DESOCUPADO|
|propertyUsageType|CASA_ESCRITORIO|
|propertyUsageType|ALUGUEL_TEMPORADA|
|destinationInsuredImportance|PREDIO|
|destinationInsuredImportance|CONTEUDO|
|destinationInsuredImportance|AMBOS|

<h2 id="tocS_Links">Links</h2>
<!-- backwards compatibility -->
<a id="schemalinks"></a>
<a id="schema_Links"></a>
<a id="tocSlinks"></a>
<a id="tocslinks"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
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
  "totalRecords": 10,
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
    "totalRecords": 10,
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
|meta|[Meta](#schemameta)|false|none|none|

<h2 id="tocS_ResponseCapitalizationTitleList">ResponseCapitalizationTitleList</h2>
<!-- backwards compatibility -->
<a id="schemaresponsecapitalizationtitlelist"></a>
<a id="schema_ResponseCapitalizationTitleList"></a>
<a id="tocSresponsecapitalizationtitlelist"></a>
<a id="tocsresponsecapitalizationtitlelist"></a>

```json
{
  "requestTime": "2021-08-20T08:30:00Z",
  "brand": {
    "name": "ACME seguros",
    "companies": [
      {
        "name": "ACME cap da ACME seguros",
        "cnpjNumber": "12345678901234",
        "product": [
          {
            "name": "ACMEcap",
            "code": "01234589_cap",
            "modality": [
              "TRADICIONAL"
            ],
            "costType": [
              "PAGAMENTO_UNICO"
            ],
            "termsAndConditions": {
              "susepProcessNumber": 15414622222222222,
              "termsRegulations": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
            },
            "quotas": [
              {
                "quota": 10,
                "capitalizationQuota": [
                  10
                ],
                "raffleQuota": [
                  10
                ],
                "chargingQuota": [
                  10
                ]
              }
            ],
            "validity": 48,
            "serieSize": 5000000,
            "capitalizationPeriod": {
              "interestRate": 0.25123,
              "updateIndex": [
                "IPCA"
              ],
              "others": [
                "Índice de atualização"
              ],
              "contributionAmount": {
                "minValue": 500,
                "maxValue": 5000,
                "frequency": "MENSAL",
                "value": 0
              },
              "earlyRedemption": [
                10
              ],
              "redemptionPercentageEndTerm": 100.002,
              "gracePeriodRedemption": 48
            },
            "latePayment": {
              "suspensionPeriod": 10,
              "termExtensionOption": true
            },
            "contributionPayment": {
              "paymentMethod": [
                "CARTAO_CREDITO"
              ],
              "updateIndex": [
                "IPCA"
              ],
              "others": [
                "Índice de atualização"
              ]
            },
            "redemption": {
              "redemption": 151.23
            },
            "raffle": {
              "raffleQty": 10000,
              "timeInterval": [
                "QUINZENAL"
              ],
              "raffleValue": 5,
              "earlySettlementRaffle": true,
              "mandatoryContemplation": true,
              "ruleDescription": "Sorteio às quartas-feiras",
              "minimumContemplationProbability": 0.000001
            },
            "additionalDetails": {
              "additionalDetails": "https://example.com/openinsurance"
            },
            "minimumRequirements": {
              "minimumRequirementDetails": "https://ey.exemplo/capitalizacao/tradicional/PU/requisitos_min",
              "targetAudiences": [
                "PESSOAL_NATURAL"
              ]
            }
          }
        ]
      }
    ]
  },
  "links": {
    "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
    "prev": "string",
    "next": "string",
    "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
  },
  "meta": {
    "totalRecords": 10,
    "totalPages": 1
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|requestTime|string(date-time)|false|none|Data e hora da consulta, conforme especificação RFC-3339, formato UTC.|
|brand|[CapitalizationTitleBrand](#schemacapitalizationtitlebrand)|true|none|Organização controladora do grupo.|
|links|[Links](#schemalinks)|true|none|none|
|meta|[Meta](#schemameta)|true|none|none|

<h2 id="tocS_CapitalizationTitleBrand">CapitalizationTitleBrand</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitlebrand"></a>
<a id="schema_CapitalizationTitleBrand"></a>
<a id="tocScapitalizationtitlebrand"></a>
<a id="tocscapitalizationtitlebrand"></a>

```json
{
  "name": "ACME seguros",
  "companies": [
    {
      "name": "ACME cap da ACME seguros",
      "cnpjNumber": "12345678901234",
      "product": [
        {
          "name": "ACMEcap",
          "code": "01234589_cap",
          "modality": [
            "TRADICIONAL"
          ],
          "costType": [
            "PAGAMENTO_UNICO"
          ],
          "termsAndConditions": {
            "susepProcessNumber": 15414622222222222,
            "termsRegulations": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
          },
          "quotas": [
            {
              "quota": 10,
              "capitalizationQuota": [
                10
              ],
              "raffleQuota": [
                10
              ],
              "chargingQuota": [
                10
              ]
            }
          ],
          "validity": 48,
          "serieSize": 5000000,
          "capitalizationPeriod": {
            "interestRate": 0.25123,
            "updateIndex": [
              "IPCA"
            ],
            "others": [
              "Índice de atualização"
            ],
            "contributionAmount": {
              "minValue": 500,
              "maxValue": 5000,
              "frequency": "MENSAL",
              "value": 0
            },
            "earlyRedemption": [
              10
            ],
            "redemptionPercentageEndTerm": 100.002,
            "gracePeriodRedemption": 48
          },
          "latePayment": {
            "suspensionPeriod": 10,
            "termExtensionOption": true
          },
          "contributionPayment": {
            "paymentMethod": [
              "CARTAO_CREDITO"
            ],
            "updateIndex": [
              "IPCA"
            ],
            "others": [
              "Índice de atualização"
            ]
          },
          "redemption": {
            "redemption": 151.23
          },
          "raffle": {
            "raffleQty": 10000,
            "timeInterval": [
              "QUINZENAL"
            ],
            "raffleValue": 5,
            "earlySettlementRaffle": true,
            "mandatoryContemplation": true,
            "ruleDescription": "Sorteio às quartas-feiras",
            "minimumContemplationProbability": 0.000001
          },
          "additionalDetails": {
            "additionalDetails": "https://example.com/openinsurance"
          },
          "minimumRequirements": {
            "minimumRequirementDetails": "https://ey.exemplo/capitalizacao/tradicional/PU/requisitos_min",
            "targetAudiences": [
              "PESSOAL_NATURAL"
            ]
          }
        }
      ]
    }
  ]
}

```

Organização controladora do grupo.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da marca reportada pelo participante do Open Insurance. O conceito a que se refere a marca é em essência uma promessa das sociedades sob ela em fornecer uma série específica de atributos, benefícios e serviços uniformes aos clientes.|
|companies|[CapitalizationTitleCompany](#schemacapitalizationtitlecompany)|true|none|none|

<h2 id="tocS_CapitalizationTitleCompany">CapitalizationTitleCompany</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitlecompany"></a>
<a id="schema_CapitalizationTitleCompany"></a>
<a id="tocScapitalizationtitlecompany"></a>
<a id="tocscapitalizationtitlecompany"></a>

```json
[
  {
    "name": "ACME cap da ACME seguros",
    "cnpjNumber": "12345678901234",
    "product": [
      {
        "name": "ACMEcap",
        "code": "01234589_cap",
        "modality": [
          "TRADICIONAL"
        ],
        "costType": [
          "PAGAMENTO_UNICO"
        ],
        "termsAndConditions": {
          "susepProcessNumber": 15414622222222222,
          "termsRegulations": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
        },
        "quotas": [
          {
            "quota": 10,
            "capitalizationQuota": [
              10
            ],
            "raffleQuota": [
              10
            ],
            "chargingQuota": [
              10
            ]
          }
        ],
        "validity": 48,
        "serieSize": 5000000,
        "capitalizationPeriod": {
          "interestRate": 0.25123,
          "updateIndex": [
            "IPCA"
          ],
          "others": [
            "Índice de atualização"
          ],
          "contributionAmount": {
            "minValue": 500,
            "maxValue": 5000,
            "frequency": "MENSAL",
            "value": 0
          },
          "earlyRedemption": [
            10
          ],
          "redemptionPercentageEndTerm": 100.002,
          "gracePeriodRedemption": 48
        },
        "latePayment": {
          "suspensionPeriod": 10,
          "termExtensionOption": true
        },
        "contributionPayment": {
          "paymentMethod": [
            "CARTAO_CREDITO"
          ],
          "updateIndex": [
            "IPCA"
          ],
          "others": [
            "Índice de atualização"
          ]
        },
        "redemption": {
          "redemption": 151.23
        },
        "raffle": {
          "raffleQty": 10000,
          "timeInterval": [
            "QUINZENAL"
          ],
          "raffleValue": 5,
          "earlySettlementRaffle": true,
          "mandatoryContemplation": true,
          "ruleDescription": "Sorteio às quartas-feiras",
          "minimumContemplationProbability": 0.000001
        },
        "additionalDetails": {
          "additionalDetails": "https://example.com/openinsurance"
        },
        "minimumRequirements": {
          "minimumRequirementDetails": "https://ey.exemplo/capitalizacao/tradicional/PU/requisitos_min",
          "targetAudiences": [
            "PESSOAL_NATURAL"
          ]
        }
      }
    ]
  }
]

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome da sociedade pertencente à marca.|
|cnpjNumber|string|true|none|CNPJ da sociedade pertencente à marca.|
|product|[CapitalizationTitleProduct](#schemacapitalizationtitleproduct)|true|none|Lista de produtos de uma empresa.|

<h2 id="tocS_CapitalizationTitleProduct">CapitalizationTitleProduct</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleproduct"></a>
<a id="schema_CapitalizationTitleProduct"></a>
<a id="tocScapitalizationtitleproduct"></a>
<a id="tocscapitalizationtitleproduct"></a>

```json
[
  {
    "name": "ACMEcap",
    "code": "01234589_cap",
    "modality": [
      "TRADICIONAL"
    ],
    "costType": [
      "PAGAMENTO_UNICO"
    ],
    "termsAndConditions": {
      "susepProcessNumber": 15414622222222222,
      "termsRegulations": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
    },
    "quotas": [
      {
        "quota": 10,
        "capitalizationQuota": [
          10
        ],
        "raffleQuota": [
          10
        ],
        "chargingQuota": [
          10
        ]
      }
    ],
    "validity": 48,
    "serieSize": 5000000,
    "capitalizationPeriod": {
      "interestRate": 0.25123,
      "updateIndex": [
        "IPCA"
      ],
      "others": [
        "Índice de atualização"
      ],
      "contributionAmount": {
        "minValue": 500,
        "maxValue": 5000,
        "frequency": "MENSAL",
        "value": 0
      },
      "earlyRedemption": [
        10
      ],
      "redemptionPercentageEndTerm": 100.002,
      "gracePeriodRedemption": 48
    },
    "latePayment": {
      "suspensionPeriod": 10,
      "termExtensionOption": true
    },
    "contributionPayment": {
      "paymentMethod": [
        "CARTAO_CREDITO"
      ],
      "updateIndex": [
        "IPCA"
      ],
      "others": [
        "Índice de atualização"
      ]
    },
    "redemption": {
      "redemption": 151.23
    },
    "raffle": {
      "raffleQty": 10000,
      "timeInterval": [
        "QUINZENAL"
      ],
      "raffleValue": 5,
      "earlySettlementRaffle": true,
      "mandatoryContemplation": true,
      "ruleDescription": "Sorteio às quartas-feiras",
      "minimumContemplationProbability": 0.000001
    },
    "additionalDetails": {
      "additionalDetails": "https://example.com/openinsurance"
    },
    "minimumRequirements": {
      "minimumRequirementDetails": "https://ey.exemplo/capitalizacao/tradicional/PU/requisitos_min",
      "targetAudiences": [
        "PESSOAL_NATURAL"
      ]
    }
  }
]

```

Lista de produtos de uma empresa.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|Nome comercial do produto, pelo qual é identificado nos canais de distribuição e atendimento da sociedade.|
|code|string|true|none|Código único a ser definido pela sociedade.|
|modality|[string]|true|none|Modalidade.|
|costType|[string]|true|none|Forma de custeio|
|termsAndConditions|[CapitalizationTitleTerms](#schemacapitalizationtitleterms)|false|none|Informações dos termos e condições conforme número do processo SUSEP.|
|quotas|[[CapitalizationTitleQuotas](#schemacapitalizationtitlequotas)]|true|none|[Quotas]|
|validity|[CapitalizationTitleValidity](#schemacapitalizationtitlevalidity)|false|none|Prazo de vigência do título de capitalização em meses.|
|serieSize|[CapitalizationTitleSerieSize](#schemacapitalizationtitleseriesize)|false|none|Os títulos de capitalização que prevejam sorteio devem ser estruturados em series, ou seja, em sequencias ou em grupos de títulos submetidos às mesmas condições e características, à exceção do valor do pagamento.|
|capitalizationPeriod|[CapitalizationTitlePeriod](#schemacapitalizationtitleperiod)|false|none|Período de Capitalização|
|latePayment|[CapitalizationTitleLatePayment](#schemacapitalizationtitlelatepayment)|false|none|Atraso de Pagamento|
|contributionPayment|[CapitalizationTitleContributionPayment](#schemacapitalizationtitlecontributionpayment)|false|none|Pagamento da contribuição|
|redemption|[CapitalizationTitleredemption](#schemacapitalizationtitleredemption)|false|none|none|
|raffle|[CapitalizationTitleRaffle](#schemacapitalizationtitleraffle)|false|none|Sorteio|
|additionalDetails|[CapitalizationTitleAdditionals](#schemacapitalizationtitleadditionals)|false|none|none|
|minimumRequirements|[CapitalizationTitleMinimumRequirements](#schemacapitalizationtitleminimumrequirements)|false|none|Requisitos mínimos.|

<h2 id="tocS_CapitalizationTitleTerms">CapitalizationTitleTerms</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleterms"></a>
<a id="schema_CapitalizationTitleTerms"></a>
<a id="tocScapitalizationtitleterms"></a>
<a id="tocscapitalizationtitleterms"></a>

```json
{
  "susepProcessNumber": 15414622222222222,
  "termsRegulations": "https://ey.exemplo/capitalizacao/tradicional/pdf/condicoes_gerais.pdf"
}

```

Informações dos termos e condições conforme número do processo SUSEP.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|susepProcessNumber|number|true|none|Número do processo SUSEP.|
|termsRegulations|string|true|none|Campo aberto (possibilidade de incluir uma url).|

<h2 id="tocS_CapitalizationTitleQuotas">CapitalizationTitleQuotas</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitlequotas"></a>
<a id="schema_CapitalizationTitleQuotas"></a>
<a id="tocScapitalizationtitlequotas"></a>
<a id="tocscapitalizationtitlequotas"></a>

```json
{
  "quota": 10,
  "capitalizationQuota": [
    10
  ],
  "raffleQuota": [
    10
  ],
  "chargingQuota": [
    10
  ]
}

```

Quotas

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|quota|integer|true|none|Número da parcela.|
|capitalizationQuota|[number]|true|none|Percentual da contribuição destinado à constituição de capital referente ao direito de resgate.|
|raffleQuota|[number]|true|none|Percentual da contribuição designado a custear os sorteios, se previstos no plano|
|chargingQuota|[number]|true|none|Percentual da contribuição destinado aos custos de despesas com corretagem, colocação e administração do título de capitalização, emissão, divulgação, lucro da sociedade de capitalização e eventuais despesas relavas ao custeio da contemplação obrigatória e da distribuição de bônus.|

<h2 id="tocS_CapitalizationTitleValidity">CapitalizationTitleValidity</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitlevalidity"></a>
<a id="schema_CapitalizationTitleValidity"></a>
<a id="tocScapitalizationtitlevalidity"></a>
<a id="tocscapitalizationtitlevalidity"></a>

```json
48

```

Prazo de vigência do título de capitalização em meses.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|integer|false|none|Prazo de vigência do título de capitalização em meses.|

<h2 id="tocS_CapitalizationTitleSerieSize">CapitalizationTitleSerieSize</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleseriesize"></a>
<a id="schema_CapitalizationTitleSerieSize"></a>
<a id="tocScapitalizationtitleseriesize"></a>
<a id="tocscapitalizationtitleseriesize"></a>

```json
5000000

```

Os títulos de capitalização que prevejam sorteio devem ser estruturados em series, ou seja, em sequencias ou em grupos de títulos submetidos às mesmas condições e características, à exceção do valor do pagamento.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|integer|false|none|Os títulos de capitalização que prevejam sorteio devem ser estruturados em series, ou seja, em sequencias ou em grupos de títulos submetidos às mesmas condições e características, à exceção do valor do pagamento.|

<h2 id="tocS_CapitalizationTitlePeriod">CapitalizationTitlePeriod</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleperiod"></a>
<a id="schema_CapitalizationTitlePeriod"></a>
<a id="tocScapitalizationtitleperiod"></a>
<a id="tocscapitalizationtitleperiod"></a>

```json
{
  "interestRate": 0.25123,
  "updateIndex": [
    "IPCA"
  ],
  "others": [
    "Índice de atualização"
  ],
  "contributionAmount": {
    "minValue": 500,
    "maxValue": 5000,
    "frequency": "MENSAL",
    "value": 0
  },
  "earlyRedemption": [
    10
  ],
  "redemptionPercentageEndTerm": 100.002,
  "gracePeriodRedemption": 48
}

```

Período de Capitalização

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|interestRate|number|true|none|Taxa que remunera a parte da mensalidade destinada a formar o Capital, ou seja, a Provisão Matemática de Resgate, também chamada de saldo de capitalização. Em porcentagem ao mês (% a.m)|
|updateIndex|[string]|true|none|Índice utilizado na correção que remunera a provisão matemática para capitalização|
|others|[string]|false|none|Preenchida pelas participantes quando houver ‘Outros’ no campo.|
|contributionAmount|[CapitalizationTitleContributionAmount](#schemacapitalizationtitlecontributionamount)|true|none|none|
|earlyRedemption|[number]|true|none|Possibilidade de o titular efetuar o resgate do capital constituído antes do fim do prazo de vigência do título, podendo ocorrer por solicitação expressa do titular ou por contemplação em sorteio com liquidação antecipada|
|redemptionPercentageEndTerm|number|true|none|Percentual mínimo da soma das contribuições efetuadas que poderá ser resgatado ao final da vigência,  tendo como condição os pagamentos das parcelas nos respectivos vencimentos.|
|gracePeriodRedemption|integer|true|none|Intervalo de tempo mínimo entre contratação e resgate do direito, em meses.|

<h2 id="tocS_CapitalizationTitleContributionAmount">CapitalizationTitleContributionAmount</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitlecontributionamount"></a>
<a id="schema_CapitalizationTitleContributionAmount"></a>
<a id="tocScapitalizationtitlecontributionamount"></a>
<a id="tocscapitalizationtitlecontributionamount"></a>

```json
{
  "minValue": 500,
  "maxValue": 5000,
  "frequency": "MENSAL",
  "value": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|minValue|number|false|none|Valor Mínimo|
|maxValue|number|false|none|Valor Máximo|
|frequency|string|false|none|Pagamento mensal, pagamento único ou periódico.|
|value|number|false|none|valor|

#### Enumerated Values

|Property|Value|
|---|---|
|frequency|MENSAL|
|frequency|UNICO|
|frequency|PERIODICO|

<h2 id="tocS_CapitalizationTitleLatePayment">CapitalizationTitleLatePayment</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitlelatepayment"></a>
<a id="schema_CapitalizationTitleLatePayment"></a>
<a id="tocScapitalizationtitlelatepayment"></a>
<a id="tocscapitalizationtitlelatepayment"></a>

```json
{
  "suspensionPeriod": 10,
  "termExtensionOption": true
}

```

Atraso de Pagamento

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|suspensionPeriod|integer|true|none|Prazo máximo (contínuo ou intermitente) em meses que o título fica suspenso por atraso de pagamento, antes de ser cancelado (não aplicável a pagamento único).|
|termExtensionOption|boolean|true|none|Alteração do prazo de vigência original, pela suspensão.|

<h2 id="tocS_CapitalizationTitleContributionPayment">CapitalizationTitleContributionPayment</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitlecontributionpayment"></a>
<a id="schema_CapitalizationTitleContributionPayment"></a>
<a id="tocScapitalizationtitlecontributionpayment"></a>
<a id="tocscapitalizationtitlecontributionpayment"></a>

```json
{
  "paymentMethod": [
    "CARTAO_CREDITO"
  ],
  "updateIndex": [
    "IPCA"
  ],
  "others": [
    "Índice de atualização"
  ]
}

```

Pagamento da contribuição

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|paymentMethod|[string]|true|none|Meio de Pagamento utilizados para pagamento da contribuição.|
|updateIndex|[string]|true|none|Índice utilizado na atualização dos pagamentos mensais (para títulos com mais de 12 meses de vigência)|
|others|[string]|false|none|Preenchida pelas participantes quando houver ‘Outros’ no campo.|

<h2 id="tocS_CapitalizationTitleredemption">CapitalizationTitleredemption</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleredemption"></a>
<a id="schema_CapitalizationTitleredemption"></a>
<a id="tocScapitalizationtitleredemption"></a>
<a id="tocscapitalizationtitleredemption"></a>

```json
{
  "redemption": 151.23
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|redemption|number|true|none|Valor percentual (%) de resgate final permitido.|

<h2 id="tocS_CapitalizationTitleRaffle">CapitalizationTitleRaffle</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleraffle"></a>
<a id="schema_CapitalizationTitleRaffle"></a>
<a id="tocScapitalizationtitleraffle"></a>
<a id="tocscapitalizationtitleraffle"></a>

```json
{
  "raffleQty": 10000,
  "timeInterval": [
    "QUINZENAL"
  ],
  "raffleValue": 5,
  "earlySettlementRaffle": true,
  "mandatoryContemplation": true,
  "ruleDescription": "Sorteio às quartas-feiras",
  "minimumContemplationProbability": 0.000001
}

```

Sorteio

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|raffleQty|integer|true|none|Número da quantidade de sorteios previstos ao longo da vigência|
|timeInterval|[string]|true|none|Intervalo de tempo regular previsto entre os sorteios.|
|raffleValue|integer|true|none|Valor dos sorteios representado por múltiplo do valor de contribuição.|
|earlySettlementRaffle|boolean|true|none|Liquidação antecipada em Sorteio. Modelo de sorteio que acarreta, ao título contemplado, o seu resgate total obrigatório (Resolução Normativa 384/20).|
|mandatoryContemplation|boolean|true|none|Contemplação obrigatória. Possibilidade de realização de sorteio com previsão de que o título sorteado seja obrigatoriamente um título comercializado, desde que atingidos os requisitos definidos nas condições gerais do plano.|
|ruleDescription|string|false|none|Campo aberto para descrição a ser feita por cada participante das regras dos sorteios do produto.|
|minimumContemplationProbability|number|true|none|Número representativo da probabilidade mínima de contemplação nos sorteios, em porcentagem (%).|

<h2 id="tocS_CapitalizationTitleAdditionals">CapitalizationTitleAdditionals</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleadditionals"></a>
<a id="schema_CapitalizationTitleAdditionals"></a>
<a id="tocScapitalizationtitleadditionals"></a>
<a id="tocscapitalizationtitleadditionals"></a>

```json
{
  "additionalDetails": "https://example.com/openinsurance"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|additionalDetails|string|true|none|Campo aberto (possibilidade de incluir URL).|

<h2 id="tocS_CapitalizationTitleMinimumRequirements">CapitalizationTitleMinimumRequirements</h2>
<!-- backwards compatibility -->
<a id="schemacapitalizationtitleminimumrequirements"></a>
<a id="schema_CapitalizationTitleMinimumRequirements"></a>
<a id="tocScapitalizationtitleminimumrequirements"></a>
<a id="tocscapitalizationtitleminimumrequirements"></a>

```json
{
  "minimumRequirementDetails": "https://ey.exemplo/capitalizacao/tradicional/PU/requisitos_min",
  "targetAudiences": [
    "PESSOAL_NATURAL"
  ]
}

```

Requisitos mínimos.

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|minimumRequirementDetails|string|true|none|Detalhamento do requisito mínimo para contratação - Campo aberto (possibilidade de incluir URL).|
|targetAudiences|[string]|true|none|Público Alvo|

<h2 id="tocS_Links">Links</h2>
<!-- backwards compatibility -->
<a id="schemalinks"></a>
<a id="schema_Links"></a>
<a id="tocSlinks"></a>
<a id="tocslinks"></a>

```json
{
  "self": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "first": "https://api.organizacao.com.br/open-insurance/products-services/v1",
  "prev": "string",
  "next": "string",
  "last": "https://api.organizacao.com.br/open-insurance/products-services/v1"
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
  "totalRecords": 10,
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
    "totalRecords": 10,
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
|meta|[Meta](#schemameta)|false|none|none|