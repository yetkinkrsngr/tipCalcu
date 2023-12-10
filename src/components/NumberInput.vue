<template>
  <label>
    {{ title }}
    <img src="@/assets/img/icon-dollar.svg" />
    <input type="text" name="bill" class="upper-margin-sm" v-model="value" />
  </label>
</template>

<script>
export default {
  data() {
    return {
      value: this.billNumber
    }
  },
  props: ['title', 'billNumber'],
  watch: {
    value(newValue) {
      this.$emit('change-bill-value', newValue)
    }
  }
}
</script>

<style>
label {
  display: flex;
  flex-direction: column;
  color: var(--neutral-2);
  font-size: var(--font-desc);
  font-weight: var(--font-weight);
  position: relative;
}

label img {
  position: absolute;
  height: var(--font-input);
  bottom: 16px;
  left: 16px;
}

input[type='text'] {
  font-size: var(--font-input);
  padding: var(--input-padding);
  border-radius: var(--input-radius);
  border: var(--input-border-size) solid transparent;
  outline: none;
  background-color: var(--neutral-5);
  transition: var(--main-transition);
  text-align: right;
  color: var(--neutral-1);
  font-weight: var(--font-weight);
}

input[type='text']:focus {
  border: var(--input-border-size) solid var(--primary);
  transition: var(--main-transition);
}
</style>
