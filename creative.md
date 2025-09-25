---
layout: page
title: Creative
permalink: /creative/
---

Beyond research, I explore creativity through various mediums that inform my understanding of human expression and design.

<!-- Updated with original PDF images -->
## Zines

{% assign zines = site.data.creative.zines | default: [] %}
{% if zines.size > 0 %}
  {% for zine in zines %}
  <div class="zine-container">
    <div class="zine-header">
      <h3>{{ zine.title }}</h3>
      <p>{{ zine.description }}</p>
      <div class="zine-meta">{{ zine.year }} • {{ zine.category }}</div>
    </div>
    
    <div class="zine-viewer">
      <!-- 横向滚动页面 -->
      <div class="zine-scroll-hint">
        <p>← Scroll to browse pages →</p>
      </div>
      
      <div class="zine-full-width">
        <div class="zine-scroll-horizontal">
          <!-- 封面页 -->
          <div class="zine-slide cover-slide">
            <div class="slide-content">
              <h1>Fragment of Life</h1>
              <p>A visual journey through moments and memories</p>
              <div class="slide-meta">2024 • photography</div>
            </div>
          </div>
          
          <!-- Fragment of Life 实际页面内容 -->
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_1.png' | relative_url }}" alt="Fragment of Life - Page 1" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_2.png' | relative_url }}" alt="Fragment of Life - Page 2" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_3.png' | relative_url }}" alt="Fragment of Life - Page 3" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_4.png' | relative_url }}" alt="Fragment of Life - Page 4" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_5.png' | relative_url }}" alt="Fragment of Life - Page 5" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_6.png' | relative_url }}" alt="Fragment of Life - Page 6" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_7.png' | relative_url }}" alt="Fragment of Life - Page 7" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_8.png' | relative_url }}" alt="Fragment of Life - Page 8" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_9.png' | relative_url }}" alt="Fragment of Life - Page 9" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_10.png' | relative_url }}" alt="Fragment of Life - Page 10" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_11.png' | relative_url }}" alt="Fragment of Life - Page 11" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_12.png' | relative_url }}" alt="Fragment of Life - Page 12" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_13.png' | relative_url }}" alt="Fragment of Life - Page 13" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_14.png' | relative_url }}" alt="Fragment of Life - Page 14" class="zine-page-image">
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <img src="{{ '/assets/images/fragments/page_15.png' | relative_url }}" alt="Fragment of Life - Page 15" class="zine-page-image">
            </div>
          </div>
          
          <!-- 结束页 -->
          <div class="zine-slide end-slide">
            <div class="slide-content">
              <h2>End of Journey</h2>
              <p>Thank you for experiencing Fragment of Life</p>
              <div class="end-message">A visual exploration of moments and memories</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  {% endfor %}
{% else %}
  <div class="zine-placeholder">
    <h4>📚 Zines</h4>
    <p>Add your zine projects here</p>
  </div>
{% endif %}

---

<style>
/* CSS变量定义 */
:root {
  --max-width: 800px;
  --text-primary: #2d3748;
  --text-secondary: #718096;
  --text-accent: #4a5568;
  --border: #e2e8f0;
  --bg-card: #ffffff;
  --spacing: 2rem;
}

/* 深色模式 */
@media (prefers-color-scheme: dark) {
  :root {
    --text-primary: #f7fafc;
    --text-secondary: #a0aec0;
    --text-accent: #cbd5e0;
    --border: #2d3748;
    --bg-card: #1a202c;
  }
}

/* Zine容器 */
.zine-container {
  margin-bottom: 0;
  border: none;
  border-radius: 0;
  overflow: hidden;
  width: 100vw !important;
  margin-left: calc(-50vw + 50%) !important;
  margin-right: calc(-50vw + 50%) !important;
  position: relative;
  left: 50% !important;
  transform: translateX(-50%) !important;
  max-width: none !important;
}

.zine-header {
  padding: 0.5rem;
  background: transparent;
  border-bottom: none;
}

.zine-header h3 {
  margin: 0 0 0.5rem;
  font-size: 1.4rem;
  font-weight: 500;
  color: var(--text-primary);
}

.zine-header p {
  margin: 0 0 1rem;
  color: var(--text-secondary);
  line-height: 1.5;
}

.zine-meta {
  font-size: 0.9rem;
  color: var(--text-accent);
}

/* Zine查看器 */
.zine-viewer {
  position: relative;
  width: 100%;
}

/* 滚动提示 */
.zine-scroll-hint {
  text-align: center;
  padding: 0;
  background: transparent;
  border: none;
  margin: 0;
}

.zine-scroll-hint p {
  margin: 0;
  color: var(--text-accent);
  font-size: 0.9rem;
  font-weight: 500;
}

/* 页面内容 */
.page-slide {
  background: white;
}

.page-content {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.zine-page-image {
  width: 100%;
  height: 100%;
  object-fit: contain;
  border-radius: 0;
  box-shadow: none;
  display: block;
}

/* 页面占位符（保留作为备用） */
.page-placeholder {
  text-align: center;
  padding: 2rem;
  color: var(--text-secondary);
}

.page-placeholder h3 {
  margin: 0 0 1rem;
  color: var(--text-primary);
  font-size: 1.5rem;
}

.page-placeholder p {
  margin: 0 0 1rem;
  font-size: 1rem;
  line-height: 1.5;
}

.page-placeholder small {
  font-style: italic;
  color: var(--text-accent);
}

/* 全屏横向滚动Zine */
.zine-full-width {
  width: 100vw !important;
  margin-left: calc(-50vw + 50%) !important;
  margin-right: calc(-50vw + 50%) !important;
  overflow-x: auto;
  overflow-y: hidden;
  scroll-behavior: smooth;
  scrollbar-width: thin;
  scrollbar-color: var(--text-accent) transparent;
  position: relative;
  z-index: 1;
  /* 突破wrapper限制 */
  left: 50% !important;
  transform: translateX(-50%) !important;
  /* 确保只能横向滚动 */
  touch-action: pan-x;
  -webkit-overflow-scrolling: touch;
  /* 消除所有间距 */
  margin-top: 0;
  margin-bottom: 0;
  padding: 0;
  max-width: none !important;
}

.zine-full-width::-webkit-scrollbar {
  height: 12px;
}

.zine-full-width::-webkit-scrollbar-track {
  background: transparent;
}

.zine-full-width::-webkit-scrollbar-thumb {
  background: var(--text-accent);
  border-radius: 6px;
}

.zine-full-width::-webkit-scrollbar-thumb:hover {
  background: var(--text-secondary);
}

.zine-scroll-horizontal {
  display: flex;
  width: max-content;
  height: 80vh;
  min-height: 500px;
  position: relative;
  /* 确保flex布局正确 */
  flex-direction: row;
  align-items: stretch;
  margin: 0;
  padding: 0;
  gap: 0;
}

.zine-slide {
  flex: 0 0 100vw;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--bg-card);
  border-right: none;
  position: relative;
  margin: 0;
  padding: 0;
  width: 100vw;
  box-sizing: border-box;
}

.zine-slide:last-child {
  border-right: none;
}

.cover-slide {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  background-size: 100% 100%;
  background-repeat: no-repeat;
}

.end-slide {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  color: white;
  background-size: 100% 100%;
  background-repeat: no-repeat;
}

.slide-content {
  max-width: 100vw;
  width: 100vw;
  text-align: center;
  padding: 2rem;
  box-sizing: border-box;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  /* 确保内容在屏幕中央 */
  position: relative;
  left: 50%;
  transform: translateX(-50%);
}

.slide-content h1 {
  font-size: 4rem;
  font-weight: 300;
  margin: 0 0 1.5rem;
  line-height: 1.1;
}

.slide-content h2 {
  font-size: 2.5rem;
  font-weight: 400;
  margin: 0 0 2rem;
  line-height: 1.2;
}

.slide-content p {
  font-size: 1.2rem;
  line-height: 1.6;
  margin: 0 0 1.5rem;
  opacity: 0.9;
}

.slide-content p:last-child {
  margin-bottom: 0;
}

.slide-meta {
  font-size: 1rem;
  opacity: 0.8;
  font-weight: 500;
  margin-top: 2rem;
}

.end-message {
  font-size: 1rem;
  opacity: 0.8;
  font-weight: 400;
  margin-top: 2rem;
  font-style: italic;
}

.zine-placeholder {
  text-align: center;
  padding: 3rem;
  background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
  border: 1px solid var(--border);
}

.zine-placeholder h4 {
  margin: 0 0 1rem;
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--text-primary);
}

.zine-placeholder p {
  margin: 0;
  color: var(--text-secondary);
}

/* 深色模式 */
@media (prefers-color-scheme: dark) {
  .book-cover {
    background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
  }
  
  .book-year, .book-category {
    background: rgba(45, 55, 72, 0.7);
  }
  
  .book-placeholder {
    background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
  }
}

/* 响应式 */
@media (max-width: 768px) {
  .creative-gallery {
    grid-template-columns: 1fr;
    gap: 1rem;
  }
  
  .music-item {
    padding: 1rem;
  }
  
  .book-item {
    flex: 0 0 240px;
  }
  
  .book-cover {
    padding: 1.5rem;
    min-height: 160px;
  }
  
  .book-preview h3 {
    font-size: 1.1rem;
  }
  
  .zine-header {
    background: #2d3748;
  }
  
  .zine-actions {
    background: #2d3748;
  }
  
  .zine-page {
    background: #1a202c;
  }
}

/* 深色模式 */
@media (prefers-color-scheme: dark) {
  .zine-slide {
    background: #1a202c;
    border-color: #374151;
  }
  
  .cover-slide {
    background: linear-gradient(135deg, #4c1d95 0%, #7c3aed 100%);
  }
  
  .end-slide {
    background: linear-gradient(135deg, #be185d 0%, #ec4899 100%);
  }
}

/* 响应式设计 */
@media (max-width: 768px) {
  .zine-scroll-horizontal {
    height: 70vh;
    min-height: 400px;
  }
  
  .slide-content h1 {
    font-size: 2.5rem;
  }
  
  .slide-content h2 {
    font-size: 2rem;
  }
  
  .slide-content p {
    font-size: 1rem;
  }
  
  .slide-content {
    padding: 1.5rem;
  }
}

</style>
