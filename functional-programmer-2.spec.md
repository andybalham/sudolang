# Order Splitter

## Types

Order
{
    orderId
    totalAmount
    [
        {
            itemId
            itemAmount
        }
    ]
}

Configuration
{
    valueThreshold
    lowValueEventBusName
    highValueEventBusName
}

## Parameters

An array of Orders
A Configuration

## Output

lowValueEvents: an array of EventBridge PutEvents commands for Configuration lowValueEventBusName, containing all Orders where totalAmount less than Configuration valueThreshold
highValueEvents: an array of EventBridge PutEvents commands for Configuration highValueEventBusName, containing all Orders where totalAmount greater than or equal to Configuration valueThreshold
