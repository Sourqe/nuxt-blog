<template>
  <div>
    <TheHead />
    <main class="main-content">
      <nuxt/>
    </main>
  </div>
</template>

<script>
import TheHead from '@/components/TheHead/TheHead'

export default {
  components: {
    TheHead
  }  
}
</script>


<style>
* {
  box-sizing: border-box;
}

body {
  font-family: "Lato", sans-serif;
}

.main-content {
  margin-top: 4.5rem;
}
</style>
