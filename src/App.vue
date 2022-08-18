<script setup>
import HelloWorld from "./components/HelloWorld.vue"
import TheWelcome from "./components/TheWelcome.vue"
</script>

<script>
export default {
  data: function () {
    return {
      count: 0,
      nama: "Azhamm",
      alamat: "Tegal",
      pekerjaan: "Frontend",
    }
  },

  methods: {
    changeText() {
      this.nama = "Ganti nama"
    },
    tambah() {
      this.count++
    },
    kurang() {
      this.count--
    },
  },
}
</script>

<template>
  <header>
    <img
      alt="Vue logo"
      class="logo"
      src="./assets/logo.svg"
      width="125"
      height="125"
    />

    <div class="wrapper">
      <!-- <HelloWorld msg="You did it!" /> -->
      <h1 v-on:click="changeText">
        {{ nama }}
      </h1>
      <h2>
        {{ alamat }}
      </h2>
      <h3>
        {{ count }}
      </h3>
      <button v-on:click="tambah">Tambah</button>
      <button v-on:click="kurang">Kurang</button>
    </div>
  </header>

  <main>
    <!-- <TheWelcome /> -->
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
