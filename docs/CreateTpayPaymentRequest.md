
# CreateTpayPaymentRequest


## Properties

Name | Type
------------ | -------------
`orderId` | string
`amount` | number
`currency` | string
`description` | string
`ip` | string
`callbackUrl` | string
`successUrl` | string
`failedUrl` | string
`deviceData` | [TpayDeviceData](TpayDeviceData.md)

## Example

```typescript
import type { CreateTpayPaymentRequest } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "orderId": null,
  "amount": null,
  "currency": null,
  "description": null,
  "ip": null,
  "callbackUrl": null,
  "successUrl": null,
  "failedUrl": null,
  "deviceData": null,
} satisfies CreateTpayPaymentRequest

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as CreateTpayPaymentRequest
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


