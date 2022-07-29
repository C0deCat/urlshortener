<template>
<form action="#">
  <div class="mdl-textfield mdl-js-textfield mdl-textfield--floating-label">
    <input class="mdl-textfield__input" type="text" id="sample3">
    <label class="mdl-textfield__label" for="sample3">URL for shortening</label>
  </div>
  <button class="mdl-button mdl-js-button mdl-button--raised mdl-js-ripple-effect mdl-button--colored">
    Shorten
  </button>
</form>
</template>

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