<script setup>
    const props = defineProps({
        options:{
            type:Array,
            default:()=>[]
        }
    })

    console.log(props,'props');
    
</script>

<template>
    <ul>
        <li v-for="item in props">{{item}}</li>
    </ul>
</template>