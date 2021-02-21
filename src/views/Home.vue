<template>
  <div>
    <h1>Home page</h1>
    <div class="home">
      <Characters />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Characters from '@/components/Characters.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Characters
  }


}
</script>
