<template>
  <button type="button" class="btn btn-secondary" v-on:click="triggerClickEvent">{{name}}</button>
</template>
<script type="text/javascript">
export default {
  props: ['name'],
  methods: {
    triggerClickEvent: function () {
      if (this.name === '=') {
        this.$emit('calculate-expression')
      } else if (this.name === 'CE') {
        this.$emit('clear-expression')
      } else {
        this.$emit('add-to-expression', this.name)
      }
    }
  }
}

</script>
