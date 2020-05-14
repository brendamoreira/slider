<template>
    <ul>
        <li v-for="(photo, index) in photos" :key="index">
            <img :src="photo" @click="$emit('select', index)"/>
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
    list-style: none;
}
 img {
     width: 280px;
 }

</style>