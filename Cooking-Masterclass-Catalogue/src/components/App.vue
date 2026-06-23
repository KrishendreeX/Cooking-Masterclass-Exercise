<template>
  <div class="app-container">
    <Header :wishlistCount="wishlist.length" />

    <div class="filter-container">
      <button 
        @click="currentFilter = 'all'" 
        :class="{ active: currentFilter === 'all' }"
      >
        All Courses
      </button>
      <button 
        @click="currentFilter = 'available'" 
        :class="{ active: currentFilter === 'available' }"
      >
        Available Only
      </button>
    </div>

    <main class="catalogue-container">
      <CourseCard 
        v-for="item in filteredCourses" 
        :key="item.id" 
        :course="item" 
        @toggle-wishlist="handleWishlist"
      />
    </main>
  </div>
</template>

<script>
import Header from './Header.vue'
import CourseCard from './CourseCard.vue'
import { courseData } from './courses.js'

export default {
  components: {
    Header,
    CourseCard
  },
  data() {
    return {
      courses: courseData,
      wishlist: [],
      currentFilter: 'all'
    }
  },
  computed: {
    filteredCourses() {
      if (this.currentFilter === 'available') {
        return this.courses.filter(course => course.available === true)
      } else {
        return this.courses
      }
    }
  },
  methods: {
    handleWishlist(courseId) {
      if (!this.wishlist.includes(courseId)) {
        this.wishlist.push(courseId)
      } else {
        this.wishlist = this.wishlist.filter(id => id !== courseId)
      }
    }
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  background-color: #f3f4f6;
}

.filter-container {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-top: 20px;
}

.filter-container button {
  padding: 10px 20px;
  border: 1px solid #d1d5db;
  background-color: white;
  border-radius: 6px;
  cursor: pointer;
  font-weight: 500;
}

.filter-container button.active {
  background-color: #2563eb;
  color: white;
  border-color: #2563eb;
}

.catalogue-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 24px;
  padding: 20px;
  margin: 0 auto;
  max-width: 1200px;
}
</style>