<template>
    <div class="entry-title d-flex justify-content-between p-2">
        <div>
            <span class="text-success fs-5 fw-bold">15</span>
            <span class="mx-1 fs-5">Julio</span>
            <span class="mx-2 fw-light">2024</span>
        </div>

        <div>
            <button class="btn btn-danger mx-2">
                borrar
                <i class="fa fa-trash-alt"></i>
            </button>

              <button class="btn btn-primary mx-2">
                Subir Foto
                <i class="fa fa-upload"></i>
            </button>
        </div>
    </div>

    <hr>
    <div class="d-flex flex-column px-3 h-75">
        <textarea placeholder="¿Qué sucedió hoy?">

        </textarea>

    </div>

    <Fab  :icon="iconProp"/>

    <img src="https://upload.wikimedia.org/wikipedia/commons/9/96/Barbados_beach.jpg"
    class="img-thumbnail">

</template>

<script>
import { defineAsyncComponent } from 'vue'
export default {
    components : {
        Fab : defineAsyncComponent (() => import('../components/Fab.vue'))
    },
    data() {
       return {
        iconProp: 'fa-save'
     };
  }
}
</script>

<style lang="scss" scoped>
    textarea {
        font-size: 20px;
        border: none;
        height: 100%;

        &:focus {
                outline: none;
        }
    }

    img {
        width: 200px;
        position: fixed;
        bottom: 150px;
        right: 20px;
        box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
    }
</style>