<template>
    <a-layout-header class="header">
      <div class="logo">🎬 MovieTicket</div>
  
      <a-menu
        theme="dark"
        mode="horizontal"
        :selected-keys="[selectedKey]"
        @click="handleMenuClick"
      >
        <a-menu-item key="home">Trang chủ</a-menu-item>
        <a-menu-item key="showtimes">Lịch chiếu</a-menu-item>
        <a-menu-item key="cinemas">Rạp chiếu</a-menu-item>
      </a-menu>
  
      <div class="auth-buttons">
        <a-button type="primary" ghost>Đăng nhập</a-button>
      </div>
    </a-layout-header>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const selectedKey = ref('home')
  
  const handleMenuClick = e => {
    selectedKey.value = e.key
  }
  </script>
  
  <style scoped>
  .header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 32px;
    background: #001529;
  }
  
  .logo {
    color: white;
    font-size: 20px;
    font-weight: bold;
    margin-right: 24px;
  }
  
  .auth-buttons {
    margin-left: auto;
  }
  </style>