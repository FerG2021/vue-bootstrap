<template>
    <div class="mt-5">
        <h1>Formularios</h1>

        <form>
            <b-row>
                <b-col md="3">
                    <b-form-input type="text" v-model="texto" :state="comprobar"></b-form-input>
                    <small>Mínimo 3 caracteres</small>
                </b-col>

                <b-col md="3">
                    
                </b-col>

                <b-col md="3">

                </b-col>
            </b-row>            
        </form>

        <p>Texto: {{texto}}</p>


    </div>
</template>

<script>
export default {
    name: 'Forms',
    data(){
        return{
            texto: ''
        }
    },
    computed:{
        comprobar(){
            return this.texto.length > 2 ? true : false
        }
    }
}
</script>