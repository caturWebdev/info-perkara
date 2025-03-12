# info-perkara
API Info perkara scrap dari sipp
=======

# API UNOFFICIAL INFO PENGADILAN dengan LIBRARY info_pengadilan

## info perkara seluruh indonesia (respon JSON)
- Pengadilan Negeri (infoperkara, tilang, jadwal sidang)
- Pengadilan Agama  (infoperkara, jadwal sidang)
- PTUN (infoperkara, jadwal sidang)
- MILITER (*not yet)
  
## Info Lain (respon format RSS dan JSON) :
- Mutasi Hakim (Badilum)
- Mutasi Panitera (Badilum)
- Surat Dinas (Badilum)
- Pengumuman MA (MA)
- Direktori Putusan(MA)

<h1 align="center">
 <img src="https://raw.githubusercontent.com/catursawahlunto/catursawahlunto/main/my-name.svg"/>
</h1>


## KEAMANAN

Librari ini menggunakan metode "web data scraping" kemudian data di ekstrak untuk di kelola dalam bentuk JSON data. Sehingga kecepatan respon data itu tergantung dari website sipp kota tujuan.

## Sample Demo

Clone this project

```bash
  git clone https://github.com/catursawahlunto/info_perkara_indonesia
```

Go to the project directory

```bash
  cd info_perkara_indonesia
```

Install dependencies

```bash
  npm i atau pnpm install atau yarn 
```

Run Demo

```bash
  node index.js atau npm run start
```


## Cara Menggunakan

lihat file index.js
atau lihat dibawah ini


## Usage/Examples

```nodeJS

const  infoPengadilan= require('./lib/info_perkara.js')
const fungsinya = new infoPengadilan(); //variabel fungsinya bisa diganti apa saja

const cari_perkara = async (pengadilan, search) => {
    const hasil = await fungsinya.infoPerkara(pengadilan, search)
    console.log(hasil)
}

const cari_tilang = async (pengadilan, search) => {
    const hasil = await fungsinya.infoTilang(pengadilan, search)
    console.log(hasil)
}
const jadwal_sidang_hariini = async (pengadilan, tanggal) => {
    const hasil = await fungsinya.infoSidang(pengadilan, tanggal)
    console.log(hasil)
}

cari_perkara("pa-balikpapan", "21/Pdt.G/2023");
cari_tilang("pn-padang", "Ade Rahman")
jadwal_sidang_hariini("pn-padang", "01/08/2023")
```


## Authors

- [@caturAdiSukrisno](https://github.com/catursawahlunto)

## DONATE 
dana : 082133381777
![Logo](https://raw.githubusercontent.com/catursawahlunto/catursawahlunto/main/donate-dana.png)


## License

[MIT](https://choosealicense.com/licenses/mit/)
>>>>>>> 03e2c9d (first commit)
