<template>
    <div class="header"> {{ header }} </div>
</template>

<script>

export default ({
    name: 'HeaderBar',
    props: {
        header: String
    }
})
</script>


<style scoped>

.header {
    /* height: 200px; */
    font-family: Arial, Helvetica, sans-serif;
    font-size: 25px;
    text-align: center;
    background-color: blueviolet;
    color: #fff;
    padding: 50px 50px;
}

</style>