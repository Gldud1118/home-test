<template>
    <div>
        <div v-for="radio in data.data" :key="radio.id" class="input-radio">
            <label :for="radio.id">{{radio.value}}</label>
            <input type="radio" :id="radio.id" :name="data.name">
        </div>
    </div>
</template>

<script>
export default {
    props :['data']

}
</script>

<style>
   .input-radio{
       display: inline-block;
   } 
</style>