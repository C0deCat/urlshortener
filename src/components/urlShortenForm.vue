<template>
<form @submit.prevent="getShortenLink">
  <div class="mdl-textfield mdl-js-textfield mdl-textfield--floating-label">
    <input class="mdl-textfield__input" type="text" id="sample3" v-model="link">
    <label class="mdl-textfield__label" for="sample3">URL for shortening</label>
  </div>
  <button type="submit" class="mdl-button mdl-js-button mdl-button--raised mdl-js-ripple-effect mdl-button--colored">Shorten</button>
</form>
</template>

<script setup>
import { ref } from 'vue';

const link = ref('');
const emit = defineEmits(['getLink']);

async function getShortenLink() {

  let TOKEN = "262500e8d2ed79e0a386d1ea94a38c8c01de43dd";
  let group_guid = "Bm7sfKTRroG";

  const response = await fetch('https://api-ssl.bitly.com/v4/shorten', {
     method: 'POST',
     headers: {
         'Authorization': 'Bearer '.concat(TOKEN),
         'Content-Type': 'application/json'
     },
     body: JSON.stringify({ "long_url": "".concat(link.value), "domain": "bit.ly", "group_guid": "".concat(group_guid) })
   });
   const data = await response.json();

  emit('getLink', data);
}

</script>

<style scoped lang="less">
    form {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
    }
    .mdl-textfield {
        width: 100%;
    }
    .mdl-button {
        flex-basis: 150px;
    }
</style>