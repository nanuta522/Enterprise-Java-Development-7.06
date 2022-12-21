<template>
  <header>
    <Navbar />
  </header>

  <main>
    <MathOperation :numbers="numbers" />

    <ImageComponent />

    <div class="container mt-5">
      <div class="row g-3">
        <div class="col-auto">
          <label for="inputOperation" class="col-form-label"><strong>Iteration 4</strong></label>
        </div>

        <CardComponent v-for="(card, idx) in cards" :card="card" :key="idx" />
      </div>
    </div>

    <BonusComponent />
  </main>

  <footer>
    <FooterComponent />
  </footer>
</template>

<script>
import Navbar from './components/NavBar.vue'
import FooterComponent from './components/FooterComponent.vue'
import MathOperation from './components/MathOperation.vue'
import ImageComponent from './components/ImageComponent.vue'
import CardComponent from './components/CardComponent.vue'
import BonusComponent from './components/BonusComponent.vue'

export default {
  data() {
    return {
      numbers: [5, 5, 2],
      cards: [{
        title: 'Title 1',
        description: 'Lorem, ipsum.',
        content: 'Lorem ipsum dolor sit amet.'
      },
      {
        title: 'Title 2',
        description: 'Quas, fugiat.',
        content: 'Veritatis perferendis omnis exercitationem explicabo!'
      },
      {
        title: 'Title 3',
        description: 'Assumenda, dolorum.',
        content: 'Modi incidunt neque nostrum pariatur.'
      }]
    }
  },
  components: {
    Navbar,
    FooterComponent,
    MathOperation,
    ImageComponent,
    CardComponent,
    BonusComponent
  }
}
</script>

<style>

</style>
