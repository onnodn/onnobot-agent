# Pertanyaan yang Sering Diajukan

## Dasar-dasar

> Apakah onnobot-agent berjalan di Windows/MacOS/Linux?

Ya! Satu-satunya batasan Anda mungkin ketersediaan kontainer docker untuk lingkungan Anda.
Tetapi Anda selalu dapat menjalankan onnobot-agent di cloud.

> Saya mendapat pesan kesalahan yang sangat panjang tentang berbagai opsi konfigurasi yang tidak berfungsi. Apa yang terjadi?

Ini mungkin karena tipe union.
Lihat [bagian ini](usage/cl_tutorial.md#union-types) untuk informasi lebih lanjut, tetapi versi singkatnya adalah bahwa beberapa opsi (misalnya, repositori atau pernyataan masalah) dapat ditentukan dengan cara yang berbeda, jadi kami mencoba setiap opsi hingga menemukan yang bekerja berdasarkan masukan Anda.
Jika tidak ada yang berfungsi, kami melempar kesalahan yang kemudian memberi tahu Anda mengapa kami tidak dapat menginisialisasi salah satu tipe, jadi ini akan menjadi agak panjang dan membingungkan.

> Mengapa gambar saya tidak diproses?

Periksa bahwa Anda menggunakan konfigurasi multimodal (lihat `default_mm_with_images.yaml` sebagai contoh), memiliki konektivitas internet, dan gambar di bawah 10MB. Lihat [Catatan penggunaan Multimodal](usage/multimodal.md) untuk detail selengkapnya.

## Model

> Model apa yang didukung? Apakah Anda mendukung model lokal?

Mungkin semuanya, termasuk model lokal! Ada bahkan beberapa untuk pengujian. Lihat [models](installation/keys.md) dan [lebih lanjut tentang model](config/models.md).

> Apakah onnobot-agent mendukung model multimodal dan gambar?

Ya! onnobot-agent mendukung model yang mampu visi yang dapat memproses gambar dari isu GitHub. Gunakan `--config config/default_mm_with_images.yaml` dan tentukan model multimodal seperti Claude Sonnet 4 atau GPT-4o. Lihat [panduan multimodal](usage/multimodal.md) untuk detail.

> Apa yang dapat saya lakukan jika model saya tidak mendukung function calling?

Anda dapat mengonfigurasi cara menguraikan respons model dengan memilih `agent.tools.parse_function`.
Standarnya sekarang adalah `function_calling`, tetapi Anda dapat mengubahnya menjadi `thought_action`.
Informasi lebih lanjut di [referensi](reference/parsers.md).
Ada juga beberapa contoh config di [folder config](https://github.com/onnobot-agent/onnobot-agent/tree/main/config) kami.

## Mengonfigurasi onnobot-agent

> Bagaimana cara mengubah demonstrasi yang diberikan kepada onnobot-agent?

Pada awal setiap jalan, kami memberi agen lintasan demonstrasi, menunjukkan bagaimana menyelesaikan contoh isu.
Ini secara substansial meningkatkan kemampuan agen untuk menyelesaikan isu novel.
Jika Anda ingin memodifikasi atau sepenuhnya mengubah demonstrasi ini, untuk lebih cocok dengan kasus penggunaan Anda, lihat [ini](config/demonstrations.md).

> Bisakah saya menambahkan alat kustom?

Ya! Lihat [tutorial ini](usage/adding_custom_tools.md).

## MISC

> Apa yang terjadi dengan semua file output?

Anda mungkin paling tertarik pada file `*.traj`, yang berisi catatan lengkap tentang proses pemikiran dan tindakan onnobot-agent. Lihat [file output](usage/trajectories.md) untuk informasi lebih lanjut.

## Ada yang lain?

> Saya memiliki pertanyaan/laporan bug/permintaan fitur...

Silakan buka [isu github!](https://github.com/onnobot-agent/onnobot-agent/issues)!


{% include-markdown "_footer.md" %}