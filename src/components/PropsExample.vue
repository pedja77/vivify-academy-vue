<template>
  <div>
      <div>
      {{ message }}
      </div>
      <div>
      {{ reverseMessage }}
      </div>
      <input type="text" v-model="searchTerm" />
      <button @click="notifyParent">Notify parent</button>
  </div>
</template>

<script>
// Container i prezentacione komponente u vue postoje
export default {
  props: ['message'],
  data() {
      return  {
          searchTerm: ''
      }
  },
  methods: {
      notifyParent() {
          this.$emit('notify-parent', 'Hello from child component');
      }
  },
  computed: {
      reverseMessage() {
          return this.message.split('').reverse().join('');
      }
  },
  watch: {
      searchTerm(newValue, oldValue) {
          console.log('New value ', newValue);
          console.log('Old value ', oldValue);
      }
  }

}
</script>
