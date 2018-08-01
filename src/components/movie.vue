<template>
    <div class="gui-card" v-bind:style="clickEffect" v-on:click="onClickEffect" v-on:mouseout="removeClickEffect">
        <div class="gui-card__media">
            <img class="gui-card__img" v-bind:src="image" alt="" />
        </div>
        <div class="gui-card__details">
            <div class="gui-card__title">
                {{name}}
            </div>
            <div class="gui-card__description">
                <h6 v-if="descriptionFlag">{{description}}</h6>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:['name', 'image', 'description'],
    data(){
        return{
            clickEffect: null,
            descriptionFlag: false
        }
    },
    methods: {
        onClickEffect: function() {
            console.log("click");
            this.clickEffect = 'transform: scale(1.9); margin-right: 110px';
            this.descriptionFlag = true;
        },
        removeClickEffect: function() {
            this.clickEffect = null;
            this.descriptionFlag = false;
        }
    }
}
</script>

<style lang="scss">

</style>

