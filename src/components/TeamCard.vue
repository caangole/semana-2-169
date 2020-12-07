<template>
    <div class="container row">
        <div class="card" style="width: 25rem;">
                    <img v-bind:src="member.imagen" class="card-image-top" alt="Fotografía de integrante" style="width: 25rem; height: 30rem;">
                <div class="card-body">
                    <h3 class="card-header bg-info text-white">{{member.nombre}}</h3>
                    <h4 class="card-title ml-5 mt-3">{{member.rol}}</h4>
                </div>
                <p class="card-footer mb-0">{{member.descripcion}}</p>
        </div>
    </div> 
</template>

<script>
    export default {
        name: "TeamCard",
        props: ['member']
    }
</script>

<style >

</style>
