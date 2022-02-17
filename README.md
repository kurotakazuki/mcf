# Tree Container Format (TCF)

### Root Node
| Name | Bytes (`Type`) | Description |
| ------------- | ------------- | ------------- |
| Node ID Size | (ULEB128) | An unsigned value identifying the size of `Node ID`. |
| Node ID | {`Node ID Size`} | `Node ID` binary data. This value can be any type. |
| Tree Size | (ULEB128) | An unsigned value identifying the size of `Tree`. This size value doesn't include the size on or before the `Node ID` field. |
| Node |  | Node. |

### Node
| Name | Bytes (`Type`) | Description |
| ------------- | ------------- | ------------- |
| Number of Child Nodes | (ULEB128) | An unsigned value identifying `Number of Child Nodes`. Unless 0, the node is not a leaf node. |
| Child_i Node ID Size | (ULEB128) | An unsigned value identifying the size of `Child_i Node ID`. |
| Child_i Node ID | {`Child_i Node ID Size`} | `Child_i Node ID` binary data. This value can be any type. |
| Child_i Node Size | (ULEB128) | An unsigned value identifying the size of `Child_i Node`. |
| Node Data | {Size from parent node} - {Size of all child nodes} | Binary data. |
| Child_i Node | {`Child_i Node Size`} | Child_i node. |
