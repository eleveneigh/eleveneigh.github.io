---
layout: page
title: Contact
permalink: /contact/
---

<div class="contact-hero">
  <img src="/assets/images/contact-hero.jpg" alt="Mountain landscape" class="hero-image">
  <div class="hero-overlay">
    <h1>Let's Connect</h1>
  </div>
</div>

<div class="contact-content">
  <div class="contact-intro">
    <p>Interested in collaborating on HCI research, AI-assisted creativity, or technology for mental well-being? I'd love to hear from you.</p>
  </div>

  <div class="contact-grid">
    <div class="contact-item">
      <h3>Academic</h3>
      <p><a href="mailto:lw403@duke.edu">lw403@duke.edu</a></p>
      <small>Research collaboration, academic inquiries</small>
    </div>
    
    <div class="contact-item">
      <h3>Personal</h3>
      <p><a href="mailto:robinwu328@gmail.com">robinwu328@gmail.com</a></p>
      <small>Creative projects, general inquiries</small>
    </div>
    
    <div class="contact-item">
      <h3>GitHub</h3>
      <p><a href="https://github.com/eleveneigh" target="_blank">eleveneigh</a></p>
      <small>Code, projects, contributions</small>
    </div>
    
    <div class="contact-item">
      <h3>LinkedIn</h3>
      <p><a href="https://www.linkedin.com/in/leyan-wu-36398b31a" target="_blank">leyan-wu</a></p>
      <small>Professional network</small>
    </div>
  </div>

  <div class="response-note">
    <p><em>I typically respond within 24-48 hours.</em></p>
  </div>
</div>

<style>
/* Contact页面样式 */
.contact-hero {
  position: relative;
  width: 100%;
  height: 300px;
  margin: -2rem -2rem 2rem -2rem;
  overflow: hidden;
}

.hero-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: brightness(0.7);
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(0, 0, 0, 0.3);
}

.hero-overlay h1 {
  color: white;
  font-size: 2.5rem;
  font-weight: 300;
  text-align: center;
  margin: 0;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.5);
}

.contact-content {
  max-width: 800px;
  margin: 0 auto;
}

.contact-intro {
  text-align: center;
  margin-bottom: 3rem;
}

.contact-intro p {
  font-size: 1.1rem;
  color: var(--text-secondary);
  line-height: 1.6;
}

.contact-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-bottom: 3rem;
}

.contact-item {
  text-align: center;
  padding: 1.5rem;
  border: 1px solid var(--border);
  transition: border-color 0.2s ease, transform 0.2s ease;
}

.contact-item:hover {
  border-color: var(--text-secondary);
  transform: translateY(-2px);
}

.contact-item h3 {
  margin: 0 0 0.5rem;
  font-size: 1.2rem;
  font-weight: 500;
  color: var(--text-primary);
}

.contact-item p {
  margin: 0 0 0.5rem;
  font-size: 1rem;
}

.contact-item a {
  color: var(--text-primary);
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.contact-item a:hover {
  border-bottom-color: var(--text-primary);
}

.contact-item small {
  font-size: 0.85rem;
  color: var(--text-accent);
  font-style: italic;
}

.response-note {
  text-align: center;
  padding: 1.5rem;
  background: #f7fafc;
  border: 1px solid var(--border);
  margin-top: 2rem;
}

.response-note p {
  margin: 0;
  color: var(--text-secondary);
}

/* 深色模式 */
@media (prefers-color-scheme: dark) {
  .response-note {
    background: #2d3748;
  }
}

/* 响应式设计 */
@media (max-width: 768px) {
  .contact-hero {
    height: 200px;
    margin: -1rem -1rem 2rem -1rem;
  }
  
  .hero-overlay h1 {
    font-size: 2rem;
  }
  
  .contact-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
  
  .contact-item {
    padding: 1rem;
  }
}

@media (max-width: 480px) {
  .contact-hero {
    height: 150px;
  }
  
  .hero-overlay h1 {
    font-size: 1.5rem;
  }
}
</style> 
