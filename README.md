# penulisan-kti

Skill **menulis-kti** untuk Claude. Skill ini dipakai untuk menulis atau merevisi karya tulis ilmiah (KTI) berbahasa Indonesia, seperti makalah, skripsi, tesis, proposal, dan artikel jurnal, agar hasilnya mudah dipahami, terasa seperti tulisan mahasiswa pascasarjana Indonesia, dan tidak terdengar seperti tulisan AI.

Acuan gayanya adalah tesis Muhammad Irfan Habibi (Magister KPI UIN Walisongo, 2025), *Konstruksi Narasi Pesan Dakwah Islam di Instagram pada @akun_salafy*.

## Kapan dipakai

Skill ini cocok saat kamu meminta Claude untuk:

- menulis bagian KTI dari awal, misalnya abstrak, latar belakang, kerangka teori, pembahasan, atau kesimpulan;
- menulis ulang draf yang terasa kaku atau "berbau AI";
- merapikan bahasa makalah, makalah komprehensif, skripsi, atau tesis tanpa mengubah isi, data, dan kutipan;
- merevisi file `.docx` dengan format, catatan kaki, dan gambar tetap utuh.

## Isi aturan

| Bagian | Isi singkat |
|---|---|
| Prinsip dasar | SPOK jelas, satu atau dua gagasan per kalimat, panjang kalimat bervariasi, istilah asing dimiringkan dan langsung dijelaskan. Isi, angka, kutipan, dan catatan kaki tidak boleh berubah. |
| Kosakata khas | Penghubung seperti "Hal ini", "Selain itu", "Sementara itu", "Meski begitu", serta istilah digital Indonesia (unggahan, takarir, warganet). |
| Pola AI yang dihindari | "Pertama, Kedua, Ketiga" berulang, pola "bukan X melainkan Y", triad, kalimat penutup "Artinya, ...", tanda pisah, dan kata seperti "lanskap", "krusial", "menyingkap". |
| Pola per bagian | Panduan untuk abstrak, latar belakang, rumusan masalah dan tujuan, metode, kerangka teori, pembahasan, kesimpulan, dan saran. |
| Penamaan temuan | Nama kategori atau tema memakai frasa Indonesia yang langsung dipahami dan dipakai konsisten dari abstrak sampai kesimpulan. |
| Revisi file .docx | Baca dulu seluruh dokumen, tulis ulang per paragraf lewat XML, validasi, render ke PDF untuk dicek, lalu simpan sebagai revisi berikutnya. |
| Contoh | Perbandingan paragraf yang terasa AI dengan versi gaya Habibi. |

Aturan lengkapnya ada di [`SKILL.md`](SKILL.md).

## Cara memasang

**Claude.ai / aplikasi Claude**

1. Unduh repo ini, lalu masukkan `SKILL.md` ke dalam folder bernama `menulis-kti`.
2. Kompres folder tersebut menjadi `menulis-kti.zip`.
3. Buka **Settings → Capabilities → Skills**, lalu unggah file zip itu.

**Claude Code**

```bash
mkdir -p ~/.claude/skills/menulis-kti
curl -o ~/.claude/skills/menulis-kti/SKILL.md \
  https://raw.githubusercontent.com/ihsnfkrii/penulisan-kti/main/SKILL.md
```

## Cara memakai

Setelah terpasang, cukup minta seperti biasa, misalnya:

- "Tulis ulang latar belakang ini supaya tidak terasa AI."
- "Rapikan bab pembahasan di file tesis saya, catatan kaki jangan diubah."
- "Buatkan abstrak dari ringkasan penelitian ini."

Kamu juga bisa memanggilnya langsung dengan `/menulis-kti`.

## Struktur repo

```
penulisan-kti/
├── README.md
└── SKILL.md
```
