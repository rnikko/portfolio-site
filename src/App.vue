<template>
  <div class="max-w-screen-lg p-6 py-10 md:p-20 md:py-24 lg:p-10 lg:py-16" style="margin: 0 auto; min-width: 375px">
    <LightSwitch />
    <Hello />
    <div class="space-y-8 md:space-y-10 lg:space-x-8 lg:space-y-0 lg:grid lg:grid-cols-2">
      <About />
      <Projects />
    </div>
    <Contact class="my-8 md:my-10" />
  </div>
</template>

<script>
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Hello from './components/Hello.vue'
import LightSwitch from './components/LightSwitch.vue'
import Projects from './components/Projects.vue'

export default {
  name: 'App',
  components: {
    About,
    Contact,
    Hello,
    LightSwitch,
    Projects
  }
}
</script>
