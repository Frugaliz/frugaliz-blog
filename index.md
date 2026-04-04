---
layout: default
title: Frugaliz
---

<style>
  body {
    background-color: #0d0d0d !important;
    color: #e0e0e0;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  }

  .site-header, .page-header {
    background: #0d0d0d !important;
    background-image: none !important;
    border-bottom: 1px solid #1e1e1e;
    padding: 24px 0;
    min-height: unset;
  }

  .main-content { max-width: 860px; margin: 0 auto; padding: 0 24px 80px; }

  /* ── Hero ── */
  .fg-hero {
    text-align: center;
    padding: 64px 0 48px;
    border-bottom: 1px solid #1e1e1e;
    margin-bottom: 56px;
  }
  .fg-logo {
    font-size: 38px;
    font-weight: 900;
    letter-spacing: 8px;
    background: linear-gradient(90deg, #00ffaa, #00ccff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    display: inline-block;
    margin-bottom: 10px;
  }
  .fg-tagline {
    color: #444;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin: 0 0 32px;
  }
  .fg-stats {
    display: inline-flex;
    gap: 40px;
    background: #111;
    border: 1px solid #1e1e1e;
    border-radius: 12px;
    padding: 18px 36px;
  }
  .fg-stat-item { text-align: center; }
  .fg-stat-num {
    font-size: 22px;
    font-weight: 700;
    background: linear-gradient(90deg, #00ffaa, #00ccff);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    display: block;
  }
  .fg-stat-label {
    color: #444;
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin-top: 2px;
    display: block;
  }

  /* ── Section header ── */
  .fg-section-header {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 28px;
  }
  .fg-section-title {
    color: #fff;
    font-size: 11px;
    letter-spacing: 3px;
    text-transform: uppercase;
    margin: 0;
  }
  .fg-section-line {
    flex: 1;
    height: 1px;
    background: #1e1e1e;
  }

  /* ── Cards ── */
  .fg-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(340px, 1fr));
    gap: 20px;
  }
  .fg-card {
    background: #111;
    border: 1px solid #1e1e1e;
    border-radius: 12px;
    padding: 24px;
    text-decoration: none;
    display: block;
    transition: border-color 0.2s, background 0.2s;
    position: relative;
    overflow: hidden;
  }
  .fg-card:hover {
    border-color: #2a2a2a;
    background: #141414;
    text-decoration: none;
  }
  .fg-card-accent {
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, #00ffaa, #00ccff);
    opacity: 0;
    transition: opacity 0.2s;
  }
  .fg-card:hover .fg-card-accent { opacity: 1; }

  .fg-card-meta {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 12px;
  }
  .fg-card-date {
    color: #444;
    font-size: 11px;
    letter-spacing: 1px;
    text-transform: uppercase;
  }
  .fg-card-score {
    display: flex;
    align-items: center;
    gap: 6px;
  }
  .fg-score-badge {
    font-size: 12px;
    font-weight: 700;
    padding: 3px 10px;
    border-radius: 20px;
    border: 1px solid;
  }
  .fg-score-high  { color: #00ffaa; border-color: #00ffaa22; background: #00ffaa0d; }
  .fg-score-mid   { color: #00ccff; border-color: #00ccff22; background: #00ccff0d; }
  .fg-score-low   { color: #ff6b6b; border-color: #ff6b6b22; background: #ff6b6b0d; }
  .fg-score-label { color: #333; font-size: 10px; letter-spacing: 1px; text-transform: uppercase; }

  .fg-card-title {
    color: #e0e0e0;
    font-size: 16px;
    font-weight: 600;
    line-height: 1.45;
    margin: 0 0 10px;
  }
  .fg-card-excerpt {
    color: #555;
    font-size: 13px;
    line-height: 1.65;
    margin: 0 0 18px;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
  }
  .fg-card-footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-top: 16px;
    border-top: 1px solid #1a1a1a;
  }
  .fg-read-more {
    color: #00ccff;
    font-size: 12px;
    letter-spacing: 1px;
    text-transform: uppercase;
  }
  .fg-arrow {
    color: #333;
    font-size: 16px;
    transition: color 0.2s, transform 0.2s;
  }
  .fg-card:hover .fg-arrow {
    color: #00ffaa;
    transform: translateX(4px);
  }

  /* ── Empty state ── */
  .fg-empty {
    text-align: center;
    padding: 80px 0;
    color: #333;
  }
  .fg-empty-icon {
    font-size: 32px;
    margin-bottom: 16px;
  }
  .fg-empty p {
    font-size: 13px;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin: 0;
  }

  /* ── Footer ── */
  .fg-footer {
    text-align: center;
    padding: 48px 0 0;
    border-top: 1px solid #1a1a1a;
    margin-top: 64px;
  }
  .fg-footer p {
    color: #333;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    margin: 0;
  }
</style>

<div class="main-content">

  <!-- Hero -->
  <div class="fg-hero">
    <div class="fg-logo">FRUGALIZ</div>
    <p class="fg-tagline">Trié par l'IA. Validé pour toi.</p>
    <div class="fg-stats">
      <div class="fg-stat-item">
        <span class="fg-stat-num">{{ site.posts | size }}</span>
        <span class="fg-stat-label">Articles publiés</span>
      </div>
      <div class="fg-stat-item">
        <span class="fg-stat-num">100%</span>
        <span class="fg-stat-label">Généré par IA</span>
      </div>
      <div class="fg-stat-item">
        <span class="fg-stat-num">0</span>
        <span class="fg-stat-label">Pub ni biais</span>
      </div>
    </div>
  </div>

  <!-- Listing -->
  <div class="fg-section-header">
    <p class="fg-section-title">Derniers bons plans</p>
    <div class="fg-section-line"></div>
  </div>

  {% if site.posts.size == 0 %}
  <div class="fg-empty">
    <div class="fg-empty-icon">📡</div>
    <p>En attente du prochain scan IA</p>
  </div>
  {% else %}
  <div class="fg-grid">
    {% for post in site.posts %}
    {% assign score = post.score_frugaliz | default: 0 %}
    {% if score >= 75 %}{% assign score_class = "fg-score-high" %}
    {% elsif score >= 50 %}{% assign score_class = "fg-score-mid" %}
    {% else %}{% assign score_class = "fg-score-low" %}{% endif %}

    <a class="fg-card" href="{{ site.baseurl }}{{ post.url }}">
      <div class="fg-card-accent"></div>
      <div class="fg-card-meta">
        <span class="fg-card-date">{{ post.date | date: "%d %b %Y" }}</span>
        {% if score > 0 %}
        <div class="fg-card-score">
          <span class="fg-score-label">Score</span>
          <span class="fg-score-badge {{ score_class }}">{{ score }}/100</span>
        </div>
        {% endif %}
      </div>
      <h2 class="fg-card-title">{{ post.title }}</h2>
      <p class="fg-card-excerpt">{{ post.excerpt | strip_html | truncatewords: 22 }}</p>
      <div class="fg-card-footer">
        <span class="fg-read-more">Lire l'analyse</span>
        <span class="fg-arrow">→</span>
      </div>
    </a>
    {% endfor %}
  </div>
  {% endif %}

  <!-- Footer -->
  <div class="fg-footer">
    <p>Frugaliz — pipeline automatisé · aucun article sponsorisé</p>
  </div>

</div>
