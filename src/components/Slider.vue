<template>
    <div>
        <img :src="photos[index]"/>
    </div>
</template>
<script>
export default {
    props: ['photos', 'index']
}
</script>
<style scoped>

</style>