# Kreatorku Circle API
- [List Circle](#list-circle)
- [Create Circle](#create-circle)
- [Update Circle](#update-circle)
- [Delete Circle](#delete-circle)

## List Circle
Get list of Circle by keywords or type

##### Headers
- `GET` HTTP METHOD

##### Resource URL
- http://api.kreatorku.com/v1/circles

##### Parameters
- `keywords` (optional) Filter berdasarkan nama circle

## Create Circle

##### Headers
- `POST` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/circles

##### Parameters
Tidak ada

##### POST Request Data
- `name` (required) Nama Circle
- `slug` (required) URI Circle
- `tagline` (optional) Tagline circle
- `description` (optional) Penjelasan tentang circle
- `picture` (optional) Foto circle

## Update Circle

##### Headers
- `PUT` HTTP METHOD
- Requires authentication
- Requires admin role

##### Resource URL
- http://api.kreatorku.com/v1/circles/{id}

##### Parameters
- `id` ID dari circle yang akan diubah

##### PUT Request Data
- `name` (optional) Nama Circle
- `slug` (optional) URI Circle
- `tagline` (optional) Tagline circle
- `description` (optional) Penjelasan tentang circle
- `picture` (optional) Foto circle

## Delete Circle

##### Headers
- `DELETE` HTTP METHOD
- Requires authentication
- Requires admin role

##### Resource URL
- http://api.kreatorku.com/v1/circles/{id}

##### Parameters
- `id` ID dari circle yang akan diubah