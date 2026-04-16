<template>
  <div class="landing">
    <!-- NAVBAR -->
    <header class="navbar" :class="{ scrolled: isScrolled }">
      <div class="container nav-inner">
        <a href="#" class="logo">
          <span class="logo-icon">✦</span>
          <span class="logo-text">Best <span>Way</span></span>
        </a>
        <nav class="nav-links">
          <a href="#about">Home</a>
          <a href="#about">About</a>
          <a href="#courses">Courses</a>
          <a href="#results">Results</a>
          <a href="#contact">Contact</a>
        </nav>
        <div class="nav-right">
          <a href="tel:+998952165951" class="nav-phone">
            <span class="phone-icon">📞</span> +998 95 216 59 51
          </a>
          <a href="#contact" class="btn btn-primary">Start Learning Today</a>
        </div>
        <button class="burger" @click="menuOpen = !menuOpen">
          <span></span><span></span><span></span>
        </button>
      </div>
      <div class="mobile-menu" :class="{ open: menuOpen }">
        <a href="#about" @click="menuOpen = false">Home</a>
        <a href="#about" @click="menuOpen = false">About</a>
        <a href="#courses" @click="menuOpen = false">Courses</a>
        <a href="#results" @click="menuOpen = false">Results</a>
        <a href="#contact" @click="menuOpen = false">Contact</a>
        <a href="#contact" class="btn btn-primary" @click="menuOpen = false"
          >Start Learning Today</a
        >
      </div>
    </header>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-bg-circle c1"></div>
      <div class="hero-bg-circle c2"></div>
      <div class="container hero-inner">
        <div class="hero-content">
          <span class="badge">🏆 #1 Choice in Shofirkon</span>
          <h1 class="hero-title">
            Achieve Your<br />
            <span class="highlight">IELTS Goals</span><br />
            with <span class="brand-name">Best Way</span>
          </h1>
          <p class="hero-sub">
            Quality teaching, proven results — tailored programs for students in
            Shofirkon and Bukhara region. Join over 1,200 successful graduates
            today.
          </p>
          <div class="hero-actions">
            <a href="#contact" class="btn btn-primary btn-lg">
              Start Learning Today <span class="arrow">→</span>
            </a>
          </div>
          <div class="hero-social-proof">
            <div class="avatars">
              <img
                v-for="i in 4"
                :key="i"
                :src="`https://i.pravatar.cc/40?img=${i + 10}`"
                :alt="`Student ${i}`"
              />
            </div>
            <span><strong>500+</strong> students enrolled this semester</span>
          </div>
        </div>
        <div class="hero-visual">
          <div class="hero-img-wrap">
            <div class="hero-img-placeholder">
              <div class="img-overlay-card">
                <div class="enrollment-dot"></div>
                <div>
                  <p class="enroll-label">ENROLLMENT OPEN</p>
                  <p class="enroll-text">Next IELTS Intensive Starts Sept 15</p>
                </div>
                <button class="btn btn-sm btn-white">Join Now</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- FOUNDER'S MISSION -->
    <section class="mission" id="about">
      <div class="container mission-inner">
        <div class="mission-visual">
          <div class="years-badge">
            <span class="years-num">10+</span>
            <span class="years-label">Years<br />Education Experience</span>
          </div>
          <div class="mission-deco"></div>
        </div>
        <div class="mission-content">
          <h2 class="section-title">Founder's Mission</h2>
          <blockquote>
            "Founded by Aziz Akhtamov — dedicated to student success and
            community growth in Shofirkon."
          </blockquote>
          <p>
            At Best Way, we believe that quality education shouldn't be a
            privilege. Our mission is to provide world-class language and
            academic training right here in the heart of Bukhara region. We
            combine modern teaching methodologies with a deep understanding of
            local needs.
          </p>
          <div class="mission-stats">
            <div class="stat-item">
              <span class="stat-num green">95%</span>
              <span class="stat-label">Satisfaction Rate</span>
            </div>
            <div class="stat-item">
              <span class="stat-num green">24/7</span>
              <span class="stat-label">Student Support</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- PROVEN EXCELLENCE -->
    <section class="excellence" id="results">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title center">Proven Excellence</h2>
          <p class="section-sub center">
            Our students consistently outperform national averages. Here is what
            dedication looks like in numbers.
          </p>
        </div>
        <div class="excellence-grid">
          <div
            v-for="stat in excellenceStats"
            :key="stat.label"
            class="excellence-card"
          >
            <span class="exc-num" :class="stat.color">{{ stat.value }}</span>
            <span class="exc-label">{{ stat.label }}</span>
          </div>
        </div>
      </div>
    </section>

    <!-- COURSES -->
    <section class="courses" id="courses">
      <div class="container">
        <div class="section-header courses-header">
          <div>
            <h2 class="section-title">Expertly Crafted Courses</h2>
            <p class="section-sub">
              Whether you're aiming for a high IELTS score or mastering core
              science subjects, we have the right program for your future.
            </p>
          </div>
          <a href="#contact" class="btn btn-outline">View All Programs</a>
        </div>
        <div class="courses-grid">
          <div
            v-for="(course, i) in courses"
            :key="i"
            class="course-card"
            :class="{ featured: i === 0 }"
          >
            <div class="course-icon">{{ course.icon }}</div>
            <h3>{{ course.title }}</h3>
            <p>{{ course.desc }}</p>
            <ul class="course-features">
              <li v-for="f in course.features" :key="f">
                <span class="check">✓</span> {{ f }}
              </li>
            </ul>
            <a href="#contact" class="learn-more">Learn more →</a>
          </div>
        </div>
      </div>
    </section>

    <!-- WHY BEST WAY -->
    <section class="why-us">
      <div class="container">
        <div class="section-header">
          <p class="eyebrow">Why Best Way?</p>
          <h2 class="section-title center">Your Success is Our Priority</h2>
        </div>
        <div class="why-grid">
          <div v-for="item in whyItems" :key="item.title" class="why-card">
            <div class="why-icon">{{ item.icon }}</div>
            <h4>{{ item.title }}</h4>
            <p>{{ item.desc }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- TESTIMONIALS -->
    <section class="testimonials">
      <div class="container">
        <div class="section-header">
          <h2 class="section-title center">What Our Students Say</h2>
          <p class="section-sub center">
            Stories of success from the Shofirkon community.
          </p>
        </div>
        <div class="testimonials-grid">
          <div v-for="t in testimonials" :key="t.name" class="testi-card">
            <div class="quote-mark">"</div>
            <p class="testi-text">{{ t.text }}</p>
            <div class="testi-author">
              <img :src="t.avatar" :alt="t.name" />
              <div>
                <strong>{{ t.name }}</strong>
                <span>{{ t.role }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA BANNER -->
    <section class="cta-banner" id="contact">
      <div class="container cta-inner">
        <h2>Ready to Change Your Future?</h2>
        <p>
          Join the next intake and start your journey towards excellence. Book a
          free consultation and level assessment today.
        </p>
        <div class="cta-actions">
          <a href="tel:+998901234567" class="btn btn-white btn-lg"
            >Join Best Way Today</a
          >
          <a href="tel:+998901234567" class="btn btn-outline-white btn-lg"
            >Call Now</a
          >
        </div>
        <p class="cta-disclaimer">
          No hidden fees • Free placement test • Money-back guarantee
        </p>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
      <div class="container footer-inner">
        <div class="footer-brand">
          <a href="#" class="logo">
            <span class="logo-icon">✦</span>
            <span class="logo-text">Best <span>Way</span></span>
          </a>
          <p>
            Empowering the next generation of students in Bukhara region with
            world-class education and local heart.
          </p>
          <div class="socials">
            <a href="#">📘</a>
            <a href="#">📸</a>
            <a href="#">✈️</a>
          </div>
        </div>
        <div class="footer-col">
          <h5>Quick Links</h5>
          <a href="#about">Home</a>
          <a href="#about">About</a>
          <a href="#about">Our Founder</a>
          <a href="#courses">IELTS Course</a>
          <a href="#results">Student Results</a>
        </div>
        <div class="footer-col">
          <h5>Support</h5>
          <a href="#contact">Contact Us</a>
          <a href="#">FAQs</a>
          <a href="#">Privacy Policy</a>
          <a href="#">LG Live</a>
        </div>
        <div class="footer-col">
          <h5>Visit Us</h5>
          <p class="footer-address">
            📍 Naved St 12, Shofirkon district, Bukhara region, Uzbekistan
          </p>
          <a href="tel:+998901234567">📞 +998 95 216 59 51</a>
          <a href="mailto:info@bestway.uz">✉ info@bestway.uz</a>
        </div>
      </div>
      <div class="footer-bottom">
        <p>© 2026 Best Way Learning Center. All rights reserved.</p>
        <div>
          <a href="#">Terms of Service</a>
          <a href="#">Accessibility</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const isScrolled = ref(false);
const menuOpen = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 60;
};

onMounted(() => window.addEventListener("scroll", handleScroll));
onUnmounted(() => window.removeEventListener("scroll", handleScroll));

const excellenceStats = [
  { value: "8.5", label: "Top Achievers", color: "ring-green" },
  { value: "7.5", label: "Average Band", color: "ring-green" },
  { value: "85%", label: "IELTS Success", color: "" },
  { value: "1.2k+", label: "Alumni", color: "" },
  { value: "4.9/5", label: "Rating", color: "" },
];

const courses = [
  {
    icon: "🎯",
    title: "IELTS Preparation",
    desc: "Our signature program designed to boost your score to Band 7.0 and above with intensive practice and strategy sessions.",
    features: [
      "Mock exams weekly",
      "Writing feedback",
      "Small groups (max 8)",
      "Study materials included",
    ],
  },
  {
    icon: "📐",
    title: "Mathematics Prep",
    desc: "Master algebra, geometry, and calculus for national entrance exams and international standardized tests.",
    features: [
      "Exam techniques",
      "Problem-solving focus",
      "Past papers analysis",
      "Personal mentorship",
    ],
  },
  {
    icon: "🔬",
    title: "Natural Sciences",
    desc: "Comprehensive tutoring for Physics and Chemistry tailored to high school curriculum and university prep.",
    features: [
      "Lab experiments",
      "Conceptual clarity",
      "Physics Olympics prep",
      "Chemistry essentials",
    ],
  },
];

const whyItems = [
  {
    icon: "⭐",
    title: "Expert Teachers",
    desc: "IELTS 8.5+ certified instructors with years of experience.",
  },
  {
    icon: "👥",
    title: "Small Groups",
    desc: "Individual attention guaranteed with maximum 8 students per class.",
  },
  {
    icon: "🤝",
    title: "Friendly Vibes",
    desc: "A supportive community that makes learning enjoyable.",
  },
  {
    icon: "📈",
    title: "Proven Method",
    desc: "Curriculum focused on results and practical application.",
  },
];

const testimonials = [
  {
    text: "I improved my IELTS from 5.8 to 7.5 in just three months. The writing workshops at Best Way are truly life-changing.",
    name: "Dilnoza Rahimova",
    role: "IELTS Student • Shofirkon",
    avatar: "https://i.pravatar.cc/48?img=47",
  },
  {
    text: "The math classes helped me get accepted into the National University. Aziz Akhtamov and his team are the best educators.",
    name: "Jasurbek Toshmatov",
    role: "Math Prep • Bukhara",
    avatar: "https://i.pravatar.cc/48?img=12",
  },
  {
    text: "Coming from a village, I felt shy at first. But the environment here is so welcoming. Now I speak English confidently!",
    name: "Mahira Sodiqova",
    role: "General English • Shofirkon",
    avatar: "https://i.pravatar.cc/48?img=32",
  },
];
</script>

<style scoped>
/* ===== RESET & BASE ===== */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.landing {
  --green: #16a34a;
  --green-light: #22c55e;
  --green-pale: #f0fdf4;
  --green-mid: #dcfce7;
  --dark: #111827;
  --dark-2: #1f2937;
  --gray: #6b7280;
  --gray-light: #f9fafb;
  --border: #e5e7eb;
  --white: #ffffff;
  --radius: 16px;
  --shadow: 0 4px 24px rgba(0, 0, 0, 0.08);
  --shadow-lg: 0 12px 48px rgba(0, 0, 0, 0.12);
  font-family: "Plus Jakarta Sans", "Nunito", sans-serif;
  color: var(--dark);
  background: var(--white);
  overflow-x: hidden;
}

@import url("https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&family=Fraunces:ital,wght@0,700;1,700&display=swap");

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 24px;
}

/* ===== BUTTONS ===== */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 12px 24px;
  border-radius: 100px;
  font-weight: 700;
  font-size: 0.95rem;
  text-decoration: none;
  cursor: pointer;
  transition: all 0.25s ease;
  border: 2px solid transparent;
  white-space: nowrap;
}
.btn-primary {
  background: var(--green);
  color: var(--white);
  border-color: var(--green);
}
.btn-primary:hover {
  background: #15803d;
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(22, 163, 74, 0.3);
}
.btn-outline {
  background: transparent;
  color: var(--green);
  border-color: var(--green);
}
.btn-outline:hover {
  background: var(--green-pale);
}
.btn-white {
  background: var(--white);
  color: var(--green);
  border-color: var(--white);
}
.btn-white:hover {
  background: #f0fdf4;
  transform: translateY(-2px);
}
.btn-outline-white {
  background: transparent;
  color: var(--white);
  border-color: rgba(255, 255, 255, 0.6);
}
.btn-outline-white:hover {
  background: rgba(255, 255, 255, 0.15);
}
.btn-sm {
  padding: 8px 16px;
  font-size: 0.85rem;
}
.btn-lg {
  padding: 16px 32px;
  font-size: 1rem;
}
.arrow {
  transition: transform 0.2s;
}
.btn:hover .arrow {
  transform: translateX(4px);
}

/* ===== NAVBAR ===== */
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  padding: 16px 0;
  transition: all 0.3s ease;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
}
.navbar.scrolled {
  padding: 10px 0;
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.08);
}
.nav-inner {
  display: flex;
  align-items: center;
  gap: 32px;
}
.logo {
  display: flex;
  align-items: center;
  gap: 8px;
  text-decoration: none;
  font-family: "Fraunces", serif;
  font-size: 1.3rem;
  font-weight: 700;
  color: var(--dark);
  flex-shrink: 0;
}
.logo span {
  color: var(--green);
}
.logo-icon {
  font-size: 1.1rem;
  color: var(--green);
}
.logo-text span {
  color: var(--green);
}
.nav-links {
  display: flex;
  gap: 28px;
  margin-left: 16px;
}
.nav-links a {
  text-decoration: none;
  color: var(--gray);
  font-weight: 600;
  font-size: 0.9rem;
  transition: color 0.2s;
}
.nav-links a:hover {
  color: var(--dark);
}
.nav-right {
  margin-left: auto;
  display: flex;
  align-items: center;
  gap: 16px;
}
.nav-phone {
  text-decoration: none;
  color: var(--dark);
  font-weight: 600;
  font-size: 0.9rem;
  display: flex;
  align-items: center;
  gap: 6px;
}
.burger {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 4px;
  margin-left: auto;
}
.burger span {
  display: block;
  width: 24px;
  height: 2px;
  background: var(--dark);
  border-radius: 2px;
  transition: 0.3s;
}
.mobile-menu {
  display: none;
  flex-direction: column;
  gap: 16px;
  padding: 20px 24px;
  background: white;
  border-top: 1px solid var(--border);
}
.mobile-menu a {
  text-decoration: none;
  color: var(--dark);
  font-weight: 600;
}
.mobile-menu.open {
  display: flex;
}

/* ===== HERO ===== */
.hero {
  padding: 140px 0 80px;
  position: relative;
  overflow: hidden;
  background: linear-gradient(135deg, #fff 60%, var(--green-pale) 100%);
}
.hero-bg-circle {
  position: absolute;
  border-radius: 50%;
  pointer-events: none;
}
.c1 {
  width: 500px;
  height: 500px;
  background: radial-gradient(
    circle,
    rgba(34, 197, 94, 0.12) 0%,
    transparent 70%
  );
  top: -100px;
  right: -100px;
}
.c2 {
  width: 300px;
  height: 300px;
  background: radial-gradient(
    circle,
    rgba(22, 163, 74, 0.08) 0%,
    transparent 70%
  );
  bottom: 0;
  left: -50px;
}
.hero-inner {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}
.badge {
  display: inline-block;
  background: var(--green-mid);
  color: var(--green);
  font-weight: 700;
  font-size: 0.85rem;
  padding: 6px 14px;
  border-radius: 100px;
  margin-bottom: 20px;
}
.hero-title {
  font-family: "Fraunces", serif;
  font-size: clamp(2.2rem, 4vw, 3.2rem);
  line-height: 1.15;
  color: var(--dark);
  margin-bottom: 20px;
}
.highlight {
  color: var(--green);
  position: relative;
}
.highlight::after {
  content: "";
  position: absolute;
  bottom: 4px;
  left: 0;
  right: 0;
  height: 3px;
  background: var(--green-light);
  border-radius: 2px;
  opacity: 0.5;
}
.brand-name {
  color: var(--green);
}
.hero-sub {
  color: var(--gray);
  font-size: 1.05rem;
  line-height: 1.7;
  margin-bottom: 32px;
  max-width: 480px;
}
.hero-actions {
  margin-bottom: 32px;
}
.hero-social-proof {
  display: flex;
  align-items: center;
  gap: 12px;
  color: var(--gray);
  font-size: 0.9rem;
}
.hero-social-proof strong {
  color: var(--dark);
}
.avatars {
  display: flex;
}
.avatars img {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  border: 2px solid white;
  margin-left: -8px;
  object-fit: cover;
}
.avatars img:first-child {
  margin-left: 0;
}
.hero-visual {
  display: flex;
  justify-content: center;
}
.hero-img-wrap {
  position: relative;
  width: 100%;
  max-width: 480px;
}
.hero-img-placeholder {
  width: 100%;
  aspect-ratio: 4/3;
  border-radius: 24px;
  background: linear-gradient(135deg, #d1fae5 0%, #a7f3d0 50%, #6ee7b7 100%);
  position: relative;
  overflow: hidden;
  box-shadow: var(--shadow-lg);
}
.hero-img-placeholder::before {
  content: "📚";
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -60%);
  font-size: 5rem;
  opacity: 0.3;
}
.img-overlay-card {
  position: absolute;
  bottom: 20px;
  left: 16px;
  right: 16px;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(8px);
  border-radius: 14px;
  padding: 14px 16px;
  display: flex;
  align-items: center;
  gap: 12px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}
.enrollment-dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: var(--green-light);
  flex-shrink: 0;
  animation: pulse 2s infinite;
}
@keyframes pulse {
  0%,
  100% {
    opacity: 1;
    transform: scale(1);
  }
  50% {
    opacity: 0.6;
    transform: scale(1.3);
  }
}
.enroll-label {
  font-size: 0.7rem;
  font-weight: 700;
  color: var(--green);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
.enroll-text {
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--dark);
}
.img-overlay-card .btn-white {
  background: var(--green);
  color: white;
  border-color: var(--green);
  margin-left: auto;
  flex-shrink: 0;
}

/* ===== MISSION ===== */
.mission {
  padding: 100px 0;
  background: var(--gray-light);
}
.mission-inner {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 80px;
  align-items: center;
}
.mission-visual {
  position: relative;
  display: flex;
  justify-content: center;
}
.years-badge {
  background: var(--green);
  color: white;
  border-radius: 20px;
  padding: 32px 40px;
  text-align: center;
  box-shadow: 0 16px 40px rgba(22, 163, 74, 0.3);
  position: relative;
  z-index: 1;
}
.years-num {
  display: block;
  font-family: "Fraunces", serif;
  font-size: 3.5rem;
  font-weight: 700;
  line-height: 1;
}
.years-label {
  font-size: 0.85rem;
  font-weight: 600;
  opacity: 0.9;
  text-transform: uppercase;
  letter-spacing: 0.5px;
  margin-top: 6px;
  display: block;
}
.mission-deco {
  position: absolute;
  width: 120px;
  height: 120px;
  border: 3px solid var(--green-mid);
  border-radius: 20px;
  bottom: -20px;
  right: -20px;
}
.mission-content .section-title {
  margin-bottom: 20px;
}
blockquote {
  font-family: "Fraunces", serif;
  font-style: italic;
  font-size: 1.15rem;
  color: var(--green);
  border-left: 4px solid var(--green);
  padding-left: 20px;
  margin: 20px 0 20px;
  line-height: 1.6;
}
.mission-content p {
  color: var(--gray);
  line-height: 1.8;
  margin-bottom: 32px;
}
.mission-stats {
  display: flex;
  gap: 40px;
}
.stat-item {
  display: flex;
  flex-direction: column;
  gap: 4px;
}
.stat-num {
  font-family: "Fraunces", serif;
  font-size: 2.2rem;
  font-weight: 700;
  color: var(--dark);
}
.stat-num.green {
  color: var(--green);
}
.stat-label {
  font-size: 0.85rem;
  color: var(--gray);
  font-weight: 600;
}

/* ===== EXCELLENCE ===== */
.excellence {
  padding: 100px 0;
  background: var(--white);
}
.section-header {
  margin-bottom: 56px;
}
.section-title {
  font-family: "Fraunces", serif;
  font-size: clamp(1.8rem, 3vw, 2.4rem);
  color: var(--dark);
  margin-bottom: 12px;
  line-height: 1.2;
}
.section-title.center {
  text-align: center;
}
.section-sub {
  color: var(--gray);
  font-size: 1rem;
  line-height: 1.7;
  max-width: 560px;
}
.section-sub.center {
  text-align: center;
  margin: 0 auto;
}
.eyebrow {
  text-align: center;
  color: var(--green);
  font-weight: 700;
  font-size: 0.85rem;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 8px;
}
.excellence-grid {
  display: flex;
  justify-content: center;
  gap: 24px;
  flex-wrap: wrap;
}
.excellence-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  background: var(--white);
  border: 2px solid var(--border);
  border-radius: 20px;
  padding: 36px 32px;
  min-width: 160px;
  text-align: center;
  transition: all 0.3s;
}
.excellence-card:hover {
  border-color: var(--green);
  box-shadow: 0 8px 32px rgba(22, 163, 74, 0.15);
  transform: translateY(-4px);
}
.exc-num {
  font-family: "Fraunces", serif;
  font-size: 2.4rem;
  font-weight: 700;
  color: var(--dark);
}
.exc-num.ring-green {
  color: var(--green);
}
.exc-label {
  font-size: 0.85rem;
  color: var(--gray);
  font-weight: 600;
}

/* ===== COURSES ===== */
.courses {
  padding: 100px 0;
  background: var(--gray-light);
}
.courses-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  margin-bottom: 48px;
}
.courses-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
.course-card {
  background: var(--white);
  border-radius: var(--radius);
  padding: 32px;
  border: 2px solid var(--border);
  transition: all 0.3s;
  display: flex;
  flex-direction: column;
  gap: 12px;
}
.course-card:hover {
  border-color: var(--green);
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
}
.course-card.featured {
  background: var(--green);
  color: white;
  border-color: var(--green);
}
.course-card.featured h3,
.course-card.featured p {
  color: rgba(255, 255, 255, 0.95);
}
.course-card.featured .course-features li {
  color: rgba(255, 255, 255, 0.85);
}
.course-card.featured .check {
  color: rgba(255, 255, 255, 0.9);
}
.course-card.featured .learn-more {
  color: white;
  border-color: rgba(255, 255, 255, 0.4);
}
.course-icon {
  font-size: 2rem;
}
.course-card h3 {
  font-family: "Fraunces", serif;
  font-size: 1.2rem;
  color: var(--dark);
}
.course-card p {
  color: var(--gray);
  font-size: 0.9rem;
  line-height: 1.6;
}
.course-features {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin-top: 4px;
}
.course-features li {
  font-size: 0.88rem;
  color: var(--gray);
  display: flex;
  align-items: center;
  gap: 8px;
}
.check {
  color: var(--green);
  font-weight: 700;
}
.learn-more {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  color: var(--green);
  font-weight: 700;
  font-size: 0.9rem;
  text-decoration: none;
  margin-top: auto;
  padding-top: 12px;
  border-top: 1px solid var(--border);
  transition: gap 0.2s;
}
.learn-more:hover {
  gap: 10px;
}

/* ===== WHY US ===== */
.why-us {
  padding: 100px 0;
  background: var(--white);
}
.why-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
}
.why-card {
  text-align: center;
  padding: 36px 24px;
  border-radius: var(--radius);
  background: var(--gray-light);
  transition: all 0.3s;
}
.why-card:hover {
  background: var(--green-pale);
  transform: translateY(-4px);
}
.why-icon {
  font-size: 2.2rem;
  margin-bottom: 16px;
}
.why-card h4 {
  font-size: 1rem;
  font-weight: 700;
  color: var(--dark);
  margin-bottom: 8px;
}
.why-card p {
  font-size: 0.88rem;
  color: var(--gray);
  line-height: 1.6;
}

/* ===== TESTIMONIALS ===== */
.testimonials {
  padding: 100px 0;
  background: var(--gray-light);
}
.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 24px;
}
.testi-card {
  background: var(--white);
  border-radius: var(--radius);
  padding: 32px;
  position: relative;
  border: 1px solid var(--border);
  transition: all 0.3s;
}
.testi-card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-4px);
}
.quote-mark {
  font-family: "Fraunces", serif;
  font-size: 5rem;
  color: var(--green-mid);
  line-height: 0.8;
  margin-bottom: 12px;
}
.testi-text {
  color: var(--dark-2);
  line-height: 1.7;
  font-size: 0.95rem;
  margin-bottom: 24px;
}
.testi-author {
  display: flex;
  align-items: center;
  gap: 12px;
}
.testi-author img {
  width: 44px;
  height: 44px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid var(--green-mid);
}
.testi-author strong {
  display: block;
  font-weight: 700;
  font-size: 0.9rem;
  color: var(--dark);
}
.testi-author span {
  font-size: 0.8rem;
  color: var(--gray);
}

/* ===== CTA BANNER ===== */
.cta-banner {
  background: linear-gradient(135deg, var(--green) 0%, #15803d 100%);
  padding: 100px 0;
  position: relative;
  overflow: hidden;
}
.cta-banner::before {
  content: "";
  position: absolute;
  top: -100px;
  right: -100px;
  width: 400px;
  height: 400px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.06);
}
.cta-inner {
  text-align: center;
  position: relative;
  z-index: 1;
}
.cta-inner h2 {
  font-family: "Fraunces", serif;
  font-size: clamp(2rem, 4vw, 3rem);
  color: white;
  margin-bottom: 16px;
}
.cta-inner p {
  color: rgba(255, 255, 255, 0.85);
  font-size: 1.05rem;
  line-height: 1.6;
  max-width: 540px;
  margin: 0 auto 36px;
}
.cta-actions {
  display: flex;
  justify-content: center;
  gap: 16px;
  flex-wrap: wrap;
  margin-bottom: 20px;
}
.cta-disclaimer {
  color: rgba(255, 255, 255, 0.6);
  font-size: 0.85rem;
  margin: 0 auto;
}

/* ===== FOOTER ===== */
.footer {
  background: var(--dark);
  padding: 64px 0 0;
  color: rgba(255, 255, 255, 0.7);
}
.footer-inner {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1.5fr;
  gap: 48px;
  padding-bottom: 48px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}
.footer-brand .logo {
  color: white;
  margin-bottom: 16px;
  display: flex;
}
.footer-brand .logo-text span {
  color: var(--green-light);
}
.footer-brand p {
  font-size: 0.9rem;
  line-height: 1.7;
  margin-bottom: 20px;
}
.socials {
  display: flex;
  gap: 12px;
}
.socials a {
  font-size: 1.3rem;
  text-decoration: none;
  transition: transform 0.2s;
}
.socials a:hover {
  transform: scale(1.2);
}
.footer-col h5 {
  color: white;
  font-weight: 700;
  margin-bottom: 16px;
  font-size: 0.95rem;
}
.footer-col a,
.footer-col p {
  display: block;
  text-decoration: none;
  color: rgba(255, 255, 255, 0.6);
  font-size: 0.88rem;
  margin-bottom: 10px;
  transition: color 0.2s;
  line-height: 1.5;
}
.footer-col a:hover {
  color: var(--green-light);
}
.footer-address {
  font-size: 0.88rem !important;
  line-height: 1.5 !important;
}
.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 24px;
  max-width: 1200px;
  margin: 0 auto;
  font-size: 0.85rem;
  color: rgba(255, 255, 255, 0.4);
}
.footer-bottom div {
  display: flex;
  gap: 24px;
}
.footer-bottom a {
  color: rgba(255, 255, 255, 0.4);
  text-decoration: none;
  transition: color 0.2s;
}
.footer-bottom a:hover {
  color: rgba(255, 255, 255, 0.8);
}

/* ===== RESPONSIVE ===== */
@media (max-width: 1024px) {
  .nav-links,
  .nav-phone {
    display: none;
  }
  .burger {
    display: flex;
  }
  .nav-right .btn {
    display: none;
  }
  .why-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .footer-inner {
    grid-template-columns: 1fr 1fr;
    gap: 32px;
  }
}

@media (max-width: 768px) {
  .hero {
    padding: 100px 0 60px;
  }
  .hero-inner {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  .hero-visual {
    order: -1;
  }
  .mission-inner {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  .courses-grid {
    grid-template-columns: 1fr;
  }
  .testimonials-grid {
    grid-template-columns: 1fr;
  }
  .courses-header {
    flex-direction: column;
    align-items: flex-start;
    gap: 16px;
  }
  .why-grid {
    grid-template-columns: 1fr 1fr;
  }
  .footer-inner {
    grid-template-columns: 1fr;
  }
  .footer-bottom {
    flex-direction: column;
    gap: 12px;
    text-align: center;
  }
  .excellence-grid {
    gap: 12px;
  }
  .excellence-card {
    min-width: 120px;
    padding: 24px 20px;
  }
}

@media (max-width: 480px) {
  .why-grid {
    grid-template-columns: 1fr;
  }
  .mission-stats {
    gap: 24px;
  }
  .cta-actions {
    flex-direction: column;
    align-items: center;
  }
}
</style>
