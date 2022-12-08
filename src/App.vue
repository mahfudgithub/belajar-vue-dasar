<template>
  <h2>Nama : {{ nama }}</h2>
  <button @click="changeName">Ubah Nama</button>
  <div class="row"></div>
  <a v-bind:href="url">go to google</a>
  <div class="row"></div>
  <input type="text" v-model="name" />
  <br />
  {{ name }}
  <div v-if="products.length">
    <ul>
      <li v-for="item in products" :key="item.id">{{ item.title }} - {{ item.price }}</li>
    </ul>
  </div>
  <div v-else>
    <p>Data tidak ditemukan</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      nama: "Myria Camellia",
      url: "https://google.com",
      name: "Myria",
      products: [
        { id: 1, title: "Product 1", price: 2000 },
        { id: 2, title: "Product 2", price: 3000 },
        { id: 3, title: "Product 3", price: 1000 },
      ],
    };
  },
  methods: {
    changeName() {
      this.nama = "Mahfudin";
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
