# Menggunakan entri anime Ryuuganime

> [!NOTE|label:Catatan]
> Berkas ini akan memandu pengguna dalam menggunakan berkas indeks/entri anime Ryuuganime, sementara kami mencoba yang terbaik untuk membuat file ini seperti dokumentasi API.

## Memulai dan inisialisasi
Saat ini, kami tidak memiliki API untuk mengakses database. Sebagai gantinya, Anda dapat menggunakan tautan GitHub Raw untuk mengakses data kami.

Untuk daftar indeks yang dapat dibaca oleh mesin, silakan gunakan `index.json` ataupun `index.yaml`.

Saat ini kami menyediakan data dalam format file HJSON, JSON, YAML, dan XML. Jadi, semua data telah distandarisasi berdasarkan berkas JSON Schema kustom kami untuk validasi.

Dokumen ini akan mencakup solusi pada proyek Anda dalam bahasa pemrograman apa pun.

## Enkoding
Ryuuganime menggunakan UTF-8 (Unicode) dengan format End of Line Sequence *nix (LF).

## Klien
Ryuuganime tidak memerlukan Anda untuk membuat klien apa pun terlebih dahulu untuk mengambil data anime pada <span style="font-style:italic;">end</span> Anda. Anda hanya perlu menggunakan URL GitHub Raw untuk melakukan `GET`, dan selesai!

## URI Fetching Data
### Fetch berkas
#### Fetch data satu entri dari repositori
<!-- tabs:start -->
##### **JSON**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/json/<RYU-ID>/<RYU-ID>.json
```

##### **YAML**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/yaml/<RYU-ID>/<RYU-ID>.yaml
```

##### **HJSON**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/hjson/<RYU-ID>/<RYU-ID>.hjson
```

##### **XML**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/xml/<RYU-ID>/<RYU-ID>.xml
```

<!-- tabs:end -->

>[!WARNING|label:Peringatan]
>Perlu diingat bahwa Anda harus mengubah `<RYU-ID>` terlebih dahulu sebelum memulai fetch data.

#### Fetch daftar indeks anime
<!-- tabs:start -->
##### **JSON**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/index.json
```

##### **YAML**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/index.yaml
```

##### **HJSON**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/index.hjson
```

##### **XML**
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/index.xml
```
<!-- tabs:end -->

## Menggunakan berkas entri
### Pendahuluan
Untuk pengenalan penggunaan dasar, kita akan menggunakan `RYU-1` (Ryuuganime ID: 1).

> [!ATTENTION|label:Perhatian]
> Silakan pilih opsi bahasa markah yang Anda ingin gunakan.
<!-- select:start -->
<!-- select-menu-labels: Markah bahasa -->

#### ~~--~~

#### --JSON--
Pertama, Anda perlu mendapatkan metadata dengan mengirimkan request `GET` HTML dari GitHub Raw:
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/json/000/001.json
```

Anda akan mendapatkan:

[](https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/json/000/001.json ':include :type=code json')

#### --YAML--
Pertama, Anda perlu mendapatkan metadata dengan mengirimkan request `GET` HTML dari GitHub Raw:
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/yaml/000/001.yaml
```

Anda akan mendapatkan:

[](https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/yaml/000/001.yaml ':include :type=code yaml')

#### --HJSON--
Pertama, Anda perlu mendapatkan metadata dengan mengirimkan request `GET` HTML dari GitHub Raw:
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/hjson/000/001.hjson
```

Anda akan mendapatkan:

[](https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/hjson/000/001.hjson ':include :type=code hjson')

#### --XML--
Pertama, Anda perlu mendapatkan metadata dengan mengirimkan request `GET` HTML dari GitHub Raw:
```curl
https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/xml/000/001.xml
```

Anda akan mendapatkan:

[](https://raw.githubusercontent.com/ryuuganime/ryuuganime-db/master/xml/000/001.xml ':include :type=code xml')

<!-- select:end -->

### Properti/Atribut berkas
Singkatnya, semua berkas dengan markah bahasa yang berbeda, telah distandarisasi berdasarkan berkas JSON Schema kustom, seperti yang telah sebutkan pada [subjudul "Memulai dan inisialisasi"](#memulai-dan-inisialisasi).

Oleh karena itu, kami akan menjelaskan apa maksud dari tiap properti dalam berkas entri berdasarkan JSON Schema.

> [!TIP|label:Tips]
> Properti pada berkas entri Ryuuganime dalam format HJSON telah diberikan komentar berupa definisi properti tersebut.

> [!WARNING|label:Peringatan]
> Bahasa pada subjudul ini menggunakan bahasa Inggris teknis. Pastikan Anda memahami apa itu Schema JSON agar dapat mengetahui fungsi properti/atribut pada berkas entri.

__**Bentuk berkas:**__
* Type: Object
* Require: `$schema`, `title`, `backdrop`, `visualKey`, `synopsis`, `information`, `scores`, `updatedDate`, `streamLinks`, `signature`
* Additional properties: `false`

#### $schema
Alamat untuk menunjukkan Schema JSON Ryuuganime untuk entri anime.
* Type: String
* RegEx Pattern: `\.\./\.\./schemas/entry\.json` atau `https://raw\.githubusercontent\.com/ryuuganime/ryuuganime-db/master/schemas/entry\.json`
* Dapat dikosongkan (`null`): `false`

> [!NOTE|label:Catatan]
> Pada berkas berformat `XML`, properti ini ditiadakan karena isu kompatibilitas.

#### title
Judul serial dalam beberapa bahasa. Berdasarkan kode locale ICU.
* Type: Object
* Require: `native`, `en_Latn`, `ar_001`, `id_ID`, `en_US`, `ja_JP`, `de_DE`, `ko_KR`, `fr_FR`, `pt_PT`, `ru_RU`, `es_ES`, `zh_Hans`, `zh_Hant`, `vi_VN`
* Additional properties: `true`
  * RegEx Pattern: `^[a-z]{2,3}_[\w]{2,4}$`
* Dapat dikosongkan (`null`): `true`, dengan catatan `native` dan `en_Latn` tidak dapat dikosongkan.

| Nama properti |  Tipe  | Catatan                                                                                                                                            |
| :-----------: | :----: | -------------------------------------------------------------------------------------------------------------------------------------------------- |
|   `native`    | String | Judul serial dalam bahasa asal. Value tidak dapat dikosongkan.                                                                                     |
|   `en_Latn`   | String | Judul serial yang telah dilatinkan (transliterasi ke aksara Latin). Diperlukan untuk judul utama pada indeks entri. Value tidak dapat dikosongkan. |
|   `ar_001`    | String | Judul serial dalam bahasa Arab Baku (العربية الفصحى).                                                                                              |
|    `id_ID`    | String | Judul serial dalam bahasa Indonesia.                                                                                                               |
|    `en_US`    | String | Judul serial dalam bahasa Inggris (AS) atau lainnya.                                                                                               |
|    `ja_JP`    | String | Judul serial dalam bahasa Jepang.                                                                                                                  |
|    `de_DE`    | String | Judul serial dalam bahasa Jerman.                                                                                                                  |
|    `ko_KR`    | String | Judul serial dalam bahasa Korea (Korsel).                                                                                                          |
|    `fr_FR`    | String | Judul serial dalam bahasa Perancis.                                                                                                                |
|    `pt_PT`    | String | Judul serial dalam bahasa Portugal.                                                                                                                |
|    `ru_RU`    | String | Judul serial dalam bahasa Rusia.                                                                                                                   |
|    `es_ES`    | String | Judul serial dalam bahasa Spanyol (Spanyol).                                                                                                       |
|   `zh_Hans`   | String | Judul serial dalam bahasa China aksara Mandarin/Sederhana.                                                                                         |
|   `zh_Hant`   | String | Judul serial dalam bahasa China aksara Kanton/Tradisional.                                                                                         |
|    `vi_VN`    | String | Judul serial dalam bahasa Vietnam.                                                                                                                 |

#### backdrop
URL gambar *backdrop*/latar belakang/sampul serial. Format tipe media yang sering digunakan adalah `image/jpeg` dan `image/png`.

> [!NOTE|label:Catatan]
> Biasanya menggunakan URL dari The Movie DB, The TVDB, atau Anime-Planet.

* Type: String
  * Format: `URI`
* RegEx Pattern: `^(https?)://`
* Dapat dikosongkan (`null`): `false`

#### visualKey
URL gambar poster/*visual key* serial. Format tipe media yang sering digunakan adalah `image/jpeg` dan `image/png`.

> [!NOTE|label:Catatan]
> Biasanya menggunakan URL dari The Movie DB, The TVDB, Anime-Planet, Kitsu, atau AniList.

* Type: String
  * Format: `URI`
* RegEx Pattern: `^(https?)://`
* Dapat dikosongkan (`null`): `false`

#### synopsis
Sinopsis/latar cerita serial dalam beberapa bahasa. Berdasarkan kode locale ICU.

* Type: Object
* Require: `en_Latn`, `ar_001`, `id_ID`, `en_US`, `ja_JP`, `de_DE`, `ko_KR`, `fr_FR`, `pt_PT`, `ru_RU`, `es_ES`, `zh_Hans`, `zh_Hant`, `vi_VN`
* Additional properties: `true`
  * One of:
    * Type: String
    * Type: Null
* Dapat dikosongkan (`null`): `false`

> [!TIP|label:Tips]
> Meskipun status "Dapat dikosongkan" `false` untuk properti ini, Anda dapat mengosongkan value properti **dalam properti** ini agar terhindar dari masalah kompatibilitas jika memang tidak ada value.

| Nama properti |  Tipe  | Catatan                                                       |
| :-----------: | :----: | ------------------------------------------------------------- |
|   `ar_001`    | String | Sinopsis serial dalam bahasa Arab Baku (العربية الفصحى).      |
|    `id_ID`    | String | Sinopsis serial dalam bahasa Indonesia.                       |
|    `en_US`    | String | Sinopsis serial dalam bahasa Inggris (AS) atau lainnya.       |
|    `ja_JP`    | String | Sinopsis serial dalam bahasa Jepang.                          |
|    `de_DE`    | String | Sinopsis serial dalam bahasa Jerman.                          |
|    `ko_KR`    | String | Sinopsis serial dalam bahasa Korea (Korsel).                  |
|    `fr_FR`    | String | Sinopsis serial dalam bahasa Perancis.                        |
|    `pt_PT`    | String | Sinopsis serial dalam bahasa Portugal.                        |
|    `ru_RU`    | String | Sinopsis serial dalam bahasa Rusia.                           |
|    `es_ES`    | String | Sinopsis serial dalam bahasa Spanyol (Spanyol).               |
|   `zh_Hans`   | String | Sinopsis serial dalam bahasa China aksara Mandarin/Sederhana. |
|   `zh_Hant`   | String | Sinopsis serial dalam bahasa China aksara Kanton/Tradisional. |
|    `vi_VN`    | String | Sinopsis serial dalam bahasa Vietnam.                         |

#### information
Sekumpulan informasi mengenai serial

* Type: Object
* Require: `synonyms`, `type`, `status`, `serialGenre`, `serialTags`, `releaseSeason`, `releaseYear`, `episode`, `releaseDate`, `endDate`, `duration`, `totalDuration`, `studio`, `rating`, `isNsfw`, `adaptation`, `country`, `officialWebsite`, `promotionalVideos`, `producers`
* Additional properties: `false`
* Dapat dikosongkan (`null`): `false`

##### synonyms
Judul serial dalam beberapa bahasa. Berdasarkan kode locale ICU.
* Type: Object
* Require: `native`, `en_Latn`, `ar_001`, `id_ID`, `en_US`, `ja_JP`, `de_DE`, `ko_KR`, `fr_FR`, `pt_PT`, `ru_RU`, `es_ES`, `zh_Hans`, `zh_Hant`, `vi_VN`
* Additional properties: `true`
  * RegEx Pattern: `^[a-z]{2,3}_[\w]{2,4}$`
* Dapat dikosongkan (`null`): `false`

##### type
Tipe serial
* Type: Object
* Require: `en_US`, `id_ID`
* Additional properties: `false`
* Dapat dikosongkan (`null`): `false`, juga pada tiap properti dalam properti ini.

| Nama properti |  Tipe  | Catatan                                                                                         |
| :-----------: | :----: | ----------------------------------------------------------------------------------------------- |
|    `en_US`    | String | Enum dari:  `TV`,  `ONA`,  `OVA`,  `OAD`,  `Special`,  `Movie`,  `Music`, dan `Unknown`         |
|    `id_ID`    | String | Enum dari:  `TV`,  `ONA`,  `OVA`,  `OAD`,  `Spesial`,  `Film`,  `Musik`, dan  `Tidak Diketahui` |

##### status
Menjelaskan status penayangan serial.
* Type: Object
* Require: `en_US`, `id_ID`
* Additional properties: `false`
* Dapat dikosongkan (`null`): `false`, juga pada tiap properti dalam properti ini.

| Nama properti |  Tipe  | Catatan                                                                                             |
| :-----------: | :----: | --------------------------------------------------------------------------------------------------- |
|    `en_US`    | String | Enum dari:  `Aired`,  `Airing`,  `Planned`,  `TBA`, dan `Unknown`                                   |
|    `id_ID`    | String | Enum dari:  `Ditayangkan`,  `Mengudara`,  `Direncanakan`,  `Akan Diumumkan`, dan  `Tidak Diketahui` |

