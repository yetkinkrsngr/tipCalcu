<template>
    <button 
        @click="setActive()" 
        :style="{backgroundColor: active ? 'red' : 'green'}" 
    >{{ tip }}%</button>
</template>

<script>
    export default{
        data(){
            return{
                active: false
            }
        },
        props: ['tip'],
        methods: {
            setActive(){
                this.active = !this.active;
            }
        },
    }

</script>

<style scope>

    button{
        font-size: var(--font-input);
        font-weight: var(--font-weight);
        background-color: var(--neutral-1);
        color: var(--neutral-4);
        padding: var(--input-padding);
        border-radius: var(--input-radius);
        width: 100%;
        outline: none;
        border: none;
        transition: var(--main-transition);
        cursor: pointer;
    }

    button:hover{
        background-color: var(--primary);
        color: var(--neutral-4);
    }

</style>