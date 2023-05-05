<template>
    <div>
        <h2>About</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque interdum consectetur vulputate. Nam sit amet accumsan libero. Pellentesque vulputate tortor magna, vitae dignissim augue sodales sed. Proin libero nisl, dictum sed nulla sit amet, dignissim dignissim sapien. Integer convallis vehicula leo. Mauris ultricies finibus nibh, rutrum posuere justo. Quisque aliquet feugiat enim, ac aliquam ante mollis at. Praesent libero ligula, imperdiet vitae blandit a, pellentesque sit amet nibh. Nunc turpis libero, dapibus a libero ac, consequat ultricies enim. Curabitur sed ligula risus. Vivamus a eros vitae dolor placerat facilisis. Maecenas commodo consectetur tortor nec rutrum. Curabitur sed feugiat magna. Vivamus laoreet velit quis aliquet aliquet. Sed lacus diam, ultricies a ante et, fringilla vulputate odio.</p>
    </div>
    <div>{{ data }}</div>
</template>

<script setup>

    // const { data } = await useFetch('/api/ninja?name=mario', {
    //     method: 'post',
    //     body: {age:30}
    // })

    const { data } = await useFetch('/api/currency/GBP')
    
</script>

<style scoped>

h2{
    margin-bottom : 20px;
font-size   :36px;
}
p{
    margin: 20px 0;
}
</style>