# Kreatorku Category API
- [List Category](#list-category)
- [Create Category](#create-category)
- [Update Category](#update-category)
- [Delete Category](#delete-category)

## List Category
Get list of category by keywords or type

##### Headers
- `GET` HTTP METHOD

##### Resource URL
- http://api.kreatorku.com/v1/categories

##### Parameters
- `keywords` (optional) Filter berdasarkan nama kategori
- `type` (optional) Tipe kategori
- `no_limit` (optional) Tampilkan seluruh kategori tanpa batas jumlah [`true` | `false`]
- `item_limit` (optional) Batas jumlah kategori yang keluar [Default: 10]

## Create Category

##### Headers
- `POST` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/categories

##### Parameters
Tidak ada

##### POST Request Data
- `name` (required) Nama kategori
- `type` (required) Tipe kategori [`Product` | `Post` | `Commission` | `Art`]
- `parent_id` (optional) Kategori utama
- `description` (optional) Penjelasan tentang kategori

## Update Category

##### Headers
- `PUT` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/categories/{id}

##### Parameters
- `id` ID dari kategori yang akan diubah

##### PUT Request Data
- `name` (optional) Nama kategori
- `type` (optional) Tipe kategori [`Product` | `Post` | `Commission` | `Art`]
- `parent_id` (optional) Kategori utama
- `description` (optional) Penjelasan tentang kategori

## Delete Category

##### Headers
- `DELETE` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/categories/{id}

##### Parameters
- `id` ID dari kategori yang akan diubah