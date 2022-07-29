<template>
<main class="mdl-layout__content">
    <div class="page-content mdl-grid">
        <div class="mdl-cell mdl-cell--middle mdl-cell--2-offset-desktop mdl-cell--0-offset-phone  mdl-cell--8-col">
            <UrlShortenForm></UrlShortenForm>
            <UrlList></UrlList>
        </div>
    </div>
</main>
</template>

<script>
import UrlShortenForm from "./urlShortenForm.vue";
import UrlList from "./urlList.vue";

export default {
    components: {
    UrlShortenForm,
    UrlList
}
};
</script>