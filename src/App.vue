<template>
  <!--  <img alt="Vue logo" src="./assets/logo.png">-->
  <h1>{{ title }}</h1>
  <p> Welcome ...</p>
  <div v-if="showModal">
    <!--        @close ("close") pt ca am folosit $emit-->
    <Modal theme="sale" @close="toggleModal">
      <template v-slot:links>
      <a href="">test </a>
      <a href="">test1</a>
      </template>
      <h1>some shit</h1>
      <p>other shit</p>
    </Modal>
    >
  </div>
  <button @click.once="toggleModal">open modal</button>

</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  data() {
    return {
      title: 'My First Vue App!',
      showModal: false,
      // showModalTwo: false,
      text: "some shit",
      header: "other shit"
    }
  },
  components: {
    Modal
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
