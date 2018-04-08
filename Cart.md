# Kreatorku Cart API
- [List Cart](#list-cart)
- [Create Cart](#create-cart)
- [Update Cart](#update-cart)
- [Delete Cart](#delete-cart)

## List Cart

##### Headers
- `GET` HTTP METHOD

##### Resource URL
- http://api.kreatorku.com/v1/carts

##### Parameters
Tidak ada

## Create Cart

##### Headers
- `POST` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/carts/{type}

##### Parameters
- `type` (optional) Tipe produk untuk keranjang belanja [`Product` | `Commission`] (Default: Product)

##### POST Request Data
- `product_id` (required)
- `quantity` (required)
- `details` (optional)

## Update Cart

##### Headers
- `PUT` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/carts/{id}

##### Parameters
- `id` ID dari Cart yang akan diubah

##### PUT Request Data
- `product_id` (required)
- `quantity` (required)
- `details` (optional)

## Delete Cart

##### Headers
- `DELETE` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/carts/{id}

##### Parameters
- `id` ID dari Cart yang akan diubah