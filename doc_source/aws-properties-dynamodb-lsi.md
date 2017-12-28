# Amazon DynamoDB Table LocalSecondaryIndex<a name="aws-properties-dynamodb-lsi"></a>

Describes local secondary indexes for the [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) resource\. Each index is scoped to a given hash key value\. Tables with one or more local secondary indexes are subject to an item collection size limit, where the amount of data within a given item collection cannot exceed 10 GB\.

## Syntax<a name="w3ab2c21c14d532b5"></a>

### JSON<a name="aws-properties-dynamodb-lsi-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-lsi-indexname)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-lsi-keyschema)" : [ KeySchema, ...],                           
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-lsi-projection)" : { Projection }
}
```

### YAML<a name="aws-properties-dynamodb-lsi-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-lsi-indexname): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-lsi-keyschema):
  KeySchema                           
[[ERROR] BAD/MISSING LINK TEXT](#cfn-dynamodb-lsi-projection):
  Projection
```

## Properties<a name="w3ab2c21c14d532b7"></a>

`IndexName`  
The name of the local secondary index\. The index name can be 3 – 255 characters long and have no character restrictions\.  
*Required: *Yes  
*Type*: String

`KeySchema`  
The complete index key schema for the local secondary index, which consists of one or more pairs of attribute names and key types\. For local secondary indexes, the hash key must be the same as that of the source table\.  
*Required: *Yes  
*Type*: List of [DynamoDB Table KeySchema](aws-properties-dynamodb-keyschema.md)

`Projection`  
Attributes that are copied \(projected\) from the source table into the index\. These attributes are additions to the primary key attributes and index key attributes, which are automatically projected\.  
*Required: *Yes  
*Type*: [DynamoDB Table Projection](aws-properties-dynamodb-projectionobject.md)

## Examples<a name="w3ab2c21c14d532b9"></a>

For an example of a declared local secondary index, see \.