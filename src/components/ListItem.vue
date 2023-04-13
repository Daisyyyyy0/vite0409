
<script setup>
    const props = defineProps({
        isOpen:{
        type: Boolean,
        default: true
        }
    })
    const listArr = reactive([
        { name: "手機揹帶" },
        { name: "吊飾" },
        { name: "小廢包" },
        { name: "波西米亞包" },
        { name: "A4包" },
    ]);
</script>

<template >
      <Transition name="open">
        <ul class="box" v-show="props.isOpen">
          <li v-for="(list, idx) in listArr" :key="list.name">
            {{ idx + 1 }}. {{ list.name }}
          </li>
        </ul>
      </Transition>



</template>

<style>
    .box {
      display: block;
      width: 100%;
      /* height: 0; */
      background-color: snow;
      transition: height 0.4s;
    }

    /* .box.open {
      height: 200px;
    } */

    .box>li {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 40px;
      border-bottom: 1px solid #d2d2d2;
      font-size: 12px;
      color: darkslategray;
    }

    
  .open-enter-from{
    height: 0;
  }
  .open-enter-to{
    height: 200px;;
  }
  .open-leave-from{
    height: 200px;;
  }
  .open-leave-to{
    height: 0;
  } 

  .open-enter-active,
  .open-leave-active {
    transition: height 1s ease;
  }
  
  .open-enter-from,
  .open-leave-to {
    opacity: 0;
    transform: translateX(30px);
  } 

</style>