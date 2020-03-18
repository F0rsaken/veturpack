<template>
  <button 
    type="button" 
    @click="onClick"
  >
    {{ msg }}
  </button>
</template>

<script>
import Vue from 'vue'

export default Vue.extend({
    props: {
        msg: {
            type: String,
            required: true
        },

        innerText: {
            type: String,
            default: ""
        }
    },

    data () {
        return {
            counter: 0
        }
    },

    computed: {
        testComputed () {
            return `Current counter: ${this.counter}`
        }
    },

    methods: {
        onClick () {
            this.$emit("click")
        }        
    },
})
</script>

<style lang="scss">
</style>
