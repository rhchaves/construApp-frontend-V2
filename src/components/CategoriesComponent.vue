<template>
  <div class="btnAmber row justify-center" style="height: 53px">
    <q-btn
      v-for="category in listCategories"
      :key="category.id"
      class="btnAmber categories"
      :label="category.label"
      @click="filterCategories(category)"
    />
  </div>
</template>

<script>
export default {
  name: 'CategoriesComponent',

  data() {
    return {
      listCategories: [
        { id: 1, name: 'construcao', label: 'Construção' },
        { id: 2, name: 'eletrica', label: 'Elétrica' },
        { id: 3, name: 'hidraulica', label: 'Hidráulica' },
        { id: 4, name: 'ferragens', label: 'Ferragens' },
        { id: 5, name: 'tintas', label: 'Tintas' },
        { id: 6, name: 'ferramentas', label: 'Ferramentas' },
      ],
    };
  },

  methods: {
    filterCategories(category) {
      // this.$emit('categoriesEmit', categories);
      console.log('Categoria', category);
    },
  },
};
</script>
