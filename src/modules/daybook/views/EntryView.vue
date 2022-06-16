<template>
    <div class="entry-title d-flex justify-content-between p-2">
        <div>
            <span class="text-success fs-3  fw-bold">16</span>
            <span class="mx-1 fs-3">de Junio</span>
            <span class="mx-2 fs-4 fw-light">2022</span>
        </div>

        <div>
            <button class="btn btn-danger mx-2">
                Borrar
                <i class="fa fa-trash-alt"></i>
            </button>
            <button class="btn btn-primary">
                Subir foto
                <i class="fa fa-upload"></i>
            </button>
        </div>
    </div>
    <hr/>
    <div class="d-flex flex-column px-3 h-75">
        <textarea placeholder="¿Que sucedió hoy?">
            
        </textarea>
    </div>
    <Fab v-bind:fabIconDefault ="fabIconDefault"/>
    <img 
        src="https://res.cloudinary.com/practicaldev/image/fetch/s--I4FWon9Y--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ll22z8mea106b4vjdjy7.jpeg" 
        alt="entry-picture"
        class="img-thumbnail"
    >   
</template>

<script>
    
    import { defineAsyncComponent } from 'vue'
    export default {
        data(){
            return{
                fabIconDefault: 1
            }
        },
        components:{
            Fab: defineAsyncComponent( () => import('@/modules/daybook/components/Fab.vue') ),
        }
    }
</script>

<style lang="scss" scoped>
    textarea{
        font-size: 20px;
        border: none;
        height: 100%;
        
        &:focus{
            outline: none;
        }
    }

    img{
        width: 200px;
        position: fixed;
        bottom: 150px;
        right: 20px;
        box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
    }

</style>