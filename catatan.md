## Go Modules
- Mengatur dependency library dalam bahasa pemrograman Go

## Membuat Module
- `go mod init <nama-module>`
- Cth: `go mod init github.com/rasyidev/learn-go-modules`

## Rilis Module
- Go lang terintegrasi baik dengan Git.
- Untuk merilis module, kita hanya perlu membuat tag di git dan push ke repository

## Menginstall Module
- `go get <nama-module>`
- Cth: `go get github.com/rasyidev/learn-go-modules`
- Module yang sudah didownload otomatis akan di simpan pada file `go.mod`

## Upgrade Module
- Context: membuat module
- Buat tag baru, push ke repository

## Upgrade Dependency
- `go get`

## Major Upgrade Module
- Major upgrade digunakan apabila saat kembali ke versi sebelumnya tidak memenuhi backward-compatible
- Hal ini sebaiknya dihindari
- Jika tidak terhindari, lebih baik mengubah nama module
- Cth: github.com/rasyidev/learn-go-modules -> github.com/rasyidev/learn-go-modules/v2
  - **Dari sisi pemilik module**
    - Hapus nama module sebelumnya seperti di atas
    - Buat tag versi baru, push tag
  - **Dari sisi pemakai module**
    - Hapus dependency module lama
    - Jalankan `go get <nama-module-baru>
    - Cth: `go get github.com/rasyidev/learn-go-modules/v2`

