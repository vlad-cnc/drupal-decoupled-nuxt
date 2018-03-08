<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="recipe-image" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
  export default {
    asyncData(context) {
      return new Promise((resolve, reject) => {
        setTimeout(()=>{
          resolve({
            recipe: [
              {
                id: "1",
                title: "Delicious Pizza",
                previewText: "Awesome Pizza!",
                descriptionText: "This is a description text",
                thumbnail: "https://c.pxhere.com/photos/9d/eb/pizza_pepperoni_slice_sliced_mozzarella_junk_salami_italian-561684.jpg!d"
              },
              {
                id: "2",
                title: "Delicious Salasd",
                descriptionText: "This is a description text",
                previewText: "AAre salads real?!",
                thumbnail: "https://static.wixstatic.com/media/f90248_717f584eb3cb4fbc96b4b79fc5a39d13~mv2.jpg"
              }
            ].find(el => el.id === context.params.id)
          })
        }, 1500)
      })
    },
  }
</script>
<style scoped>
  .single-recipe {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
    box-sizing: border-box;
    flex-flow: column;
    box-shadow: 0 2px 2px #3cc;
  }
  .recipe-image {
    width: 100px;
    height: auto;
  }
</style>