<template>
  <nav  class="fixed w-full z-30 top-0 bg-white py-2">
    <div
      class="w-full container mx-auto flex flex-wrap items-center justify-between mt-0 py-2"
    >


      <div
        class="w-full flex-grow lg:flex lg:items-center lg:w-auto  mt-2 lg:mt-0  text-black p-4 lg:p-0 z-20"
      >
        <ul class="list-reset lg:flex justify-start flex-1 items-center">
          <li class="mr-3">
            <a
              class="inline-block py-2 px-4 text-xl text-gray-800   no-underline"
              href="#"
              >What's different</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block text-xl text-gray-800 no-underline hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#"
              >Resources</a
            >
          </li>
          <li class="mr-3">
            <a
              class="inline-block text-xl text-gray-800 no-underline hover:text-gray-800 hover:text-underline py-2 px-4"
              href="#"
              >Products</a
            >
          </li>
        </ul>
        <button
          class="mx-auto lg:mx-0 text-blue-600  hover:underline font-bold border-none mt-4 lg:mt-0 py-4 px-8 "
        >
          Sign in
        </button>
           <button
          class="mx-auto lg:mx-0 text-blue-600 bg-blue-100 hover:underline font-bold rounded-full mt-4 lg:mt-0 py-4 px-8 shadow opacity-75"
        >
          Get early access
        </button>
      </div>
    </div>
    <hr class="border-b border-gray-100 opacity-25 my-0 py-0" />
  </nav>
</template>

<script>
import Logo from '@/components/Logo'

export default {
  name: 'TheHeader',
  components: {
    logo: Logo
  },
  data() {
    return {
      scrollY: 0,
      isOpen: false
    }
  },
  computed: {
    isSticky() {
      return this.scrollY > 10
    },
    headerClassList() {
      return this.isSticky ? 'bg-white shadow' : ''
    },
    navActionClassList() {
      return this.isSticky ? 'gradient text-white' : 'bg-white text-gray-800'
    },
    navContentClassList() {
      let classList = this.isSticky ? 'bg-white' : 'bg-gray-100'
      if (!this.isOpen) {
        classList += ` hidden`
      }
      return classList
    }
  },
  methods: {
    onClick() {
      this.isOpen = false
    },
    onScroll() {
      this.scrollY = window.scrollY
    },
    onToggleClick() {
      this.isOpen = !this.isOpen
    }
  },
  mounted() {
    this.scrollY = window.scrollY
    document.addEventListener('click', this.onClick)
    document.addEventListener('scroll', this.onScroll)
  },
  beforeDestroy() {
    document.removeEventListener('click', this.onClick, true)
    document.removeEventListener('scroll', this.onScroll, true)
  }
}
</script>
