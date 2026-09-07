
# PendingRefund


## Properties

Name | Type
------------ | -------------
`paymentId` | string
`amount` | number
`currency` | string
`status` | string
`reason` | string
`failureCode` | string
`failureMessage` | string
`acceptedAt` | Date
`declinedAt` | Date
`createdAt` | Date
`updatedAt` | Date

## Example

```typescript
import type { PendingRefund } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "paymentId": null,
  "amount": null,
  "currency": null,
  "status": null,
  "reason": null,
  "failureCode": null,
  "failureMessage": null,
  "acceptedAt": null,
  "declinedAt": null,
  "createdAt": null,
  "updatedAt": null,
} satisfies PendingRefund

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PendingRefund
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


