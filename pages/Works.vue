<template>
  <section class="container">
    <div>
      <my-header/>
      <h1 class="title">
        Works
      </h1>
    </div>
  </section>
</template>

<script>
import MyHeader from '~/components/MyHeader.vue'

export default {
  components: {
    MyHeader
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