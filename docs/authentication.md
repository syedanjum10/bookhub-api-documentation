# Authentication

The BookHub API uses token-based authentication to protect API requests.

## Overview

Clients must include a valid access token in the `Authorization` header when making authenticated requests.

## Authorization Header

Include the access token in the `Authorization` header using the Bearer authentication scheme.

```http
Authorization: Bearer YOUR_ACCESS_TOKEN
```git st

## Example Request

The following example shows how to make an authenticated request:

```http
GET /books
Authorization: Bearer Your_Access_Token
```