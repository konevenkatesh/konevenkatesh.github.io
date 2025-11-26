---
layout: page
icon: fas fa-graduation-cap
order: 3
---

<style>
    /* Hide Chirpy default elements */
    h1.dynamic-title,
    .post-title,
    .page-title,
    #page-title,
    .post-meta,
    .breadcrumb,
    nav[aria-label="breadcrumb"] {
        display: none !important;
    }

    /* Main Container */
    .research-container {
        max-width: 900px;
        margin: 0 auto;
        padding: 2rem 1rem 3rem;
        font-family: Roboto, Arial, sans-serif;
        font-size: 14px;
        line-height: 1.6;
        color: #222;
    }

    .research-container * {
        box-sizing: border-box;
    }

    /* Research Interests Tags */
    .research-interests {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-bottom: 48px;
        padding-bottom: 24px;
        border-bottom: 1px solid #e0e0e0;
    }

    .interest-tag {
        padding: 8px 16px;
        background: #f1f3f4;
        border-radius: 20px;
        font-size: 13px;
        color: #5f6368;
        text-decoration: none;
        transition: background 0.2s;
    }

    .interest-tag:hover {
        background: #e8eaed;
    }

    /* Category Section */
    .publication-category {
        margin-bottom: 48px;
    }

    .category-header {
        font-size: 20px;
        font-weight: 500;
        color: #202124;
        margin-bottom: 24px;
        padding-bottom: 12px;
        border-bottom: 2px solid #1a73e8;
    }

    /* Publication Item */
    .publication-item {
        padding: 20px 0;
        border-bottom: 1px solid #f1f3f4;
        transition: background 0.1s;
    }

    .publication-item:hover {
        background: #f8f9fa;
        margin-left: -12px;
        margin-right: -12px;
        padding-left: 12px;
        padding-right: 12px;
        border-radius: 4px;
    }

    .pub-year {
        display: inline-block;
        font-size: 14px;
        font-weight: 600;
        color: #1a73e8;
        min-width: 45px;
        margin-right: 16px;
    }

    .pub-title {
        font-size: 16px;
        margin-bottom: 8px;
        line-height: 1.4;
    }

    .pub-title a {
        color: #1a0dab;
        text-decoration: none;
    }

    .pub-title a:visited {
        color: #681da8;
    }

    .pub-title a:hover {
        text-decoration: underline;
    }

    .pub-authors {
        font-size: 13px;
        color: #5f6368;
        margin-bottom: 4px;
    }

    .pub-venue {
        font-size: 13px;
        color: #5f6368;
        line-height: 1.5;
    }

    .pub-badge {
        display: inline-block;
        padding: 2px 8px;
        margin-left: 8px;
        background: #e8f0fe;
        color: #1967d2;
        font-size: 11px;
        border-radius: 3px;
        font-weight: 500;
    }

    .pub-badge.new {
        background: #fce8e6;
        color: #c5221f;
    }

    .pub-badge.access {
        background: #e6f4ea;
        color: #137333;
    }

    /* Footer */
    .research-footer {
        margin-top: 64px;
        padding: 32px;
        background: #f8f9fa;
        border-radius: 8px;
        text-align: center;
    }

    .research-footer p {
        font-size: 14px;
        color: #5f6368;
        margin-bottom: 16px;
    }

    .scholar-link {
        display: inline-flex;
        align-items: center;
        gap: 8px;
        padding: 10px 24px;
        background: #1a73e8;
        color: white;
        text-decoration: none;
        border-radius: 4px;
        font-size: 14px;
        font-weight: 500;
        transition: background 0.2s;
    }

    .scholar-link:hover {
        background: #1557b0;
        color: white;
    }

    /* Responsive */
    @media (max-width: 768px) {
        .research-container {
            padding: 1.5rem 1rem 2rem;
        }

        .research-interests {
            margin-bottom: 32px;
        }

        .category-header {
            font-size: 18px;
            margin-bottom: 16px;
        }

        .pub-year {
            display: block;
            margin-bottom: 8px;
        }

        .pub-title {
            font-size: 15px;
        }

        .publication-item {
            padding: 16px 0;
        }
    }

    /* Print */
    @media print {
        .publication-item:hover {
            background: none;
        }
        
        .research-footer {
            display: none;
        }
    }
</style>

<div class="research-container">
    <!-- Research Interests -->
    <div class="research-interests">
        <span class="interest-tag">Construction Management</span>
        <span class="interest-tag">Knowledge Management</span>
        <span class="interest-tag">BIM</span>
        <span class="interest-tag">Digital Transformation</span>
        <span class="interest-tag">Ontology Engineering</span>
        <span class="interest-tag">Semantic Web Technologies</span>
    </div>

    <!-- Journal Articles -->
    <div class="publication-category">
        <h2 class="category-header">Journal Articles</h2>

        <!-- 2025 -->
        <div class="publication-item">
            <span class="pub-year">2025</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1080/15623599.2025.2562105" target="_blank" rel="noopener">
                    The IproK ontology: a unified approach to managing construction project information
                </a>
                <span class="pub-badge new">New</span>
            </div>
            <div class="pub-authors">V Kone, G Mahesh</div>
            <div class="pub-venue">International Journal of Construction Management, 1-30</div>
        </div>

        <!-- 2020 -->
        <div class="publication-item">
            <span class="pub-year">2020</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1016/j.matpr.2020.02.086" target="_blank" rel="noopener">
                    A study on factors involved in implementation of supply chain management in construction industry
                </a>
            </div>
            <div class="pub-authors">VR Battula, SK Namburu, V Kone</div>
            <div class="pub-venue">Materials Today: Proceedings 33, 446-449</div>
        </div>

        <div class="publication-item">
            <span class="pub-year">2020</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1016/j.matpr.2020.02.078" target="_blank" rel="noopener">
                    Monitoring of varadhi road bridge using accelerometer sensor
                </a>
            </div>
            <div class="pub-authors">K Chilamkuri, V Kone</div>
            <div class="pub-venue">Materials Today: Proceedings 33, 367-371</div>
        </div>

        <div class="publication-item">
            <span class="pub-year">2020</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1016/j.matpr.2020.02.132" target="_blank" rel="noopener">
                    Forecasting the construction cost by using unit based estimation model
                </a>
            </div>
            <div class="pub-authors">K Pujitha, K Venkatesh</div>
            <div class="pub-venue">Materials Today: Proceedings 33, 613-619</div>
        </div>

        <div class="publication-item">
            <span class="pub-year">2020</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1016/j.matpr.2020.02.074" target="_blank" rel="noopener">
                    A study on ground water problems, artificial recharge techniques in Musunuru
                </a>
            </div>
            <div class="pub-authors">MSS Reddy, NS Kumar, K Venkatesh</div>
            <div class="pub-venue">Materials Today: Proceedings 33, 353-359</div>
        </div>

        <!-- 2019 -->
        <div class="publication-item">
            <span class="pub-year">2019</span>
            <div class="pub-title">
                <a href="https://www.ijrte.org/wp-content/uploads/papers/v8i4/D7876118419.pdf" target="_blank" rel="noopener">
                    Simulation of construction sequence using BIM 4D techniques
                </a>
            </div>
            <div class="pub-authors">HV Tirunagari, V Kone</div>
            <div class="pub-venue">International Journal of Recent Technology and Engineering 8(4), 21-23</div>
        </div>

        <!-- 2018 -->
        <div class="publication-item">
            <span class="pub-year">2018</span>
            <div class="pub-title">
                <a href="#" target="_blank" rel="noopener">
                    Evaluation of reducing waste materials in construction projects using ranking analysis
                </a>
            </div>
            <div class="pub-authors">B Sayed, SS Asadi, K Venkatesh</div>
            <div class="pub-venue">International Journal of Civil Engineering and Technology 9, 831-838</div>
        </div>
    </div>

    <!-- Conference Papers -->
    <div class="publication-category">
        <h2 class="category-header">Conference Papers</h2>

        <!-- 2025 -->
        <div class="publication-item">
            <span class="pub-year">2025</span>
            <div class="pub-title">
                <a href="https://dfbi.org" target="_blank" rel="noopener">
                    Ontology-Driven Project Management: A Framework for Structured Data and Automation
                </a>
                <span class="pub-badge new">New</span>
            </div>
            <div class="pub-authors">V Kone, G Mahesh</div>
            <div class="pub-venue">Proceedings of Digital Frontiers in Buildings and Infrastructure International Conference Series, 77-88</div>
        </div>

        <!-- 2023 -->
        <div class="publication-item">
            <span class="pub-year">2023</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1007/978-981-96-4902-0_14" target="_blank" rel="noopener">
                    Enhancing Knowledge Management in the Construction Industry: Exploring the Impact of Semantic Web Technologies
                </a>
            </div>
            <div class="pub-authors">V Kone, G Mahesh, PV Ingle</div>
            <div class="pub-venue">Advances in Construction Management. ICCRIP 2023. Lecture Notes in Civil Engineering, vol 601. Springer, Singapore</div>
        </div>

        <!-- 2020 -->
        <div class="publication-item">
            <span class="pub-year">2020</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1088/1757-899X/912/6/062049" target="_blank" rel="noopener">
                    Feasibility study and implementation of BIM in small scale projects
                </a>
                <span class="pub-badge access">Open Access</span>
            </div>
            <div class="pub-authors">DP Munagala, V Kone</div>
            <div class="pub-venue">IOP Conference Series: Materials Science and Engineering, 912(6), 062049</div>
        </div>

        <!-- 2019 -->
        <div class="publication-item">
            <span class="pub-year">2019</span>
            <div class="pub-title">
                <a href="#" target="_blank" rel="noopener">
                    Study on implementing smart construction with various applications using internet of things techniques
                </a>
            </div>
            <div class="pub-authors">HG Reddy, V Kone</div>
            <div class="pub-venue">International Conference on Advances in Civil Engineering (ICACE-2019), 21-23</div>
        </div>

        <div class="publication-item">
            <span class="pub-year">2019</span>
            <div class="pub-title">
                <a href="https://doi.org/10.1007/978-981-13-6374-0_50" target="_blank" rel="noopener">
                    Effect of twist angle and RPM on the natural vibration of composite beams made up of hybrid laminates
                </a>
            </div>
            <div class="pub-authors">R Potluri, V Diwakar, K Venkatesh, R Sravani</div>
            <div class="pub-venue">Advances in Manufacturing Technology: Select Proceedings of ICAMT 2018, 443-452</div>
        </div>
    </div>

    <!-- Footer -->
    <div class="research-footer">
        <p>View complete publication list and citation metrics</p>
        <a href="https://scholar.google.com/citations?user=0aKzihMAAAAJ&hl=en" target="_blank" rel="noopener" class="scholar-link">
            <span>🎓</span>
            <span>Google Scholar Profile</span>
        </a>
    </div>
</div>
