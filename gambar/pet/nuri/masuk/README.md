# Animasi masuk Kelas Al-Quran (aset sahaja)

Disediakan oleh Ravi (Studio) 2026-11-13. Pemasangan: Cikgu Mei Ling. Asal besar: `~/Pejabat/studio/cikgu-ceria/pet-ungu/masuk/`.

## Fail

| Fail | Saiz piksel | Nota |
|---|---|---|
| nuri-kapal.png | 640x500 | PNG telus (palet 256 warna + alfa). Nuri dalam kapal terbang, menghadap KANAN. Arah kiri = cermin dengan `scaleX(-1)`. |
| pintu-kiri.png | 251x700 | PNG telus RGBA. Daun kiri; tepi kanan fail = garis tengah pintu. |
| pintu-kanan.png | 251x700 | PNG telus RGBA. Daun kanan; tepi kiri fail = garis tengah pintu. |
| awan-potret.jpg | 1080x1620 | Latar awan (telefon/potret). Guna `background-size: cover`. |
| awan-landskap.jpg | 1620x1080 | Latar awan (Mac/landskap). |
| masuk-terbang.mp3 | 1.50 s | Whoosh kapal mainan, mono, kira-kira -16 LUFS. |
| masuk-pintu.mp3 | 1.25 s | Pintu terbuka + loceng kilau, mono, kira-kira -16 LUFS. |

Tiada `bingkai.png`: pintu dijana tanpa bingkai/dinding; dua daun rapat membentuk satu gerbang lengkung (502x700). Luar bentuk gerbang adalah telus, jadi awan kelihatan di sekeliling pintu.

## Susunan pintu

- Letak dua daun bersebelahan TANPA jarak (kiri kemudian kanan), sama tinggi; nisbah gabungan 502:700.
- Cadangan saiz: tinggi kira-kira 80vh (potret: lebar maksimum 92vw), di tengah skrin.
- Titik engsel (tepi luar setiap daun):
  - pintu-kiri: `transform-origin: 0% 50%` (x=0), buka dengan `rotateY(-105deg)`
  - pintu-kanan: `transform-origin: 100% 50%` (x=251), buka dengan `rotateY(105deg)`
- Bekas induk: `perspective: 1200px`; setiap daun `backface-visibility: hidden` tidak perlu (pudar sebelum 90 darjah lebih kemas).

## Cadangan urutan masa (jumlah kira-kira 2.9 s)

1. 0-1.4 s: nuri-kapal terbang dari luar kiri ke luar kanan skrin (translateX -30vw ke 130vw), naik turun sedikit (translateY +-12px, 2 kitaran), condong -4deg. Mainkan `masuk-terbang.mp3` pada 0 s.
2. 1.2-1.6 s: lapisan awan + pintu tertutup pudar masuk/meluncur naik menutup skrin (awan di belakang, pintu di depan).
3. 1.6-2.6 s: dua daun berpusing terbuka (rotateY, ease-in-out). Mainkan `masuk-pintu.mp3` pada 1.6 s. Awan kelihatan melalui bukaan.
4. 2.6-2.9 s: pudar ke Kelas Al-Quran.

Hormati `prefers-reduced-motion`: langkau terus ke langkah 4. Jika bunyi app dimatikan, jangan mainkan mp3.
