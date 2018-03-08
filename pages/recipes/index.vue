<template>
  <section class="recipes">
    <Recipe
        v-for="recipe in recipes"
        :key="recipe.id"
        :thumbnail = "recipe.thumbnail"
        :title = "recipe.title"
        :previewText = "recipe.previewText"
        :id="recipe.id"
    />
  </section>
</template>

<style scoped>
  .recipes {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
  }
</style>

<script>
  import Recipe from '@/components/Recipe'
  export default {
    components: {
      Recipe,
    },
    asyncData() {
      return new Promise((resolve, reject) => {
        setTimeout(()=>{
          resolve({
            recipes: [
              {
                id: "1",
                title: "Delicious Pizza",
                previewText: "Awesome Pizza!",
                thumbnail: "https://c.pxhere.com/photos/9d/eb/pizza_pepperoni_slice_sliced_mozzarella_junk_salami_italian-561684.jpg!d"
              },
              {
                id: "1",
                title: "Delicious Salasd",
                previewText: "AAre salads real?!",
                thumbnail: "https://static.wixstatic.com/media/f90248_717f584eb3cb4fbc96b4b79fc5a39d13~mv2.jpg"
              }
            ]
          })
        }, 1500)
      })
    },
  }
</script>