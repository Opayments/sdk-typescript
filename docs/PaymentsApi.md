# PaymentsApi

All URIs are relative to *https://api.opayments.io/api/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getPayment**](PaymentsApi.md#getpayment) | **GET** /payments/{paymentId} | Получить платёж |
| [**listPayments**](PaymentsApi.md#listpayments) | **GET** /payments | Найти платежи |



## getPayment

> PaymentDetails getPayment(paymentId)

Получить платёж

### Example

```ts
import {
  Configuration,
  PaymentsApi,
} from '@opayments/sdk';
import type { GetPaymentRequest } from '@opayments/sdk';

async function example() {
  console.log("🚀 Testing @opayments/sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: RequestSignature
    apiKey: "YOUR API KEY",
    // To configure API key authorization: ProjectIdentity
    apiKey: "YOUR API KEY",
  });
  const api = new PaymentsApi(config);

  const body = {
    // string
    paymentId: c9ee7c85-4cc0-494f-a0de-0af7257a66a6,
  } satisfies GetPaymentRequest;

  try {
    const data = await api.getPayment(body);
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

[**PaymentDetails**](PaymentDetails.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Платёж. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **404** | Ресурс не найден. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## listPayments

> PaymentList listPayments(orderId, status, paymentMethod, amountFrom, amountTo, createdFrom, createdTo, sort, sortDirection, cursor, limit)

Найти платежи

Возвращает список платежей проекта.

### Example

```ts
import {
  Configuration,
  PaymentsApi,
} from '@opayments/sdk';
import type { ListPaymentsRequest } from '@opayments/sdk';

async function example() {
  console.log("🚀 Testing @opayments/sdk SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: RequestSignature
    apiKey: "YOUR API KEY",
    // To configure API key authorization: ProjectIdentity
    apiKey: "YOUR API KEY",
  });
  const api = new PaymentsApi(config);

  const body = {
    // string | Идентификатор заказа в системе мерчанта. (optional)
    orderId: orderId_example,
    // Array<'pending' | 'succeeded' | 'cancelled' | 'chargebacked' | 'refunded'> (optional)
    status: ...,
    // 'sbp' | 'tpay' (optional)
    paymentMethod: paymentMethod_example,
    // number | Не больше amountTo, если он передан. (optional)
    amountFrom: 56,
    // number | Не меньше amountFrom, если он передан. (optional)
    amountTo: 56,
    // Date | Не позже createdTo, если он передан. (optional)
    createdFrom: 2013-10-20T19:20:30+01:00,
    // Date | Не раньше createdFrom, если он передан. (optional)
    createdTo: 2013-10-20T19:20:30+01:00,
    // 'createdAt' | 'amount' (optional)
    sort: sort_example,
    // 'asc' | 'desc' (optional)
    sortDirection: sortDirection_example,
    // string | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. (optional)
    cursor: cursor_example,
    // number | Количество записей в ответе. (optional)
    limit: 56,
  } satisfies ListPaymentsRequest;

  try {
    const data = await api.listPayments(body);
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
| **orderId** | `string` | Идентификатор заказа в системе мерчанта. | [Optional] [Defaults to `undefined`] |
| **status** | `pending`, `succeeded`, `cancelled`, `chargebacked`, `refunded` |  | [Optional] [Enum: pending, succeeded, cancelled, chargebacked, refunded] |
| **paymentMethod** | `sbp`, `tpay` |  | [Optional] [Defaults to `undefined`] [Enum: sbp, tpay] |
| **amountFrom** | `number` | Не больше amountTo, если он передан. | [Optional] [Defaults to `undefined`] |
| **amountTo** | `number` | Не меньше amountFrom, если он передан. | [Optional] [Defaults to `undefined`] |
| **createdFrom** | `Date` | Не позже createdTo, если он передан. | [Optional] [Defaults to `undefined`] |
| **createdTo** | `Date` | Не раньше createdFrom, если он передан. | [Optional] [Defaults to `undefined`] |
| **sort** | `createdAt`, `amount` |  | [Optional] [Defaults to `&#39;createdAt&#39;`] [Enum: createdAt, amount] |
| **sortDirection** | `asc`, `desc` |  | [Optional] [Defaults to `&#39;desc&#39;`] [Enum: asc, desc] |
| **cursor** | `string` | Непрозрачный курсор из предыдущего ответа. Используйте только с теми же фильтрами и сортировкой. | [Optional] [Defaults to `undefined`] |
| **limit** | `number` | Количество записей в ответе. | [Optional] [Defaults to `20`] |

### Return type

[**PaymentList**](PaymentList.md)

### Authorization

[RequestSignature](../README.md#RequestSignature), [ProjectIdentity](../README.md#ProjectIdentity)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Страница платежей. |  * X-Request-Id -  <br>  |
| **400** | Некорректные параметры запроса. |  * X-Request-Id -  <br>  |
| **401** | Не пройдена аутентификация или проверка подписи. |  * X-Request-Id -  <br>  |
| **403** | Операция недоступна для проекта. |  * X-Request-Id -  <br>  |
| **429** | Превышен лимит запросов. |  * X-Request-Id -  <br>  * X-RateLimit-Limit -  <br>  * X-RateLimit-Remaining -  <br>  * X-RateLimit-Reset - Unix-время сброса лимита. <br>  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

