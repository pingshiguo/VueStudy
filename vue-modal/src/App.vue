<template>
  <div id="app">
    <button type="button" class="btn" @click="showModal">Open Modal</button>
    <modal v-show="isShowModal" @close="closeModal"></modal>
  </div>
</template>

<script>
import Modal from '@/components/Modal'

export default {
  name: 'App',
  data () {
    return {
      isShowModal: false
    }
  },
  components: {
    Modal
  },
  methods: {
    showModal: function () {
      this.isShowModal = true
    },
    closeModal: function () {
      this.isShowModal = false
    }
  }
}
</script>

<style>
.btn {
  display: block;
  margin: 15px auto;
  padding: 10px 15px;
  border: 1px solid rgb(209, 209, 209);
  border-radius: 5px;
}
</style>
