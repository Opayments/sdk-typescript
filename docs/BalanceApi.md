# BalanceApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getBalance**](BalanceApi.md#getbalance) | **GET** /balance | Получить баланс |



## getBalance

> Balance getBalance()

Получить баланс

Возвращает текущий баланс проекта.

### Example

```ts
import {
  Configuration,
  BalanceApi,
} from '@opayments/sdk';
import type { GetBalanceRequest } from '@opayments/sdk';

async function example() {
  console.log("🚀 Testing @opayments/sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: RequestSignature
    apiKey: "YOUR API KEY",
    // To configure API key authorization: ProjectIdentity
    apiKey: "YOUR API KEY",
  });
  const api = new BalanceApi(config);

  try {
    const data = await api.getBalance();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**Balance**](Balance.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Баланс проекта. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |
| **503** | Сервис временно недоступен. |  * X-Request-Id -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

