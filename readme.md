# Vue Intro

## What is [Vue.js?](https://vuejs.org/guide/introduction.html)

Berdasarkan dokumentasi, kita bisa tau bahwa Vue adalah sebuah framework javascript untuk membuat user interfaces. Pada dasarnya, Vue dibangun di atas HTML, CSS, dan JavaScript, dan juga memberikan model pemrograman deklaratif berbasis komponen yang membantu kamu untuk mengembangkan  dengan lebih efisien, baik yang sederhana maupun yang kompleks.

Ingat yah penekanannya di sini adalah sebuah Framework Ya, bukan library.

**Apa perbedaan antara library & framework?**

TL;DR: Framework memiliki magic yang lebih banyak dibanding library.

Secara garis besarnya, Framework memiliki fitur yang wah dibandingkan dengan library, tetapi memiliki aturannya tersendiri, tidak seperti library yang menggunakan aturan umum javascript.

## Why use Vue.js?
1. Mudah dipelajari
2. Dokumentasi yang Lebih Jelas
3. Struktur yang Lebih Terorganisir, menggunakan `Single File Component` (SFC) untuk memisahkan antara HTML, CSS, dan JavaScript dalam satu file
4. Pendekatan "Progressive Framework", Vue bisa diintegrasikan secara bertahap ke dalam proyek yang sudah ada
5. Performance, Vue termasuk framework ringan

## [API Styles](https://vuejs.org/guide/introduction.html#api-styles)

Komponen Vue bisa ditulis dengan dua gaya API yang berbeda: **Options API** dan **Composition API.**

**Bedanya apa?** 

- **Options API** lebih cocok untuk aplikasi kecil, newbie friendly.

- **Composition API** lebih ideal untuk aplikasi kompleks, fitur lebih modern, dan secara performance lebih oke.

## Demo (Options API)

[**Setup**](https://vuejs.org/guide/quick-start.html)

1. Install extension [Vue.volar](https://marketplace.visualstudio.com/items/?itemName=Vue.volar) agar kita bisa menggunakan fitur Vue di VSCode
2. `npm create vue@latest`
3. Masukkan `<nama_folder>`
4. Pilih `ESLint`
5. Pilih `Prettier`
6. `cd <nama_folder>`
7. `npm install`
8. `npm run dev`
9. Ganti Title dan Jika menggunakan Framework CSS dengan CDN , tambahkan script yang dibutuhkan di `index.html`
10. Hapus folder components
11. Hapus seluruh file yang ada dalam folder `src/assets` kecuali main.css (akan menjadi file css utama kita) 
12. Hapus seluruh code yang ada di dalam `src/App.vue`
13. Copy isi dari body yang ada di template (template.html) ke src/App.jsx 

**Part 1 ([Reactivity](https://vuejs.org/guide/essentials/reactivity-fundamentals.html) , [Form input biding](https://vuejs.org/guide/essentials/forms.html)  & [Event Handling](https://vuejs.org/guide/essentials/event-handling.html))**

1. Pada part ini kita akan mensimulasikan form login simple menggunakan Vue.js
2. Buatlah reactive state untuk email dan password
3. Gunakan `v-model` untuk mengikat inputan email dan password ke reactive state yang sudah kita buat sebelumnya
4. Tampilkan reactive data email & password di html menggunakan `{{}}`
5. Buatlah sebuah function `login` yang berisikan console.log email & password untuk menangani event submit form, dan gunakan `@submit.prevent` pada form kita untuk mencegah reload halaman

**Part 2 ([List Rendering](https://vuejs.org/guide/essentials/list.html))** 

1. Pada part ini kita akan menampilkan list data menggunakan Vue.js
2. Buatlah reactive state `products` yang berisikan array of object dari `data.json` yang sudah disiapkan
3. Gunakan `v-for` untuk menampilkan list data dari reactive state `products` ke dalam html
4. Gunakan ternary untuk menghandle tampilan description produk yang terlalu panjang.

**Part 3 ([Conditional Rendering](https://vuejs.org/guide/essentials/conditional.html))**

1. Pada part ini kita akan menggunakan conditional rendering untuk menampilkan halaman login dan halaman produk secara terpisah
2. Buatlah reactive state `isLogin` yang berisikan boolean untuk menandakan apakah user sudah login atau belum
3. Gunakan `v-if` untuk menampilkan halaman login jika `isLogin` bernilai false, dan menampilkan halaman produk jika `isLogin` bernilai true
4. tambahkan codingan di function `login` untuk mengubah nilai `isLogin` menjadi true jika login berhasil
5. Buatlah function `logout` untuk mengubah nilai `isLogin` menjadi false jika user logout
6. Gunakan `@click` untuk menangani event logout pada button logout
