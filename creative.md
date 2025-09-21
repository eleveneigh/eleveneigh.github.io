---
layout: page
title: Creative
permalink: /creative/
---

# Creative Projects

Beyond research, I explore creativity through various mediums that inform my understanding of human expression and design.

## Photography

Visual storytelling through different perspectives and techniques.

### Featured Work

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

---

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
        <div class="zine-pages" id="zine-{{ forloop.index }}">
          <!-- 这里需要添加zine的页面图片 -->
          <div class="zine-page">
            <div class="page-placeholder">
              <h4>{{ zine.title }}</h4>
              <p>Page 1</p>
              <small>Upload page images to enable browsing</small>
            </div>
          </div>
          <div class="zine-page">
            <div class="page-placeholder">
              <h4>{{ zine.title }}</h4>
              <p>Page 2</p>
              <small>Upload page images to enable browsing</small>
            </div>
          </div>
          <div class="zine-page">
            <div class="page-placeholder">
              <h4>{{ zine.title }}</h4>
              <p>Page 3</p>
              <small>Upload page images to enable browsing</small>
            </div>
          </div>
        </div>
        
        <div class="zine-controls">
          <button class="zine-btn prev-btn" onclick="scrollZine('zine-{{ forloop.index }}', -1)">←</button>
          <span class="zine-counter">
            <span class="current-page">1</span> / <span class="total-pages">3</span>
          </span>
          <button class="zine-btn next-btn" onclick="scrollZine('zine-{{ forloop.index }}', 1)">→</button>
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

## Digital Art & Design

Exploring the intersection of technology and visual creativity.

<div class="creative-gallery">
  {% assign designs = site.data.creative.design | default: [] %}
  {% if designs.size > 0 %}
    {% for design in designs %}
    <div class="creative-item">
      <img src="{{ design.image }}" alt="{{ design.title }}" loading="lazy">
      <div class="creative-caption">
        <h4>{{ design.title }}</h4>
        <p>{{ design.description }}</p>
        {% if design.tools %}
        <div class="tools">
          {% for tool in design.tools %}<span class="tool-tag">{{ tool }}</span>{% endfor %}
        </div>
        {% endif %}
      </div>
    </div>
    {% endfor %}
  {% else %}
    <div class="creative-item placeholder">
      <div class="placeholder-content">
        <h4>🎨 Design Portfolio</h4>
        <p>UI/UX concepts, generative art, and visual experiments</p>
        <small>Add design work to <code>_data/creative.yml</code></small>
      </div>
    </div>
  {% endif %}
</div>

---

## Music & Sound

Investigating audio's role in emotional experience and creativity.

<div class="music-projects">
  {% assign music = site.data.creative.music | default: [] %}
  {% if music.size > 0 %}
    {% for track in music %}
    <div class="music-item">
      <h4>{{ track.title }}</h4>
      <p>{{ track.description }}</p>
      {% if track.audio %}
        <audio controls>
          <source src="{{ track.audio }}" type="audio/mpeg">
          Your browser does not support the audio element.
        </audio>
      {% endif %}
      {% if track.demo %}
        <a href="{{ track.demo }}" target="_blank" class="demo-link">View Demo →</a>
      {% endif %}
      {% if track.tools %}
      <div class="tools">
        {% for tool in track.tools %}<span class="tool-tag">{{ tool }}</span>{% endfor %}
      </div>
      {% endif %}
    </div>
    {% endfor %}
  {% else %}
    <div class="music-item placeholder-music">
      <h4>🎵 Audio Portfolio</h4>
      <p>Sound design, music production, and audio research projects</p>
      <small>Add audio work to <code>_data/creative.yml</code></small>
    </div>
  {% endif %}
</div>

---

## Creative Philosophy

*"Creativity is not just about making something beautiful—it's about understanding how design and art can serve human needs and emotions. My creative work directly informs my research in HCI and affective computing."*

---

*Want to collaborate on creative projects? [Get in touch](/contact)*

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

.zine-pages {
  display: flex;
  overflow-x: auto;
  scroll-behavior: smooth;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

.zine-pages::-webkit-scrollbar {
  display: none;
}

.zine-page {
  flex: 0 0 100%;
  min-height: 400px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #f9f9f9;
  border-right: 1px solid var(--border);
}

.zine-page:last-child {
  border-right: none;
}

.page-placeholder {
  text-align: center;
  padding: 2rem;
  color: var(--text-secondary);
}

.page-placeholder h4 {
  margin: 0 0 1rem;
  color: var(--text-primary);
}

.page-placeholder small {
  font-style: italic;
  color: var(--text-accent);
}

.zine-controls {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  padding: 1rem;
  background: var(--bg-card);
  border-top: 1px solid var(--border);
}

.zine-btn {
  background: var(--text-primary);
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 4px;
  cursor: pointer;
  font-size: 1rem;
  transition: background-color 0.2s ease;
}

.zine-btn:hover {
  background: var(--text-secondary);
}

.zine-btn:disabled {
  background: var(--text-accent);
  cursor: not-allowed;
}

.zine-counter {
  font-size: 0.9rem;
  color: var(--text-secondary);
  min-width: 60px;
  text-align: center;
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

/* JavaScript for zine navigation */
<script>
function scrollZine(zineId, direction) {
  const zinePages = document.getElementById(zineId);
  const pageWidth = zinePages.offsetWidth;
  const currentScroll = zinePages.scrollLeft;
  const newScroll = currentScroll + (direction * pageWidth);
  
  zinePages.scrollTo({
    left: newScroll,
    behavior: 'smooth'
  });
  
  // Update page counter
  setTimeout(() => {
    updatePageCounter(zineId);
  }, 300);
}

function updatePageCounter(zineId) {
  const zinePages = document.getElementById(zineId);
  const pageWidth = zinePages.offsetWidth;
  const currentPage = Math.round(zinePages.scrollLeft / pageWidth) + 1;
  const totalPages = zinePages.children.length;
  
  const counter = zinePages.parentElement.querySelector('.zine-counter');
  if (counter) {
    counter.querySelector('.current-page').textContent = currentPage;
    counter.querySelector('.total-pages').textContent = totalPages;
  }
  
  // Update button states
  const prevBtn = zinePages.parentElement.querySelector('.prev-btn');
  const nextBtn = zinePages.parentElement.querySelector('.next-btn');
  
  if (prevBtn) prevBtn.disabled = currentPage === 1;
  if (nextBtn) nextBtn.disabled = currentPage === totalPages;
}

// Initialize page counters when page loads
document.addEventListener('DOMContentLoaded', function() {
  const zineContainers = document.querySelectorAll('.zine-pages');
  zineContainers.forEach((container, index) => {
    updatePageCounter(`zine-${index + 1}`);
  });
});
</script>
</style>
