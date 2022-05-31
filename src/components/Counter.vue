<template>
  <div>
    <p>My name is {{ toUpperCase }}</p>
    <p>{{ count }}</p>
    <input type="number" name="value" v-model.number="value"/>
    <button @click="increase(value)">+</button>
    <button @click="decrease(value)">-</button>
  </div>
</template>
<script>
import { mapMutations, mapState } from 'vuex'
export default {
  data () {
    return {
      name: 'Duy',
      value: 0
    }
  },
  computed: {
    toUpperCase: function () {
      return this.name.toUpperCase()
    },
    ...mapState(['count'])
  },
  methods: {
    ...mapMutations(['increase', 'decrease'])
  }
}
</script>
