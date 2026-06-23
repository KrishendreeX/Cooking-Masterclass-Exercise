<template>
  <header class="header">
    <h1>Cooking Masterclass Catalogue</h1>
    <div class="wishlist-counter">
      ❤️ Wishlist: <span>{{ wishlistCount }}</span>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    wishlistCount: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2.5rem 2rem;
  background-color: #1f2937;
  color: white;
  margin-bottom: 2rem;
}
.wishlist-counter span {
  background-color: #ef4444;
  padding: 2px 10px;
  border-radius: 12px;
  font-weight: bold;
  margin-left: 5px;
}
</style>
