<template>
    <div class="dialog" v-if="show" @click="hideDialog">
        <div class="dialog_content" @click.stop>
            <a href="#" @click="hideDialog" class="close">&times;</a>
            <slot>Default</slot>
        </div>
    </div>
</template>

<script>
export default{
    name: "MyDialog",
    props: {
        show: {
            type: Boolean,
            default: false
        }
    },
    methods: {
        hideDialog(){
            this.$emit('update:show', false);
        }
    }
}
</script>

<style scoped>

.close{
    float: right;
    text-decoration: none;
    color:blue;
}
.close::after{
    content: "";
}
.dialog{
    position:fixed;
    display: flex;
    height: 100%;
    top:0;
    left:0;
    right:0;
    background: rgba(0,0,0,0.5);
}
.dialog_content{
    margin: auto;
    background: white;
    border-radius:  16px;
    min-height: 50px;
    width:200px;
    padding: 5px;
}
p{
    margin: 5px;
}
</style>