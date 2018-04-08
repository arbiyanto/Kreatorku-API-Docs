# Kreatorku Products API
- [List Product](#list-product)
- [Create Product](#create-product)
- [Update Product](#update-product)
- [Delete Product](#delete-product)

## List Product

##### Headers
- `GET` HTTP METHOD

##### Resource URL
- http://api.kreatorku.com/v1/products

##### Parameters
- `keywords` (optional) Filter berdasarkan judul
- `order_by` (optional) Filter berdasarkan nama field
- `sort_by` (optional) Sorting [`ASC` | `DESC` *Default: DESC]
- `price` (optional) Filter berdasarkan harga
- `price_range` (optional) Filter berdasarkan rentang harga, Format: price_start-price_end  (strip symbol is seperator)
- `procurement` (optional) Filter berdasarkan tipe pemesanan [`Pre-order` | `Order`]
- `pickup` (optional) Filter berdasarkan pickup [`true` | `false`]
- `stock` (optional) Filter berdasarkan jumlah stok [`true` | `false` | integer]
- `discount` (optional) Filter berdasarkan diskon [`true` | `false` | integer]
- `discount_range` (optional) Filter berdasarkan rentang harga, Format: discount_start-discount_end  (strip symbol is seperator)
- `line_id` (optional) Filter berdasarkan kategori

## Create Product

##### Headers
- `POST` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/products

##### Parameters
Tidak ada

##### POST Request Data
- `class` (required) Kelas Produk [`Digital` | `Physical`]
- `name` (required) Judul Produk / Katalog
- `type` (required) Tipe Produk [`Catalog` | `Item`]
- `procurement` (required) Tipe Pemesanan [`Pre-order` | `Order`]
- `line_id` (required) Kategori Produk [`Check on Category`]
    - Gunakan nilai `0` jika `type` bernilai `Catalog`
- `price` (required) Harga produk 
- `stock` (required) Stok produk
    - Gunakan nilai `0` sebagai default jika jenis produk tidak membutuhkan field ini
- `weight` (required) Berat produk
    - Gunakan nilai `0` sebagai default jika jenis produk tidak membutuhkan field ini
- `description` (required) Deskripsi produk
- `images` (required | `JSON`) Kumpulan image
    Field yang harus ada di dalam masing-masing image:
    - `image` Nama file
- `preorder` (required if `procurement` = `Pre-Order` | `JSON`)
    - `date` (required) Tanggal pre-order dimulai
    - `duration_days` (required) Durasi waktu pre-order dibuka
    - `limit ` (optional) Batas stok pemesanan produk [`0`]
- `tags` (optional | `JSON`)
    - `tag_id` Tag identifier
- `files` (required if `class` = `Digital` | `JSON`)
    - `filename` (required) Nama file

## Update Product

##### Headers
- `PUT` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/products/{id}

##### Parameters
- `id` ID dari produk yang akan diubah

##### PUT Request Data
- `name` (optional) Judul Produk / Katalog
- `line_id` (optional) Kategori Produk [`Check on Category`]
- `price` (optional) Harga produk 
- `stock` (optional) Stok produk
- `weight` (optional) Berat produk
- `description` (optional) Deskripsi produk
- `images` (optional | `JSON`) Kumpulan image
    Field yang harus ada di dalam masing-masing image:
    - `image` Nama file
- `preorder` (optional if `procurement` = `Pre-Order` | `JSON`)
    - `date` (optional) Tanggal pre-order dimulai
    - `duration_days` (optional) Durasi waktu pre-order dibuka
    - `limit ` (optional) Batas stok pemesanan produk [`0`]
- `tags` (optional | `JSON`)
    - `tag_id` Tag identifier
- `files` (optional if `class` = `Digital` | `JSON`)
    - `filename` (optional) Nama file

## Delete Product

##### Headers
- `DELETE` HTTP METHOD
- Requires authentication

##### Resource URL
- http://api.kreatorku.com/v1/products/{id}

##### Parameters
- `id` ID dari produk yang akan diubah