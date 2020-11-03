# Berkontribusi di database

!> Berikut ini adalah seperangkat pedoman untuk berkontribusi ke `ryuuganime-db`. Sebagian besar dari dokumen ini adalah pedoman, bukan aturan. Gunakan penilaian terbaik Anda, dan jangan ragu untuk mengusulkan perubahan pada dokumen ini dalam pull request.

## Kode Etik
Proyek ini, juga semua kontributor yang berpartisipasi di repo berikut diatur oleh [Kode Etik Contributor Covenant versi 2.0](id_ID/Kode_etik.md). Dengan berpartisipasi, Anda diharapkan untuk menjunjung tinggi kode etik ini. Laporkan perilaku yang tidak dapat diterima kepada [contact@ryuuganime.my.id](mailto:contact@ryuuganime.my.id).

## Memulai
### Ekstensi, aplikasi, dan layanan yang digunakan

?> Ini merupakan rekomendasi dari pihak pengembang. Anda juga dapat menggunakan aplikasi/ekstensi utama Anda, tetapi risiko terdapat pada Anda. 

* [Microsoft Visual Studio Code](https://code.visualstudio.com/) untuk editor kode. <dl>
    <dd>
        Jika Anda menggunakan Visual Studio Code, Anda mungkin akan mendapatkan prompt untuk menginstal beberapa ekstensi yang direkomendasikan. Silakan untuk menginstal dan menggunakan ekstensi yang disebutkan.
    </dd>
</dl>

* [Google Chrome](https://www.google.com/chrome/) untuk akses internet.
* [SIMKL Search](https://chrome.google.com/webstore/detail/mdofghopgfobjkgepojjmcfljnocaaff), ekstensi utilitas untuk mencari entri berdasarkan teks terpilih.
* [1&#46;1&#46;1&#46;1](https://1.1.1.1), aplikasi DNS+VPN. Sangat membantu untuk membuka website yang diblokir oleh ISP maupun pemerintah.
* [Git]

!> **Khusus untuk pengguna asal Indonesia**: Unduh dan pasangkan [Bebasid](https://github.com/bebasid/bebasid) sebagai alternatif VPN (yang mana memanfaatkan file host di sistem operasi) untuk <span style="font-style:italic;">bypass</span> website yang terblokir.

### Akses situs
Berikut adalah tabel untuk situs yang digunakan pada repositori database Ryuuganime. Pastikan Anda dapat mengakses website tersebut.

|                                 Favicon                                 | Situs                                 | Tautan                                                                             | Catatan tambahan                                                                                                                                    |
| :---------------------------------------------------------------------: | ------------------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
|        ![](https://www.google.com/s2/favicons?domain=anidb.net)         | AniDB                                 | <https://anidb.net>                                                                |                                                                                                                                                     |
|        ![](https://www.google.com/s2/favicons?domain=anilist.co)        | AniList                               | <https://anilist.co>                                                               |                                                                                                                                                     |
|   ![](https://www.google.com/s2/favicons?domain=www.anime-planet.com)   | Anime-Planet                          | <https://anime-planet.com>                                                         |                                                                                                                                                     |
| ![](https://www.google.com/s2/favicons?domain=www.animenewsnetwork.com) | Anime News Network                    | <https://animenewsnetwork.com>                                                     |                                                                                                                                                     |
|    ![](https://www.google.com/s2/favicons?domain=www.anisearch.com)     | AniSearch                             | <https://anisearch.com> *atau* <https://anisearch.de>                              |                                                                                                                                                     |
|        ![](https://www.google.com/s2/favicons?domain=annict.com)        | Annict                                | <https://annict.com> *atau* <https://annict.jp>                                    | VPN atau Proxy harus diaktifkan untuk kontributor Indonesia, Bebasid tidak berfungsi.                                                               |
|  ![](https://www.google.com/s2/favicons?domain=db.silveryasha.web.id/)  | DB Fansub Indonesia oleh Silver Yasha | <https://db.silveryasha.web.id/>                                                   | Tidak ada dukungan bahasa Inggris. Hanya untuk mengambil tautan fansub Indonesia.                                                                   |
|       ![](https://www.google.com/s2/favicons?domain=www.imdb.com)       | IMDb                                  | <https://imdb.com>                                                                 |                                                                                                                                                     |
|     ![](https://www.google.com/s2/favicons?domain=www.kinopoisk.ru)     | Kinopoisk                             | <https://kinopoisk.ru>                                                             | Tidak ada dukungan bahasa Inggris.                                                                                                                  |
|         ![](https://www.google.com/s2/favicons?domain=kitsu.io)         | Kitsu                                 | <https://kitsu.io>                                                                 |                                                                                                                                                     |
|     ![](https://www.google.com/s2/favicons?domain=www.livechart.me)     | LiveChart                             | <https://livechart.me>                                                             |                                                                                                                                                     |
|     ![](https://www.google.com/s2/favicons?domain=myanimelist.net)      | MyAnimeList                           | <https://myanimelist.net>                                                          |                                                                                                                                                     |
|      ![](https://www.google.com/s2/favicons?domain=en.myshows.me)       | MyShows                               | <https://en.myshows.me> *atau* <https://ru.myshows.me> *atau* <https://myshows.me> |                                                                                                                                                     |
|    ![](https://www.google.com/s2/favicons?domain=www.nautiljon.com)     | Nautiljon                             | <https://nautiljon.com>                                                            | Tidak ada dukungan bahasa Inggris.                                                                                                                  |
|        ![](https://www.google.com/s2/favicons?domain=notify.moe)        | Notify.moe                            | <https://notify.moe>                                                               |                                                                                                                                                     |
|      ![](https://www.google.com/s2/favicons?domain=otakotaku.com)       | Otak Otaku                            | <https://otakotaku.com>                                                            | Tidak ada dukungan bahasa Inggris.                                                                                                                  |
|      ![](https://www.google.com/s2/favicons?domain=shikimori.one)       | Shikimori                             | <https://shikimori.one> *atau* <https://shikimori.org>                             | Kontributor perlu mendaftar untuk mengubah bahasa ke bahasa Inggris.                                                                                |
|        ![](https://www.google.com/s2/favicons?domain=simkl.com)         | Simkl                                 | <https://simkl.com>                                                                |                                                                                                                                                     |
|    ![](https://www.google.com/s2/favicons?domain=www.themoviedb.org)    | The Movie Database                    | <https://themoviedb.org>                                                           |                                                                                                                                                     |
|       ![](https://www.google.com/s2/favicons?domain=thetvdb.com)        | The TVDB                              | <https://thetvdb.com>                                                              |                                                                                                                                                     |
|         ![](https://www.google.com/s2/favicons?domain=trakt.tv)         | Trakt                                 | <https://trakt.tv>                                                                 |                                                                                                                                                     |
|        ![](https://www.google.com/s2/favicons?domain=tvtime.com)        | TVTime                                | <https://tvtime.com>                                                               | Kontributor harus mendaftar melalui telepon mereka untuk mendapatkan akses ke situs, atau memaksanya lewat [tautan berikut](https://tvtime.com/en). |

### Repositori rekomendasi
Jika Anda memahami rekonstruksi berkas JSON dari repositori khusus database offline dari pihak ketiga, kami sangat merekomendasikan Anda untuk <span style="font-style:italic;">melirik</span> repositori [manami-project/anime-offline-database](https://github.com/manami-project/anime-offline-database).

## Commit dan pull request
### Mengkloning repositori
Untuk dapat mengklon repositori database, pastikan aplikasi [Git] telah terinstall pada perangkat Anda. Juga pastikan repositori telah di-fork ke akun GitHub Anda.

Melalui command line/terminal, ketik:
```sh
git clone https://github.com/<USERNAME ANDA>/ryuuganime-db
```
!>Ingatlah untuk mengubah <code>&lt;USERNAME ANDA&gt;</code> ke nama pengguna GitHub Anda.

### Menambahkan indeks anime
_Artikel utama: [](#)_

### Modifikasi dokumen bermarkah MediaWiki (`.wiki`)
Silakan untuk mempelajari terlebih dahulu format markah dokumen MediaWiki melalui [dokumentasi resmi MediaWiki dari Wikimedia Foundation](https://www.mediawiki.org/wiki/Help:Formatting) dan [ekstensi GitHub untuk <span style="font-style:italic;">rendering</span> dokumen MediaWiki](https://github.com/nricciar/wikicloth).

Namun, MediaWiki di GitHub lebih dibatasi pada kustomisasi. Jadi perlu diingat bahwa Anda tidak dapat membuat teks berwarna, <span style="font-style:italic;">oke</span>?

### Penamaan berkas
_Artikel utama: [](#)_

### Commit perubahan
Tidak ada pedoman ketat untuk menambahkan pesan commit. Namun, yang terbaik adalah membuatnya "seragam".

Kami biasanya menggunakan awalan berikut:

* `Add`<br/>digunakan apabila berkas <span style="font-style:italic;">untracked</span> oleh Git.
* `Modify` atau `Fix`<br/>digunakan ketika ada beberapa baris kode diubah.
* `Batch update`<br/>~~digunakan ketika kontributor sedang <span style="font-style:italic;">mager ngetrack</span> semua perubahan~~
* `Update`<br/>Memiliki fungsi yang sama dengan `Modify` ataupun `Fix`, tetapi lebih dikhususkan untuk dokumentasi.
* `Remove` atau `Delete`<br/>menjelaskan bahwa berkas `x` dihapus dari repositori.

### Mengirimkan permintaan penggabungan pull request

1. Pastikan Anda sudah menamakan commit Anda dengan petunjuk [Commit perubahan](#commit-perubahan).
2. Namai pull request Anda pada kolom Judul (Title) dengan:
   ```sh
   <DETAIL>: <KOMENTAR>
   ```
   Dengan catatan sebagai berikut:
   * `Detail`<br/>Mendefinisikan apa tujuan dari pull request ini.<br/>Argumen yang tersedia, saat ini:
     * `Add`, `Modify`, `Fix`, `Update`, `Remove`
   * `Komentar`<br/>Menjelaskan secara singkat semua perubahan yang Anda <span style="font-style:italic;">commit</span>.
3. Pada kolom komentar (Comment), isi segala informasi yang menurut Anda penting.
4. Setelah memastikan semua informasi benar, ketuk tombol hijau yang bertuliskan "Send pull request" (Kirimkan pull request) untuk mulai mengirim.
5. Anda kini dapat melihat pull request Anda memiliki status `Open`.

## Mengirim isu saran atau masalah
Punya ide bagus atau menemukan masalah tetapi tidak dapat menjalankan juga, atau tidak terbiasa dengan antarmuka Git? Sekarang, Anda bisa tenang karena GitHub memiliki fitur yang amat membantu, bernama [GitHub Issue](https://github.com/ryuuganime/ryuuganime-db/issues). Fitur tersebut membantu pengguna untuk "berinteraksi" pengembang dengan 0 pengetahuan tentang pengodean.

<!-- References -->
[Git]: https://git-scm.com/download