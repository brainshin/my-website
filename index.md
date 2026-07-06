---
---

<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Brainshin Study Notes</title>
  <meta name="description" content="GitHub, Vibe, Codex, Cloud 공부 내용을 정리하는 개인 기술 노트입니다.">
  <style>
    :root {
      color-scheme: light;
      --bg: #f6f4ee;
      --surface: #ffffff;
      --surface-soft: #ebe7dd;
      --text: #1f2328;
      --muted: #626b74;
      --line: #d9d4c8;
      --blue: #2563eb;
      --green: #15803d;
      --orange: #c2410c;
      --ink: #111827;
      --shadow: 0 18px 45px rgba(31, 35, 40, 0.08);
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      background: var(--bg);
      color: var(--text);
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .site-header {
      position: sticky;
      top: 0;
      z-index: 10;
      border-bottom: 1px solid rgba(217, 212, 200, 0.82);
      background: rgba(246, 244, 238, 0.9);
      backdrop-filter: blur(16px);
    }

    .nav {
      width: min(1120px, calc(100% - 40px));
      min-height: 68px;
      margin: 0 auto;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      min-width: 0;
      font-weight: 800;
      letter-spacing: 0;
    }

    .brand-mark {
      width: 38px;
      height: 38px;
      border: 1px solid var(--line);
      border-radius: 8px;
      object-fit: cover;
      background: var(--surface);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 6px;
      color: var(--muted);
      font-size: 14px;
      font-weight: 650;
    }

    .nav-links a {
      padding: 8px 10px;
      border-radius: 7px;
    }

    .nav-links a:hover {
      background: var(--surface-soft);
      color: var(--text);
    }

    main {
      width: min(1120px, calc(100% - 40px));
      margin: 0 auto;
    }

    .container {
      width: min(1120px, calc(100% - 40px));
      margin: 0 auto;
    }

    .hero {
      min-height: calc(100vh - 150px);
      padding: 86px 0 48px;
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(300px, 0.9fr);
      align-items: center;
      gap: 52px;
    }

    .eyebrow {
      width: fit-content;
      margin: 0 0 18px;
      padding: 6px 10px;
      border: 1px solid var(--line);
      border-radius: 999px;
      background: var(--surface);
      color: var(--muted);
      font-size: 13px;
      font-weight: 750;
    }

    h1 {
      max-width: 760px;
      margin: 0;
      color: var(--ink);
      font-size: clamp(46px, 8vw, 88px);
      line-height: 0.96;
      letter-spacing: 0;
    }

    .hero-copy {
      max-width: 660px;
      margin: 24px 0 0;
      color: var(--muted);
      font-size: 18px;
    }

    .hero-actions {
      margin-top: 34px;
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .button {
      min-height: 46px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 0 16px;
      border: 1px solid var(--line);
      border-radius: 8px;
      background: var(--surface);
      color: var(--text);
      font-weight: 780;
      box-shadow: 0 10px 24px rgba(31, 35, 40, 0.06);
    }

    .button.primary {
      border-color: var(--ink);
      background: var(--ink);
      color: #ffffff;
    }

    .hero-panel {
      border: 1px solid var(--line);
      border-radius: 8px;
      background: var(--surface);
      box-shadow: var(--shadow);
      overflow: hidden;
    }

    .panel-top {
      padding: 18px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 14px;
      border-bottom: 1px solid var(--line);
    }

    .panel-title {
      margin: 0;
      font-size: 15px;
      font-weight: 850;
    }

    .status {
      padding: 5px 8px;
      border-radius: 999px;
      background: #dcfce7;
      color: #166534;
      font-size: 12px;
      font-weight: 800;
      white-space: nowrap;
    }

    .note-list {
      margin: 0;
      padding: 8px;
      list-style: none;
    }

    .note-list li {
      display: grid;
      grid-template-columns: 42px minmax(0, 1fr);
      gap: 12px;
      padding: 14px 10px;
      border-radius: 7px;
    }

    .note-list li + li {
      border-top: 1px solid #ede9df;
    }

    .note-icon {
      width: 42px;
      height: 42px;
      display: grid;
      place-items: center;
      border-radius: 8px;
      color: #ffffff;
      font-size: 13px;
      font-weight: 900;
    }

    .note-icon.blue {
      background: var(--blue);
    }

    .note-icon.green {
      background: var(--green);
    }

    .note-icon.orange {
      background: var(--orange);
    }

    .note-title {
      margin: 0;
      color: var(--ink);
      font-weight: 820;
    }

    .note-desc {
      margin: 2px 0 0;
      color: var(--muted);
      font-size: 14px;
    }

    .section {
      padding: 42px 0 74px;
    }

    .section-heading {
      display: flex;
      align-items: end;
      justify-content: space-between;
      gap: 20px;
      margin-bottom: 20px;
    }

    h2 {
      margin: 0;
      color: var(--ink);
      font-size: 28px;
      line-height: 1.2;
      letter-spacing: 0;
    }

    .section-heading p {
      max-width: 460px;
      margin: 0;
      color: var(--muted);
      font-size: 15px;
    }

    .category-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 16px;
    }

    .category-card {
      min-height: 210px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      border: 1px solid var(--line);
      border-radius: 8px;
      background: var(--surface);
      box-shadow: 0 12px 30px rgba(31, 35, 40, 0.05);
      transition: transform 160ms ease, box-shadow 160ms ease;
    }

    .category-card:hover {
      transform: translateY(-3px);
      box-shadow: var(--shadow);
    }

    .category-meta {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
    }

    .category-code {
      width: 44px;
      height: 44px;
      display: grid;
      place-items: center;
      border-radius: 8px;
      background: var(--surface-soft);
      color: var(--ink);
      font-size: 13px;
      font-weight: 900;
    }

    .category-count {
      color: var(--muted);
      font-size: 13px;
      font-weight: 760;
    }

    .category-card h3 {
      margin: 24px 0 8px;
      color: var(--ink);
      font-size: 22px;
      letter-spacing: 0;
    }

    .category-card p {
      margin: 0;
      color: var(--muted);
      font-size: 15px;
    }

    .category-link {
      margin-top: 22px;
      color: var(--ink);
      font-size: 14px;
      font-weight: 850;
    }

    .footer {
      border-top: 1px solid var(--line);
      padding: 24px 0 34px;
      color: var(--muted);
      font-size: 14px;
    }

    @media (max-width: 820px) {
      .nav {
        width: min(100% - 28px, 1120px);
      }

      .nav-links {
        display: none;
      }

      main {
        width: min(100% - 28px, 1120px);
      }

      .hero {
        min-height: auto;
        padding: 54px 0 28px;
        grid-template-columns: 1fr;
        gap: 30px;
      }

      h1 {
        font-size: 48px;
      }

      .hero-copy {
        font-size: 16px;
      }

      .section-heading {
        align-items: start;
        flex-direction: column;
      }

      .category-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
  <header class="site-header">
    <nav class="nav" aria-label="메인 메뉴">
      <a class="brand" href="./">
        <img class="brand-mark" src="https://github.com/brainshin.png" alt="Brainshin profile image">
        <span>Brainshin Notes</span>
      </a>
      <div class="nav-links">
        <a href="#categories">Categories</a>
        <a href="https://github.com/brainshin">GitHub</a>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero">
      <div>
        <p class="eyebrow">Personal Study Archive</p>
        <h1>공부한 내용을 오래 남기는 기술 노트</h1>
        <p class="hero-copy">
          GitHub, Vibe, Codex, Cloud 실습 내용을 주제별로 정리합니다.
          명령어, 설정 파일, 실수했던 에러와 해결 과정을 다시 찾기 쉽게 모아둡니다.
        </p>
        <div class="hero-actions">
          <a class="button primary" href="#categories">카테고리 보기</a>
          <a class="button" href="https://github.com/brainshin/my-website">저장소 보기</a>
        </div>
      </div>

      <aside class="hero-panel" aria-label="최근 정리 예정 항목">
        <div class="panel-top">
          <p class="panel-title">Next Notes</p>
          <span class="status">Draft</span>
        </div>
        <ul class="note-list">
          <li>
            <span class="note-icon blue">GH</span>
            <div>
              <p class="note-title">GitHub Pages 배포 흐름</p>
              <p class="note-desc">저장소, 브랜치, Pages 설정을 한 번에 정리</p>
            </div>
          </li>
          <li>
            <span class="note-icon green">VX</span>
            <div>
              <p class="note-title">Vibe 작업 기록</p>
              <p class="note-desc">아이디어를 코드로 옮길 때 사용한 패턴 정리</p>
            </div>
          </li>
          <li>
            <span class="note-icon orange">CX</span>
            <div>
              <p class="note-title">Codex 협업 가이드</p>
              <p class="note-desc">수정 요청, 검증, Git 반영 흐름 정리</p>
            </div>
          </li>
        </ul>
      </aside>
    </section>

    <section class="section" id="categories">
      <div class="section-heading">
        <h2>Categories</h2>
        <p>처음에는 큰 주제 단위로 시작하고, 글이 쌓이면 세부 카테고리로 나눕니다.</p>
      </div>

      <div class="category-grid">
        <a class="category-card" href="#github-guide">
          <div>
            <div class="category-meta">
              <span class="category-code">GH</span>
              <span class="category-count">Git & Pages</span>
            </div>
            <h3>GitHub 가이드</h3>
            <p>Git 기본 명령어, 브랜치 전략, GitHub Pages 배포 과정을 정리합니다.</p>
          </div>
          <span class="category-link">정리 예정</span>
        </a>

        <a class="category-card" href="#vibe-guide">
          <div>
            <div class="category-meta">
              <span class="category-code">VX</span>
              <span class="category-count">Workflow</span>
            </div>
            <h3>바이브 가이드</h3>
            <p>아이디어를 빠르게 만들고 다듬는 작업 방식과 프롬프트 흐름을 기록합니다.</p>
          </div>
          <span class="category-link">정리 예정</span>
        </a>

        <a class="category-card" href="#codex-guide">
          <div>
            <div class="category-meta">
              <span class="category-code">CX</span>
              <span class="category-count">AI Coding</span>
            </div>
            <h3>Codex 가이드</h3>
            <p>코드 수정 요청, 에러 분석, Terraform 검증처럼 반복되는 협업 패턴을 정리합니다.</p>
          </div>
          <span class="category-link">정리 예정</span>
        </a>

        <a class="category-card" href="#cloud-guide">
          <div>
            <div class="category-meta">
              <span class="category-code">AWS</span>
              <span class="category-count">Cloud</span>
            </div>
            <h3>AWS 가이드</h3>
            <p>계정 전환, IAM, S3, EC2, 네트워크 구성에서 배운 내용을 모읍니다.</p>
          </div>
          <span class="category-link">정리 예정</span>
        </a>

        <a class="category-card" href="#terraform-guide">
          <div>
            <div class="category-meta">
              <span class="category-code">TF</span>
              <span class="category-count">IaC</span>
            </div>
            <h3>Terraform 가이드</h3>
            <p>변수, remote state, module, plan 에러 해결 과정을 예제로 남깁니다.</p>
          </div>
          <span class="category-link">정리 예정</span>
        </a>

        <a class="category-card" href="#error-notes">
          <div>
            <div class="category-meta">
              <span class="category-code">ERR</span>
              <span class="category-count">Troubleshooting</span>
            </div>
            <h3>에러 노트</h3>
            <p>실습 중 만난 에러 메시지와 실제로 해결한 명령어를 짧게 정리합니다.</p>
          </div>
          <span class="category-link">정리 예정</span>
        </a>
      </div>
    </section>
  </main>

  <footer class="footer">
    <div class="container">© 2026 Brainshin. Built with GitHub Pages.</div>
  </footer>
</body>
</html>
