<template>
  <label>
    <input
      type="radio"
      :name="groupName"
      :value="radioButtonValue"
      class="visually-hidden"
      @change="$emit('change', radioButtonValue)"
    />
    <slot></slot>
  </label>
</template>
<script>
export default {
  name: "RadioButton",
  props: {
    groupName: {
      required: true,
      type: String,
    },
    radioButtonValue: {
      required: true,
      type: String,
    },
  },
};
</script>
