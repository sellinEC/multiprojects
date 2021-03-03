<template>
  <Header />
  <Card @yes="yes" @no="no" @reset="reset" :db="db"/>
</template>

<script>

import Header from './components/Header'
import Card from './components/Card'
export default {
  name: 'App',
  components: {
  Header,
  Card
  },
  data() {
    return {
      db: [],
      count: 0,
  }
  },
  methods: {
    yes(choice) {
      switch (choice) {
       case 'a':
         this.db[0].show = false
         this.db[1].show = true
        break;
        case 'b':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'c':
          this.db[2].show= false
          this.db[4].show = true
        break;
        case 'd':
          this.db[3].show= false
          this.db[5].show = true
        break;
        case 'e':
          this.db[4].show= false
          this.db[9].show = true
        break;
        case 'f':
          this.db[5].show= false
          this.db[6].show = true
        break;
        case 'g':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'h':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'i':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'j':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'k':
          this.db[1].show= false
          this.db[8].show = true
        break;

       default:
         break;
     }
      
      
      
    },
    no(choice) {
      switch (choice) {
       case 'a':
         this.db[0].show = false
         this.db[3].show = true
        break;
        case 'b':
          this.db[1].show= false
          this.db[2].show = true
        break;
        case 'c':
          this.db[2].show= false
          this.db[8].show = true
        break;
        case 'd':
          this.db[3].show= false
          this.db[1].show = true
        break;
        case 'e':
          this.db[4].show= false
          this.db[10].show = true
        break;
        case 'f':
          this.db[5].show= false
          this.db[7].show = true
        break;
        case 'g':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'h':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'i':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'j':
          this.db[1].show= false
          this.db[8].show = true
        break;
        case 'k':
          this.db[1].show= false
          this.db[8].show = true
        break;

       default:
         break;
     }
    },
    reset(){
      this.db.forEach(item => {
        item.show = false
      });
      this.db[0].show = true
    }
  },
  created() {   
    this.db = [
      {id: 1, choice: 'a', title: 'Do you own yourself?', btnY: 'Yes', btnN: 'No', final: false, show: true},
      {id: 2, choice: 'b', title: 'Do you want to initiate violence towards anyone?', btnY: 'Yes', btnN: 'No', final: false, show: false},
      {id: 3, choice: 'c', title: 'Do you think that ALL interactions should be volountary and based on consent?', btnY: 'Yes', btnN: 'No', final: false, show: false},
      {id: 4, choice: 'd', title: 'Someone else has better claim to your body than you do?', btnY: 'Yes', btnN: 'Fine, I own myself', final: false, show: false},
      {id: 5, choice: 'e', title: 'Do you support government?', btnY: 'Yes', btnN: 'No', final: false, show: false},
      {id: 6, choice: 'f', title: 'You are a slave', btnY: "No, I'm not!", btnN: 'I sure am', final: false, show: false},
      {id: 7, choice: 'g', title: 'You have Stockholm Syndrome', btnY: 'string', btnN: 'string', final: true, show: false},
      {id: 8, choice: 'h', title: 'You are a proud slave', btnY: 'string', btnN: 'string', final: true, show: false},
      {id: 9, choice: 'i', title: 'You are a sociopath or a psychopath', btnY: 'YEAH!', btnN: 'BABY!', final: true, show: false},
      {id: 10, choice: 'j', title: 'You are confused', btnY: 'string', btnN: 'string', final: true, show: false},
      {id: 11, choice: 'k', title: 'You are an Anarchist', btnY: 'string', btnN: 'string', final: true, show: false},
    ]
  }
}
</script>

<style>

*{
  margin: 0;
  padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
