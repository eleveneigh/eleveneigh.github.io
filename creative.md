---
layout: page
title: Creative
permalink: /creative/
---

# Creative Projects

Beyond research, I explore creativity through various mediums that inform my understanding of human expression and design.

## Zines

<div class="zine-showcase">
  {% assign zines = site.data.creative.zines | default: [] %}
  {% if zines.size > 0 %}
    {% for zine in zines %}
    <div class="zine-container">
      <div class="zine-header">
        <h3>{{ zine.title }}</h3>
        <p>{{ zine.description }}</p>
        <div class="zine-meta">
          <span>{{ zine.year }}</span> • <span>{{ zine.category }}</span>
        </div>
      </div>
      
      <div class="zine-viewer">
        <div class="zine-scroll-container">
          <div class="zine-scroll" id="zine-{{ forloop.index }}">
            <!-- 封面页 -->
            <div class="zine-page-wide">
              <div class="page-content">
                <div class="cover-section">
                  <h2>{{ zine.title }}</h2>
                  <p>{{ zine.description }}</p>
                  <div class="cover-meta">{{ zine.year }} • {{ zine.category }}</div>
                </div>
              </div>
            </div>
            
            <!-- 内容页1 -->
            <div class="zine-page-wide">
              <div class="page-content">
                <h3>About This Zine</h3>
                <p>Fragment of Life is a visual exploration of moments and memories, capturing the essence of everyday experiences through photography and storytelling.</p>
                <p>This project represents a journey through different perspectives, finding beauty in the ordinary and meaning in the fleeting.</p>
              </div>
            </div>
            
            <!-- 内容页2 -->
            <div class="zine-page-wide">
              <div class="page-content">
                <h3>Process & Inspiration</h3>
                <p>Created as a course project, this zine combines photographic storytelling with thoughtful design to create an immersive reading experience.</p>
                <p>Each page tells a story, each image captures a moment, and together they form a complete narrative of life's fragments.</p>
              </div>
            </div>
            
            <!-- 内容页3 -->
            <div class="zine-page-wide">
              <div class="page-content">
                <h3>Visual Storytelling</h3>
                <p>The zine explores themes of memory, time, and human connection through carefully curated imagery and thoughtful layout design.</p>
                <p>Each spread invites the reader to pause and reflect on the beauty found in everyday moments.</p>
              </div>
            </div>
            
            <!-- 内容页4 -->
            <div class="zine-page-wide">
              <div class="page-content">
                <h3>Reflection</h3>
                <p>Through this project, I discovered how visual narratives can capture emotions and experiences that words alone cannot express.</p>
                <p>Fragment of Life serves as both a creative expression and a meditation on the fleeting nature of our most precious moments.</p>
              </div>
            </div>
          </div>
        </div>
        
        <div class="zine-actions">
          <a href="{{ zine.pdf }}" target="_blank" class="view-pdf">Download PDF →</a>
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
</div>

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

/* Zine展示 */
.zine-showcase {
  margin: 2rem 0;
}

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

.zine-viewer {
  background: var(--bg-card);
}

.zine-scroll-container {
  overflow-x: auto;
  overflow-y: hidden;
  scroll-behavior: smooth;
  scrollbar-width: thin;
  scrollbar-color: var(--text-accent) transparent;
  margin: -2rem;
  padding: 2rem;
}

.zine-scroll-container::-webkit-scrollbar {
  height: 8px;
}

.zine-scroll-container::-webkit-scrollbar-track {
  background: transparent;
}

.zine-scroll-container::-webkit-scrollbar-thumb {
  background: var(--text-accent);
  border-radius: 4px;
}

.zine-scroll-container::-webkit-scrollbar-thumb:hover {
  background: var(--text-secondary);
}

.zine-scroll {
  display: flex;
  gap: 2rem;
  width: max-content;
  padding: 1rem 0;
}

.zine-page-wide {
  flex: 0 0 600px;
  min-height: 400px;
  background: white;
  border: 1px solid var(--border);
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.zine-page-wide:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
}

.page-content {
  padding: 2rem;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.cover-section {
  text-align: center;
}

.cover-section h2 {
  font-size: 2.5rem;
  font-weight: 300;
  margin: 0 0 1rem;
  color: var(--text-primary);
  line-height: 1.2;
}

.cover-section p {
  font-size: 1.2rem;
  color: var(--text-secondary);
  margin: 0 0 2rem;
  line-height: 1.5;
}

.cover-meta {
  font-size: 1rem;
  color: var(--text-accent);
  font-weight: 500;
}

.page-content h3 {
  font-size: 1.5rem;
  font-weight: 500;
  margin: 0 0 1.5rem;
  color: var(--text-primary);
  border-bottom: 2px solid var(--border);
  padding-bottom: 0.5rem;
}

.page-content p {
  font-size: 1rem;
  color: var(--text-secondary);
  margin: 0 0 1.2rem;
  line-height: 1.6;
}

.page-content p:last-child {
  margin-bottom: 0;
}

.zine-actions {
  padding: 1rem;
  text-align: center;
  background: #f7fafc;
  border-top: 1px solid var(--border);
}

.view-pdf {
  color: var(--text-primary);
  text-decoration: none;
  font-weight: 500;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.view-pdf:hover {
  border-bottom-color: var(--text-primary);
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

</style>
