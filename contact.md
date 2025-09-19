---
layout: page
title: Contact
permalink: /contact/
---

<div class="contact-layout">
  <div class="contact-info">
    <p>Interested in collaborating on HCI research, AI-assisted creativity, or technology for mental well-being? I'd love to hear from you.</p>
    
    <div class="contact-list">
      <div class="contact-item">
        <strong>Academic</strong><br>
        <a href="mailto:lw403@duke.edu">lw403@duke.edu</a>
      </div>
      
      <div class="contact-item">
        <strong>Personal</strong><br>
        <a href="mailto:robinwu328@gmail.com">robinwu328@gmail.com</a>
      </div>
      
      <div class="contact-item">
        <strong>GitHub</strong><br>
        <a href="https://github.com/eleveneigh" target="_blank">eleveneigh</a>
      </div>
      
      <div class="contact-item">
        <strong>LinkedIn</strong><br>
        <a href="https://www.linkedin.com/in/leyan-wu-36398b31a" target="_blank">leyan-wu</a>
      </div>
    </div>
    
    <p class="response-time"><em>I typically respond within 24-48 hours.</em></p>
  </div>
  
  <div class="contact-image">
    <img src="/assets/images/contact-hero.jpg" alt="Mountain landscape">
  </div>
</div>

<style>
.contact-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  align-items: start;
  margin: 2rem 0;
}

.contact-info p {
  margin-bottom: 2rem;
  color: var(--text-secondary);
  line-height: 1.6;
}

.contact-list {
  margin-bottom: 2rem;
}

.contact-item {
  margin-bottom: 1.5rem;
  padding-bottom: 1rem;
  border-bottom: 1px solid var(--border);
}

.contact-item:last-child {
  border-bottom: none;
  margin-bottom: 0;
}

.contact-item strong {
  color: var(--text-primary);
  font-weight: 500;
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

.response-time {
  color: var(--text-accent);
  font-size: 0.9rem;
  margin: 0;
}

.contact-image img {
  width: 100%;
  height: auto;
  border: 1px solid var(--border);
}

/* 响应式设计 */
@media (max-width: 768px) {
  .contact-layout {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
  
  .contact-image {
    order: -1;
  }
}
</style> 
