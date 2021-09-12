<template>
  <div id="app">
    <Header :navList="nav" :nomeSaluto="nome"/>
    <Main :products="products"/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data: function(){
    return {
      nome:'boh',
        nav:[
        {
          id:0,
          name:'Home',
          link: '/home'
        },
        {
          id:1,
          name:'Prodotti',
          link: '/product'
        },
        {
          id: 2,
          name: 'Chi Siamo',
          link: '/who-we-are'
        },
        {
          id: 3,
          name: 'Contatti',
          link: '/contacts'
        }
        ],
        products: [
              {
                  "id": 0,
                  "src":"https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg",
                  "titolo":"Spaghetto Quadrato",
                  "tipo": "lunga",
                  "cottura": 13

              },
              {
                  "id": 1,
                  "src":"https://www.lamolisana.it/wp-content/uploads/2021/04/5-fettuccine.jpg",
                  "titolo":"Fettuccine",
                  "tipo": "lunga",
                  "cottura": 13

              },
              {
                  "id": 2,
                  "src":"https://www.lamolisana.it/wp-content/uploads/2021/04/19-mezze-penne-rigate.jpg",
                  "titolo":"Mezze Penne Rigate",
                  "tipo": "corta",
                  "cottura": 11

              },
              {
                  "id": 3,
                  "src":"https://www.lamolisana.it/wp-content/uploads/2021/05/26-gnocchi.jpg",
                  "titolo":"Gnocchi",
                  "tipo": "corta",
                  "cottura": 8

              },
              {
                  "id": 4,
                  "src":"https://www.lamolisana.it/wp-content/uploads/2021/05/108-fusilli-corti-bucati.jpg",
                  "titolo":"Fusilli Corti Bucati",
                  "tipo": "media",
                  "cottura": 7

              },
              {
                  "id": 5,
                  "src":"https://www.lamolisana.it/wp-content/uploads/2021/05/34-succhietti.jpg",
                  "titolo":"Succhietti",
                  "tipo": "media",
                  "cottura": 8

              }
            ]
    }


  }
}
</script>

<style lang="scss">
  @import './style/app.scss'
</style>
