<template>
    <input :type="typeInput??'text'" @input="updateInput"/>
</template>

<script>
export default{
    name: "FormInput", 
    props: ['modelValue', 'typeInput'],
    methods:{
        updateInput(event){
            this.$emit('update:modelValue', event.target.value);
        }
    }
}
</script>

<style scoped>

</style>