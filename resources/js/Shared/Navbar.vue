<script setup>
import { computed } from 'vue';
import { Link } from '@inertiajs/vue3';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faEnvelope } from '@fortawesome/free-solid-svg-icons'

// const props = defineProps({
//     href: String,
//     active: Boolean,
// });

// const classes = computed(() => {
//     return props.active
//         ? 'inline-flex items-center px-1 pt-1 border-b-2 border-indigo-400 text-sm font-medium leading-5 text-gray-900 focus:outline-none focus:border-indigo-700 transition duration-150 ease-in-out'
//         : 'inline-flex items-center px-1 pt-1 border-b-2 border-transparent text-sm font-medium leading-5 text-gray-500 hover:text-gray-700 hover:border-gray-300 focus:outline-none focus:text-gray-700 focus:border-gray-300 transition duration-150 ease-in-out';
// });
</script>

<script>
export default {
  name: 'Welcome',

  data() {
    return {
      scrollingUp: false,
      scrollingDown: false,
      prevScrollpos: window.pageYOffset,
    };
  },

  computed: {
    getMainNavClasses() {
      return {
        'scroll-up': this.scrollingUp,
        'scroll-down': this.scrollingDown,
      };
    },
  },

  methods: {
    scrollNow() {
      const currentScrollPos = window.pageYOffset;
      console.log(currentScrollPos);

      if (currentScrollPos == 0) {
        this.scrollingUp = false;
        this.scrollingDown = false;
        return;
      }

      if (currentScrollPos < 100) return; // set offset here

      if (this.prevScrollpos > currentScrollPos) {
        // up
        this.scrollingDown = false;
        this.scrollingUp = true;
      } else {
        // down
        this.scrollingUp = false;
        this.scrollingDown = true;
      }

      this.prevScrollpos = currentScrollPos;
    },

    handleScroll() {
      let doScoll;

      window.onscroll = () => {
        clearTimeout(doScoll);
        doScoll = setTimeout(this.scrollNow, 0); // firing less scroll events
      };
    },
  },

  created() {
    this.handleScroll();
  },
};
</script>

<template>
    <div class="relative max-w-[1200px] mx-auto">
        <div :class="{'bg-white': scrollingDown, '': !scrollingDown}" class="right-0 fixed flex justify-center items-center bg-transparent w-full h-[100px] z-50 duration-500 ease-in">
            <!-- <div class="fixed top-0 bg-transparent w-full h-[100px] z-50 duration-150"> -->
                <div class="flex justify-between items-center h-full w-full max-w-[1200px]">
                    <div class="">
                        <p class="text-3xl font-medium text-light-black">Product</p>
                    </div>
                    <div class="flex gap-10 text-lg text-light-black">
                        <p>Home</p>
                        <p>Producs</p>
                        <p>Contact Us</p>
                  
                    </div>
                    <div class="flex gap-5 text-light-black">
                        <Link :href="route('login')" class="text-lg">
                            <p>Login</p>
                        </Link>
                        <div class="text-2xl">
                            <font-awesome-icon :icon="['fas', 'heart']" />
                        </div>
                        <div class="text-2xl">
                            <font-awesome-icon :icon="['fas', 'bag-shopping']" />
                        </div>
                    </div>
                </div>
            </div>
    </div>

</template>
