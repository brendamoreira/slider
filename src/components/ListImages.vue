<template>
    <ul>
        <li>
            <img v-for="(photo, index) in photos" :src="photo" :key="index"/>
        </li>
    </ul>
</template>
<script>
export default {
    props: ['photos']
}
</script>
<style scoped>
li {
    width: 300px;
    padding: 10px;
}
 img {
     width: 280px;
 }
</style>