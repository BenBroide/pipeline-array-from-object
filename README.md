# pipeline-array-from-object

Actions get array from object with keys

## Inputs
### `array`
**required** keys of array
### `object`
**required** data of object.
### `environment`
**required** string - key.

## Output
### outputArray
Array containing values
```json
["first", "second"]
```

## Example Usage

```yml
- uses: BenBroide/pipeline-array-from-object@master
    id: data
    with:
      array: ${{array}}
      object: ${{objectJson}}
      environment: 'dev'
- run: | 
    echo "${{ steps.data.outputs.outputArray}}"
  ```
