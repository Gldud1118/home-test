<template>
  <div id="app">
      <Form v-for="(json, index) in jsonData" :key="index"  :data="json" /> 
  </div>
</template>

<script>
import Form from '@/components/Form.vue'

export default {
  name: 'App',
  components: {
    Form
  },

  data() {
    return {
      jsonData : [
            {
            "component_type": "text",
            "name": "First Name",
            "data": {}
            },
            {
            "component_type": "text",
            "name": "Last Name",
            "data": {}
            },
            {
            "component_type": "text",
            "name": "Mobile Number",
            "data": {}
            },
            {
            "component_type": "textarea",
            "name": "Misson",
            "data": {}
            },
            {
            "component_type": "radio",
            "name": "Citizenship",
            "data": [
                {
                "id": "sg",
                "value": "Singaporean"
                },
                {
                "id": "foreigner",
                "value": "Foreigner"
                }
            ]
            },
            {
            "component_type": "dropdown",
            "name": "Citizenship",
            "data": [
                {
                "id": "sg",
                "value": "Singaporean"
                },
                {
                "id": "foreigner",
                "value": "Foreigner"
                }
            ]
            }
        ]
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
