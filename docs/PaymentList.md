
# PaymentList


## Properties

Name | Type
------------ | -------------
`items` | [Array&lt;Payment&gt;](Payment.md)
`nextCursor` | string
`hasMore` | boolean

## Example

```typescript
import type { PaymentList } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "items": null,
  "nextCursor": null,
  "hasMore": null,
} satisfies PaymentList

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PaymentList
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


