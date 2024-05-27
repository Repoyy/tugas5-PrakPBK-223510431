<template>
    <header class="sales-header">
      <div class="container">
        <div class="logo">
          <a href="#">ReppShop
          </a>
        </div>
        <nav class="nav-links">
          <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">Products</a></li>
            <li><a href="#">Kategori</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </nav>
        <div class="search-bar">
          <input 
            type="text" 
            placeholder="Search for products..." 
            v-model="searchQuery"
            @keyup.enter="search"
          />
          <button @click="search">Search</button>
        </div>
      </div>
    </header>
  </template>
  
  <script>
  export default {
    name: 'Header',
    data() {
      return {
        searchQuery: ''
      };
    },
    methods: {
      search() {
        console.log('Searching for:', this.searchQuery);
      }
    }
  };
  </script>
  
  <style scoped>
  .sales-header {
    background: linear-gradient(to right, #01204E, #028391); /* Gradien merah ke oranye */
    padding: 20px 0;
    color: white;
  }
  
  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .logo a {
    color: white;
    text-decoration: none;
    font-size: 24px;
    margin-left: 10px;
  }
  
  .nav-links ul {
    list-style: none;
    display: flex;
    gap: 20px;
    margin: 0;
    padding: 0;
  }
  
  .nav-links a {
    color: white;
    text-decoration: none;
  }
  
  .search-bar {
    display: flex;
    gap: 10px;
  }
  
  .search-bar input {
    padding: 5px;
    font-size: 16px;
  }
  
  .search-bar button {
    padding: 5px 10px;
    background-color: #028391;
    border: none;
    color: white;
    cursor: pointer;
  }
  </style>
  