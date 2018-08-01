<template>
    <div class="gui-card">
        <div class="gui-card__media">
            <img class="gui-card__img" v-bind:src="image" alt="" />
        </div>
        <div class="gui-card__details">
            <div class="gui-card__title">
                {{name}}
            </div>
            <div class="gui-card__description">
                <h6>{{description}}</h6>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:['name', 'image', 'description']
}
</script>

<style lang="scss">

</style>

