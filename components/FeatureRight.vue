<template>
  <div class="flex flex-wrap">
    <div class=" w-1/2 p-10 ">
      <h3 class="text-3xl text-gray-800 font-semibold mb-6 ">
        {{ headline }}
      </h3>
      <p class="text-gray-600 text-xl  mb-8">
        {{ content }}
        <br />
       
      </p>
    </div>
    <div class="w-full sm:w-1/2 p-6">
      <slot name="svg" />
    </div>
  </div>
</template>

<script>
export default {
  name: 'FeatureRight',
  props: {
    headline: {
      type: String,
      required: false
    },
    content: {
      type: String,
      required: false
    }
  }
}
</script>
