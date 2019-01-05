<template>
    <div class="ui page dimmer" :class={active:showMessage}>
        <div class="ui info message" id="k_head_message">
            <div class="ui container">
                <div class="content">
                    {{message}}
                    <button class="ui green small label close" @click="showMessage=0">OK, I see</button>
                </div>
            </div>
            <i class="close icon"></i>
        </div>
    </div>
</template>
<script>
    export default {
        name:'Dimmer',
        data:function(){
            return {
                message:'',
                showMessage:this.show
            }
        },
        methods:{
            
        },
        props:['show'],
        mounted:function(){
            let self=this;
            this.$nextTick(function(){
                console.log('Showing dimmer...')
            })
        }
    }
</script>
<style scoped>
    button{
        cursor: pointer;
    }
</style>