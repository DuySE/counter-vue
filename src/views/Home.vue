<template>
  <div class="home">
    <Counter />
  </div>
</template>

<script>
// @ is an alias to /src
import Counter from '@/components/Counter.vue'

export default {
  name: 'Home',
  components: {
    Counter
  }
}
</script>
