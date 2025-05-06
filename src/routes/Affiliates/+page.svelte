<svelte:head>
  <title>Affiliates</title>
</svelte:head>

<script>
  import { base } from '$app/paths';
</script>


<section class="affiliates-section">
  <h1>Affiliated Projects</h1>
  <hr />

  <div class="projects-grid">
    <div class="project-card">
      <img src={base + '/images/amsterdam_theater.jpeg'} alt="Amsterdam Theater">
      <hr />
      <a href="https://www.vondel.humanities.uva.nl/onstage/" target="_blank" class="project-title">Onstage (Amsterdam)</a>
      <p class="project-description">
        This is your address for questions about the repertoire, performances, popularity and revenues of the cultural program in Amsterdam’s public theatre during the period 1637 - 1772.
      </p>
    </div>

    <div class="project-card">
      <img src={base + '/images/lond_theat.jpg'} alt="London Theater">
      <hr />
      <a href="https://www.theatronomics.com/" target="_blank" class="project-title">Theatronomics (London)</a>
      <p class="project-description">
        Theatronomics offers an account of the eighteenth-century London stage. We tell the story of the commercial side of the entertainment industry to understand why some people made it…. and others did not.
      </p>
    </div>

    <div class="project-card">
      <img src={base + '/images/comed_fran.jpg'} alt="Comédie-Française">
      <hr />
      <a href="https://www.cfregisters.org/#!/" target="_blank" class="project-title">Comédie-Française (Paris)</a>
      <p class="project-description">
        Since its establishment in 1680, the Comédie-Française has produced and preserved daily registers documenting the company’s income and expenses, as well as the plays performed and their casting.
      </p>
    </div>

    <div class="project-card">
      <img src={base + '/images/perf_hait.jpg'} alt="Saint Domingue Theater">
      <hr />
      <a href="https://www.theatreinsaintdomingue.org/" target="_blank" class="project-title">Theatre in St Domingue</a>
      <p class="project-description">
        This website and database seek to make known the rich and varied culture of public theatre as documented in the local newspapers between 1764 and 1791.
      </p>
    </div>

    <div class="project-card">
      <img src={base + '/images/copen_theat.jpg'} alt="Copenhagen Theater">
      <hr />
      <a href="https://artex.au.dk/" target="_blank" class="project-title">Artistic Exchanges (Copenhagen)</a>
      <p class="project-description">
        Artistic Exchanges explores the transnational currents of Danish theatre. Follow the routes of travelling artists on the interactive mobility map, discover artists and their works, and delve into the repertoire of the Danish stage.
      </p>
    </div>
  </div>
</section>

<section class="timeline-section">
  <h2>Timeline of Projects</h2>
  <p class="subtitle">Sorted by beginning of time period examined</p>

  <hr />
  <br />

  <div class="horizontal-timeline">
    <div class="timeline-line"></div>

    <div class="timeline-item">
      <div class="dot"></div>
      <div class="label">
        <strong>Onstage (Amsterdam)</strong><br />
        1637–1940
      </div>
    </div>

    <div class="timeline-item">
      <div class="dot"></div>
      <div class="label">
        <strong>Comédie-Française (Paris)</strong><br />
        1680–1793, 1799–1900<br />
        <span class="note">(6-year hiatus during the French Revolution)</span>
      </div>
    </div>


    <div class="timeline-item">
      <div class="dot"></div>
      <div class="label">
        <strong>Theatronomics (London)</strong><br />
        1732–1809
      </div>
    </div>

    <div class="timeline-item">
      <div class="dot"></div>
      <div class="label">
        <strong>Royal Danish Theatre (Copenhagen)</strong><br />
        1748–1900
      </div>
    </div>

    <div class="timeline-item">
      <div class="dot"></div>
      <div class="label">
        <strong>Theatre in St Domingue</strong><br />
        1764–1791
      </div>
    </div>
  </div>
</section>





<style>

.project-card img {
  width: 100%;
  height: 180px; /* or 200px if you want slightly taller */
  object-fit: cover;
  border-radius: 8px;
  margin-bottom: 1rem;
}

:global(body) {
  font-family: 'Inter', sans-serif;
  color: #1f1f1f;
  margin: 0;
  background-color: #f9f9f9;
}

h1, h2 {
  font-family: 'Playfair Display', serif;
  font-weight: 700;
  text-align: center;
  margin-bottom: 2rem;
  color: #333;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1rem;
  margin-top: 2rem;
}

.project-card {
  background-color: white;
  border-radius: 5px;
  padding: 1rem;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.project-title {
  font-size: 1.3rem;
  color: #3b6f6b;
  font-weight: bold;
  text-decoration: none;
}

.project-title:hover {
  text-decoration: underline;
}

.project-description {
  margin-top: 0.8rem;
  font-size: 1rem;
  line-height: 1.6;
  color: #000000;
}
.timeline-section {
  max-width: 1200px;
  margin: 4rem auto;
  padding: 0 2rem;
  text-align: center;
}

h2 {
  font-family: 'Playfair Display', serif;
  font-size: 2.5rem;
  margin-bottom: 2rem;
  color: #333;
}

.horizontal-timeline {
  background: #e0e0e0;
  padding: 3rem 1rem 1rem 1rem;
  border-radius: 12px;
  position: relative;
  overflow: hidden;
}

.timeline-line {
  position: absolute;
  top: 21%;
  left: 5%;
  right: 5%;
  height: 4px;
  background-color: #3b6f6b;
  z-index: 1;
  border-radius: 2px;
}

.timeline-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 20%; /* 5 items → 100%/5 = 20% */
  position: relative;
  float: left;
  text-align: center;
  z-index: 2;
}

.dot {
  width: 16px;
  height: 16px;
  background-color: #3b6f6b;
  border: 2px solid white;
  border-radius: 50%;
  margin-bottom: 0.5rem;
  position: relative;
  top: -8px; /* Move dot onto the timeline line */
}

.label {
  margin-top: 0.5rem;
  font-size: 1rem;
  color: #333;
  line-height: 1.4;
  max-width: 160px;
}

.label .note {
  font-size: 0.8rem;
  color: #666;
  margin-top: 0.2rem;
  display: block;
}


.label strong {
  font-family: 'Playfair Display', serif;
  font-size: 1.1rem;
}

@media (max-width: 768px) {
  .timeline-item {
    width: 100%;
    margin-bottom: 2rem;
    float: none;
  }
  .horizontal-timeline {
    height: auto;
    padding: 2rem 1rem;
  }
  .timeline-line {
    top: auto;
    bottom: 0;
    left: 10%;
    right: 10%;
  }
}



</style>
