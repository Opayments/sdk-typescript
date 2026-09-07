# PaymentApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createSbpPayment**](PaymentApi.md#createsbppaymentoperation) | **POST** /payments/sbp | Создать платёж по СБП |
| [**createTpayPayment**](PaymentApi.md#createtpaypaymentoperation) | **POST** /payments/tpay | Создать платёж через T-Pay |



## createSbpPayment

> Payment createSbpPayment(createSbpPaymentRequest)

Создать платёж по СБП

### Example

```ts
import {
  Configuration,
  PaymentApi,
} from '@opayments/sdk';
import type { CreateSbpPaymentOperationRequest } from '@opayments/sdk';

async function example() {
  console.log("🚀 Testing @opayments/sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: RequestSignature
    apiKey: "YOUR API KEY",
    // To configure API key authorization: ProjectIdentity
    apiKey: "YOUR API KEY",
  });
  const api = new PaymentApi(config);

  const body = {
    // CreateSbpPaymentRequest
    createSbpPaymentRequest: ...,
  } satisfies CreateSbpPaymentOperationRequest;

  try {
    const data = await api.createSbpPayment(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createSbpPaymentRequest** | [CreateSbpPaymentRequest](CreateSbpPaymentRequest.md) |  | |

### Return type

[**Payment**](Payment.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ранее созданный платёж СБП. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **201** | Платёж через СБП создан. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
| **409** | Запрос конфликтует с текущим состоянием ресурса. |  * X-Request-Id -  <br>  |
| **415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  |
| **504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## createTpayPayment

> Payment createTpayPayment(createTpayPaymentRequest)

Создать платёж через T-Pay

### Example

```ts
import {
  Configuration,
  PaymentApi,
} from '@opayments/sdk';
import type { CreateTpayPaymentOperationRequest } from '@opayments/sdk';

async function example() {
  console.log("🚀 Testing @opayments/sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: RequestSignature
    apiKey: "YOUR API KEY",
    // To configure API key authorization: ProjectIdentity
    apiKey: "YOUR API KEY",
  });
  const api = new PaymentApi(config);

  const body = {
    // CreateTpayPaymentRequest
    createTpayPaymentRequest: ...,
  } satisfies CreateTpayPaymentOperationRequest;

  try {
    const data = await api.createTpayPayment(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **createTpayPaymentRequest** | [CreateTpayPaymentRequest](CreateTpayPaymentRequest.md) |  | |

### Return type

[**Payment**](Payment.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ранее созданный платёж T-Pay. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **201** | Платёж через T-Pay создан. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
| **409** | Запрос конфликтует с текущим состоянием ресурса. |  * X-Request-Id -  <br>  |
| **415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  |
| **504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

