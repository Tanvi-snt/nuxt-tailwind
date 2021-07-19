<template>
  <section class="bg-white py-28">
    <div class="container max-w-7xl mx-auto ">
      <h1
        class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-800"
      >
        All you need is in one place
      </h1>
      <p class="text-gray-500 text-xl text-center
      ">Everything you need is now on a single platform built from scratch.</p>
      <div class="w-full mb-4">
      
      </div>
      <feature-right
        headline="Your new home screen that manages half of your work."
        content="Replace multiple tools, fragmented and unsecure workflows with first complete lifecycle platform for all your documents."
      >
        <img src="~assets/img/travel-booking.svg?inline" alt slot="svg" />
      </feature-right>
      <feature-left
        headline="Powerful & dynamic documents  and contacts every-time."
        content="Replace multiple tools, fragmented and unsecure workflows with first complete lifecycle platform for all your documents and contracts."
      >
        <img src="~assets/img/connected-world.svg?inline" alt slot="svg" />
      </feature-left>
        <feature-right
        headline="Real time, internally, externally and for the first time- contextually."
        content="Replace multiple tools, fragmented and unsecure workflows with first complete lifecycle platform for all your documents and contracts."
      >
        <img src="~assets/img/travel-booking.svg?inline" alt slot="svg" />
      </feature-right>
        <feature-left
        headline="Your documents, your platforms. You decide how it works!"
        content="Replace multiple tools, fragmented and unsecure workflows with first complete lifecycle platform for all your documents and contracts."
      >
        <img src="~assets/img/connected-world.svg?inline" alt slot="svg" />
      </feature-left>
          <feature-right
        headline="Close fast with legally binding native eSignature"
        content="Replace multiple tools, fragmented and unsecure workflows with first complete lifecycle platform for all your documents and contracts."
      >
        <img src="~assets/img/travel-booking.svg?inline" alt slot="svg" />
      </feature-right>
            <feature-left
        headline="Manage better decisions and manage risks with insights you never had."
        content="Replace multiple tools, fragmented and unsecure workflows with first complete lifecycle platform for all your documents and contracts."
      >
        <img src="~assets/img/connected-world.svg?inline" alt slot="svg" />
      </feature-left>
    </div>

    <div class=" bg-pink-50  mx-auto container py-24 rounded-lg mt-32">
      <h1 class="text-black text-4xl font-bold text-center mx-auto pb-14  w-98">Since we're both serious about your work, let's make it official</h1>
      <button class="bg-blue-500 text-center text-white py-4 px-24 rounded-full mx-auto block">Get early access</button>
    </div>
  </section>
</template>

<script>
import FeatureRight from '@/components/FeatureRight'
import FeatureLeft from '@/components/FeatureLeft'

export default {
  name: 'Features',
  components: {
    'feature-right': FeatureRight,
    'feature-left': FeatureLeft
  }
}
</script>
