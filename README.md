# ansible-module-dynamodb-item

This module will put, update, delete an item into a DynamoDB table.

## Requirements: 
 * json 
 * botocore 
 * boto3

## Variables:

```yaml

    state:
        description:
          - The desiredtem into the DynamoDB table
        required: false
        default: present
        choices: ["present", "absent"]
    table:
        description:
          - The name of the DynamoDB table
        required: true
        default: none
    item:
        description:
          - The item to put, this item is mutually exclusive with key and is mandatory when the state is `present`
        required: false
        default: none
    key:
        description:
          - The key to delete, this item is mutually exclusive with key and is mandatory when the state is `absent`
        required: false
        default: none
```