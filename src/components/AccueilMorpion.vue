<template>
  <Push>
    <ReglesMorpion></ReglesMorpion>
  </Push>
  <section id="page-wrap" class=" spaceAround tailleMax">
    <img class="tailleImg" src="../img/morpion.png" alt="">
    <input class="designBoutton texteCenter red clignote" type="button" value="Jouer" @click="morpion">
  </section>

</template>

<script>
import { Push } from 'vue3-burger-menu'
import ReglesMorpion from './ReglesMorpion.vue'

export default {
  name: 'AccueilMorpion',
  components: { ReglesMorpion, Push },
  props: {

  },
  methods: {

    morpion() {
      this.$emit('morpion')
    }

  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.spaceAround {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.tailleImg {
  width: 50vw;
  align-self: center;
}

.clignote {
  color: #f07171;
  text-shadow: 0px 0px 10px #f07171;
  animation: clignote 3s linear infinite;
}

@keyframes clignote {
  50% {
    opacity: 0;
  }
}

@media(min-width: 768px) {
  .tailleImg {
    width: 40vw;
    align-self: center;
  }
}

@media(min-width: 1024px) {
  .tailleImg {
    width: 30vw;
    align-self: center;
  }
}
</style>
