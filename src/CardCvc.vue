<template>
  <stripe-element
    ref='element'
    type='cardCvc'
    :stripe='stripe'
    :value='value'
    :options='options'
    @blur='$emit("blur", $event)'
    @focus='$emit("focus", $event)'
    @change='$emit("change", $event)'
  />
</template>

<script>
import props from './props'
import StripeElement from './StripeElement'

export default {
  props,
  components: { StripeElement },
  // methods: {
  //   blur (event) { this.$refs.element.blur(event) },
  //   focus (event) { this.$refs.element.focus(event) },
  //   update (options) { this.$refs.element.update(options) }
  // }
}
</script>
