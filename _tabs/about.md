---
layout: page
icon: fas fa-rss
order: 2
---

<style>
    /* Hide default theme title, metadata, and breadcrumbs */
    h1.dynamic-title,
    .post-title,
    .page-title,
    #page-title,
    .post-meta,
    .pl-xl-3,
    #breadcrumbs,
    .breadcrumb,
    nav[aria-label="breadcrumb"] {
        display: none !important;
    }

    .container {
        --accent: #1d4ed8;
        --text: #0f172a;
        --text-medium: #475569;
        --text-light: #64748b;
        --border: #cbd5e0;
        --surface: #f1f5f9;
        
        font-family: 'EB Garamond', serif;
        line-height: 1.8;
        color: var(--text);
        background: #ffffff;
        font-size: 18px;
        max-width: 900px;
        margin: 0 auto;
        padding: 0 2rem 6rem;
    }
    
    .container * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    /* Intro Section */
    .container .about-intro {
        text-align: center;
        padding: 1rem 0 1.5rem;
        border-bottom: 1px solid var(--border);
        margin-bottom: 2rem;
    }

    .container .about-subtitle {
        font-family: 'Inter', sans-serif;
        font-size: 1rem;
        color: var(--text-medium);
        margin-bottom: 0.5rem;
    }

    .container .about-affiliation {
        font-family: 'Inter', sans-serif;
        font-size: 0.9rem;
        color: var(--text-light);
        font-style: italic;
        margin-bottom: 1rem;
    }

    .container .contact-links {
        display: flex;
        justify-content: center;
        gap: 1.5rem;
        margin-top: 1rem;
        flex-wrap: wrap;
    }

    .container .contact-link {
        font-family: 'Inter', sans-serif;
        font-size: 0.85rem;
        color: var(--accent);
        text-decoration: none;
        border-bottom: 1px solid transparent;
        transition: border-color 0.2s;
    }

    .container .contact-link:hover {
        border-bottom-color: var(--accent);
    }

    .container .cv-button {
        display: inline-block;
        margin-top: 1rem;
        padding: 0.4rem 0.8rem;
        background: var(--accent);
        color: white;
        font-family: 'Inter', sans-serif;
        font-size: 0.75rem;
        font-weight: 600;
        text-decoration: none;
        border-radius: 50px;
        transition: background 0.2s, transform 0.2s;
    }

    .container .cv-button:hover {
        background: #1e3a8a;
        transform: translateY(-2px);
        text-decoration: none;
    }

    /* Typography */
    .container h2 {
        font-size: 1.75rem;
        font-weight: 600;
        margin: 3rem 0 1.5rem;
        padding-bottom: 0.5rem;
        border-bottom: 1px solid var(--border);
    }

    .container h3 {
        font-size: 1.25rem;
        font-weight: 600;
        margin: 2rem 0 0.75rem;
    }

    .container h4 {
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        font-weight: 600;
        color: var(--text-medium);
        text-transform: uppercase;
        letter-spacing: 0.05em;
        margin: 2rem 0 1rem;
    }

    .container p {
        margin-bottom: 1.25rem;
        color: var(--text-medium);
    }

    .container .lead {
        font-size: 1.25rem;
        line-height: 1.7;
        margin-bottom: 2rem;
        color: var(--text);
    }

    /* Research Interests */
    .container .interests {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 1rem;
        margin: 1.5rem 0;
    }

    .container .interest-item {
        font-family: 'Inter', sans-serif;
        padding: 1rem;
        background: var(--surface);
        border-left: 3px solid var(--accent);
        font-size: 0.9375rem;
    }

    /* Expertise Box */
    .container .expertise-box {
        background: var(--surface);
        padding: 2rem;
        border-radius: 4px;
        margin: 2rem 0;
    }

    .container .expertise-box h3 {
        margin-top: 0;
    }

    .container .expertise-list {
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 1rem;
        list-style: none;
        font-family: 'Inter', sans-serif;
        font-size: 0.9375rem;
    }

    .container .expertise-list li {
        padding-left: 1.5rem;
        position: relative;
        color: var(--text-medium);
    }

    .container .expertise-list li:before {
        content: "▸";
        position: absolute;
        left: 0;
        color: var(--accent);
    }

    /* Publications */
    .container .publication {
        margin-bottom: 2rem;
        padding-bottom: 2rem;
        border-bottom: 1px solid #e2e8f0;
    }

    .container .publication:last-child {
        border-bottom: none;
    }

    .container .pub-authors {
        font-family: 'Inter', sans-serif;
        font-size: 0.9375rem;
        color: var(--text-medium);
        margin-bottom: 0.5rem;
    }

    .container .pub-title {
        font-size: 1.125rem;
        font-weight: 600;
        margin-bottom: 0.5rem;
        color: var(--text);
    }

    .container .pub-venue {
        font-family: 'Inter', sans-serif;
        font-size: 0.9375rem;
        font-style: italic;
        color: var(--text-light);
        margin-bottom: 0.5rem;
    }

    .container .pub-links {
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        display: flex;
        gap: 1rem;
    }

    .container .pub-link {
        color: var(--accent);
        text-decoration: none;
        border-bottom: 1px solid transparent;
        transition: border-color 0.2s;
    }

    .container .pub-link:hover {
        border-bottom-color: var(--accent);
    }

    /* Projects */
    .container .project {
        margin-bottom: 2.5rem;
        padding: 1.5rem;
        background: var(--surface);
        border-left: 4px solid var(--accent);
    }

    .container .project-header {
        display: flex;
        justify-content: space-between;
        align-items: start;
        margin-bottom: 1rem;
    }

    .container .project h3 {
        margin: 0 0 0.5rem 0;
    }

    .container .project-type {
        font-family: 'Inter', sans-serif;
        font-size: 0.8125rem;
        color: var(--accent);
        font-weight: 600;
        text-transform: uppercase;
        letter-spacing: 0.05em;
    }

    .container .project-link {
        font-family: 'Inter', sans-serif;
        color: var(--accent);
        text-decoration: none;
        font-size: 0.875rem;
    }

    .container .project p {
        margin: 0;
        font-size: 0.9375rem;
    }

    /* Stats */
    .container .stats-grid {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 2rem;
        margin: 2rem 0;
        padding: 2rem;
        background: var(--surface);
        text-align: center;
    }

    .container .stat-number {
        font-family: 'Inter', sans-serif;
        font-size: 2.5rem;
        font-weight: 700;
        color: var(--accent);
        display: block;
        margin-bottom: 0.5rem;
    }

    .container .stat-label {
        font-family: 'Inter', sans-serif;
        font-size: 0.8125rem;
        color: var(--text-medium);
    }

    /* Education */
    .container .education-item {
        margin-bottom: 2rem;
    }

    .container .education-item h3 {
        margin-top: 0;
        margin-bottom: 0.25rem;
    }

    .container .education-meta {
        font-family: 'Inter', sans-serif;
        font-size: 0.9375rem;
        color: var(--text-light);
        font-style: italic;
        margin-bottom: 0.5rem;
    }

    .container .education-details {
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        color: var(--text-medium);
    }

    /* Awards & Certifications */
    .container .award-item, .container .cert-item {
        margin-bottom: 1.5rem;
        padding-left: 0;
        position: relative;
    }

    /* Removed icons
    .container .award-item:before, .container .cert-item:before {
        content: "⭐";
        position: absolute;
        left: 0;
        top: 0.25rem;
    }

    .container .cert-item:before {
        content: "📜";
    }
    */

    .container .award-item h4, .container .cert-item h4 {
        font-family: 'EB Garamond', serif;
        font-size: 1rem;
        font-weight: 600;
        color: var(--text);
        margin: 0 0 0.25rem 0;
        text-transform: none;
        letter-spacing: normal;
    }

    .container .award-meta, .container .cert-meta {
        font-family: 'Inter', sans-serif;
        font-size: 0.875rem;
        color: var(--text-light);
        font-style: italic;
    }

    .container .cert-link {
        font-family: 'Inter', sans-serif;
        font-size: 0.8125rem;
        color: var(--accent);
        text-decoration: none;
        border-bottom: 1px solid transparent;
        transition: border-color 0.2s;
        margin-left: 0.5rem;
    }

    .container .cert-link:hover {
        border-bottom-color: var(--accent);
    }

    /* Quote */
    .container .quote-box {
        margin: 3rem 0;
        padding: 2rem;
        border-left: 4px solid var(--accent);
        background: var(--surface);
        font-style: italic;
        font-size: 1.125rem;
        line-height: 1.7;
    }

    /* Footer CTA */
    .container .footer-cta {
        margin-top: 4rem;
        padding: 3rem 0;
        border-top: 2px solid var(--border);
        text-align: center;
    }

    .container .footer-cta h2 {
        border: none;
        margin-bottom: 1rem;
        padding-bottom: 0;
    }

    .container .footer-cta p {
        max-width: 600px;
        margin: 0 auto 2rem;
    }

    .container .cta-button {
        display: inline-block;
        padding: 1rem 2rem;
        background: var(--accent);
        color: white;
        font-family: 'Inter', sans-serif;
        font-size: 0.9375rem;
        font-weight: 600;
        text-decoration: none;
        border-radius: 4px;
        transition: background 0.2s;
    }

    .container .cta-button:hover {
        background: #1e3a8a;
    }

    /* Responsive */
    @media (max-width: 768px) {
        .container {
            padding: 2rem 1.5rem 4rem;
        }

        .container .about-intro {
            padding: 0.5rem 0 1rem;
        }

        .container h2 {
            font-size: 1.5rem;
        }

        .container .interests,
        .container .expertise-list {
            grid-template-columns: 1fr;
        }

        .container .stats-grid {
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
        }

        .container .contact-links {
            gap: 1rem;
        }
    }
</style>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:wght@400;500;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">

<div class="container">
    <div class="about-intro">
        <p class="about-subtitle">PhD Researcher · AI Engineer · Construction Tech Specialist</p>
        <p class="about-affiliation">National Institute of Technology Karnataka, Surathkal</p>
        <div class="contact-links">
            <a href="mailto:venkateshkone.connect@gmail.com" class="contact-link">Email</a>
            <a href="https://github.com/konevenkatesh" target="_blank" class="contact-link">GitHub</a>
            <a href="https://www.linkedin.com/in/venkatesh-kone-66149a13b/" target="_blank" class="contact-link">LinkedIn</a>
            <a href="https://scholar.google.com/citations?user=0aKzihMAAAAJ&hl=en" target="_blank" class="contact-link">Google Scholar</a>
        </div>
        <div style="margin-top: 0.5rem;">
            <a href="/assets/cv/venkateshkone_cv.pdf" target="_blank" class="cv-button">
                <i class="fas fa-download" style="margin-right: 0.5rem;"></i>Download CV
            </a>
        </div>
    </div>

    <main>
        <section>
            <p class="lead">I am a researcher and AI engineer developing intelligent systems for the construction industry. My work bridges civil engineering and computer science, focusing on semantic frameworks, knowledge graphs, and natural language processing to transform how construction projects manage and utilize information.</p>
        </section>

        <section>
            <h2>Research Interests</h2>
            <div class="interests">
                <div class="interest-item">Applied AI & Large Language Models</div>
                <div class="interest-item">Retrieval-Augmented Generation (RAG)</div>
                <div class="interest-item">Knowledge Graphs & Ontology Engineering</div>
                <div class="interest-item">Building Information Modeling (BIM)</div>
                <div class="interest-item">Natural Language Processing</div>
                <div class="interest-item">Graph Neural Networks</div>
                <div class="interest-item">Semantic Web Technologies</div>
                <div class="interest-item">Digital Twins & Smart Cities</div>
            </div>
        </section>

        <section>
            <h2>Research Overview</h2>
            <p>My doctoral research addresses the critical challenge of knowledge management in construction projects. The industry generates vast amounts of heterogeneous data—from BIM models and schedules to contracts and reports—yet this information remains largely disconnected and underutilized.</p>
            
            <p>I develop semantic frameworks and AI systems that integrate construction project knowledge, making it queryable, analyzable, and actionable. My primary contribution is the <strong>IproK (Integrated Project Knowledge) ontology</strong>, a novel semantic model that unifies schedule, cost, and resource data into a coherent knowledge graph. This work has been published in the International Journal of Construction Management.</p>

            <div class="quote-box">
                "The goal is not just to digitize construction data, but to make it intelligent—to create systems that understand project context, relationships, and temporal dependencies, enabling truly informed decision-making."
            </div>

            <p>Beyond ontology development, I build practical applications: natural language interfaces for knowledge graph querying, multimodal RAG systems for document intelligence, and Graph Neural Network models for predictive project analytics.</p>
        </section>

        <section>
            <h2>Research Impact</h2>
            <div class="stats-grid">
                <div>
                    <span class="stat-number">125+</span>
                    <span class="stat-label">Total Citations</span>
                </div>
                <div>
                    <span class="stat-number">11</span>
                    <span class="stat-label">Publications</span>
                </div>
                <div>
                    <span class="stat-number">7</span>
                    <span class="stat-label">h-index</span>
                </div>
                <div>
                    <span class="stat-number">6+</span>
                    <span class="stat-label">Research Projects</span>
                </div>
            </div>
        </section>

        <section>
            <h2>Selected Publications</h2>
            
            <div class="publication">
                <p class="pub-authors"><strong>Kone, V.</strong> & Mahesh, G.</p>
                <p class="pub-title">The IproK ontology: a unified approach to managing construction project information</p>
                <p class="pub-venue">International Journal of Construction Management, 2025, 1–30</p>
                <div class="pub-links">
                    <a href="https://doi.org/10.1080/15623599.2025.2562105" target="_blank" class="pub-link">DOI: 10.1080/15623599.2025.2562105</a>
                </div>
            </div>

            <div class="publication">
                <p class="pub-authors"><strong>Kone, V.</strong> & Mahesh, G.</p>
                <p class="pub-title">Ontology-Driven Project Management: A Framework for Structured Data and Automation</p>
                <p class="pub-venue">Proceedings of Digital Frontiers in Buildings and Infrastructure International Conference Series, 2025, 77-88</p>
                <div class="pub-links">
                    <a href="https://dfbi.org" target="_blank" class="pub-link">Conference Link</a>
                </div>
            </div>

            <div class="publication">
                <p class="pub-authors"><strong>Kone, V.</strong>, Mahesh, G., & Ingle, P.V.</p>
                <p class="pub-title">Enhancing Knowledge Management in the Construction Industry: Exploring the Impact of Semantic Web Technologies</p>
                <p class="pub-venue">Advances in Construction Management. ICCRIP 2023. Lecture Notes in Civil Engineering, vol 601. Springer, Singapore</p>
                <div class="pub-links">
                    <a href="https://doi.org/10.1007/978-981-96-4902-0_14" target="_blank" class="pub-link">DOI: 10.1007/978-981-96-4902-0_14</a>
                </div>
            </div>

            <div class="publication">
                <p class="pub-authors">Munagala, D. P., & <strong>Kone, V.</strong></p>
                <p class="pub-title">Feasibility study and implementation of BIM in small scale projects</p>
                <p class="pub-venue">IOP Conference Series: Materials Science and Engineering, 2020, 912(6), 062049</p>
                <div class="pub-links">
                    <a href="https://doi.org/10.1088/1757-899X/912/6/062049" target="_blank" class="pub-link">DOI: 10.1088/1757-899X/912/6/062049</a>
                </div>
            </div>

            <p style="margin-top: 1.5rem;"><em>Complete publication list available on <a href="https://scholar.google.com/citations?user=0aKzihMAAAAJ&hl=en" target="_blank" class="pub-link">Google Scholar</a></em></p>
        </section>

        <section>
            <h2>Key Research Projects</h2>
            
            <div class="project">
                <div class="project-header">
                    <div>
                        <span class="project-type">Doctoral Research</span>
                        <h3>IproK: Integrated Project Knowledge Framework</h3>
                    </div>
                    <a href="https://github.com/konevenkatesh" class="project-link">GitHub →</a>
                </div>
                <p>Novel ontology-based framework for construction project knowledge management. Includes semantic data model (w3id.org/iprok/), web application for project planning and visualization, bi-directional BIM integration workflow, and GNN-based predictive analytics for risk assessment. Published in international journal.</p>
            </div>

            <div class="project">
                <div class="project-header">
                    <div>
                        <span class="project-type">Applied Research</span>
                        <h3>ChatGraphDB: Natural Language Knowledge Graph Interface</h3>
                    </div>
                    <a href="https://github.com/konevenkatesh/ChatGraphDB" class="project-link">GitHub →</a>
                </div>
                <p>LLM-powered conversational interface for querying construction project knowledge graphs. Achieves 82.5% accuracy in natural language to SPARQL translation. Transforms IFC models into queryable ontologies, enabling intuitive data access for non-technical stakeholders.</p>
            </div>

            <div class="project">
                <div class="project-header">
                    <div>
                        <span class="project-type">Applied Research</span>
                        <h3>Multimodal Agentic RAG for Construction Contracts</h3>
                    </div>
                    <a href="https://github.com/konevenkatesh" class="project-link">GitHub →</a>
                </div>
                <p>Advanced retrieval-augmented generation system for analyzing complex construction documents. Handles multimodal content (text, tables, diagrams) through specialized pipeline combining Docling, ontology integration, vector databases, and agentic workflows for accurate context-aware information extraction.</p>
            </div>

            <div class="project">
                <div class="project-header">
                    <div>
                        <span class="project-type">Doctoral Research</span>
                        <h3>Predictive Analytics for Project Control using Graph Neural Networks</h3>
                    </div>
                    <a href="https://github.com/konevenkatesh" class="project-link">GitHub →</a>
                </div>
                <p>Created a predictive model to forecast task-level delay and cost-overrun risks in construction projects. Engineered temporal, resource, and cost features from the IproK knowledge graph and used this data to train Graph Neural Network (GNN) models.</p>
            </div>
        </section>

        <section>
            <h2>Education & Professional Experience</h2>
            
            <div class="education-item">
                <h3>Ph.D. in Civil Engineering (Construction Informatics & AI)</h3>
                <p class="education-meta">National Institute of Technology Karnataka, Surathkal · 2020 – Present</p>
                <p class="education-details">CPI: 8.75 | Specialization: Knowledge Management, Applied AI, Semantic Web Technologies</p>
            </div>

            <div class="education-item">
                <h3>Assistant Professor of Civil Engineering</h3>
                <p class="education-meta">KL University, Vijayawada · 2017 – 2020</p>
                <p class="education-details">Taught undergraduate courses, integrated computational tools into curriculum, mentored 15+ student research projects resulting in peer-reviewed publications.</p>
            </div>

            <div class="education-item">
                <h3>M.Tech in Construction Technology Management</h3>
                <p class="education-meta">Visvesvaraya National Institute of Technology, Nagpur · 2015 – 2017</p>
                <p class="education-details">CPI: 7.19 | Focus: BIM Technology, Project Management Systems</p>
            </div>

            <div class="education-item">
                <h3>B.Tech in Civil Engineering</h3>
                <p class="education-meta">J.B. Institute of Engineering and Technology, JNTUH · 2010 – 2014</p>
                <p class="education-details">Percentage: 74.10%</p>
            </div>
        </section>

        <section>
            <h2>Scholarships</h2>
            
            <div class="award-item">
                <h4>PhD Research Scholarship</h4>
                <p class="award-meta">Ministry of Education (MHRD), Government of India · 2020 – 2025</p>
            </div>

            <div class="award-item">
                <h4>M.Tech Postgraduate Scholarship</h4>
                <p class="award-meta">Ministry of Education (MHRD), Government of India · 2015 – 2017</p>
            </div>
        </section>

        <section>
            <h2>Professional Certifications</h2>
            
            <div class="cert-item">
                <h4>IBM RAG and Agentic AI: Build Next-Gen AI Systems Professional Certificate</h4>
                <p class="cert-meta">Issued by: IBM (via Coursera)
                    <a href="https://coursera.org/verify/professional-cert/GGXH2B9LNRYL" target="_blank" class="cert-link">Verify →</a>
                </p>
            </div>
            <div class="cert-item">
                <h4> Building AI Agents and Agentic Workflows Specialization Certificate</h4>
                <p class="cert-meta">Issued by: IBM (via Coursera)
                    <a href="https://coursera.org/verify/specialization/6N17YPAB1KO2" target="_blank" class="cert-link">Verify →</a>
                </p>
            </div>

            <div class="cert-item">
                <h4>BIM Fundamentals for Engineers</h4>
                <p class="cert-meta">Issued by: National Taiwan University (via Coursera)
                    <a href="https://coursera.org/verify/WJRUR5A9AUJ6" target="_blank" class="cert-link">Verify →</a>
                </p>
            </div>

            <div class="cert-item">
                <h4>Foundations of Project Management</h4>
                <p class="cert-meta">Issued by: Google (via Coursera)
                    <a href="https://coursera.org/verify/WJRUR5A9AUJ6" target="_blank" class="cert-link">Verify →</a>
                </p>
            </div>
        </section>

        <div class="expertise-box">
            <h3>Technical Competencies</h3>
            <ul class="expertise-list">
                <li>Python, JavaScript</li>
                <li>TensorFlow, PyTorch, Scikit-learn</li>
                <li>LangChain, LangGraph, RAG Systems</li>
                <li>RDF, OWL, SPARQL, Turtle</li>
                <li>Protégé, Owlready2, RDFlib</li>
                <li>Apache Jena Fuseki, ChromaDB</li>
                <li>Flask, FastAPI, Streamlit</li>
                <li>Revit, NavisWorks, IFC Standards</li>
                <li>Graph Neural Networks (PyG, DGL)</li>
                <li>Natural Language Processing</li>
            </ul>
        </div>

        <div class="footer-cta">
            <h2>Research Collaboration</h2>
            <p>I am interested in collaborative research opportunities around construction AI, semantic web technologies, knowledge graph applications, and intelligent document systems. I am also available for consulting on construction informatics projects and speaking engagements.</p>
            <div style="display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;">
                <a href="mailto:venkateshkone.connect@gmail.com" class="cta-button">Contact for Collaboration</a>
                <a href="/projects/" class="cta-button" style="background: #059669;">View My Work</a>
            </div>
        </div>
    </main>
</div>
