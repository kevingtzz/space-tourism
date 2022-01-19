<template>
  <div>
    <Header />
    <main>
      <Nuxt />
    </main>
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  name: 'LayoutDefault',
  components: { Header },
}
</script>
