<script setup>
import dashboardImg from '@/assets/dashboardImg.png'

// Import Team Images
import annikaImg from '@/assets/Annika.png'
import collinImg from '@/assets/Collin.png'
import neelImg from '@/assets/Neel.png'
import jasonImg from '@/assets/Jason.png'
import alexImg from '@/assets/Alex.png'

// Team Data Configuration
const team = [
  { name: 'Annika Andersson', role: 'Project Lead', img: annikaImg },
  { name: 'Collin Knowles', role: 'Developer', img: collinImg },
  { name: 'Neel Ranawat', role: 'Developer', img: neelImg },
  { name: 'Jason Thai', role: 'Documentation', img: jasonImg },
  { name: 'Alex Thomas', role: 'Developer', img: alexImg }
]
</script>

<template>
  <div class="home-container">
    
    <section class="hero">
      <div class="hero-content">
        <h1>Sales Performance Dashboard</h1>
        <p class="subtitle">
          A strategic market analysis tool designed to benchmark performance, 
          identify stocking trends, and drive data-based business decisions.
        </p>
        
        <ul class="key-points">
          <li><strong>Global Analysis:</strong> Track sales across North America, Europe, and Japan.</li>
          <li><strong>Tactical Insights:</strong> Monitor top-performing genres and consoles.</li>
          <li><strong>Power BI:</strong> Built with robust ETL processes and dynamic filtering.</li>
        </ul>
      </div>

      <div class="hero-visual">
        <img :src="dashboardImg" alt="Power BI Dashboard Preview" class="dashboard-img" />
      </div>
    </section>

    <section class="features">
      <div class="feature-card">
        <h3>📊 Admin Dashboard</h3>
        <p>Strategic overview for management including Year-over-Year growth and regional market share analysis.</p>
      </div>
      <div class="feature-card">
        <h3>🏷️ Sales Dashboard</h3>
        <p>Tactical views for identifying top-selling titles and platform preferences to assist with stocking.</p>
      </div>
      <div class="feature-card">
        <h3>📂 Data Integrity</h3>
        <p>Utilizing Kaggle's 2024 Video Game Sales dataset with verified data cleaning and normalization.</p>
      </div>
    </section>

    <section class="team-section">
      <h2>Meet the Development Team</h2>
      <div class="team-grid">
        <div class="team-member" v-for="member in team" :key="member.name">
          <img :src="member.img" :alt="member.name" class="member-avatar" />
          <p class="member-name">{{ member.name }}</p>
          <span class="member-role">{{ member.role }}</span>
        </div>
      </div>
    </section>

  </div>
</template>

<style scoped>
.home-container {
  padding-bottom: 4rem;
}

/* HERO SECTION */
.hero {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 4rem;
  margin-bottom: 5rem;
  margin-top: 2rem;
  text-align: left;
}

.hero-content {
  flex: 1;
  padding-right: 2rem;
  padding-left: 1rem;
}

h1 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
  color: #2c3e50;
  line-height: 1.2;
}

.subtitle {
  font-size: 1.2rem;
  color: #666;
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.key-points {
  list-style: none;
  padding: 0;
}

.key-points li {
  margin-bottom: 0.8rem;
  font-size: 1rem;
  color: #444;
}

.key-points strong {
  color: #42b883;
}

/* HERO IMAGE */
.hero-visual {
  flex: 1;
  display: flex;
  justify-content: center;
}

.dashboard-img {
  width: 100%;
  max-width: 550px;
  height: auto;
  object-fit: contain;
  border-radius: 8px;
  box-shadow: 0 10px 25px rgba(0,0,0,0.15);
  border: 1px solid #ddd;
}

/* FEATURES GRID */
.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-bottom: 5rem;
}

.feature-card {
  background: #f9f9f9;
  padding: 1.5rem;
  border-radius: 8px;
  text-align: left;
  border: 1px solid #eee;
  transition: transform 0.2s;
}

.feature-card:hover {
  transform: translateY(-5px);
  border-color: #42b883;
}

.feature-card h3 {
  margin-top: 0;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.feature-card p {
  font-size: 0.95rem;
  color: #666;
  line-height: 1.5;
}

/* TEAM SECTION */
.team-section {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid #eee;
}

.team-section h2 {
  margin-bottom: 2rem;
  color: #2c3e50;
}

.team-grid {
  display: flex;
  justify-content: center;
  gap: 2rem;
  flex-wrap: wrap;
}

.team-member {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 180px; /* Increased width to fit full names */
}

.member-avatar {
  width: 120px;
  height: 120px;
  border-radius: 50%; /* Makes the image a perfect circle */
  object-fit: cover;  /* Ensures the photo fills the circle without stretching */
  margin-bottom: 1rem;
  border: 3px solid #f0f0f0;
  transition: border-color 0.2s;
}

.team-member:hover .member-avatar {
  border-color: #42b883; /* Green ring on hover */
}

.member-name {
  font-weight: bold;
  margin: 0;
  font-size: 1.1rem;
  color: #333;
}

.member-role {
  font-size: 0.9rem;
  color: #888;
  margin-top: 4px;
}

/* RESPONSIVE */
@media (max-width: 768px) {
  .hero {
    flex-direction: column-reverse;
    text-align: center;
    gap: 2rem;
  }
  
  .hero-content {
    padding: 0;
  }
}
</style>