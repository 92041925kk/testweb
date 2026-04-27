<template>
  <main>
    <!-- Hero -->
    <section id="home" class="hero">
      <div class="container">
        <div class="hero-content">
          <h1 class="glitch-text">您好，我是劉擎</h1>
          <p class="subtitle">一個碩士生 | 持續探索與學習新知</p>
          <a href="#projects" class="btn-primary">探索我的專案</a>
        </div>
      </div>
    </section>

    <div class="divider"></div>

    <!-- 關於我 -->
    <section id="about" class="about text-center">
      <div class="container section-inner">
        <h2>關於我</h2>
        <p>目前為一名碩士生。對未知的領域保持好奇，致力於在學術與實務中尋找平衡，並透過專案實作解決問題。</p>
        <div style="margin-top: 30px;">
          <router-link to="/mountain" class="btn-outline btn-mountain">⛰️ 探索我的另一面</router-link>
        </div>
      </div>
    </section>

    <div class="divider"></div>

    <!-- 技能 -->
    <section id="skills" class="skills">
      <div class="container section-inner">
        <h2 class="text-center">目前狀態與技能</h2>
        <div class="skill-grid">
          <div v-for="skill in skills" :key="skill" class="skill-item">{{ skill }}</div>
        </div>
      </div>
    </section>

    <div class="divider"></div>

    <!-- 專案 -->
    <section id="projects" class="projects">
      <div class="container section-inner">
        <h2 class="text-center">專案經歷</h2>
        <div class="project-grid">
          <div v-for="project in projects" :key="project.title" class="project-card">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <div class="divider"></div>

    <!-- 聯絡我 -->
    <section id="contact" class="contact text-center">
      <div class="container section-inner">
        <h2>聯絡我</h2>
        <p>有任何合作機會或交流想法？歡迎隨時與我聯絡！</p>
        <div class="contact-links">
          <a href="mailto:92041925kk@gmail.com?subject=來自網站的聯絡詢問" class="contact-icon">
            <i class="fas fa-envelope"></i>
          </a>
          <a href="https://www.youtube.com/@kevint2829" target="_blank" class="youtube-btn">
            <i class="fab fa-youtube"></i>
          </a>
          <a href="https://www.twitch.tv/kevint_1001" target="_blank" class="twitch-btn">
            <i class="fab fa-twitch"></i>
          </a>
        </div>
      </div>
    </section>
  </main>

  <!-- 登山 Modal -->
  <div class="modal" :style="{ display: showModal ? 'flex' : 'none' }">
    <div class="modal-content">
      <span class="close-btn" @click="showModal = false">&times;</span>
      <h3 style="color: var(--accent); margin-bottom: 15px;">海拔 3000m+ 的視角</h3>
      <p>當我不在電腦前寫程式或做研究時，我通常在山林裡。我是登山社的一員，這項運動教會了我如何在極限環境下保持冷靜，以及團隊合作的重要性。</p>
      <div class="mountain-stats">
        <div class="stat">
          <h4>5+</h4>
          <span>攀登百岳</span>
        </div>
        <div class="stat">
          <h4>3952m</h4>
          <span>最高海拔</span>
        </div>
        <div class="stat">
          <h4>團隊嚮導</h4>
          <span>社團角色</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const showModal = ref(false)

const skills = ['在學中 (碩士)', '資料收集與分析', '專案研究與規劃', 'HTML / CSS 基礎']

const projects = [
  {
    title: '研究所專案 A',
    description: '負責文獻回顧與數據分析，這裡可以簡述您的研究內容。'
  },
  {
    title: '課堂實作專案 B',
    description: '結合課堂所學，與團隊共同開發的期末專題，負責統籌與規劃。'
  }
]
</script>
