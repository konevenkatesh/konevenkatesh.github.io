---
layout: page
icon: fas fa-rss
order: 3
---

<style>
    .blog-card {
        background: var(--card-bg);
        border: 1px solid var(--border-color);
        border-radius: 12px;
        padding: 1.5rem;
        transition: transform 0.2s, box-shadow 0.2s;
        display: block;
        text-decoration: none;
        color: inherit;
        margin-bottom: 2rem;
    }

    .blog-card:hover {
        transform: translateY(-4px);
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        text-decoration: none;
        color: inherit;
    }

    .blog-meta {
        font-size: 0.85rem;
        color: var(--text-muted-color);
        margin-bottom: 0.5rem;
        text-transform: uppercase;
        letter-spacing: 0.5px;
    }

    .blog-title {
        font-size: 1.4rem;
        margin-bottom: 0.75rem;
        color: var(--heading-color);
        font-weight: 600;
    }

    .blog-excerpt {
        color: var(--text-color);
        line-height: 1.6;
        font-size: 0.95rem;
    }
</style>

<div id="blog-list">
    <a href="/blog/ai-in-construction.html" class="blog-card">
        <div class="blog-meta">December 2024 &bull; Technical Deep Dive</div>
        <h3 class="blog-title">AI and Construction Data: Bridging Complexity Through Intelligent Document Systems</h3>
        <p class="blog-excerpt">
            A technical exploration of Retrieval-Augmented Generation (RAG) applications in construction project
            management. Learn how we can bridge the gap between complex construction data and intelligent systems.
        </p>
    </a>

    {% for post in site.posts %}
    <a href="{{ post.url | relative_url }}" class="blog-card">
        <div class="blog-meta">{{ post.date | date: "%B %Y" }} &bull; {{ post.categories | join: ", " }}</div>
        <h3 class="blog-title">{{ post.title }}</h3>
        <p class="blog-excerpt">
            {{ post.excerpt | strip_html | truncate: 150 }}
        </p>
    </a>
    {% endfor %}
</div>
