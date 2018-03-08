<template>
  <section class="recipes">
    <Recipe
        thumbnail = "https://c.pxhere.com/photos/9d/eb/pizza_pepperoni_slice_sliced_mozzarella_junk_salami_italian-561684.jpg!d"
        title = "Delicious"
        previewText = "Testing preview text."
        id="1"
    />
    <Recipe
        thumbnail = "https://static.wixstatic.com/media/f90248_717f584eb3cb4fbc96b4b79fc5a39d13~mv2.jpg"
        title = "Have a Salad "
        previewText = "Are salads real?"
        id
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
    }
  }
</script>