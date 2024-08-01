<template>
    <img :src="url" :alt="title">
</template>

<script>
export default {
    name: 'PictureInfo',
    data() {
        return {
            url: 'https://via.placeholder.com/150',
            title: 'A picture'
        }
    }
}
</script>