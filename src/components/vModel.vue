<template>
    <div>
        <!--
            3. usamos v-model para coja el valor de nuestra variable porque referencia al input
        -->
        <input type="text" v-model="input">
   <!--
   4. Le decimos al h3 que coja el valor del input en este caso esta vacio 
   -->
    <h3>{{ input }}</h3>
    <button @click="text">Send</button>
    
    <input type="checkbox" v-model="check">

    <select v-bind="option" name="film" id="film">
        <option value="anillos">señor de los añillos</option>
        <option value="hobbit">hobbit</option>
    </select>
    <textarea v-model="textarea">
     
  </textarea>
</div>
</template>

<script setup>
// 1. importamos la referencia de vue 
import  {ref} from 'vue'
// 2. decimos que le referencia del input esta vacia 
let input = ref('')
let check = ref('true')
let option = ref ('')
 let textarea = ref('')
</script>

<style scoped>
div{
    display: flex;
    flex-direction: column;
    gap: 1em;
}
</style>