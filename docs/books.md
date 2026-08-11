# Books API

The Books API guides you how to manage APIs 

## Overview

The Books API allows clients to retrieve and manage books in the BookHub catalog.

## Get All Books

Retrieves a list of books from the BookHub catalog.

### EndPoint 

```http
GET /books
```

### Request

No Request body is required

### Example Request

```http
GET /books
Authorization: Bearer YOUR_ACCESS_TOKEN
```

### Example Response

{
    "books":[
        {
            "id": 1,
            "title": "The Alchemist",
            "Author": "Paul Ceoulho"
        }
    ]    
}