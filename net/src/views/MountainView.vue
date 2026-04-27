<template>
  <main style="padding-top: 100px;">
    <!-- 大首圖 -->
    <section class="container">
      <div class="hero-banner">
        <img src="https://i.postimg.cc/KzyLdv46/20240421-053558.jpg" alt="登山大首圖" />
        <div class="banner-overlay">
          <span class="location-tag">📍 奇萊南峰 | 海拔 3358m 黃金草原</span>
        </div>
      </div>
    </section>

    <!-- 標題介紹 -->
    <section class="text-center">
      <div class="container section-inner">
        <h1 class="glitch-text" style="color: #fff; font-size: 3rem; margin-bottom: 20px;">
          海拔 3000m+ 的視角
        </h1>
        <p>
          當我不在電腦前寫程式或做研究時，我通常在山林裡。<br />
          身為登山社的一員，這項運動教會了我如何在極限環境下保持冷靜，以及團隊合作的重要性。
        </p>
      </div>
    </section>

    <!-- 相簿 -->
    <section class="gallery-section">
      <div class="container">
        <div class="photo-gallery">
          <div v-for="photo in photos" :key="photo.title" class="photo-card">
            <img :src="photo.src" :alt="photo.alt" />
            <div class="photo-caption">
              <h3>{{ photo.title }}</h3>
              <p>{{ photo.caption }}</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 返回主頁 -->
    <div class="text-center" style="padding-bottom: 60px;">
      <router-link to="/" class="btn-outline">← 返回主頁</router-link>
    </div>
  </main>
</template>

<script setup>
const photos = [
  {
    src: 'https://i.postimg.cc/85rpB1tZ/20240625-0919452.jpg',
    alt: '百岳登頂照',
    title: '百岳登頂紀錄',
    caption: '克服高山症的極限挑戰'
  },
  {
    src: 'https://i.postimg.cc/V64Rg8vX/IMG-8680.jpg',
    alt: '團隊合作',
    title: '團隊嚮導',
    caption: '帶領社員安全下山是最大的責任'
  },
  {
    src: 'https://i.postimg.cc/DZFF9thJ/20240915-130341.jpg',
    alt: '泳渡日月潭',
    title: '其他運動',
    caption: '除了爬山，泳渡日月潭也是可以的'
  }
]
</script>
