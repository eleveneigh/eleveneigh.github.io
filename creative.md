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

<div class="book-showcase">
  {% assign books = site.data.creative.zines | default: [] %}
  {% if books.size > 0 %}
    <div class="book-scroll">
      {% for book in books %}
      <div class="book-item">
        <div class="book-cover">
          <div class="book-preview">
            <h3>{{ book.title }}</h3>
            <p>{{ book.description }}</p>
            <div class="book-meta">
              <span class="book-year">{{ book.year }}</span>
              <span class="book-category">{{ book.category }}</span>
            </div>
          </div>
        </div>
        <div class="book-actions">
          <a href="{{ book.pdf }}" target="_blank" class="view-book">View PDF →</a>
        </div>
      </div>
      {% endfor %}
    </div>
  {% else %}
    <div class="book-placeholder">
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

/* 书籍展示 */
.book-showcase {
  margin: 2rem 0;
  overflow: hidden;
}

.book-scroll {
  display: flex;
  gap: 2rem;
  overflow-x: auto;
  padding: 1rem 0;
  scroll-behavior: smooth;
  scrollbar-width: thin;
  scrollbar-color: var(--text-accent) transparent;
}

.book-scroll::-webkit-scrollbar {
  height: 6px;
}

.book-scroll::-webkit-scrollbar-track {
  background: transparent;
}

.book-scroll::-webkit-scrollbar-thumb {
  background: var(--text-accent);
  border-radius: 3px;
}

.book-item {
  flex: 0 0 280px;
  display: flex;
  flex-direction: column;
  border: 1px solid var(--border);
  transition: border-color 0.2s ease, transform 0.2s ease;
}

.book-item:hover {
  border-color: var(--text-secondary);
  transform: translateY(-2px);
}

.book-cover {
  background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
  padding: 2rem;
  text-align: center;
  min-height: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.book-preview h3 {
  margin: 0 0 1rem;
  font-size: 1.3rem;
  font-weight: 500;
  color: var(--text-primary);
}

.book-preview p {
  margin: 0 0 1rem;
  font-size: 0.9rem;
  color: var(--text-secondary);
  line-height: 1.4;
}

.book-meta {
  display: flex;
  gap: 1rem;
  justify-content: center;
  margin-top: 1rem;
}

.book-year, .book-category {
  font-size: 0.8rem;
  color: var(--text-accent);
  background: rgba(255, 255, 255, 0.7);
  padding: 0.2rem 0.5rem;
  border-radius: 3px;
}

.book-actions {
  padding: 1rem;
  text-align: center;
  background: var(--bg-card);
}

.view-book {
  color: var(--text-primary);
  text-decoration: none;
  font-weight: 500;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.view-book:hover {
  border-bottom-color: var(--text-primary);
}

.book-placeholder {
  text-align: center;
  padding: 3rem;
  background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
  border: 1px solid var(--border);
}

.book-placeholder h4 {
  margin: 0 0 1rem;
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--text-primary);
}

.book-placeholder p {
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
}
</style>
