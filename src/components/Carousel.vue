<template>
  <div class="carousel-container">
    <div class="carousel">
      <div class="carousel-slide" :class="{ active: slide === 0 }">
        <img src="/src/assets/IMG-20240526-WA0019.jpg" alt="Slide 1" class="carousel-img" />
      </div>
      <div class="carousel-slide" :class="{ active: slide === 1 }">
        <img src="https://down-id.img.susercontent.com/file/sg-11134201-22120-rohabay0oplv05" alt="Slide 2" class="carousel-img" />
      </div>
      <div class="carousel-slide" :class="{ active: slide === 2 }">
        <img src="https://down-id.img.susercontent.com/file/sg-11134201-22120-y52btabtpplv95" alt="Slide 3" class="carousel-img" />
      </div>
      <div class="carousel-slide" :class="{ active: slide === 3 }">
        <img src="https://down-id.img.susercontent.com/file/id-11134207-7qukw-lhxmo4v9a67e02" alt="Slide 4" class="carousel-img" />
      </div>
    </div>
    <div class="carousel-controls">
      <button @click="prevSlide">Previous</button>
      <button @click="nextSlide">Next</button>
    </div>
    <div class="carousel-indicators">
      <span :class="{ active: slide === 0 }" @click="goToSlide(0)"></span>
      <span :class="{ active: slide === 1 }" @click="goToSlide(1)"></span>
      <span :class="{ active: slide === 2 }" @click="goToSlide(2)"></span>
      <span :class="{ active: slide === 3 }" @click="goToSlide(3)"></span>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Carousel',
  setup () {
    const slide = ref(0)

    const prevSlide = () => {
      slide.value = (slide.value + 3) % 4
    }

    const nextSlide = () => {
      slide.value = (slide.value + 1) % 4
    }

    const goToSlide = (index) => {
      slide.value = index
    }

    return {
      slide,
      prevSlide,
      nextSlide,
      goToSlide
    }
  }
}
</script>

<style scoped>
.carousel-container {
  position: relative;
  width: 100%;
  overflow: hidden;
}

.carousel {
  display: flex;
  transition: transform 0.5s ease;
}

.carousel-slide {
  min-width: 100%;
  transition: opacity 0.5s ease;
  opacity: 0;
  position: absolute;
  top: 0;
  left: 0;
}

.carousel-slide.active {
  opacity: 1;
  position: relative;
}

.carousel-img {
  width: 100%;
  height: auto;
}

.carousel-controls {
  position: absolute;
  top: 50%;
  width: 100%;
  display: flex;
  justify-content: space-between;
  transform: translateY(-50%);
}

.carousel-controls button {
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
}

.carousel-indicators {
  position: absolute;
  bottom: 10px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
}

.carousel-indicators span {
  width: 10px;
  height: 10px;
  margin: 0 5px;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 50%;
  cursor: pointer;
}

.carousel-indicators span.active {
  background-color: white;
}
</style>
