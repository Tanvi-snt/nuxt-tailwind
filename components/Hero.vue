<template>
  <div>
    <hero-content />
    
    
  </div>
</template>

<script>
import HeroContent from '@/components/HeroContent'

export default {
  name: 'Hero',
  components: {
    'hero-content': HeroContent
  }
}
</script>
