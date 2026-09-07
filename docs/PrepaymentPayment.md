
# PrepaymentPayment


## Properties

Name | Type
------------ | -------------
`paymentId` | string
`orderId` | string
`amount` | number
`currency` | string
`description` | string
`paymentMethod` | string
`status` | string
`paymentUrl` | string
`expiresAt` | Date
`failureCode` | string
`failureMessage` | string
`completedAt` | Date
`createdAt` | Date
`updatedAt` | Date

## Example

```typescript
import type { PrepaymentPayment } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "paymentId": null,
  "orderId": null,
  "amount": null,
  "currency": null,
  "description": null,
  "paymentMethod": null,
  "status": null,
  "paymentUrl": null,
  "expiresAt": null,
  "failureCode": null,
  "failureMessage": null,
  "completedAt": null,
  "createdAt": null,
  "updatedAt": null,
} satisfies PrepaymentPayment

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PrepaymentPayment
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


