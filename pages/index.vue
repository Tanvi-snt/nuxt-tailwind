<template>
  <div>
    <hero />
    <features />
    <card/>
    <life/>
  </div>
</template>

<script>
import Hero from '@/components/Hero'
import Features from '@/components/Features'
import Card from '@/components/card'
import Life from '@/components/life'

export default {
  name: 'LandingPage',
  components: {
    hero: Hero,
    features: Features,
    card:Card,
    life:Life
  
  }
}
</script>
