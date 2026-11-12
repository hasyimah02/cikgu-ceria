# Animasi Lottie (Cikgu Ceria, Tahap 1 BM)

Muat dalam index.html: `lottie_light.min.js` (tempatan) kemudian `lottie-data.js`. Berfungsi luar talian di file://.
Guna: `lottie.loadAnimation({container, renderer:'svg', loop:true, autoplay:true, animationData: window.LT_BACA})`.

| Pemboleh ubah | Kegunaan | Tempoh | Sumber | Lesen |
|---|---|---|---|---|
| `LT_BACA` | Kucing membaca buku (pengepala hub BM / Buku Bacaan), ulang | 2 s, 686x540 | kucing.json (LottieFiles, "GIF 2 CAT READING") | Lottie Simple License |
| `LT_BINTANG` | Bintang bercermin mata + konfeti, jawapan BETUL, main sekali (loop:false) | 1.6 s, 180x220 | bintang.json (LottieFiles), dipotong ke bingkai 8-56 | Lottie Simple License |
| `LT_CUBA` | Muka lembut lavender + anak panah ulang, CUBA LAGI, ulang | 2 s, 512x512 | Dibuat sendiri (Studio), palet app | Hak milik projek |
| `LT_PENSEL` | Pensel menulis garis (hub Menulis), ulang | 2 s, 800x800 | pensel.json (LottieFiles "Pencil"), warna dilaras ke ungu/koral app | Lottie Simple License |

Juga `LT_DATA.LT_*` (objek sama). Nota: lottie_light.min.js = lottie-web (MIT, lihat LICENSE-lottie-web.txt).
Fail JSON draf sudah dibuang (semua sudah dalam lottie-data.js).
Sumber URL: LT_BACA = https://lottiefiles.com/animations/reading-cat-RvnINkLacs ; LT_BINTANG = https://lottiefiles.com/animations/a-cute-little-star-QviWMSqHZG ; LT_PENSEL = https://lottiefiles.com/animations/pencil-write-2uiJisiCCo ; LT_CUBA = buatan sendiri (Ravi).
Dipasang dalam index.html: fungsi LT_kepala (hub BM Tahap 1, Buku Bacaan, Menulis), LT_main (bintang dalam bmJaya, cuba lagi dalam bqSalah).
