<script setup>
import Card from './Card.vue'

const onClickAdd = () => {
  alert('Добавлено!')
}
</script>

<template>
  <div class="grid grid-cols-4 gap-5">
    <Card
      title="Мужские кроссовки Nike Blazer Mid Suede"
      image-url="/sneakers/sneakers-1.jpg"
      :price="5000"
      :is-added="false"
      :is-favorite="false"
      :on-click-add="onClickAdd"
    />
  </div>
</template>
