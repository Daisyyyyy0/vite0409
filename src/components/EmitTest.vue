<script setup>
    const num = ref(0)
    onMounted(
        () => {
            console.log("context:",context);
        }
    )

</script>

 
<template >
    <h1>{{ num }}</h1>
</template>
 
<style scoped>
    
</style>