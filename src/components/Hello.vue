<template>
  <div id="hello">
    <transition mode="out-in" name="hello-fade">
      <p
        id="hello-text"
        ref="helloTextP"
        :key="hello"
        class="text-6xl font-bold"
        :class="ruText === true ? 'ru' : ''"
        style="letter-spacing: -0.15rem;"
      >
        {{ hello }}
      </p>
    </transition>
    <p class="text-4xl font-semibold my-6" style="letter-spacing: -0.1rem;">
      I'm Raphael Muli
    </p>
  </div>
</template>

<script>
import { ref, onMounted, computed } from 'vue'

export default {
  name: 'Hello',
  setup: () => {
    const hellos = [
      'Hello',
      'こんにちは',
      'Yo',
      'よー',
      'Привет'
    ]

    const hello = ref(hellos[0])
    const helloTextP = ref(null)

    onMounted(() => {
      setInterval(() => {
        hellos.push(hellos.shift())
        hello.value = hellos[0]
      }, 3500)
    })

    const ruText = computed(() => {
      return hello.value === 'Привет'
    })

    return {
      ruText,
      helloTextP,
      hello
    }
  }
}
</script>
