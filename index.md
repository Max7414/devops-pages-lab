title: Home
---

<link rel="stylesheet" href="{{ '/assets/css/custom.css' | relative_url }}">

<section class="hero">
  <h1>Max7414 · DevOps Pages Lab</h1>
  <p>Automated activity dashboards and Pages deployments for the 2025 DevOps course.</p>
</section>

{% capture readme_content %}{% include_relative README.md %}{% endcapture %}
<div class="activity-highlight">
{{ readme_content | markdownify }}
</div>
