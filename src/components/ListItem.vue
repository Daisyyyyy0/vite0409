
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
        <ul :class="['box', { open: props.isOpen }]">
          <li v-for="(list, idx) in listArr" :key="list.name">
            {{ idx + 1 }}. {{ list.name }}
          </li>
        </ul>


</template>

<style>
    .box {
      display: block;
      width: 100%;
      height: 0;
      background-color: snow;
      transition: height 0.4s;
    }

    .box.open {
      height: 200px;
    }

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
</style>