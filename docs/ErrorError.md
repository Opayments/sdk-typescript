
# ErrorError


## Properties

Name | Type
------------ | -------------
`type` | string
`code` | string
`message` | string
`details` | [Array&lt;ErrorErrorDetailsInner&gt;](ErrorErrorDetailsInner.md)
`requestId` | string

## Example

```typescript
import type { ErrorError } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "type": null,
  "code": null,
  "message": null,
  "details": null,
  "requestId": null,
} satisfies ErrorError

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ErrorError
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


