<template>
  <h1 id="mensagem">{{ msg }}</h1>
  <router-Link to="/task">Task</router-Link><br>
  <router-Link to="/image">Image</router-Link>
  <router-view v-slot="{Component}">
    <keep-alive>
      <component :is="Component"/>
    </keep-alive>
  </router-view>
</template>

<script>
export default (await import('vue')).defineComponent({
  name: 'App',
  data() {
    return {
      msg: 'Welcome',

    }
  }
})

</script>

<style>
#mensagem{
  color: aqua;
}
</style>
