<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <!-- <router-link to="/siswa">Data Siswa</router-link>
    <router-link to="/kelas">Data Kelas</router-link>
    <router-view/> --> <!-- update data yg di klik -->
    <h1>{{ nama }}</h1>
    <h2>Nama: <input v-model="nama"><br></h2>
    <h2>Nilai Anda:&nbsp{{ nilai }}</h2>
    <button @click="totalnilai">Kirim </button>  
    <h2>1. Apa nama burung endemik pulau Papua ?</h2>
    <input type="radio" v-model="soal1" value="Cendrawasih">Cendrawasih &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Jalak Bali">Jalak Bali &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Cucak Ijo">Cucak Ijo &nbsp&nbsp
    <input type="radio" v-model="soal1" value="Elang Jawa">Elang Jawa &nbsp&nbsp<br>
    <h2>2. Apa nama rumah adat Jawa Barat ?</h2>
    <input type="radio" v-model="soal2" value="Betang">Betang &nbsp&nbsp
    <input type="radio" v-model="soal2" value="Jolopong">Jolopong &nbsp&nbsp
    <input type="radio" v-model="soal2" value="Honai">Honai &nbsp&nbsp
    <input type="radio" v-model="soal2" value="Gapura Candi Bentar">Gapura Candi Bentar &nbsp&nbsp<br>
    <h2>3. Yang bukan merupakan aplikasi untuk Coding adalah ?</h2>
    <input type="radio" v-model="soal3" value="Netbeans IDE">Netbeans IDE &nbsp&nbsp
    <input type="radio" v-model="soal3" value="Notepad++">Notepad++ &nbsp&nbsp
    <input type="radio" v-model="soal3" value="PUBG">PUBG &nbsp&nbsp
    <input type="radio" v-model="soal3" value="Sublime">Sublime &nbsp&nbsp<br>
  </div>
</template>

<script>
/*import HelloWorld from './components/HelloWorld.vue'*/

export default {
  name: 'app',
  data() {
    return{
      nama: '',
      nilai: 0,
      soal1: '',
      soal2: '',
      soal3: ''
      /*components: {
        HelloWorld
      }*/
    }
  },
methods: {
  totalnilai(){
    if (this.soal1 == 'Cendrawasih' && this.soal2 == 'Jolopong' && this.soal3 == 'PUBG') {
      this.nilai=+3    
    }
    else if (this.soal1 == 'Cendrawasih' && this.soal2 == 'Jolopong') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Cendrawasih' && this.soal3 == 'PUBG') {
      this.nilai=+2 
    }
    else if (this.soal2 == 'Jolopong' && this.soal3 == 'PUBG') {
      this.nilai=+2 
    }
    else if (this.soal1 == 'Cendrawasih') {
      this.nilai=+1 
    }
    else if (this.soal2 == 'Jolopong') {
      this.nilai=+1 
    }
    else if (this.soal3 == 'PUBG') {
      this.nilai=+1 
    }
    else {
      this.nilai = 0 
    }
  }
}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
