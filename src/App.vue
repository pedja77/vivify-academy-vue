<template>
  <div id="app">
    <!-- <ContactsList /> -->
    <!-- <PropsExample :message="message"
    @notify-parent="handleNotifyParent"/> -->
    <router-view />
  </div>
</template>

<script>
// import ContactsList from './components/ContactsList.vue'
// import PropsExample from './components/PropsExample.vue'

export default {
  name: 'app',
  components: {
    // ContactsList,
    // PropsExample
  },
  // data() {
  //   return {
  //     message: 'Hello, World!'
  //   }
  // },
  // created() {
  //   setTimeout(() => {
  //     this.message = 'New message';
  //   }, 3000)
  // },
  // methods: {
  //   handleNotifyParent(message) {
  //     this.message = message;
  //   }
  // }
}
</script>


