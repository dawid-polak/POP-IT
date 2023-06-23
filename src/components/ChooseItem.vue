<template>
     <div class="item">
          <img class="item--img" :src="props.data.img_src" :alt="props.data.img_name" />
          <p class="item--description">{{ props.data.description }}</p>
          <button class="item--btn">BUY</button>
     </div>
</template>

<script setup>
const props = defineProps(["data"]);
</script>

<style scoped>
.item {
     max-width: 200px;
     display: flex;
     flex-flow: column;
     align-items: center;
     margin: 50px;
}

.item .item--img {
     width: 100%;
}

.item .item--description {
     font-weight: 900;
     text-align: center;
}

.item .item--btn {
     width: 150px;
     height: 40px;
     background-color: #febf69;
     color: #000;
     font-weight: 900;
     border: 0;
     cursor: pointer;
}
</style>
