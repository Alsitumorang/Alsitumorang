- 👋 Horas, saya @Alsitumorang
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Alsitumorang/Alsitumorang is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->



Contoh
Elemen templat menyimpan kode HTML tanpa menampilkannya:

<template>
  <div>Name:
    <slot name="Panggoaran"></slot>
  </div>
  <div>Birthday:
    <slot name="Ultah"></slot>
  </div>
</template>
Definisi dan Penggunaan
Tag <slot> adalah pengganti .....

Konten di dalam tag <template> tidak akan dirender.

Konten dapat dibuat terlihat dan dirender nanti dengan menggunakan JavaScript.

Gunakan tag <template> ketika Anda memiliki kode HTML yang ingin Anda gunakan berulang kali, namun jangan sampai Anda memintanya.

Dukungan Peramban
Element					
<slot>	53.0	79.0	63.0	10.0	40.0
Atribut
Attribute	Value	Description
name	 	Specifies the name of the slot
Atribut Global
Tag <slot> mendukung Atribut Global dalam HTML .

Contoh Lainnya
Contoh
Gunakan JavaScript untuk mendapatkan konten dari template, dan menambahkannya ke halaman:

function showContent() {
  let temp = document.getElementsByTagName("template")[0];
  let clon = temp.content.cloneNode(true);
  document.body.appendChild(clon);
}
Contoh
Gunakan konten templat untuk setiap item dalam array:

<template>
  <div class="myClass">I like: </div>
</template>

<script>
let myArr = ["Audi", "BMW", "Ford", "Honda", "Jaguar", "Nissan"];

function showContent() {
  let temp, item, a, i;
  // Get the template element:
  temp = document.getElementsByTagName("template")[0];
  // Get the DIV element from the template:
  item = temp.content.querySelector("div");
  // For each item in the array:
  for (i = 0; i < myArr.length; i++) {
    // Create a new node, based on the template:
    a = document.importNode(item, true);
    // Add data from the array:
    a.textContent += myArr[i];
    // Append the new node wherever you like:
    document.body.appendChild(a);
  }
}
</script>