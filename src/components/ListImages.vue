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
ul {
    margin: 0;
    padding: 0;
}
li {
    width: 300px;
    list-style: none;
}
 img {
     width: 280px;
     height: 196px;
 }

</style>