<template>
    <button class="btn btn-primary">
        <i v-if="fabIconDefault==0" class="fa fa-2x fa-plus"></i>
        <i v-else class="fa fa-2x fa-save"></i>
    </button>
    {{ fabIconDefault }}
</template>

<script>
    export default {
        
        props:{
            fabIconDefault: {
                type: Number,
                required: true,
                default: 0
            }
        }
    }

</script>

<style lang="scss" scoped>
    button {
        position: fixed;
        bottom: 20px;
        right: 20px;
        width: 60px;
        height: 60px;
        border-radius: 100%;
    }
</style>