<script setup lang="ts">
const today = new Date();
const year = today.getFullYear().toString();
const month = (today.getMonth() + 1).toString().padStart(2, "0");
const day = today.getDate().toString().padStart(2, "0");

const baseUrl = "https://scrapbox.io/dorary/";
const subUrl = year + month + day;
const bodyString = "?body=" + encodeURIComponent(`#${year}年${month}月`);

const fullUrl = baseUrl + subUrl + bodyString;
</script>

<template>
<div>
  <a :href="fullUrl">link</a>
</div>
</template>

<style scoped>
</style>