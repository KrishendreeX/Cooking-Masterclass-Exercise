<template>
  <div class="course-card" :class="{ 'sold-out-card': !course.available }">
    <h3>{{ course.title }}</h3>
    <p><strong>Chef:</strong> {{ course.chef }}</p>
    <p><strong>Level:</strong> {{ course.level }}</p>
    <p><strong>Price:</strong> R{{ course.price }}</p>
    
    <span v-if="!course.available" class="badge sold-out">Sold Out</span>
    <span v-else class="badge available">Available</span>

    <button 
      :disabled="!course.available" 
      @click="$emit('toggle-wishlist', course.id)"
      class="save-btn"
    >
      Save to Wishlist
    </button>
  </div>
</template>

<script>
export default {
  props: {
    course: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>
.course-card {
  border: 1px solid #e5e7eb;
  border-radius: 8px;
  padding: 16px;
  background: white;
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.sold-out-card {
  opacity: 0.6;
}
.badge {
  padding: 4px 8px;
  font-size: 12px;
  border-radius: 4px;
  width: max-content;
}
.available { background-color: #d1fae5; color: #065f46; }
.sold-out { background-color: #fee2e2; color: #991b1b; }
.save-btn {
  margin-top: auto;
  background-color: #2563eb;
  color: white;
  border: none;
  padding: 8px;
  border-radius: 4px;
  cursor: pointer;
}
.save-btn:disabled {
  background-color: #9ca3af;
  cursor: not-allowed;
}
</style>