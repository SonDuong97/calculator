<template>
  <div class="container d-flex justify-content-center flex-column p-0 mt-5">
    <display :expression="expression"></display>
    <div class="d-flex flex-wrap">
      <BaseButton v-for="btn in buttons" :key="btn.id" :name="btn" @add-to-expression="expression += $event" @calculate-expression="calculate" @clear-expression="clearExpression"></BaseButton>
    </div>
  </div>
</template>
<script>
import BaseButton from './BaseButton.vue'
import display from './Display.vue'

export default {
  name: 'HelloWorld',
  components: {
    BaseButton,
    display
  },
  data: () => {
    return {
      buttons: [
        '1', '2', '3', '+',
        '4', '5', '6', '-',
        '7', '8', '9', '*',
        '0', 'CE', '/', '='
      ],
      expression: ''
    }
  },
  methods: {
    calculate: function () {
      // eslint-disable-next-line
      this.expression = eval(this.expression);
    },
    clearExpression: function () {
      this.expression = ''
    }
  }
}

</script>
