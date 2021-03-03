<template>

<div :key="data.choice" v-for="data in db">
  <div class="container">
  <div v-if="data.show">
  <div class="center">  
    <div class="card mx-auto my-5" style="width: 25rem;">
      <div class="card-body">
      <h5 class="card-title p-3 mb-3" >{{data.title}}</h5>
    <!-- <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6> -->
    <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p> -->
      <button v-if="!data.final" @click="yesBtn(data.choice)" class="btn btn-primary m-3 px-4">{{data.btnY}}</button>
      <button v-if="!data.final" @click="noBtn(data.choice)" class="btn btn-primary m-3 px-4">{{data.btnN}}</button>
      <i v-if="data.final" @click="reset" class="fas fa-undo-alt text-primary"></i>
      </div>
    </div>
  </div>
</div>
</div>
</div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    // questions: Array,
    // title: String,
    db: Array,
    // btnY: String,
    // btnN: String,
  },
  data() {
    return{
     
   }
  },
  methods: {
    yesBtn(choice) {
      this.$emit('yes', choice)
      // console.log(choice);
    },
    noBtn(choice) {
      this.$emit('no', choice)
      // console.log(choice);
    },
    reset() {
      this.$emit('reset')
    }
  },
  emits: ['yes', 'no', 'reset']
}
</script>

<style scoped>
/* .centered {
  display: flex;
  margin-top: 10rem !important;
} */
i {
  font-size: 2rem;
  cursor: pointer;
  
}
.container {
  max-width: 100%;
}

</style>