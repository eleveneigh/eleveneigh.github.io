---
layout: page
title: Creative
permalink: /creative/
---

Beyond research, I explore creativity through various mediums that inform my understanding of human expression and design.

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
              <h1>{{ zine.title }}</h1>
              <p>{{ zine.description }}</p>
              <div class="slide-meta">{{ zine.year }} • {{ zine.category }}</div>
            </div>
          </div>
          
          <!-- 示例页面 - 这里可以替换为实际的PDF页面图片 -->
          <div class="zine-slide page-slide">
            <div class="page-content">
              <div class="page-placeholder">
                <h3>Page 1</h3>
                <p>Upload page images from your PDF to showcase the actual content</p>
                <small>Convert PDF pages to images and add them here</small>
              </div>
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <div class="page-placeholder">
                <h3>Page 2</h3>
                <p>Each page can display your actual zine content</p>
                <small>Add real page images for full experience</small>
              </div>
            </div>
          </div>
          
          <div class="zine-slide page-slide">
            <div class="page-content">
              <div class="page-placeholder">
                <h3>Page 3</h3>
                <p>Visual storytelling and photography</p>
                <small>Showcase your creative work</small>
              </div>
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

## Photography

Visual storytelling through different perspectives and techniques.

<div class="creative-gallery">
  {% assign photos = site.data.creative.photography | default: [] %}
  {% if photos.size > 0 %}
    {% for photo in photos %}
    <div class="creative-item">
      <img src="{{ photo.image }}" alt="{{ photo.title }}" loading="lazy">
      <div class="creative-caption">
        <h4>{{ photo.title }}</h4>
        <p>{{ photo.description }}</p>
      </div>
    </div>
    {% endfor %}
  {% else %}
    <div class="creative-item placeholder">
      <div class="placeholder-content">
        <h4>📸 Photography Portfolio</h4>
        <p>Add your photos to showcase your visual work</p>
        <small>Upload images and update <code>_data/creative.yml</code></small>
      </div>
    </div>
  {% endif %}
</div>

<style>
.creative-gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.5rem;
  margin: 2rem 0;
}

.creative-item {
  border: 1px solid var(--border);
  transition: border-color 0.2s ease;
  overflow: hidden;
}

.creative-item:hover {
  border-color: var(--text-secondary);
}

.creative-item img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  display: block;
}

.creative-item.placeholder {
  background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
  min-height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.placeholder-content h4 {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
  font-weight: 500;
  color: var(--text-primary);
}

.placeholder-content p {
  margin: 0 0 0.5rem;
  font-size: 0.9rem;
  color: var(--text-secondary);
}

.placeholder-content small {
  font-size: 0.8rem;
  color: var(--text-accent);
  font-style: italic;
}

.creative-caption {
  padding: 1rem;
  background: var(--bg-card);
}

.creative-caption h4 {
  margin: 0 0 0.5rem;
  font-size: 1rem;
  font-weight: 500;
  color: var(--text-primary);
}

.creative-caption p {
  margin: 0;
  font-size: 0.9rem;
  color: var(--text-secondary);
  line-height: 1.4;
}

/* 深色模式 */
@media (prefers-color-scheme: dark) {
  .creative-item.placeholder {
    background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
  }
}

/* 音乐项目 */
.music-projects {
  margin: 2rem 0;
}

.music-item {
  border: 1px solid var(--border);
  padding: 1.5rem;
  margin-bottom: 1.5rem;
  transition: border-color 0.2s ease;
}

.music-item:hover {
  border-color: var(--text-secondary);
}

.music-item h4 {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
  font-weight: 500;
  color: var(--text-primary);
}

.music-item p {
  margin: 0 0 1rem;
  color: var(--text-secondary);
}

.music-item audio {
  width: 100%;
  margin: 1rem 0;
}

.demo-link {
  display: inline-block;
  color: var(--text-primary);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
  margin: 0.5rem 0;
}

.demo-link:hover {
  border-bottom-color: var(--text-primary);
}

.placeholder-music {
  background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
  text-align: center;
  padding: 2rem;
}

.placeholder-music h4 {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
  font-weight: 500;
  color: var(--text-primary);
}

.placeholder-music p {
  margin: 0 0 0.5rem;
  color: var(--text-secondary);
}

.placeholder-music small {
  font-size: 0.8rem;
  color: var(--text-accent);
  font-style: italic;
}

/* 工具标签 */
.tools {
  margin-top: 1rem;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tool-tag {
  font-size: 0.8rem;
  color: var(--text-accent);
  background: #f7fafc;
  padding: 0.2rem 0.5rem;
  border: 1px solid var(--border);
  border-radius: 3px;
}

/* 深色模式 */
@media (prefers-color-scheme: dark) {
  .creative-item.placeholder {
    background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
  }
  
  .placeholder-music {
    background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
  }
  
  .tool-tag {
    background: #2d3748;
    border-color: var(--border);
  }
}

/* Zine容器 */
.zine-container {
  margin-bottom: 3rem;
  border: 1px solid var(--border);
  border-radius: 8px;
  overflow: hidden;
}

.zine-header {
  padding: 1.5rem;
  background: #f7fafc;
  border-bottom: 1px solid var(--border);
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
  padding: 1rem;
  background: transparent;
  border: none;
  margin: 1rem;
}

.zine-scroll-hint p {
  margin: 0;
  color: var(--text-accent);
  font-size: 0.9rem;
  font-weight: 500;
}

/* 页面占位符 */
.page-slide {
  background: white;
}

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
  width: 100vw;
  margin-left: calc(-50vw + 50%);
  margin-right: calc(-50vw + 50%);
  overflow-x: auto;
  overflow-y: hidden;
  scroll-behavior: smooth;
  scrollbar-width: thin;
  scrollbar-color: var(--text-accent) transparent;
  position: relative;
  z-index: 1;
  /* 突破wrapper限制 */
  left: 50%;
  transform: translateX(-50%);
  /* 确保只能横向滚动 */
  touch-action: pan-x;
  -webkit-overflow-scrolling: touch;
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
}

.zine-slide {
  flex: 0 0 100vw;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--bg-card);
  border-right: 1px solid var(--border);
  position: relative;
}

.zine-slide:last-child {
  border-right: none;
}

.cover-slide {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.end-slide {
  background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
  color: white;
}

.slide-content {
  max-width: 800px;
  text-align: center;
  padding: 2rem;
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
