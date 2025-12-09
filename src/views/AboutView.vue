<template>
  <div class="about-container">
    
    <section class="page-header">
      <h1>Project Documentation</h1>
      <p class="intro-text">
        A technical breakdown of the Sales Performance Dashboard, including data modeling, 
        ETL processes, and functional requirements.
      </p>
    </section>

    <div class="content-grid">
      
      <div class="main-column">
        
        <section class="doc-section">
          <h2>Overview & Objectives</h2>
          <p>
            The goal of this project is to create a strategic market analysis tool for in-store use. 
            It benchmarks performance and identifies stocking trends using data from the 
            <strong>Video Game Sales 2024 (Kaggle)</strong> dataset.
          </p>
          <p>
            The system is designed with two distinct user views:
          </p>
          <ul>
            <li><strong>Admin Dashboard:</strong> Strategic overview for management (Global Sales, YoY Growth).</li>
            <li><strong>Sales Dashboard:</strong> Tactical page for stocking and regional trends.</li>
          </ul>
        </section>

        <section class="doc-section">
          <h2>Data Architecture & ETL</h2>
          <p>
            The project utilizes a <strong>hybrid star and snowflake schema</strong>. 
            Data is extracted from CSV sources, cleaned in Power BI Desktop, and normalized.
          </p>
          <ul class="tech-list">
            <li><strong>Source:</strong> CSV (Comma-Separated Values) / Excel</li>
            <li><strong>Transformation:</strong> Unpivoted regional sales; normalized Publisher/Developer tables.</li>
            <li><strong>Modeling:</strong> Relationships established between <em>Games</em> (One) and <em>Sales</em> (Many).</li>
          </ul>
        </section>

        <section class="doc-section">
          <h2>Key Performance Indicators (KPIs)</h2>
          <div class="kpi-grid">
            <div class="kpi-card">Global Market Sales</div>
            <div class="kpi-card">Regional Market Share %</div>
            <div class="kpi-card">Year-over-Year Growth</div>
            <div class="kpi-card">Top N Titles by Sales</div>
            <div class="kpi-card">Platform Market Share</div>
            <div class="kpi-card">Average Critic Score</div>
          </div>
        </section>

      </div>

      <aside class="sidebar">
        
        <div class="tool-box">
          <h3>🛠️ Tech Stack</h3>
          <ul>
            <li>Microsoft Power BI Desktop</li>
            <li>Power BI Online Service</li>
            <li>Vue.js 3 (Documentation Site)</li>
            <li>Kaggle Datasets</li>
          </ul>
        </div>

        <div class="github-box">
          <h3>📂 Project File</h3>
          <p>View the full project source code, including DAX measures.</p>
          <a href="/TestingPBI.pbix" download="TestingPBI.pbix" class="github-btn">
            Download Dashboard File <span class="icon">↓</span>
          </a>
        </div>

      </aside>

    </div>
  </div>
</template>

<style scoped>
.about-container {
  max-width: 1000px;
  margin: 0 auto;
  padding-bottom: 4rem;
  text-align: left; /* Resets text alignment */
}

/* HEADER */
.page-header {
  margin-bottom: 3rem;
  border-bottom: 1px solid #eee;
  padding-bottom: 2rem;
}

.page-header h1 {
  font-size: 2.5rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.intro-text {
  font-size: 1.2rem;
  color: #666;
  max-width: 700px;
}

/* LAYOUT GRID */
.content-grid {
  display: grid;
  grid-template-columns: 2fr 1fr; /* 2/3rds for content, 1/3rd for sidebar */
  gap: 4rem;
}

/* SECTIONS */
.doc-section {
  margin-bottom: 3rem;
}

.doc-section h2 {
  color: #42b883; /* Vue Green */
  font-size: 1.5rem;
  margin-bottom: 1rem;
  border-left: 4px solid #42b883;
  padding-left: 1rem;
}

.doc-section p, .doc-section li {
  line-height: 1.6;
  color: #444;
  margin-bottom: 1rem;
}

/* KPI GRID */
.kpi-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
  gap: 1rem;
}

.kpi-card {
  background: #f4f4f4;
  padding: 1rem;
  border-radius: 6px;
  font-weight: bold;
  font-size: 0.9rem;
  color: #555;
  text-align: center;
  border: 1px solid #e0e0e0;
}

/* SIDEBAR TOOLS */
.tool-box {
  background: #2c3e50;
  color: white;
  padding: 1.5rem;
  border-radius: 8px;
  margin-bottom: 2rem;
}

.tool-box h3 {
  margin-top: 0;
  border-bottom: 1px solid #4a5d70;
  padding-bottom: 0.5rem;
  margin-bottom: 1rem;
}

.tool-box ul {
  list-style: none;
  padding: 0;
}

.tool-box li {
  margin-bottom: 0.8rem;
  padding-left: 1.5rem;
  position: relative;
}

.tool-box li::before {
  content: "✓";
  color: #42b883;
  position: absolute;
  left: 0;
  font-weight: bold;
}

/* GITHUB BOX */
.github-box {
  background: #f9f9f9;
  border: 1px solid #ddd;
  padding: 1.5rem;
  border-radius: 8px;
}

.github-box h3 {
  margin-top: 0;
}

.github-btn {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #24292e; /* GitHub Black */
  color: white;
  text-decoration: none;
  padding: 10px 15px;
  border-radius: 6px;
  font-weight: bold;
  margin-top: 1rem;
  transition: background-color 0.2s;
}

.github-btn:hover {
  background-color: #444;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .content-grid {
    grid-template-columns: 1fr; /* Stack columns on mobile */
    gap: 2rem;
  }
}
</style>