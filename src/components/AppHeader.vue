<template>
  <header>
    <div class="container header-container">
      <div class="brand">
        <img
          src="https://i.postimg.cc/t4QzDqwN/Screenshot-20260312-164028-Instagram1.jpg"
          alt="劉擎的頭貼"
          class="profile-pic"
        />
        <router-link to="/" class="logo">劉擎</router-link>
      </div>

      <div class="menu-toggle" :class="{ 'is-active': menuOpen }" @click="toggleMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>

      <nav>
        <ul class="nav-links" :class="{ active: menuOpen }">
          <li><a href="#home" class="nav-item" @click="closeMenu">首頁</a></li>
          <li><a href="#about" class="nav-item" @click="closeMenu">關於我</a></li>
          <li><a href="#skills" class="nav-item" @click="closeMenu">技能</a></li>
          <li><a href="#projects" class="nav-item" @click="closeMenu">專案</a></li>
          <li class="mobile-only">
            <a href="#contact" class="btn-outline nav-item" @click="closeMenu">聯絡我</a>
          </li>
        </ul>
      </nav>
      <a href="#contact" class="btn-outline desktop-only">聯絡我</a>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

function toggleMenu() {
  menuOpen.value = !menuOpen.value
}

function closeMenu() {
  menuOpen.value = false
}
</script>
