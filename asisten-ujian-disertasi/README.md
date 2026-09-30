# Asisten Ujian Tutup Disertasi

Aplikasi web satu file (`index.html`) untuk mendampingi promovendus menjawab pertanyaan dewan penguji.

## Cara pakai
1. Buka `index.html` di **Google Chrome / Microsoft Edge**. Agar mikrofon diizinkan, jalankan dari localhost:
   `cd asisten-ujian-disertasi && python3 -m http.server 8000` lalu buka `http://localhost:8000`.
2. Unggah disertasi (PDF disarankan agar nomor halaman terbaca; DOCX/TXT juga bisa).
3. Isi kunci API Anthropic (console.anthropic.com) dan pilih model.
4. Tekan 🎙️. Sistem mendengar penguji; setelah hening ±3 detik, jawaban 2–3 menit tersusun otomatis.

## Yang ditampilkan
- **Jawaban siap ucap**: Inti jawaban → Penjelasan → Penguatan argumen → Penutup → Lokasi di disertasi.
- **Kutipan [S#]**: klik untuk melihat potongan disertasi (bab/subbab/halaman).
- **Blok kuning ➕**: argumen tambahan yang *tidak* tertulis di disertasi (penguat/argumentasi).
- **Prediksi pertanyaan penguji** dari peta disertasi, riwayat tanya-jawab, opsi bacakan jawaban.

## Catatan
- File diproses di browser; hanya ±10 potongan relevan yang dikirim ke API saat menjawab.
- Tanpa kunci API / internet, aplikasi tetap menampilkan potongan disertasi paling relevan.
- Sistem dilarang mengarang referensi eksternal; bila perlu ditandai "(perlu verifikasi)".
- Pastikan penggunaan alat bantu ini diizinkan oleh aturan ujian di institusi Anda.
