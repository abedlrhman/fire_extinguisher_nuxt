<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <smallCardDisplay
        v-for="cardInfo in smallCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  name: 'IndexPage',
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections,
    }
  },
}
</script>
