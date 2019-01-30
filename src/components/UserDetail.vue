<template>
  <div class="component">
    <h3>You may view the User Details here</h3>
    <p>Many Details</p>
    <p>User name: {{ switchName() }}</p>
    <p>User age: {{ userAge }}</p>
    <button @click="resetName()">Reset Naam</button>
    <button @click="resetFn()">Reset Naam</button>
  </div>
</template>

<script>
  import { eventBus } from '../main';

  export default {
    props: {
      myName: {
        type: String
        // required: true,
        // default: 'Til'
      },
      resetFn: Function,
      userAge: Number
    },
    methods: {
      switchName() {
        return this.myName.split("").reverse().join("");
      },
      resetName() {
        this.myName = 'Tilly';
        this.$emit('nameWasReset', this.myName);
      },
      created() {
        eventBus.$on('ageWasEdited', (age) => {
          this.userAge = age;
        });
      }
    }
  }
</script>

<style scoped>
div {
  background-color: lightcoral;
}
</style>
