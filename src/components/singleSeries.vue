<script>
export default {
    name: "",
    props: {
        thumb: String,
        price: Number,
        series: String,
        type: String
    }
}
</script>

<template>
    <div class="card">
        <div class="card-img">
            <img :src="thumb" alt="series">
        </div>
        <div class="card-text">
            <h4>{{series}}</h4>
            <p>{{price}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .card {
        width: calc(100% / 6 - 1rem);
        margin: 0 .5rem;
        margin-bottom: 2rem;
        text-align: center;
        
        h4 {
            color: white;
        }

        p {
            color: white;
        }
    }
</style>