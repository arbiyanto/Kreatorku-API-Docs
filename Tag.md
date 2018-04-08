# Kreatorku Tag API
- [List Tag](#list-tag)
- [Create Tag](#create-tag)
- [Delete Tag](#delete-tag)

## List Tag
Get list of tag by keywords or type

##### Headers
- `GET` HTTP METHOD

##### Resource URL
- http://api.kreatorku.com/v1/tags

##### Parameters
- `keywords` (optional) Filter berdasarkan nama
- `type` (optional) Tipe tag

## Create Tag

##### Headers
- `POST` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/tags

##### Parameters
Tidak ada

##### POST Request Data
- `name` (required) Nama tag
- `type` (required) Tipe tag [`Product` | `Post` | `Commission`]

## Delete Tag

##### Headers
- `DELETE` HTTP METHOD
- Requires authentication
- Requires admin role

##### Resource URL
- http://api.kreatorku.com/v1/tags/{id}

##### Parameters
- `id` ID dari tag yang akan diubah