# Pesanan Manufaktur

Pesananan Manufaktur bisa kita buat manual atau bisa dapat di buat oleh system dengan cara [Make To Order](../inventory/persediaan.md#make-to-order-manufacture).<br>
<br>
Dengan "Pesanan Manufaktur" kita bisa monitor 2 proses:

1. Mengadakan pengambilan/picking raw material 
2. Memindahkan Produk Jadi ke gudang

## 1. Membuat Pesanan Manufaktur (Manual)

![mo form](img/mo_form.png)

|Field|Required|Description|Default|
|-----|--------|-----------|-------|
|Produk|Yes|||
|Quantity To Produce|Yes|Jumlah yang kita perlukan||
|Bahan Baku|Yes|BoM yang kita akan pakai||
|Deadline Start|Yes|Tanggal yang harus kita sediakan produk jadi||
|Bertanggung Jawab|No|User yang tanggung jawab||
|Sumber|No|Nomor document untuk perintah pesanan ini||

Setelah data yang di data di isikan dengan benar:<br>

![Create workorders](img/manufactur_create_workorders.png)

> Klik > Create Workorders

![mo form1](img/mo_form_1.png)

**Consume Materials** dan **Produk Selesai** akan di isikan automatik oleh system.

## 2. Check Kecukupan Bahan Baku

### a. Kondisi Bahan Baku Tidak Mencukupi

![mo check](img/mo_checkavailability.png)

User bisa klik "Check Availibity" untuk mengechek apakah bahan baku cukup di
proses produksi ini.

![mo form1](img/mo_form_1.png)

```
Note:
Bila Bahan baku tidak memenuhi kebutuhan. System akan stop di sana dan user
tidak bisa melakukan proses next.
User perlu melakukan persediaan inventory untuk memenuhi kebutuhan.
```

### b. Kondisi Bahan Baku Mencukupi
![mo available](img/mo_available.png)

Bila bahan baku itu mencukupi, di `Consume Materials > Kuantitas yang tersedia`
akan di isikan oleh system.


## 3. Pegambilan/Picking Bahan Baku

Print Manufacture Order (MO)/Pesanan Produksi sebagai perintah Produksi dan juga instruksi picking:

![mo print](img/mo_print_button.png)

**Contoh Laporan Produksi dan juga Instruksi Picking**

![mo list](img/mo_list.png)


## 4. Proses Produksi

![MO Produce](img/mo_produce.png)

> Klik > Produce

System akan meng-update status MO ini menjadi `Proses`

![MO Produce](img/mo_produced.png)

Setelah proses, system akan mengadakan pemotongan stock bahan baku dan
penambahan barang jadi di inventory.

User bisa lihat gerakan inventory dengan klik button seperti gambah di bawah
ini:

![Inventory Move](img/inventory_moves.png)

## 5. Pengecheckan Terakhir

Di step ini kita bisa lakukan check terakhir:

1. Apakah ada `Waste` yang harus kita laporan/rekor?
2. Bila tidak ada masalah, kita bisa **Complete** MO ini

### 1. Rekor Waste

![Final Step](img/mo_final.png)

> Klik > Pertarungan

System akan pop up form, user bisa isikan bahan baku yang di rekor sebagai waste

### 2. Produksi Selesai

![Final Step](img/mo_final.png)

> Klik > Mark as Done

Untuk menyelesaikan MO ini.
