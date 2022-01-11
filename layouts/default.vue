<template>
    <div class='content-wrapper'>
        <Header />
        <Nuxt />
    </div>
</template>

<script>
    import Header from '@/components/Header';

    export default {
        name: 'LayoutDefault',
        components: { Header },
    }
</script>

<style>
* {
    margin: 0;
    padding: 0;
}
</style>