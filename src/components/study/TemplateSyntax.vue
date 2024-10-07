<script setup>
import { ref } from "vue";
const message = ref("<h1 style='text-align: center'>Hello, world</h1>");
const bgDanger = ref("bg-danger");
</script>

<template>
<!--      <div v-html="message" v-bind:class="bgDanger"></div>-->

      <div>
        <p :class="(message.indexOf('<') != -1)?bgDanger:''"> {{ message.replace(/[^\w\s]/g, '') }} </p>
      </div>

</template>

<style scoped>

div{
  width: 100%;
  margin: 250px auto;

}

p{
  font-size: 5rem;
  text-align: center;
}

.bg-danger{
  background: red !important;
}

</style>