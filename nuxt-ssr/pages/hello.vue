<template>
  <div>
    {{ data }}
  </div>
</template>


<script>
  export default {
    async asyncData ({ app }) {
      const data = await app.$axios.$get(`http://127.0.0.1:8000/api`)
      return { data }
    }
  }
</script>
