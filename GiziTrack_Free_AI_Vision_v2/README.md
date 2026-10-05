# GiziTrack — Free AI Vision Edition

Versi ini memakai **Transformers.js + model ONNX Food-101** yang dijalankan langsung di browser. Transformers.js mendukung image classification dan menjalankan model dengan ONNX Runtime di browser, termasuk akselerasi WebGPU. Model `onnx-community/swin-finetuned-food101-ONNX` tersedia khusus untuk Food-101 dan menyediakan varian quantized `model_q4f16.onnx` berukuran sekitar 52.7 MB. citeturn197622search8turn197622search14turn938202search4

## Kelebihan
- Tidak perlu Gemini API key.
- Tidak perlu OpenAI API key.
- Setelah model ter-cache, analisis gambar dapat dijalankan lokal.
- Foto tidak perlu dikirim ke API untuk tahap klasifikasi makanan.
- WebGPU digunakan bila perangkat/browser mendukung, dengan fallback WASM/CPU.

## Batasan penting
Food-101 memiliki 101 kategori makanan. Itu bukan model khusus semua makanan Indonesia. Karena itu GiziTrack menampilkan confidence/prediksi alternatif dan menyediakan koreksi nama, porsi, kalori, protein, karbohidrat, serta lemak sebelum menyimpan. Model Food-101 yang dipakai dilaporkan memperoleh akurasi evaluasi sekitar 92.1% pada dataset Food-101, bukan berarti 92.1% akurat pada foto makanan Indonesia sehari-hari. citeturn938202search5

Angka gizi adalah estimasi awal, bukan pengukuran berat/porsi.

## Cara menjalankan
1. Upload folder ini ke HTTPS hosting seperti Netlify.
2. Buka URL di Chrome Android.
3. Install ke Home Screen.
4. Masuk `Setelan → AI Food Scanner`.
5. Tekan `🚀 Siapkan AI Vision`.
6. Tunggu model selesai diunduh pada pemakaian pertama.
7. Masuk `Scan → Kamera → Analisis makanan`.

## Catatan cache
Model diambil dari Hugging Face saat pertama kali dipakai. Transformers.js secara default meng-cache model di browser, sehingga penggunaan berikutnya dapat lebih cepat. citeturn197622search12

## Instalasi singkat
- Ekstrak ZIP.
- Upload seluruh folder ke hosting HTTPS (Netlify/GitHub Pages/Vercel).
- Buka URL di Chrome Android dan pilih Install app/Tambahkan ke layar utama.
- Masuk Setelan → AI Food Scanner → Siapkan AI Vision.
- Tunggu model selesai diunduh.
- Scan → foto makanan → Analisis makanan.

