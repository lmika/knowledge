---
title: Detecting When GetItem On DynamoDB Returns Nothing
type: howto
---

The best way to detect when a GetItem call to DynamoDB returns no values is to check that the returned `Item` field is `nil`:

    out, err := p.client.GetItem(ctx, &dynamodb.GetItemInput{
        Key:       key,
        TableName: tableName,
    })
    if err != nil {
        // Error getting the item
        return nil, err
    } else if out.Item == nil {
        // No item found
        return nil, nil
    }
    
    // Do the thing with out.Item