<template>
        <div>
            <div v-if="componentType === 'text'">
                <InputText :data="data"/>
            </div>
            <div v-else-if="componentType === 'dropdown'">
                <Dropdown :data="data" />
            </div>
            <div v-else-if="componentType === 'radio'">
                <InputRadio :data="data" />
            </div>
            <div v-else-if="componentType === 'textarea'">
                <Textarea :data="data" />
            </div>

        </div>

</template>
<script>
import Dropdown from '@/components/Dropdown.vue'
import InputText from '@/components/InputText.vue'
import Textarea from '@/components/Textarea.vue'
import InputRadio from '@/components/InputRadio.vue'

export default {
    props : ['data'],
    computed: {
        componentType(){
            return this.data.component_type
        }
    },
    components :{
       InputText,
       Dropdown,
       Textarea,
       InputRadio
    },
    

}
</script>


