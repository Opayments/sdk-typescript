
# DeviceData


## Properties

Name | Type
------------ | -------------
`platformType` | string
`os` | string
`browser` | string
`language` | string
`timezoneName` | string
`userAgent` | string

## Example

```typescript
import type { DeviceData } from '@opayments/sdk'

// TODO: Update the object below with actual values
const example = {
  "platformType": null,
  "os": null,
  "browser": null,
  "language": null,
  "timezoneName": null,
  "userAgent": null,
} satisfies DeviceData

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DeviceData
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


