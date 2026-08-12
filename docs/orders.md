# Orders API

## Overview 

The Orders API allows you to create and retrive orders in the BookHub System.

## Create an Order

Create s anew order for one or more books.

### EndPoint

```http
POST /orders
```

### Request 

The request body must contain the book details required to create the order.

### Example Request

```json
{
    "book id": 1,
    "quantity": 1
}
```

### Exmaple Response

```json
{
    "order id": 101,
    "status": "confirmed",
    "book id": 1,
    "quantity": 1
}
```