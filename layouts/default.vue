<template>
  <div class="content-wrapper">
    <Header />
    <Nuxt />
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  name: 'LayoutDefault',
  components: { Header },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Barlow+Condensed&family=Bellefair&display=swap');

:root {
  --black: #0b0d17;
  --white: #fff;
  --light-blue: #d0d6f9;
}

* {
  margin: 0;
  padding: 0;
}

p {
  color: var(--light-blue);
  font-family: Barlow, sans-serif;
  font-style: normal;
  font-weight: normal;
}

h1,
h2,
h3,
h4 {
  font-family: Bellefair, serif;
  font-style: normal;
  font-weight: normal;
  color: var(--white);
}

span {
  font-family: 'Barlow Condensed', sans-serif;
  font-style: normal;
  font-weight: normal;
  color: var(--light-blue);
}

.content-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: var(--black);
  height: 100%;
}
</style>