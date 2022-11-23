<template>
  <VContainer fluid class="fill-height pa-0">
    <VRow no-gutters align="center" justify="center" class="fill-height">

      <VImg
          src="https://wallpaper.dog/large/5557744.jpg"
          cover
          class="h-100 d-flex  text-white"
      >

        <VRow no-gutters align="start" justify="center">
          <VCol cols="11" md="4" sm="6">
            <h1>Filtres</h1>
            <p>Sélectionner la catégorie</p>
            <VSelect :items="items" v-model="category"></VSelect>
          </VCol>
        </VRow>

        <VRow align="center" justify="center" align-content="center">
          <VCol v-if="category === all || category === 'But'" cols="12" md="4" sm="6" class="pa-5" >
            <iframe src="https://www.instagram.com/p/B7EIccTASzv/embed"
                    frameborder="0" width="100%" height="480"></iframe>
          </VCol>
          <VCol v-if="category === all || category === 'Défense'" cols="12" md="4" sm="6"  class="pa-5">
            <iframe width="100%" height="400"
                    src="https://www.facebook.com/plugins/video.php?href=https%3A%2F%2Fwww.facebook.com%2Ffacebook%2Fvideos%2F1197132850712708%2F&width=500&show_text=true&height=400&appId"
                    style="border:none;overflow:hidden" scrolling="no" frameborder="0" allowfullscreen="true"
                    allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
                    allowFullScreen="true"></iframe>
          </VCol>
          <VCol v-if="category === all || category === 'Attaquant'" cols="12" md="4" sm="6"  class="pa-5">
            <iframe width="100%" height="400" src="https://www.youtube.com/embed/Bq8G5w0tXt4"
                    title="YouTube video player" frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen></iframe>
          </VCol>
          <VCol v-if="category === all || category === 'But'" cols="12" md="4" sm="6"  class="pa-5">
            <iframe width="100%" height="400" src="https://www.youtube.com/embed/bKOTKHtbM54"
                    title="YouTube video player" frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen></iframe>
          </VCol>
          <VCol v-if="category === all || category === 'But'" cols="12" md="4" sm="6"  class="pa-5" >
            <iframe src="https://www.instagram.com/p/Ck5yLWLNiki/embed"
                    frameborder="0" width="100%" height="480"></iframe>
          </VCol>
        </VRow>
      </VImg>
    </VRow>
  </VContainer>
</template>

<script lang="ts">
import {defineComponent} from 'vue'

export default defineComponent({
  setup() {
    const all = "Afficher tout";
    const category = ref(all)
    const items = [all, 'But', 'Attaquant', "Défense"]


    return {
      category,
      items,
      all
    }
  }
})
</script>

