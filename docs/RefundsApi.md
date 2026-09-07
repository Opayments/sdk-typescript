# RefundsApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPaymentRefund**](RefundsApi.md#createpaymentrefund) | **POST** /payments/{paymentId}/refund | Создать возврат |
| [**getPaymentRefund**](RefundsApi.md#getpaymentrefund) | **GET** /payments/{paymentId}/refund | Получить возврат |



## createPaymentRefund

> Refund createPaymentRefund(paymentId, createRefundRequest)

Создать возврат

### Example

```ts
import {
  Configuration,
  RefundsApi,
} from '@opayments/sdk';
import type { CreatePaymentRefundRequest } from '@opayments/sdk';

async function example() {
  console.log("🚀 Testing @opayments/sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: RequestSignature
    apiKey: "YOUR API KEY",
    // To configure API key authorization: ProjectIdentity
    apiKey: "YOUR API KEY",
  });
  const api = new RefundsApi(config);

  const body = {
    // string
    paymentId: c9ee7c85-4cc0-494f-a0de-0af7257a66a6,
    // CreateRefundRequest
    createRefundRequest: ...,
  } satisfies CreatePaymentRefundRequest;

  try {
    const data = await api.createPaymentRefund(body);
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
| **paymentId** | `string` |  | [Defaults to `undefined`] |
| **createRefundRequest** | [CreateRefundRequest](CreateRefundRequest.md) |  | |

### Return type

[**Refund**](Refund.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Ранее созданный возврат с теми же параметрами. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **202** | Возврат принят в обработку. |  * Location -  <br>  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **404** | Ресурс не найден. |  * X-Request-Id -  <br>  |
| **409** | Параметры ранее созданного возврата отличаются. |  * X-Request-Id -  <br>  |
| **415** | Тело запроса должно быть JSON. |  * X-Request-Id -  <br>  |
| **422** | Операция невозможна в текущем статусе платежа. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **500** | Внутренняя ошибка сервиса. |  * X-Request-Id -  <br>  |
| **502** | Внешний сервис вернул некорректный ответ. |  * X-Request-Id -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  |
| **504** | Внешний сервис не ответил вовремя. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getPaymentRefund

> Refund getPaymentRefund(paymentId)

Получить возврат

### Example

```ts
import {
  Configuration,
  RefundsApi,
} from '@opayments/sdk';
import type { GetPaymentRefundRequest } from '@opayments/sdk';

async function example() {
  console.log("🚀 Testing @opayments/sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: RequestSignature
    apiKey: "YOUR API KEY",
    // To configure API key authorization: ProjectIdentity
    apiKey: "YOUR API KEY",
  });
  const api = new RefundsApi(config);

  const body = {
    // string
    paymentId: c9ee7c85-4cc0-494f-a0de-0af7257a66a6,
  } satisfies GetPaymentRefundRequest;

  try {
    const data = await api.getPaymentRefund(body);
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
| **paymentId** | `string` |  | [Defaults to `undefined`] |

### Return type

[**Refund**](Refund.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Возврат. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **404** | Возврат не найден. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

