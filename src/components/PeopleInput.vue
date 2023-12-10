<template>
  <label :mainKey="mainKey">
    <div class="text-box">
      <p>{{ title }}</p>
      <p class="people-information-alert" v-if="this.value == 0">Can't be zero!</p>
    </div>
    <img src="@/assets/img/icon-person.svg" />
    <input
      type="text"
      name="people"
      class="upper-margin-sm people-input"
      v-model="value"
      :class="{ 'red-border': value == 0 }"
    />
  </label>
</template>

<script>
export default {
  data() {
    return {
      value: this.peopleNumber,
      mainKey: 1
    }
  },
  props: ['title', 'peopleNumber'],
  watch: {
    value(newVal) {
      this.$emit('change-people-value', newVal)
    }
  },
  created() {
    window.addEventListener('resize', () => {
      this.mainKey = this.mainKey + 1 // reload main if there is mobile screen
    })
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

.text-box {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: flex-start;
}

.people-information-alert {
  color: var(--red);
}

.red-border {
  border: var(--input-border-size) solid var(--red) !important;
}

@media only screen and (max-width: 375px) {
}
</style>
