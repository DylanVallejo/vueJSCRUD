<template>
    <div class="container">
        <h3>Creando formularios con v-model para vincular/bindear inputs</h3>
        <form>
            <!-- v-model bindea y le dice que esta vinculado directamente -->
            <input type="text" v-model="inputText"  placeholder="texto"/>
            <p>Valor : {{ inputText }}</p>
            <h3>Vinculacion de formulario a travez de checkbox tambien acepta booleans</h3>
            <input type="checkbox" v-model="agree"/> Acepto terminos y condiciones
            <h3>Vinculacion de formulario a travez de selects tambien acepta valores por defecto</h3>
            
            <select v-model="country">
                <!-- si las opciones no tienen value nos selecciona el texto de la etiqueta -->
                <option value="spain">Spain</option>
                <option value="france">France</option>
                <option value="netherlands"> Netherlands</option>
                <option value="rusia">Rusia</option>
            </select>
        </form>
    </div>
</template>
<script setup>

import {ref} from 'vue';
let inputText = ref('');
let agree = ref(true);
let country = ref('rusia');

</script>
<style scope>

</style>