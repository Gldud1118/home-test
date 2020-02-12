<template>
    <div>
        <select>
            <option :id="option.id" value="" v-for="option in data.data" :key="option.id">{{option.value}}</option>
        </select>
    </div>
</template>

<script>
export default {
    props : ['data'],
    data(){
        return{

        }
    }
}
</script>