
# PrepaymentWebhookNotification


## Properties

Name | Type
------------ | -------------
`notificationId` | string
`notificationType` | string
`notificationDate` | Date
`payment` | [PrepaymentPayment](PrepaymentPayment.md)

## Example

```typescript
import type { PrepaymentWebhookNotification } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "notificationId": null,
  "notificationType": null,
  "notificationDate": null,
  "payment": null,
} satisfies PrepaymentWebhookNotification

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PrepaymentWebhookNotification
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


