---
layout: page
icon: fas fa-code-branch
order: 4
---

<style>
    /* Import fonts */
    @import url('https://fonts.googleapis.com/css2?family=EB+Garamond:wght@400;500;600;700&family=Inter:wght@400;500;600&display=swap');

    /* Hide Chirpy default elements */
    h1.dynamic-title,
    .post-title,
    .page-title,
    #page-title,
    .post-meta {
        display: none !important;
    }

    /* Projects Container */
    .projects-portfolio {
        max-width: 1100px;
        margin: 0 auto;
        padding: 0 1rem 4rem;
        font-family: 'EB Garamond', serif;
        line-height: 1.8;
        font-size: 18px;
    }

    .projects-portfolio * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    /* Custom color variables */
    .projects-portfolio {
        --accent: #1d4ed8;
        --accent-light: #3b82f6;
        --text: #0f172a;
        --text-medium: #475569;
        --text-light: #64748b;
        --border: #cbd5e0;
        --surface: #f1f5f9;
        --success: #059669;
        --warning: #d97706;
        --info: #0284c7;
    }

    /* Header */
    .projects-portfolio .portfolio-header {
        text-align: center;
        padding: 2.5rem 0 3rem;
        border-bottom: 2px solid var(--border);
        margin-bottom: 4rem;
    }

    .projects-portfolio .breadcrumb {
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        margin-bottom: 1.5rem;
    }

    .projects-portfolio .breadcrumb a {
        color: var(--accent);
        text-decoration: none;
        border-bottom: 1px solid transparent;
        transition: border-color 0.2s;
    }

    .projects-portfolio .breadcrumb a:hover {
        border-bottom-color: var(--accent);
    }

    .projects-portfolio .breadcrumb span {
        color: var(--text-light);
        margin: 0 0.5rem;
    }

    .projects-portfolio h1 {
        font-size: 3rem;
        font-weight: 600;
        margin-bottom: 1rem;
        letter-spacing: -0.01em;
        color: var(--text);
    }

    .projects-portfolio .page-description {
        font-size: 1.125rem;
        color: var(--text-medium);
        max-width: 700px;
        margin: 0 auto;
        line-height: 1.7;
    }

    /* Stats Summary */
    .projects-portfolio .stats-summary {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 2rem;
        margin: 3rem 0;
        padding: 2rem;
        background: var(--surface);
        border-radius: 8px;
    }

    .projects-portfolio .stat-item {
        text-align: center;
    }

    .projects-portfolio .stat-value {
        font-family: 'Inter', sans-serif;
        font-size: 2rem;
        font-weight: 700;
        color: var(--accent);
        display: block;
        margin-bottom: 0.5rem;
    }

    .projects-portfolio .stat-label {
        font-family: 'Inter', sans-serif;
        font-size: 0.8125rem;
        color: var(--text-medium);
    }

    /* Section Headers */
    .projects-portfolio h2 {
        font-size: 1.75rem;
        font-weight: 600;
        margin: 3.5rem 0 1rem;
        padding-bottom: 0.5rem;
        border-bottom: 1px solid var(--border);
        display: flex;
        align-items: center;
        gap: 0.75rem;
        color: var(--text);
    }

    .projects-portfolio h2:first-of-type {
        margin-top: 0;
    }

    .projects-portfolio .section-icon {
        font-size: 1.5rem;
    }

    .projects-portfolio .section-description {
        font-family: 'Inter', sans-serif;
        font-size: 0.9375rem;
        color: var(--text-light);
        margin-bottom: 2rem;
    }

    /* Featured Project */
    .projects-portfolio .featured-project {
        background: linear-gradient(135deg, #1e3a8a 0%, #1d4ed8 100%);
        color: white;
        padding: 3rem;
        border-radius: 12px;
        margin-bottom: 3rem;
        position: relative;
        overflow: hidden;
    }

    .projects-portfolio .featured-project::before {
        content: '';
        position: absolute;
        top: -50%;
        right: -10%;
        width: 400px;
        height: 400px;
        background: rgba(255, 255, 255, 0.05);
        border-radius: 50%;
    }

    .projects-portfolio .featured-badge {
        display: inline-block;
        padding: 0.375rem 0.875rem;
        background: rgba(255, 255, 255, 0.15);
        border-radius: 999px;
        font-family: 'Inter', sans-serif;
        font-size: 0.75rem;
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 0.05em;
        margin-bottom: 1rem;
        backdrop-filter: blur(10px);
    }

    .projects-portfolio .featured-project h3 {
        font-size: 2rem;
        font-weight: 600;
        margin-bottom: 1rem;
        position: relative;
        z-index: 1;
        color: white;
    }

    .projects-portfolio .featured-description {
        font-size: 1.125rem;
        line-height: 1.7;
        margin-bottom: 1.5rem;
        opacity: 0.95;
        position: relative;
        z-index: 1;
    }

    .projects-portfolio .featured-meta {
        display: flex;
        flex-wrap: wrap;
        gap: 2rem;
        margin-bottom: 1.5rem;
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        position: relative;
        z-index: 1;
    }

    .projects-portfolio .meta-item {
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }

    .projects-portfolio .featured-tags {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
        margin-bottom: 1.5rem;
        position: relative;
        z-index: 1;
    }

    .projects-portfolio .featured-tag {
        padding: 0.375rem 0.875rem;
        background: rgba(255, 255, 255, 0.2);
        border-radius: 999px;
        font-family: 'Inter', sans-serif;
        font-size: 0.8125rem;
        backdrop-filter: blur(10px);
    }

    .projects-portfolio .featured-links {
        display: flex;
        gap: 1rem;
        position: relative;
        z-index: 1;
        flex-wrap: wrap;
    }

    .projects-portfolio .btn {
        display: inline-flex;
        align-items: center;
        gap: 0.5rem;
        padding: 0.75rem 1.5rem;
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        font-weight: 600;
        text-decoration: none;
        border-radius: 6px;
        transition: all 0.2s;
    }

    .projects-portfolio .btn-primary {
        background: white;
        color: var(--accent);
    }

    .projects-portfolio .btn-primary:hover {
        transform: translateY(-2px);
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
    }

    .projects-portfolio .btn-secondary {
        background: rgba(255, 255, 255, 0.1);
        color: white;
        border: 1px solid rgba(255, 255, 255, 0.3);
        backdrop-filter: blur(10px);
    }

    .projects-portfolio .btn-secondary:hover {
        background: rgba(255, 255, 255, 0.2);
    }

    .projects-portfolio .btn svg {
        width: 16px;
        height: 16px;
    }

    /* Project Grid */
    .projects-portfolio .projects-grid {
        display: grid;
        gap: 2rem;
        margin-top: 2rem;
    }

    /* Project Card */
    .projects-portfolio .project-card {
        background: var(--surface);
        border: 1px solid var(--border);
        border-radius: 8px;
        padding: 2rem;
        transition: all 0.3s;
        position: relative;
    }

    .projects-portfolio .project-card::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 4px;
        height: 100%;
        background: var(--accent);
        border-radius: 8px 0 0 8px;
        transform: scaleY(0);
        transition: transform 0.3s;
    }

    .projects-portfolio .project-card:hover {
        box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
        transform: translateY(-2px);
    }

    .projects-portfolio .project-card:hover::before {
        transform: scaleY(1);
    }

    .projects-portfolio .project-header {
        display: flex;
        justify-content: space-between;
        align-items: start;
        margin-bottom: 1rem;
        gap: 1rem;
        flex-wrap: wrap;
    }

    .projects-portfolio .project-type {
        display: inline-flex;
        align-items: center;
        gap: 0.375rem;
        padding: 0.25rem 0.75rem;
        background: white;
        border: 1px solid var(--border);
        border-radius: 4px;
        font-family: 'Inter', sans-serif;
        font-size: 0.75rem;
        font-weight: 600;
        color: var(--accent);
        text-transform: uppercase;
        letter-spacing: 0.05em;
        margin-bottom: 0.75rem;
    }

    .projects-portfolio .status-badge {
        font-family: 'Inter', sans-serif;
        font-size: 0.75rem;
        font-weight: 600;
        padding: 0.25rem 0.75rem;
        border-radius: 4px;
        text-transform: uppercase;
        letter-spacing: 0.05em;
    }

    .projects-portfolio .status-published {
        background: #d1fae5;
        color: var(--success);
    }

    .projects-portfolio .status-ongoing {
        background: #dbeafe;
        color: var(--info);
    }

    .projects-portfolio .status-concept {
        background: #fef3c7;
        color: var(--warning);
    }

    .projects-portfolio .project-card h3 {
        font-size: 1.375rem;
        font-weight: 600;
        margin-bottom: 1rem;
        color: var(--text);
    }

    .projects-portfolio .project-description {
        font-size: 0.9375rem;
        color: var(--text-medium);
        margin-bottom: 1.5rem;
        line-height: 1.7;
    }

    .projects-portfolio .project-highlights {
        background: white;
        padding: 1rem;
        border-radius: 6px;
        margin-bottom: 1.5rem;
        border: 1px solid var(--border);
    }

    .projects-portfolio .project-highlights h4 {
        font-family: 'Inter', sans-serif;
        font-size: 0.8125rem;
        font-weight: 600;
        color: var(--text-medium);
        text-transform: uppercase;
        letter-spacing: 0.05em;
        margin-bottom: 0.75rem;
    }

    .projects-portfolio .project-highlights ul {
        list-style: none;
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        color: var(--text-medium);
    }

    .projects-portfolio .project-highlights li {
        padding-left: 1.25rem;
        position: relative;
        margin-bottom: 0.5rem;
    }

    .projects-portfolio .project-highlights li:before {
        content: "✓";
        position: absolute;
        left: -1rem;
        color: var(--success);
        font-weight: bold;
    }

    .projects-portfolio .project-tech {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
        margin-bottom: 1.5rem;
    }

    .projects-portfolio .tech-tag {
        padding: 0.25rem 0.75rem;
        background: white;
        color: var(--accent);
        font-family: 'Inter', sans-serif;
        font-size: 0.75rem;
        font-weight: 500;
        border-radius: 4px;
        border: 1px solid var(--border);
    }

    .projects-portfolio .project-links {
        display: flex;
        gap: 1rem;
        padding-top: 1rem;
        border-top: 1px solid var(--border);
        flex-wrap: wrap;
    }

    .projects-portfolio .project-link {
        display: inline-flex;
        align-items: center;
        gap: 0.5rem;
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        color: var(--accent);
        text-decoration: none;
        transition: gap 0.2s;
    }

    .projects-portfolio .project-link:hover {
        gap: 0.75rem;
    }

    .projects-portfolio .project-link svg {
        width: 16px;
        height: 16px;
    }

    /* Impact Metrics */
    .projects-portfolio .impact-box {
        background: white;
        padding: 1rem;
        border-radius: 6px;
        border: 1px solid var(--border);
        margin-bottom: 1.5rem;
    }

    .projects-portfolio .impact-box h4 {
        font-family: 'Inter', sans-serif;
        font-size: 0.8125rem;
        font-weight: 600;
        color: var(--text-medium);
        text-transform: uppercase;
        letter-spacing: 0.05em;
        margin-bottom: 0.75rem;
    }

    .projects-portfolio .impact-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
        gap: 1rem;
    }

    .projects-portfolio .impact-item {
        text-align: center;
    }

    .projects-portfolio .impact-value {
        font-family: 'Inter', sans-serif;
        font-size: 1.5rem;
        font-weight: 700;
        color: var(--accent);
        display: block;
    }

    .projects-portfolio .impact-label {
        font-family: 'Inter', sans-serif;
        font-size: 0.75rem;
        color: var(--text-light);
    }

    /* Call to Action */
    .projects-portfolio .cta-section {
        margin-top: 4rem;
        padding: 3rem;
        background: var(--surface);
        border-radius: 12px;
        text-align: center;
    }

    .projects-portfolio .cta-section h2 {
        border: none;
        margin: 0 0 1rem 0;
        padding: 0;
        justify-content: center;
    }

    .projects-portfolio .cta-section p {
        color: var(--text-medium);
        margin-bottom: 2rem;
        max-width: 600px;
        margin-left: auto;
        margin-right: auto;
    }

    /* Video Embedding */
    .projects-portfolio .featured-video {
        margin-top: 2rem;
        margin-bottom: 1.5rem;
        position: relative;
        z-index: 1;
    }

    .projects-portfolio .video-caption {
        font-size: 0.875rem;
        color: rgba(255, 255, 255, 0.9);
        margin-bottom: 12px;
        font-weight: 600;
        display: flex;
        align-items: center;
        gap: 6px;
        font-family: 'Inter', sans-serif;
    }

    .projects-portfolio .video-wrapper {
        position: relative;
        padding-bottom: 56.25%; /* 16:9 aspect ratio */
        height: 0;
        overflow: hidden;
        border-radius: 8px;
        background: #000;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
    }

    .projects-portfolio .video-wrapper iframe {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        border: none;
    }

    /* Project Card Video */
    .projects-portfolio .project-video {
        margin-top: 1.5rem;
        margin-bottom: 1.5rem;
    }

    .projects-portfolio .project-video .video-caption {
        color: var(--text-medium);
        font-size: 0.8125rem;
        margin-bottom: 10px;
    }

    .projects-portfolio .project-video .video-wrapper {
        box-shadow: 0 2px 12px rgba(0, 0, 0, 0.1);
    }

    /* Responsive */
    @media (max-width: 768px) {
        .projects-portfolio {
            padding: 0 1rem 3rem;
        }

        .projects-portfolio .portfolio-header {
            padding: 2rem 0 2.5rem;
        }

        .projects-portfolio h1 {
            font-size: 2rem;
        }

        .projects-portfolio .stats-summary {
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
        }

        .projects-portfolio .featured-project {
            padding: 2rem 1.5rem;
        }

        .projects-portfolio .featured-project h3 {
            font-size: 1.5rem;
        }

        .projects-portfolio .featured-meta {
            flex-direction: column;
            gap: 0.75rem;
        }

        .projects-portfolio .featured-links {
            flex-direction: column;
        }

        .projects-portfolio .btn {
            width: 100%;
            justify-content: center;
        }

        .projects-portfolio .project-links {
            flex-direction: column;
        }

        .projects-portfolio .featured-video {
            margin-left: -1.5rem;
            margin-right: -1.5rem;
        }

        .projects-portfolio .video-wrapper {
            border-radius: 0;
        }
    }
</style>

<div class="projects-portfolio">
    <div class="portfolio-header">
        <div class="breadcrumb">
            <a href="{{ site.baseurl }}/">Home</a>
            <span>/</span>
            <span>Projects</span>
        </div>
        <h1>Research & Development Projects</h1>
        <p class="page-description">A comprehensive portfolio of research, applied systems, and future concepts bridging construction engineering and artificial intelligence.</p>
    </div>

    <!-- Stats Summary -->
    <div class="stats-summary">
        <div class="stat-item">
            <span class="stat-value">10+</span>
            <span class="stat-label">Total Projects</span>
        </div>
        <div class="stat-item">
            <span class="stat-value">4</span>
            <span class="stat-label">Published Systems</span>
        </div>
        <div class="stat-item">
            <span class="stat-value">82.5%</span>
            <span class="stat-label">NL Accuracy</span>
        </div>
        <div class="stat-item">
            <span class="stat-value">125+</span>
            <span class="stat-label">Research Citations</span>
        </div>
    </div>

    <!-- Featured Project -->
    <div class="featured-project">
        <span class="featured-badge">⭐ Featured Research</span>
        <h3>IproK: Integrated Project Knowledge Ontology Framework</h3>
        <p class="featured-description">A novel semantic framework for construction project knowledge management that unifies schedule, cost, and resource data into a coherent knowledge graph. Published in the International Journal of Construction Management and registered at w3id.org/iprok/.</p>
        
        <div class="featured-meta">
            <div class="meta-item">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="16" height="16"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                Published in Int. Journal
            </div>
            <div class="meta-item">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="16" height="16"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"/></svg>
                Doctoral Research
            </div>
            <div class="meta-item">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="16" height="16"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                2020 - 2025
            </div>
        </div>

        <div class="featured-tags">
            <span class="featured-tag">Ontology Engineering</span>
            <span class="featured-tag">Knowledge Graphs</span>
            <span class="featured-tag">Web Application</span>
            <span class="featured-tag">Graph Neural Networks</span>
            <span class="featured-tag">BIM Integration</span>
        </div>

        <!-- Video Demo -->
        <div class="featured-video">
            <div class="video-caption">📹 System Demonstration & Features</div>
            <div class="video-wrapper">
                <iframe 
                    src="https://www.youtube.com/embed/p3OcnVIPMIM?si=nyqAvigYo7Tw7xl-" 
                    title="IproK System Demo"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                    referrerpolicy="strict-origin-when-cross-origin"
                    allowfullscreen>
                </iframe>
            </div>
        </div>

        <div class="featured-links">
            <a href="https://w3id.org/iprok/" target="_blank" rel="noopener" class="btn btn-primary">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01"/></svg>
                View Ontology
            </a>
            <a href="https://iprok-web.streamlit.app/" target="_blank" rel="noopener" class="btn btn-primary">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"/></svg>
                Live WebApp
            </a>
            <a href="https://doi.org/10.1080/15623599.2025.2562105" target="_blank" rel="noopener" class="btn btn-secondary">
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                Read Publication
            </a>
        </div>
    </div>

    <!-- Doctoral Research Projects -->
    <section>
        <h2><span class="section-icon">🔬</span>Doctoral Research Projects</h2>
        <p class="section-description">Core PhD research projects developing novel frameworks and systems for construction knowledge management.</p>

        <div class="projects-grid">
            <!-- Project 1 -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"/></svg>
                            Web Application
                        </span>
                    </div>
                    <span class="status-badge status-published">Published</span>
                </div>

                <h3>IproK Web Platform for Project Data Management</h3>
                <p class="project-description">Developed a comprehensive web-based application serving as the user interface for the IproK ontology. Enables non-technical project managers to easily manage, visualize, and interact with integrated construction data in real-time.</p>

                <div class="project-highlights">
                    <h4>Key Features</h4>
                    <ul>
                        <li>Project creation and planning workflows</li>
                        <li>Real-time dashboard visualization with NetworkX</li>
                        <li>Interactive scheduling and resource management</li>
                        <li>Ontology manipulation with Owlready2</li>
                    </ul>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">Streamlit</span>
                    <span class="tech-tag">Owlready2</span>
                    <span class="tech-tag">NetworkX</span>
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">RDF/OWL</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/VenkateshKone-1/Iprok-web.git" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        GitHub Repository
                    </a>
                    <a href="https://lnkd.in/gPQ4GETz" target="_blank" rel="noopener" class="project-link">
                        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"/></svg>
                        Live Demo
                    </a>
                </div>
            </div>

            <!-- Project 2 -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z"/></svg>
                            NLP System
                        </span>
                    </div>
                    <span class="status-badge status-published">Published</span>
                </div>

                <h3>ChatGraphDB: LLM-Powered Conversational Interface</h3>
                <p class="project-description">Developed a conversational AI interface for querying project knowledge graphs using natural language. Built a dual-web-application framework using Streamlit and fine-tuned GPT-4 with ontology-aware prompts to translate questions into SPARQL queries.</p>

                <div class="impact-box">
                    <h4>Performance Metrics</h4>
                    <div class="impact-grid">
                        <div class="impact-item">
                            <span class="impact-value">82.5%</span>
                            <span class="impact-label">Translation Accuracy</span>
                        </div>
                        <div class="impact-item">
                            <span class="impact-value">~5s</span>
                            <span class="impact-label">Avg Response Time</span>
                        </div>
                        <div class="impact-item">
                            <span class="impact-value">100%</span>
                            <span class="impact-label">IFC Coverage</span>
                        </div>
                    </div>
                </div>

                <!-- Video Demo -->
                <div class="project-video">
                    <div class="video-caption">📹 ChatGraphDB Demo & Query Examples</div>
                    <div class="video-wrapper">
                        <iframe 
                            src="https://www.youtube.com/embed/8WEuozXKnEg?si=V82lMCrMi7Z5H7gL" 
                            title="ChatGraphDB Demo"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                            referrerpolicy="strict-origin-when-cross-origin"
                            allowfullscreen>
                        </iframe>
                    </div>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">GPT-4</span>
                    <span class="tech-tag">SPARQL</span>
                    <span class="tech-tag">Streamlit</span>
                    <span class="tech-tag">RDFlib</span>
                    <span class="tech-tag">IFC/BIM</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/konevenkatesh/ChatGraphDB" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        GitHub Repository
                    </a>
                </div>
            </div>

            <!-- Continue with remaining projects... -->
            <!-- I'll add a few more key projects to demonstrate the pattern -->
            
            <!-- Project 3 -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"/></svg>
                            Machine Learning
                        </span>
                    </div>
                    <span class="status-badge status-published">Published</span>
                </div>

                <h3>Predictive Analytics Using Graph Neural Networks</h3>
                <p class="project-description">Created a predictive model to forecast task-level delay and cost-overrun risks in construction projects. Engineered temporal, resource, and cost features from the IproK knowledge graph and used this data to train Graph Neural Network models.</p>

                <div class="project-highlights">
                    <h4>Key Contributions</h4>
                    <ul>
                        <li>Feature engineering from knowledge graphs</li>
                        <li>Temporal dependency modeling</li>
                        <li>Risk pattern identification</li>
                        <li>Proactive project control system</li>
                    </ul>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">PyTorch Geometric</span>
                    <span class="tech-tag">DGL</span>
                    <span class="tech-tag">Graph Neural Networks</span>
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">Knowledge Graphs</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/konevenkatesh/GNN-Project-Control" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        GitHub Repository
                    </a>
                </div>
            </div>

            <!-- Project 4 -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7h12m0 0l-4-4m4 4l-4 4m0 6H4m0 0l4 4m-4-4l4-4"/></svg>
                            Integration Framework
                        </span>
                    </div>
                    <span class="status-badge status-published">Published</span>
                </div>

                <h3>Ontology-Driven Bi-Directional BIM/IFC Workflow</h3>
                <p class="project-description">Architected a novel bi-directional workflow to integrate project management data (from the IproK ontology) with building data (from the IFC standard). Developed Python-based process to programmatically generate new, enriched IFC models from the unified knowledge graph.</p>

                <div class="project-highlights">
                    <h4>Key Achievements</h4>
                    <ul>
                        <li>Registered ontology at w3id.org/iprok/</li>
                        <li>Seamless BIM-to-ontology conversion</li>
                        <li>Ontology-to-IFC generation</li>
                        <li>Standards-compliant data consistency</li>
                    </ul>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">Python</span>
                    <span class="tech-tag">IFC</span>
                    <span class="tech-tag">ifcopenshell</span>
                    <span class="tech-tag">RDF/OWL</span>
                    <span class="tech-tag">BIM</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/konevenkatesh/Semantic-BIM-Workflow" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        GitHub Repository
                    </a>
                    <a href="https://doi.org/10.1080/15623599.2025.2562105" target="_blank" rel="noopener" class="project-link">
                        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                        Publication
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Applied & Personal Projects -->
    <section>
        <h2><span class="section-icon">⚙️</span>Applied & Personal Projects</h2>
        <p class="section-description">Practical applications and tools demonstrating real-world implementation of AI and BIM technologies.</p>

        <div class="projects-grid">
            <!-- Multimodal RAG -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"/></svg>
                            Document Intelligence
                        </span>
                    </div>
                    <span class="status-badge status-ongoing">Ongoing</span>
                </div>

                <h3>Multimodal Agentic RAG for Construction Contracts</h3>
                <p class="project-description">Developing an agentic Retrieval-Augmented Generation system for querying multimodal construction documents. The system architecture combines Docling, an ontology, Graphiti, a Vector DB, and a custom AgenticRAG flow.</p>

                <div class="project-highlights">
                    <h4>Capabilities</h4>
                    <ul>
                        <li>Text, diagram, and table processing</li>
                        <li>Context-aware information extraction</li>
                        <li>Accurate retrieval from complex documents</li>
                        <li>Support for contracts, tenders, reports</li>
                    </ul>
                </div>

                <!-- Video Demo -->
                <div class="project-video">
                    <div class="video-caption">📹 Multimodal RAG System Walkthrough</div>
                    <div class="video-wrapper">
                        <iframe 
                            src="https://www.youtube.com/embed/Wv66eZFJ42E?si=ScU-hNUQvN_OV4_S" 
                            title="Multimodal RAG Demo"
                            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
                            referrerpolicy="strict-origin-when-cross-origin"
                            allowfullscreen>
                        </iframe>
                    </div>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">Docling</span>
                    <span class="tech-tag">LangGraph</span>
                    <span class="tech-tag">ChromaDB</span>
                    <span class="tech-tag">Graphiti</span>
                    <span class="tech-tag">RAG</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/konevenkatesh/tender_rag_project" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        GitHub Repository
                    </a>
                    <a href="https://konevenkatesh.github.io/blog/ai-in-construction.html" target="_blank" rel="noopener" class="project-link">
                        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z"/></svg>
                        Read Blog Post
                    </a>
                </div>
            </div>

            <!-- A.U.R.A. -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                            Smart City AI
                        </span>
                    </div>
                    <span class="status-badge status-ongoing">Ongoing</span>
                </div>

                <h3>A.U.R.A.: AI Urban Reporting Agent for Smart Cities</h3>
                <p class="project-description">Architected "A.U.R.A." (Amaravati Urban Resilience Agent), a collaborative multi-agent AI system for smart city data. Utilized IBM watsonx Orchestrate for agent collaboration and developed a custom data pipeline using QGIS and a new ontology (ADTO) to convert geospatial data into an RDF knowledge graph.</p>

                <div class="project-highlights">
                    <h4>System Features</h4>
                    <ul>
                        <li>Multi-agent collaboration framework</li>
                        <li>Custom ADTO (Amaravati Digital Twin Ontology)</li>
                        <li>Geospatial data to RDF conversion</li>
                        <li>Intelligent urban infrastructure querying</li>
                    </ul>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">IBM watsonx</span>
                    <span class="tech-tag">QGIS</span>
                    <span class="tech-tag">RDF</span>
                    <span class="tech-tag">Multi-Agent Systems</span>
                    <span class="tech-tag">Geospatial</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/konevenkatesh/IBM_TechXchange_2025_Aegis-Roads.git" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        GitHub Repository
                    </a>
                </div>
            </div>

            <!-- Add remaining applied projects following same pattern... -->
        </div>
    </section>

    <!-- Future Research Concepts -->
    <section>
        <h2><span class="section-icon">🔮</span>Future Research Concepts</h2>
        <p class="section-description">Visionary projects exploring the next generation of construction intelligence and digital twins.</p>

        <div class="projects-grid">
            <!-- Digital Twin -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"/></svg>
                            Concept
                        </span>
                    </div>
                    <span class="status-badge status-concept">Future Work</span>
                </div>

                <h3>Digital Twin of Amaravathi with A.U.R.A. Integration</h3>
                <p class="project-description">A large-scale, high-fidelity digital twin of the city of Amaravathi. Planned for development using Unreal Engine for physics-based simulation, Cesium for lightweight 3D tiles, and an AI Assistant for conversational interaction.</p>

                <div class="project-highlights">
                    <h4>Proposed Features</h4>
                    <ul>
                        <li>Real-time urban systems modeling</li>
                        <li>Physics-based simulations</li>
                        <li>AI-powered conversational queries</li>
                        <li>Integration with A.U.R.A. agent system</li>
                    </ul>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">Unreal Engine</span>
                    <span class="tech-tag">Cesium</span>
                    <span class="tech-tag">Digital Twin</span>
                    <span class="tech-tag">AI Assistant</span>
                    <span class="tech-tag">3D Tiles</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/konevenkatesh/SmartCity-Amaravathi-DT" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        Concept Repository
                    </a>
                </div>
            </div>

            <!-- ATLAS -->
            <div class="project-card">
                <div class="project-header">
                    <div>
                        <span class="project-type">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" width="12" height="12"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11a7 7 0 01-7 7m0 0a7 7 0 01-7-7m7 7v4m0 0H8m4 0h4m-4-8a3 3 0 01-3-3V5a3 3 0 116 0v6a3 3 0 01-3 3z"/></svg>
                            Concept
                        </span>
                    </div>
                    <span class="status-badge status-concept">Future Work</span>
                </div>

                <h3>ATLAS: Local Voice Assistant for Project Management</h3>
                <p class="project-description">"ATLAS," an on-device, local-first, multilingual (Telugu/English) voice assistant for construction knowledge management. Proposing an architecture using advanced STT/TTS models (e.g., Whisper, ViTs) to ensure privacy and offline functionality.</p>

                <div class="project-highlights">
                    <h4>Proposed Capabilities</h4>
                    <ul>
                        <li>Hands-free project monitoring</li>
                        <li>Multilingual support (Telugu/English)</li>
                        <li>Offline, privacy-preserving operation</li>
                        <li>Real-time data entry and status updates</li>
                    </ul>
                </div>

                <div class="project-tech">
                    <span class="tech-tag">Whisper</span>
                    <span class="tech-tag">ViTs</span>
                    <span class="tech-tag">Local LLMs</span>
                    <span class="tech-tag">Voice Interface</span>
                    <span class="tech-tag">Multilingual</span>
                </div>

                <div class="project-links">
                    <a href="https://github.com/konevenkatesh/Local-PM-Voice-Agent" target="_blank" rel="noopener" class="project-link">
                        <svg fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                        Concept Repository
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <div class="cta-section">
        <h2>Interested in Collaboration?</h2>
        <p>I'm always open to discussing research collaborations, consulting opportunities, or speaking engagements related to construction AI, knowledge graphs, and intelligent document systems.</p>
        <a href="mailto:venkateshkone.connect@gmail.com" class="btn btn-primary">
            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>
            Get in Touch
        </a>
    </div>
</div>
