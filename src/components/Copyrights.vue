<template>
  <footer class="footer">
    <div class="text">
      © {{ data.companyName }} {{ data.yearText }}. All rights reserved.
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      data: {
        companyName: 'Revi/Repp Shop',
        startYear: 2020,
        currentYear: new Date().getFullYear()
      }
    };
  },
  computed: {
    yearText() {
      return this.data.startYear === this.data.currentYear
        ? this.data.startYear.toString()
        : `${this.data.startYear} - ${this.data.currentYear}`;
    }
  }
};
</script>

<style scoped>
.footer {
  margin-bottom: -40px;
  padding: 10px 0;
  background-color: #000000;
  text-align: center;
  width: 100%;
}

.text {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-size: small;
}
</style>
