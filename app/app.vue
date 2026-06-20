<script setup>
const navLinks = [
  { label: 'Services', href: '#services' },
  { label: 'Team', href: '#team' },
  { label: 'Gallery', href: '#gallery' },
  { label: 'Contact', href: '#contact' },
]

const services = [
  {
    name: 'Signature Haircut',
    price: '$38',
    description: 'A detailed cut finished with a hot towel and clean neckline.',
  },
  {
    name: 'Skin Fade',
    price: '$45',
    description: 'Sharp fade work blended to your preferred length and style.',
  },
  {
    name: 'Beard Trim',
    price: '$24',
    description: 'Shape, line work, and conditioning for a polished beard.',
  },
  {
    name: 'Gel Manicure',
    price: '$42',
    description: 'Clean shaping, cuticle care, gel polish, and a glossy finish.',
  },
  {
    name: 'Nail Art Set',
    price: '$65+',
    description: 'Custom designs, chrome, charms, or seasonal accent work.',
  },
  {
    name: 'Blowout & Style',
    price: '$48',
    description: 'Fresh wash, round brush blowout, and polished styling.',
  },
]

const teamMembers = [
  {
    name: 'Sam Holmes',
    title: 'Barber',
    bio: 'A barber focused on sharp service, clean detail work, and a smooth appointment experience.',
    specialty: 'Fades, beard work',
    image: '/images/sam-holmes-logo.jpg',
  },
  {
    name: 'Juan Garcia',
    title: 'Barber',
    bio: 'Known for detailed barbering and a station built around focused, one-on-one service.',
    specialty: 'Tapers, custom cuts',
    image: '/images/juan-work-station.jpg',
  },
  {
    name: 'Alize Hildago',
    title: 'Hairstylist',
    bio: 'Offers polished hair services with brows and waxing available by appointment.',
    specialty: 'Hair, eyebrows, waxing',
    image: '/images/alize-hidalgo-work.jpg',
  },
  {
    name: 'Nails by Oz',
    title: 'Nail Tech',
    bio: 'Creates playful nail sets with color, texture, and custom art details.',
    specialty: 'Themed sets, nail art',
    image: '/images/nails-sea-theme.jpg',
  },
  {
    name: 'Daisy Daisy Nails',
    title: 'Nail Tech',
    bio: 'Brings bright, detailed nail work with a polished finish and creative style.',
    specialty: 'Detailed sets, nail art',
    image: '/images/daisy-work.jpg',
  },
]

const galleryImages = [
  '/images/hair-before-after.png',
  '/images/hair-before-after-2.jpg',
  '/images/hair-3.jpg',
  '/images/nails-green-blue.jpg.png',
  '/images/nails-cheetah-variety.jpg',
  '/images/nails-dark-black.jpg',
  '/images/fade-design-1.jpg.png',
  '/images/star-design-cut.jpg.png',
  '/images/neckline-design.jpg.png',
]

const experienceItems = [
  'Appointments that start on time',
  'Detailed consultations before every service',
  'Sharp barbering, polished nails, and finished hair',
  'Clean stations, fresh tools, and relaxed music',
]

const heroBackground = {
  backgroundImage:
    "linear-gradient(90deg, rgba(12, 11, 9, 0.95), rgba(12, 11, 9, 0.74), rgba(12, 11, 9, 0.34)), url('/images/station-1.jpg.png')",
}
</script>

<template>
  <main class="site-shell">
    <nav class="navbar" aria-label="Primary navigation">
      <a class="brand" href="#top">Tapered & Tipped</a>

      <div class="nav-links">
        <a v-for="link in navLinks" :key="link.label" :href="link.href">
          {{ link.label }}
        </a>
      </div>

      <a class="nav-cta" href="#team">Book with GlossGenius</a>
    </nav>

    <section id="top" class="hero section" :style="heroBackground">
      <div class="hero-content">
        <p class="eyebrow">Cuts, nails, and finished styles</p>
        <h1>Tapered cuts, tipped nails, and polished style in one chair-to-chair studio.</h1>
        <p class="hero-copy">
          Placeholder concept for Tapered and Tipped, built around sharp barbering,
          detailed nail work, finished hair, and simple GlossGenius booking.
        </p>

        <div class="hero-actions">
          <a class="button primary" href="#team">Book with GlossGenius</a>
          <a class="button secondary" href="#services">View Services</a>
        </div>
      </div>

      <div class="hero-card" aria-label="Featured appointment details">
        <img
          class="hero-logo"
          src="/images/tapered-and-tipped-facebook.jpg"
          alt="Tapered and Tipped Facebook logo"
        >
        <span>Today&apos;s vibe</span>
        <strong>Clean fades, glossy sets, and styles that leave finished.</strong>
        <p>By appointment only in Durant, Oklahoma.</p>
      </div>
    </section>

    <section id="services" class="section">
      <div class="section-heading">
        <p class="eyebrow">Services & pricing</p>
        <h2>Popular cuts, nail services, and styling</h2>
      </div>

      <div class="services-grid">
        <article v-for="service in services" :key="service.name" class="service-card">
          <div>
            <h3>{{ service.name }}</h3>
            <p>{{ service.description }}</p>
          </div>
          <strong>{{ service.price }}</strong>
        </article>
      </div>
    </section>

    <section id="team" class="section team-section">
      <div class="section-heading">
        <p class="eyebrow">Meet our team</p>
        <h2>Two barbers, two nail techs, and one hairstylist with their own booking links</h2>
      </div>

      <div class="team-grid">
        <article v-for="member in teamMembers" :key="member.name" class="team-card">
          <img :src="member.image" :alt="`${member.name} placeholder portrait`">
          <div class="team-body">
            <p>{{ member.title }}</p>
            <h3>{{ member.name }}</h3>
            <span>{{ member.specialty }}</span>
            <p>{{ member.bio }}</p>
            <a class="button small" href="#">Book with GlossGenius</a>
          </div>
        </article>
      </div>
    </section>

    <section id="gallery" class="section">
      <div class="section-heading split">
        <div>
          <p class="eyebrow">Gallery</p>
          <h2>Placeholder visuals for cuts, nails, styling, and the studio</h2>
        </div>
        <a
          class="text-link"
          href="https://www.facebook.com/profile.php?id=61578779285623"
          target="_blank"
          rel="noopener noreferrer"
        >
          Follow on Facebook
        </a>
      </div>

      <div class="gallery-grid">
        <img
          v-for="(image, index) in galleryImages"
          :key="image"
          :src="image"
          :alt="`Tapered and Tipped gallery placeholder ${index + 1}`"
        >
      </div>
    </section>

    <section class="section experience-section">
      <div class="experience-copy">
        <p class="eyebrow">Why choose us</p>
        <h2>A balanced studio experience from check-in to final mirror check.</h2>
        <p>
          This Phase 1 concept keeps the experience focused: clear services,
          strong team profiles, visual proof, and a simple path to each provider&apos;s
          GlossGenius booking page.
        </p>
      </div>

      <div class="experience-list">
        <div v-for="item in experienceItems" :key="item" class="experience-item">
          <span></span>
          <p>{{ item }}</p>
        </div>
      </div>
    </section>

    <section id="contact" class="section contact-section">
      <div class="section-heading">
        <p class="eyebrow">Contact & location</p>
        <h2>Pull up, check in, and leave sharpened, styled, or freshly tipped.</h2>
      </div>

      <div class="contact-grid">
        <div class="contact-card">
          <span>Address</span>
          <p>201 E Main St<br>Durant, OK 74701</p>
        </div>
        <div class="contact-card">
          <span>Hours</span>
          <p>Mon - Fri: 9:00 AM - 7:00 PM<br>Sat: 9:00 AM - 6:00 PM<br>Sun: Closed</p>
        </div>
        <div class="contact-card">
          <span>Booking</span>
          <p>By appointment only<br>Book each provider through GlossGenius</p>
        </div>
        <div class="contact-card">
          <span>Social</span>
          <p>Tapered and Tipped<br>Hablamos Espanol</p>
        </div>
      </div>

      <a class="button primary contact-button" href="#team">Book with GlossGenius</a>
    </section>

    <footer class="footer">
      <p>Tapered & Tipped</p>
      <p>Placeholder Phase 1 website prototype. No backend, accounts, or custom booking logic.</p>
    </footer>
  </main>
</template>

<style scoped>
:global(*) {
  box-sizing: border-box;
}

:global(html) {
  scroll-behavior: smooth;
}

:global(body) {
  margin: 0;
  background: #0c0b09;
  color: #f7f1e8;
  font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

:global(a) {
  color: inherit;
  text-decoration: none;
}

.site-shell {
  min-height: 100vh;
  overflow: hidden;
  background:
    radial-gradient(circle at 78% 0%, rgba(205, 116, 144, 0.2), transparent 28rem),
    radial-gradient(circle at 10% 12%, rgba(198, 137, 69, 0.16), transparent 26rem),
    linear-gradient(180deg, #11100d 0%, #0c0b09 42%, #171116 100%);
}

.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding: 1rem;
  background: rgba(12, 11, 9, 0.84);
  border-bottom: 1px solid rgba(255, 255, 255, 0.08);
  backdrop-filter: blur(18px);
}

.brand {
  font-size: 1.05rem;
  font-weight: 800;
  letter-spacing: 0;
}

.nav-links {
  display: none;
}

.nav-cta {
  display: none;
}

.section {
  scroll-margin-top: 5rem;
  width: min(1120px, calc(100% - 2rem));
  margin: 0 auto;
  padding: 4.5rem 0;
}

.hero {
  position: relative;
  display: grid;
  min-height: 100vh;
  align-items: end;
  padding-top: 7rem;
  background-position: center;
  background-size: cover;
  width: 100%;
  max-width: none;
  padding-left: max(1rem, calc((100vw - 1120px) / 2));
  padding-right: max(1rem, calc((100vw - 1120px) / 2));
}

.hero-content {
  max-width: 760px;
  padding-bottom: 4rem;
}

.eyebrow {
  margin: 0 0 0.8rem;
  color: #d98ba8;
  font-size: 0.75rem;
  font-weight: 800;
  letter-spacing: 0.12em;
  text-transform: uppercase;
}

h1,
h2,
h3,
p {
  margin-top: 0;
}

h1 {
  margin-bottom: 1.15rem;
  font-size: clamp(3rem, 13vw, 6.8rem);
  line-height: 0.92;
  letter-spacing: 0;
}

h2 {
  margin-bottom: 0;
  max-width: 760px;
  font-size: clamp(2rem, 7vw, 4rem);
  line-height: 1;
  letter-spacing: 0;
}

h3 {
  margin-bottom: 0.55rem;
  font-size: 1.2rem;
}

.hero-copy {
  max-width: 610px;
  color: #d6cab9;
  font-size: 1.05rem;
  line-height: 1.7;
}

.hero-actions {
  display: flex;
  flex-direction: column;
  gap: 0.85rem;
  margin-top: 1.6rem;
}

.button {
  display: inline-flex;
  min-height: 3.15rem;
  align-items: center;
  justify-content: center;
  border-radius: 999px;
  padding: 0.85rem 1.25rem;
  font-weight: 800;
  transition: transform 160ms ease, border-color 160ms ease, background 160ms ease;
}

.button:hover {
  transform: translateY(-2px);
}

.primary {
  background: linear-gradient(135deg, #d89a50, #e6a2bc);
  color: #15100a;
}

.secondary {
  border: 1px solid rgba(255, 255, 255, 0.28);
  color: #f7f1e8;
}

.small {
  width: 100%;
  min-height: 2.8rem;
  margin-top: 1.2rem;
  background: #f7f1e8;
  color: #15100a;
}

.hero-card {
  width: min(100%, 390px);
  margin-bottom: 1rem;
  padding: 1.25rem;
  border: 1px solid rgba(255, 255, 255, 0.16);
  border-radius: 8px;
  background: rgba(17, 16, 13, 0.76);
  backdrop-filter: blur(14px);
}

.hero-logo {
  display: block;
  width: 100%;
  aspect-ratio: 16 / 10;
  margin-bottom: 1rem;
  border-radius: 8px;
  object-fit: cover;
  object-position: center;
}

.hero-card span,
.contact-card span {
  color: #d98ba8;
  font-size: 0.78rem;
  font-weight: 800;
  letter-spacing: 0.1em;
  text-transform: uppercase;
}

.hero-card strong {
  display: block;
  margin: 0.5rem 0;
  font-size: 1.35rem;
  line-height: 1.25;
}

.hero-card p {
  margin-bottom: 0;
  color: #d6cab9;
}

.section-heading {
  margin-bottom: 2rem;
}

.section-heading.split {
  display: grid;
  gap: 1rem;
}

.services-grid,
.team-grid,
.contact-grid {
  display: grid;
  gap: 1rem;
}

.service-card,
.contact-card {
  display: flex;
  justify-content: space-between;
  gap: 1rem;
  padding: 1.15rem;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  background: rgba(255, 255, 255, 0.045);
}

.service-card p,
.team-body p,
.experience-copy p,
.contact-card p,
.footer p {
  color: #cfc4b4;
  line-height: 1.65;
}

.service-card p,
.contact-card p {
  margin-bottom: 0;
}

.service-card strong {
  color: #f0b66d;
  font-size: 1.25rem;
  white-space: nowrap;
}

.team-section {
  width: 100%;
  max-width: none;
  padding-left: max(1rem, calc((100vw - 1120px) / 2));
  padding-right: max(1rem, calc((100vw - 1120px) / 2));
  background:
    linear-gradient(135deg, rgba(216, 154, 80, 0.08), rgba(217, 139, 168, 0.11)),
    #171411;
}

.team-card {
  overflow: hidden;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  background: #211c17;
}

.team-card img,
.gallery-grid img {
  display: block;
  width: 100%;
  object-fit: cover;
}

.team-card img {
  height: 270px;
}

.team-body {
  padding: 1.15rem;
}

.team-body > p:first-child {
  margin-bottom: 0.35rem;
  color: #d98ba8;
  font-size: 0.82rem;
  font-weight: 800;
  text-transform: uppercase;
}

.team-body span {
  display: block;
  margin-bottom: 0.85rem;
  color: #f0b66d;
  font-weight: 700;
}

.text-link {
  color: #e6a2bc;
  font-weight: 800;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 0.7rem;
}

.gallery-grid img {
  aspect-ratio: 1;
  border-radius: 8px;
}

.experience-section {
  display: grid;
  gap: 2rem;
}

.experience-copy p {
  max-width: 620px;
}

.experience-list {
  display: grid;
  gap: 0.85rem;
}

.experience-item {
  display: flex;
  align-items: center;
  gap: 0.85rem;
  padding: 1rem;
  border-left: 3px solid #d98ba8;
  background: rgba(255, 255, 255, 0.05);
}

.experience-item span {
  width: 0.6rem;
  height: 0.6rem;
  flex: 0 0 auto;
  border-radius: 999px;
  background: #d98ba8;
}

.experience-item p {
  margin-bottom: 0;
  color: #f7f1e8;
  font-weight: 700;
}

.contact-section {
  padding-bottom: 3rem;
}

.contact-card {
  display: block;
}

.contact-card p {
  margin-top: 0.5rem;
}

.contact-button {
  width: 100%;
  margin-top: 1.2rem;
}

.footer {
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
  padding: 1.5rem 1rem;
  border-top: 1px solid rgba(255, 255, 255, 0.08);
  text-align: center;
}

.footer p {
  margin-bottom: 0;
  font-size: 0.92rem;
}

.footer p:first-child {
  color: #f7f1e8;
  font-weight: 800;
}

@media (min-width: 700px) {
  .navbar {
    padding: 1rem 2rem;
  }

  .nav-links {
    display: flex;
    gap: 1.2rem;
    color: #d6cab9;
    font-size: 0.94rem;
    font-weight: 700;
  }

  .hero-actions {
    flex-direction: row;
  }

  .button {
    width: auto;
  }

  .services-grid,
  .contact-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .gallery-grid {
    grid-template-columns: repeat(3, 1fr);
  }

  .section-heading.split,
  .experience-section {
    grid-template-columns: 1fr 0.75fr;
    align-items: end;
  }

  .text-link {
    justify-self: end;
  }
}

@media (min-width: 980px) {
  .nav-cta {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    border-radius: 999px;
    background: #f7f1e8;
    color: #15100a;
    padding: 0.75rem 1rem;
    font-weight: 800;
  }

  .hero {
    grid-template-columns: 1fr 390px;
    align-items: end;
    gap: 2rem;
  }

  .hero-card {
    margin-bottom: 4rem;
  }

  .services-grid {
    grid-template-columns: repeat(3, 1fr);
  }

  .service-card {
    min-height: 190px;
    flex-direction: column;
  }

  .team-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>
