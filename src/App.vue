<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import WidgetCall from '@/components/WidgetCall.vue'
import Form from '@/components/Form.vue'
</script>

<template>
  <Header/>
  <main>
    <RouterView />
  </main>
  <Footer/>
  <WidgetCall/>
  <Form/>
</template>

<style>
@import '@/assets/css/base.css';

</style>

<script>
export default {
  props: ['isShow'],
  methods: {
    toggleForm() {
      console.log(21212)
      event.preventDefault()
      this.isShow = !this.isShow
      console.log(this.isShow)
    }
  }
}
</script>
