<template>
  <div class="max-w-screen-lg p-6 py-10 md:p-20 md:py-24 lg:p-10 lg:py-16" style="margin: 0 auto">
    <LightSwitch />
    <Hello />
    <div class="space-y-8 md:space-y-10 lg:space-x-8 lg:space-y-0 lg:grid lg:grid-cols-2">
      <About />
      <Projects />
    </div>
  </div>
</template>

<script>
import About from './components/About.vue'
import Hello from './components/Hello.vue'
import LightSwitch from './components/LightSwitch.vue'
import Projects from './components/Projects.vue'

export default {
  name: 'App',
  components: {
    About,
    Hello,
    LightSwitch,
    Projects
  }
}
</script>
