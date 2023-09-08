<template>
  <div>
    <h1>Hello Vue!</h1>
    <p v-if="showMessage">{{ message }}</p>
    <p v-else>No message to show.</p>
    
    <button @click="toggleMessage">Toggle Message</button>
    
    <div v-show="showDiv">
      This div is shown with v-show.
    </div>
    
    <ul>
      <li v-for="item in items" :key="item.id">{{ item.name }}</li>
    </ul>
    
    <div v-if="showItemsWithVif">
      <p v-for="item in items" :key="item.id">Item: {{ item.name }}</p>
    </div>
    
    <input type="text" v-model="inputValue" />
    <p>You typed: {{ inputValue }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Welcome to Vue.js!',
      showMessage: true,
      showDiv: true,
      items: [
        { id: 1, name: 'Item 1' },
        { id: 2, name: 'Item 2' },
        { id: 3, name: 'Item 3' },
      ],
      showItemsWithVif: true,
      inputValue: '',
    };
  },
  methods: {
    toggleMessage() {
      this.showMessage = !this.showMessage;
    },
  },
};
</script>

<style scoped>
/* Add your component-specific styles here */
</style>
