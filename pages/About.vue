<template>
  <section class="container">
    <my-header/>
      <div>
        <h1 class="title">
          About
        </h1>
      </div>
    <my-footer/>
  </section>
</template>

<script>
import MyHeader from '~/components/MyHeader.vue'
import MyFooter from '~/components/MyFooter.vue'

export default {
  components: {
    MyHeader,
    MyFooter
  }
}
</script>


<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>