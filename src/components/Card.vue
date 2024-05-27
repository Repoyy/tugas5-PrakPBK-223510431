<template>
  <div class="q-pa-md">
    <div class="grid-wrapper q-gutter-md">
      <q-card class="my-card">
        <img src="/src/assets/IMG-20240526-WA0019.jpg" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp polo Shirt</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="/src/assets/IMG-20240526-WA0020.jpg" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp polo Shirt</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="/src/assets/IMG-20240526-WA0021.jpg" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp polo Shirt</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="/src/assets/IMG-20240526-WA0022.jpg" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp polo Shirt</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="/src/assets/IMG-20240526-WA0023.jpg" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp polo Shirt</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="/src/assets/IMG-20240526-WA0024.jpg" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp polo Shirt</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="/src/assets/IMG-20240526-WA0025.jpg" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp polo Shirt</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="https://down-id.img.susercontent.com/file/id-11134207-7qula-li0d0hr3hxisb9" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp kemeja</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="https://down-id.img.susercontent.com/file/id-11134207-7qul7-li0d0hr3m584e1" class="card-img">
        <q-card-section>
          <div class="text-h6">Repp kemeja</div>
          <div class="text-subtitle2">Rp 200.000</div>
        </q-card-section>
        <q-card-section class="q-pt-none">
          <!-- Add the card description here if needed -->
        </q-card-section>
      </q-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  setup() {
    return {
      // No need to define cards in setup since they are directly in the template now
    };
  }
};
</script>

<style scoped>
.grid-wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 16px;
}

.my-card {
  width: 100%;
  max-width: 100%;
  background-image: linear-gradient(163deg, #01204E 10%, #028391 100%);
  border-radius: 5px;
  transition: all .3s;
  cursor: pointer;
}

.card-img {
  width: 100%;
  height: auto;
}

.my-card:hover {
  transform: scale(0.98);
}

@media (max-width: 600px) {
  .grid-wrapper {
    grid-template-columns: 1fr;
  }

  .my-card {
    margin-bottom: 16px;
  }
}
</style>
