<template>
  <div class="about-container">
    <!-- HEADER AREA -->
    <div class="header">
      <img class="profile-img" src="profile.png" alt="profile" />
      <h1>황현지</h1>
      <p class="subtitle">Backend Engineer</p>
      <p class="description">좋아하는 것을 구조화하고, 흐름이 자연스러운 서비스를 지향합니다.</p>

      <!-- NAV TOGGLE -->
      <nav class="nav-tabs">
        <button @click="scrollToSection('profile')">Profile</button>
        <button @click="scrollToSection('career')">Career</button>
        <button @click="scrollToSection('project')">Project</button>
        <button @click="scrollToSection('contact')">Contact</button>
      </nav>
    </div>

    <!-- SECTIONS -->
    <div ref="profile" class="section-card">
      <h2>Profile</h2>
      <p>
        좋아하는 것을 구조화하고 흐름이 자연스럽게 이어지는 서비스를 지향하는 백엔드 개발자
        황현지입니다.
      </p>
      <p>
        제조 · MES · ERP 환경에서 3년간 근무하며, 현장 업무 프로세스와 데이터 흐름을 이해하고 이를
        시스템 구조로 옮기는 일을 경험했습니다. 단순 기능 구현보다는 ‘왜 필요한가’와 ‘어떻게
        이어져야 자연스러운가’를 고민하는 편입니다.
      </p>
      <p>
        협업은 역할을 나누는 일이 아니라, 같은 문제의 맥락을 공유하는 과정이라고 생각합니다. 그래서
        요구사항 논의부터 설계 → 개발 → 검토까지의 흐름을 명확하게 유지하려 노력합니다. 서로가 같은
        장면을 보고 있다고 느껴질 때 협업은 유연하고 즐거워진다고 믿습니다.
      </p>
      <p>
        현재는 개인 프로젝트 MusicMap을 통해 취향의 흐름을 태그와 데이터 구조로 표현하는 실험을 하고
        있습니다. 도메인에서 출발해 사람과 데이터의 관계를 연결하는 서비스에 관심이 많습니다.
      </p>
    </div>

    <div ref="career" class="section-card">
      <h2>Career</h2>
      <p class="info-note">Backend Engineer · 3 years · MES/ERP 도메인</p>
      <p>
        제조 · MES · ERP 환경에서 3년간 Backend Engineer로 근무하며, 현장 운영 프로세스와 데이터
        흐름을 이해하고 이를 시스템 구조로 옮기는 경험을 쌓았습니다.
      </p>
      <ul>
        <li>PLC 및 생산/재고 데이터 흐름 분석 기반 MES 기능 구현 및 모니터링 화면 개발</li>
        <li>기존 PHP/Delphi 시스템의 Kotlin · Vue 기반 재구축 및 구조 개선</li>
        <li>LOT/BOM 기반 재고 관리, 바코드 출고/출하, 실적 가시화 기능 설계 및 구현</li>
        <li>DB 구조 재정립 및 QueryDSL 도입을 통한 조회 성능 최적화 (3분 → 2초 단축)</li>
      </ul>
      <p>
        단순 기능 개발이 아니라, 현장에서 발생하는 요구의 맥락을 이해하고 설계 → 개발 → 검토까지의
        흐름을 명확하게 유지하는 협업 방식을 지향합니다.
      </p>
    </div>

    <div ref="project" class="section-card">
      <h2>MusicMap</h2>

      <p>
        MusicMap은 개인의 음악 취향을 태그 기반으로 구조화하여, 곡을 단순히 ‘재생’하는 것을 넘어
        ‘탐색하고 연결짓는 과정’까지 자연스럽게 이어지도록 설계한 음악 큐레이션 서비스입니다.
      </p>

      <p>
        기존의 플레이리스트 중심 탐색 방식은 큐레이터가 만든 결과물을 소비하는 형태에 가깝습니다.
        하지만 사람들은 음악을 장르보다는
        <strong>감정, 분위기, 질감, 시대성, 악기 표현</strong> 등의 더 미세한 결로 기억하고
        연결짓습니다.
      </p>

      <p>
        MusicMap은 곡에 여러 개의 태그를 중첩해 부여하고, 그 태그들이 곡과 곡 사이의 관계망을
        형성하도록 합니다. 사용자는 이 태그 스펙트럼을 조절하며, 마치 “자신의 생각 흐름을 따라가는
        것처럼” 취향의 지도를 확장해 나갈 수 있습니다.
      </p>

      <ul>
        <li>Track – Tag – Vote 기반의 사용자 참여형 큐레이션 구조</li>
        <li>한 곡을 다양한 관점(감정/질감/편곡/시기 등)에서 분류 가능</li>
        <li>태그 조합으로 취향의 스펙트럼을 점진적으로 좁혀가는 탐색 UI</li>
        <li>자신만의 Music Mind-map을 구축하는 경험 제공</li>
      </ul>

      <p>
        또한 MusicMap은 사용자의 참여 데이터를 빠르고 정확하게 반영하기 위해
        <strong>Redis 기반 실시간 반응 시스템</strong>을 도입했습니다. 트랙/플레이리스트의 좋아요와
        조회수를 Redis에서 관리함으로써, 데이터베이스 부담 없이 즉각적인 응답성과 부드러운
        인터랙션을 제공합니다. 이는 이후 태그 기반 추천 알고리즘을 고도화하기 위한 중요한 기반이
        됩니다.
      </p>

      <p>
        실제 음악 작업자와 플레이리스트 큐레이터와의 대화를 통해 “음악을 듣는 방식은 각자의 세계관을
        반영한다"는 관점에서 출발했습니다. MusicMap은 그 세계관을 자연스럽게 드러내고 확장할 수 있는
        도구를 지향합니다.
      </p>

      <img src="musicmap1.png" alt="MusicMap UI" />
      <img src="musicmap2.png" alt="MusicMap UI" />

      <p class="tech-stack">
        Vue3 + Quasar · Kotlin + Spring Boot · JPA · PostgreSQL · Redis (태그 추천 및 연관도 기반
        탐색 알고리즘 고도화 예정)
      </p>
    </div>

    <div ref="contact" class="section-card">
      <h2>Contact</h2>
      <p class="contact-line">
        <span class="label">Email</span>
        <a href="mailto:hyunji.9513@gmail.com" class="no-link">hyunji.9513@gmail.com</a>
      </p>
      <p class="contact-line">
        <span class="label">GitHub</span>
        <a href="https://github.com/pogeunpogeun" class="no-link" target="_blank"
          >github.com/pogeunpogeun</a
        >
      </p>
      <p class="contact-line">
        <span class="label">Instagram</span>
        <a href="https://instagram.com/pogeunpogeun" class="no-link" target="_blank"
          >@pogeunpogeun</a
        >
      </p>
    </div>
  </div>
  <button v-show="showScrollTop" class="scroll-top" @click="scrollToTop">↑</button>
</template>

<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue';

const profile = ref<HTMLElement | null>(null);
const career = ref<HTMLElement | null>(null);
const project = ref<HTMLElement | null>(null);
const contact = ref<HTMLElement | null>(null);

function scrollToSection(section: keyof typeof sections) {
  const target = sections[section];
  if (!target?.value) return;
  window.scrollTo({
    top: target.value.offsetTop - 80,
    behavior: 'smooth',
  });
}

const sections = { profile, career, project, contact };

const showScrollTop = ref(false);

function handleScroll() {
  showScrollTop.value = window.scrollY > 200;
}

function scrollToTop() {
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
.about-container {
  max-width: 820px;
  margin: 0 auto;
  padding: 40px 24px;
}

.header {
  text-align: center;
  margin-bottom: 32px;
}

.header h1 {
  font-size: 42px;
  font-weight: 600;
  margin: 6px 0;
}

.profile-img {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin-bottom: 16px;
}

.subtitle {
  margin-top: 4px;
  color: #666;
  font-size: 14px;
}

.description {
  margin-top: 12px;
  color: #777;
  font-size: 15px;
}

/* ▼▼ 여기 변경됨 ▼▼ */
.nav-tabs {
  margin-top: 24px;
  display: flex;
  justify-content: center;
  gap: 24px;
  border-bottom: 1px solid #eee; /* 기준 라인 추가 */
  padding-bottom: 8px;
}

.nav-tabs button {
  background: none;
  border: none;
  font-size: 15px;
  cursor: pointer;
  padding-bottom: 4px;

  /* 글씨 힘 실어줌 */
  font-weight: 500;
  color: #444;

  /* hover 시 높이 변화 없도록 border 자리 확보 */
  border-bottom: 2px solid transparent;

  /* 부드러운 전환 */
  transition:
    border-color 0.25s ease,
    color 0.25s ease;
}

.nav-tabs button:hover,
.nav-tabs button.active {
  border-bottom-color: #111;
  color: #000;
}
/* ▲▲ 여기까지 변경 ▲▲ */

.section-card {
  background: white;
  border-radius: 12px;
  padding: 36px;
  margin-bottom: 48px;
  line-height: 1.6;
}

.section-card img {
  max-width: 100%;
  margin-top: 14px;
  border-radius: 8px;
}

.tech-stack {
  margin-top: 16px;
  font-size: 14px;
  color: #666;
}

.contact-line {
  display: flex;
  gap: 12px;
  align-items: center;
  font-size: 15px;
  margin: 6px 0;
}

.label {
  width: 72px;
  color: #666;
}

.no-link {
  color: #444;
  text-decoration: none;
  transition: color 0.2s ease;
}

.no-link:hover {
  color: #000;
}

.scroll-top {
  position: fixed;
  right: 24px;
  bottom: 24px;
  width: 46px;
  height: 46px;
  border-radius: 50%;
  border: none;
  background: #111;
  color: #fff;
  font-size: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  opacity: 0.8;
  transition:
    opacity 0.25s ease,
    transform 0.25s ease;
}

.scroll-top:hover {
  opacity: 1;
  transform: translateY(-3px);
}
</style>
