# GIDA Simulator TCO: struktur folder untuk hosting

```
gida_site/
├── gida_simulator_v6.html                    Simulator TCO (tombol Export Excel)
└── templates/
    └── GIDA_Simulator_template.xlsx          Template Excel untuk TCO
```

Folder `templates/` harus berada di sebelah file HTML dan namanya tidak boleh diubah.
Saat tombol Export ditekan, HTML mengambil template dari `templates/`, mengisi sel input
sesuai setelan di layar, lalu mengunduh hasilnya. Seluruh rumus, grafik, dan format sudah ada di template.

## Hosting
- **Netlify:** drag and drop seluruh folder `gida_site` ke Netlify Drop, atau hubungkan ke repo GitHub.
- **GitHub Pages:** push folder ini ke repo, lalu Settings > Pages > pilih branch dan folder.
- Perlu koneksi internet pada saat export (library JSZip dimuat dari cdnjs).

## Dibuka langsung dari komputer (tanpa hosting)
Browser memblokir pengambilan file template. Saat Export ditekan, muncul dialog yang meminta
Anda memilih file template dari folder `templates/`. Pilih file yang sesuai, lalu export berjalan normal.

## Memperbarui template
Template adalah file Excel biasa. Jika rumus atau layout Excel diubah, ganti file di `templates/`
dengan nama yang sama. Sel input yang diisi web dicari lewat nama (defined name, awalan `in`),
jadi jangan menghapus atau mengganti nama sel input tersebut.
