<script setup>
  const isOpen = ref(true)
  const handOpenClass = () => {
    console.log(isOpen.value);
    isOpen.value = !isOpen.value
  }
</script>

<template>
  <div id="center">
      <TitleBar :handOpenClass="handOpenClass"/>
      <ListItem :isOpen ="isOpen"  />
    <!-- <EmitTest/> -->
  </div>

</template>

<style>
    * {
      padding: 0;
      margin: 0;
      box-sizing: border-box;
    }

    html,
    body {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 100%;
      background-color: slategray;
    }

    #center {
      width: 400px;
      overflow: hidden;
      border: 1px solid #42b983;
      border-radius: 10px;
    }

</style>