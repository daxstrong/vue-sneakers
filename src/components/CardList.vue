<script setup>
import { inject } from 'vue'
import Card from './Card.vue'

defineProps({
  items: Array
})

const onClickAdd = () => {
  alert('Добавлено!')
}

const addToFavorite = inject('addToFavorite')
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      v-for="item in items"
      :key="item.id"
      :id="item.id"
      :title="item.title"
      :image-url="item.imageUrl"
      :price="item.price"
      :on-click-add="onClickAdd"
      :is-favorite="items.isFavorite"
      :onClickFavorite="() => addToFavorite(item)"
      :isFavorite="items.isFavorite"
    />
  </div>
</template>
