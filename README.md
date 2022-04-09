# Tree Container Format (TCF)

## Specification

### Node
| Name | Bytes (`Type`) | Description |
| ------------- | ------------- | ------------- |
| Node ID | (ULEB128) | An unsigned value identifying the ID of `Node`. |
| Node Size | (ULEB128) | An unsigned value identifying the size of `Node`. |
| Node Data | { Value of `Node Size` } | Binary data. |


#### Node Data
`Node Data` is either `Leaf Node` or `Internal Node`.

##### Leaf Node
| Name | Bytes (`Type`) | Description |
| ------------- | ------------- | ------------- |
| Raw Data |  | Raw data. |


##### Internal Node
`Internal Node` contains `Node`s for the size of parent node.

| Name | Bytes (`Type`) | Description |
| ------------- | ------------- | ------------- |
| Node i |  | Node i. |
