# Bill of Manufacture (BOM)

## Introduction

Bill of Manufacture adalah list of produk untuk mengolah menjadi produk lain.
<br>
Contohnya: Untuk produksi

**Produk: Smoke Salmon, 40pack**<br>
Perlu bahan-bahan sebagai berikut:

|Product|Jumlah|Satuan Unit|
|-------|-----:|:----------|
|Salmon Fresh|1200|gram|
|Kayu Bakar|10|Kg|

List di atas lah, kita menyebutkan nya sebagai Bill of Material.


## Menu

> Pabrik > Data Maste > Bill of Material

![BOM Menu](img/BOM_menu.png)

## Membuat Bill of Material

![BOM Form](img/bom_form.png)

|Field|Required|Description|Default|
|-----|--------|-----------|-------|
|Produk|Yes|Produk Jadi|-|
|Jumlah|Yes|Kuantitas di produksi|-|
|Rujukan|No|Kode Resep bila ada|-|
|BoM Jenis|No|`Manufacture this Product`<br> Produk ini perlu di produksi|Manufacture this product|
|||`Ship this product as a set of components(kit)`<br> Produk perlu/tidak produksi dan bisa di kirim raw materialnya langsung<br> **Contoh:**<br> Product Jadi: Detergen ABC Promo Bulan Ramadhan<br> BoM Nya: <br> 1. Detergen ABC:  1 Bks<br> 2. Piring: 1 pcs<br> Bila ada orderan Untuk "Detergen ABC promo Bulan Ramadhan", akan di kirim langsung BoM nya

**Komponen**

|Field|Required|Description|Default|
|-----|--------|-----------|-------|
|Produk|Yes|||
|Kuantitas|Yes|||
|Satuan Unit|Yes|||
