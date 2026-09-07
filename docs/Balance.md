
# Balance


## Properties

Name | Type
------------ | -------------
`projectId` | string
`balance` | number
`currency` | string

## Example

```typescript
import type { Balance } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "projectId": null,
  "balance": null,
  "currency": null,
} satisfies Balance

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Balance
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


