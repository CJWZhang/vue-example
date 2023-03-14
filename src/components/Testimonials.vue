<script>
import NavBar from './NavBar.vue'
// Should inherit from app. 
export default {
    data() {
        return {
            hotdog: this.hotdog,
        }
    },
    props: {
        hotdog: String
    },
    components: {NavBar},

}
</script>

<template>
  <header>
    <NavBar></NavBar>
    Testimonials 
  </header>
  “i like the hot dog” - a guy said that
</template>

<style scoped>
</style>
