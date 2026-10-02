# 🚀 Space Adventure — Game Web Design System

> 캐주얼 우주 모험 게임 웹사이트용 디자인 시스템
> 키워드: **Candy Glossy · Cosmic Purple · Chunky & Bouncy · Playful Sci-fi**

---

## 1. 디자인 원칙

| 원칙 | 설명 |
|---|---|
| **Candy Glossy** | 모든 UI는 사탕/젤리처럼 통통하고 광택 있게. 평면(flat) 금지, 하이라이트 + 하단 두께감 필수 |
| **Deep Space Contrast** | 배경은 어둡고 깊은 보라·남색, 그 위에 채도 높은 시안/옐로/마젠타가 튀어나오도록 |
| **Chunky & Round** | 모서리는 크고 둥글게, 선은 두껍게, 폰트는 굵고 동글동글하게 |
| **Always Alive** | 별은 반짝이고, 행성은 둥둥 뜨고, 버튼은 눌리면 튕긴다. 정지된 화면 없음 |
| **Friendly Sci-fi** | 차갑고 기계적인 SF가 아닌, 귀엽고 다정한 우주 |

---

## 2. Color

### 2-1. Background (Space)

| Token | HEX | 용도 |
|---|---|---|
| `--space-900` | `#0E0626` | 가장 깊은 배경, 비네팅 |
| `--space-800` | `#1A0B3D` | 기본 배경 |
| `--space-700` | `#2B1260` | 성운 레이어, 카드 배경 |
| `--space-600` | `#3D1A80` | 성운 하이라이트 |
| `--nebula-500` | `#5B2A9E` | 성운 블롭, 큰 행성 그림자 |

**배경 그라디언트 (기본)**
```css
background:
  radial-gradient(ellipse at 20% 30%, rgba(91,42,158,.55) 0%, transparent 55%),
  radial-gradient(ellipse at 80% 70%, rgba(224,64,251,.25) 0%, transparent 50%),
  linear-gradient(180deg, #1A0B3D 0%, #0E0626 100%);
```

### 2-2. Primary Accent

| Token | Top (Light) | Base | Bottom (Edge) | 용도 |
|---|---|---|---|---|
| **Cosmic Cyan** `--cyan` | `#9BE7FF` | `#3BB4F5` | `#1A6FC4` | 메인 타이틀, 일반 버튼, 로봇 눈 |
| **Star Yellow** `--yellow` | `#FFE680` | `#FFC23D` | `#E07B12` | CTA(START), 코인, 프로그레스 |
| **Nebula Magenta** `--magenta` | `#F79CFF` | `#D94BF0` | `#8A1FB0` | 로고 서브카피, 강조 텍스트, 하이라이트 |
| **Candy Pink** `--pink` | `#FFA3D1` | `#FF4FA3` | `#C2186B` | 하트/HP, 경고(LOW), 뱃지 |
| **Moon White** `--white` | `#FFFFFF` | `#E9E6F7` | `#A9A3C9` | 서브 버튼(일시정지 등), 로봇 바디 |

### 2-3. Semantic

| Token | HEX | 용도 |
|---|---|---|
| `--success` | `#4DE8B0` | 클리어, 획득 |
| `--warning` | `#FFC23D` | 주의 (= Star Yellow) |
| `--danger` | `#FF4F7B` | HP 부족, 실패 |
| `--text-primary` | `#FFFFFF` | 본문 |
| `--text-secondary` | `#C9BFF0` | 보조 텍스트 |
| `--text-on-yellow` | `#C4500A` | 노란 버튼 위 텍스트 (주황 계열) |
| `--text-on-cyan` | `#0F4C9C` | 시안 버튼 위 아이콘/텍스트 |

### 2-4. Planet Palette (일러스트용)

| 행성 | Base | Shade | Detail |
|---|---|---|---|
| Ocean Blue | `#2E5BD9` | `#1B2F8A` | `#5E8BFF` 소용돌이 |
| Mars Red | `#C9573A` | `#7A2A1E` | `#E8855A` 줄무늬 |
| Sun Orange | `#FFB020` | `#E06A00` | `#FFE27A` 크레이터 |
| Ice Cyan | `#4FC3F7` | `#1E7FCF` | `#B3ECFF` 대륙 |
| Moon Gray | `#6E6577` | `#3D3545` | `#958BA0` 균열 |
| Ringed Lilac | `#A8C8F0` | `#6F8FC9` | `#E2EEFF` 링 |
| Gas Pink | `#E0558A` | `#9B2A5C` | `#F59BB8` 띠 |

---

## 3. Typography

### 3-1. Font Family

| 역할 | 영문 | 한글 | 특징 |
|---|---|---|---|
| **Display / Logo** | `Lilita One`, `Luckiest Guy` | `Jua`, `BM 주아` | 아주 굵고 둥근 장식형 |
| **Script Accent** | `Pacifico`, `Kalam` | `Gaegu` | "Adventure" 같은 손글씨 서브카피 |
| **UI / Button** | `Fredoka` (600–700) | `Jua` | 버튼, 라벨, 수치 |
| **Body** | `Nunito` (500–800) | `Pretendard` | 설명, 본문 |

```html
<link href="https://fonts.googleapis.com/css2?family=Lilita+One&family=Fredoka:wght@500;600;700&family=Pacifico&family=Nunito:wght@500;700;800&family=Jua&family=Gaegu:wght@700&display=swap" rel="stylesheet">
```

### 3-2. Type Scale

| Token | Size / Line | Font | 용도 |
|---|---|---|---|
| `display-xl` | 96 / 0.95 | Lilita One | 메인 로고 |
| `display-l` | 64 / 1.0 | Lilita One | 섹션 히어로 |
| `script` | 40 / 1.1 | Pacifico | 로고 서브카피 |
| `h1` | 40 / 1.15 | Fredoka 700 | 페이지 타이틀 |
| `h2` | 28 / 1.2 | Fredoka 700 | 섹션 타이틀 |
| `h3` | 20 / 1.3 | Fredoka 600 | 카드 타이틀 |
| `button` | 20 / 1.0 | Fredoka 700, `letter-spacing: .04em` | 버튼 |
| `body` | 16 / 1.6 | Nunito 600 | 본문 |
| `caption` | 13 / 1.4 | Nunito 700 | 수치, 라벨 |

### 3-3. Logo Text Effect (핵심)

레퍼런스 로고는 **① 그라디언트 채움 → ② 흰/밝은 외곽선 → ③ 진한 보라 외곽선 → ④ 아래로 밀린 입체 그림자** 4겹 구조.

```css
.logo {
  font-family: 'Lilita One', 'Jua', sans-serif;
  font-size: 96px;
  line-height: .95;
  /* ① 그라디언트 채움 */
  background: linear-gradient(180deg, #C8F2FF 0%, #5CC8FF 45%, #2F7BF0 100%);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  /* ② 외곽선 */
  -webkit-text-stroke: 3px #3A1F8F;
  paint-order: stroke fill;
  /* ③④ 입체 두께 + 글로우 */
  filter:
    drop-shadow(0 4px 0 #6A2BD9)
    drop-shadow(0 8px 0 #3A1F8F)
    drop-shadow(0 0 24px rgba(92,200,255,.45));
}

/* 마젠타 버전 (SPACE TRAVEL 스타일) */
.logo--magenta {
  background: linear-gradient(180deg, #F7B6FF 0%, #D94BF0 50%, #7B3BFF 100%);
  -webkit-background-clip: text; background-clip: text;
}

/* 손글씨 서브카피 */
.logo-script {
  font-family: 'Pacifico', 'Gaegu', cursive;
  color: #E35BFF;
  text-shadow: 0 3px 0 #5A1680, 0 0 16px rgba(227,91,255,.5);
  transform: rotate(-3deg);
}
```

---

## 4. Shape · Spacing · Elevation

### 4-1. Radius
| Token | Value | 용도 |
|---|---|---|
| `--r-sm` | 10px | 뱃지, 태그 |
| `--r-md` | 16px | 아이콘 버튼 |
| `--r-lg` | 24px | 일반 버튼, 카드 |
| `--r-xl` | 32px | 모달, 큰 패널 |
| `--r-full` | 999px | 프로그레스 바, 필 버튼 |

### 4-2. Spacing (4px base)
`4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96`

### 4-3. Glossy Depth 공식 (모든 버튼/패널 공통)

```
┌──────────────────────┐  ← 상단 inner highlight (흰색 30~60%, 위쪽 40% 영역)
│   ▔▔▔▔▔▔▔▔▔▔▔▔▔      │
│        LABEL         │  ← Base 컬러 그라디언트 (Top → Base)
│                      │
└──────────────────────┘
 ▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀   ← 하단 edge (Bottom 컬러, 6px 두께)
   ░░░░░░░░░░░░░░░░░░     ← 드롭 섀도 (보라 계열, 흐리게)
```

```css
--depth-edge: 6px;
--shadow-drop: 0 10px 20px rgba(14, 6, 38, .55);
--glow-cyan:   0 0 24px rgba(59,180,245,.55);
--glow-yellow: 0 0 24px rgba(255,194,61,.55);
--glow-magenta:0 0 24px rgba(217,75,240,.55);
```

---

## 5. Components

### 5-1. Candy Button

| Variant | 색 | 용도 |
|---|---|---|
| `primary` | Star Yellow | START, PLAY, 구매 등 핵심 CTA (화면당 1개) |
| `secondary` | Cosmic Cyan | 다음, 확인, 일반 액션 |
| `tertiary` | Moon White | 일시정지, 뒤로, 보조 액션 |
| `danger` | Candy Pink | 나가기, 삭제 |

| Size | Height | Padding X | Font |
|---|---|---|---|
| L | 72px | 48px | 28px |
| M | 56px | 32px | 20px |
| S | 44px | 20px | 16px |

```css
.btn {
  --top: #FFE680; --base: #FFC23D; --edge: #E07B12; --ink: #C4500A;
  position: relative;
  height: 56px; padding: 0 32px;
  border: 3px solid rgba(255,255,255,.55);
  border-radius: 20px;
  font: 700 20px/1 'Fredoka', 'Jua', sans-serif;
  letter-spacing: .04em;
  color: var(--ink);
  background: linear-gradient(180deg, var(--top) 0%, var(--base) 55%);
  box-shadow:
    inset 0 -4px 0 rgba(0,0,0,.08),
    0 var(--depth-edge, 6px) 0 var(--edge),
    var(--shadow-drop);
  cursor: pointer;
  transition: transform .12s cubic-bezier(.34,1.56,.64,1), box-shadow .12s;
}
/* 상단 광택 */
.btn::before {
  content: ''; position: absolute; left: 10%; right: 10%; top: 5px; height: 35%;
  border-radius: 999px;
  background: linear-gradient(180deg, rgba(255,255,255,.75), rgba(255,255,255,0));
  pointer-events: none;
}
.btn:hover  { transform: translateY(-2px) scale(1.03); }
.btn:active { transform: translateY(var(--depth-edge, 6px));
              box-shadow: 0 0 0 var(--edge), 0 4px 8px rgba(14,6,38,.5); }

.btn--secondary { --top:#9BE7FF; --base:#3BB4F5; --edge:#1A6FC4; --ink:#0F4C9C; }
.btn--tertiary  { --top:#FFFFFF; --base:#E9E6F7; --edge:#A9A3C9; --ink:#6E66A0; }
.btn--danger    { --top:#FFA3D1; --base:#FF4FA3; --edge:#C2186B; --ink:#FFFFFF; }
```

### 5-2. Icon Button (정사각 젤리)
- 크기 `64×64` (M) / `52×52` (S), radius `--r-md`
- 아이콘 stroke 두께 **4px**, 끝 둥글게(`round`)
- 아이콘 세트: ✕ 닫기 · ‹ › 이전/다음 · ❚❚ 일시정지 · ▶ 재생 · ＋ 추가 · ☰ 메뉴 · ⌂ 홈 · ⚙ 설정 · 🔊 사운드
- 색 규칙: 내비게이션=Cyan, 시스템(메뉴/홈/설정)=Yellow, 일시정지/재생=White

### 5-3. Progress Bar (로딩 / XP / HP)

```css
.progress {
  height: 32px; padding: 4px;
  border-radius: 999px;
  background: linear-gradient(180deg, #2B1260, #1A0B3D);
  border: 3px solid #E9E6F7;
  box-shadow: 0 4px 0 #A9A3C9, inset 0 2px 6px rgba(0,0,0,.4);
}
.progress__fill {
  height: 100%; border-radius: 999px;
  background:
    repeating-linear-gradient(-45deg,
      rgba(255,255,255,.35) 0 10px, transparent 10px 20px),
    linear-gradient(180deg, #FFE680, #FFB020);
  background-size: 28px 28px, 100% 100%;
  animation: stripe-move 1s linear infinite;
}
@keyframes stripe-move { to { background-position: 28px 0, 0 0; } }
```
- 수치 라벨: 바 오른쪽 안쪽, `caption` + `--text-on-yellow` 또는 흰색
- HP 바는 Pink, XP 바는 Cyan, 로딩은 Yellow

### 5-4. Card / Panel
- 배경: `rgba(43,18,96,.75)` + `backdrop-filter: blur(12px)`
- 테두리: `3px solid rgba(155,231,255,.35)`
- radius `--r-xl`, 하단 edge `0 6px 0 #120838`
- 상단에 얇은 하이라이트 라인 (`inset 0 2px 0 rgba(255,255,255,.15)`)

### 5-5. Collectibles (재화 아이콘)
| 아이템 | 형태 | 색 |
|---|---|---|
| Coin | 원형 + 두꺼운 테두리 + 중앙 문양 | Yellow / Pink |
| Gem | 6각/다이아 컷, 면 3톤 분할 | Cyan `#7FE0FF / #3BB4F5 / #1A6FC4` |
| Crystal Ring | 세로 타원 링 | White ↔ Magenta 그라디언트 |

### 5-6. Mascot (가이드라인)
레퍼런스처럼 **둥근 헬멧형 머리 + 짙은 남색 페이스 스크린 + 시안 발광 눈** 구조의 오리지널 로봇 캐릭터 권장.
- 바디: Moon White 3톤 (`#FFFFFF / #E9E6F7 / #A9A3C9`)
- 스크린: `#1A1F4A`, 눈·입은 Cyan 발광 (`--glow-cyan`)
- 감정 표현은 **스크린 안 표정/텍스트**로 (예: 😊, `LOW`, 하트 픽셀)
- 포인트 파츠(귀/가슴 코어) 1색만: Cyan 또는 Pink
- 포즈 세트: 인사 · 날기 · 아이템 들기 · 게임 중 · 슬픔(LOW)

---

## 6. Background Elements

| 요소 | 규칙 |
|---|---|
| **Stars** | 2~3px 원 + 십자 반짝이(✦) 혼합, 흰색/연보라, 밀도 낮게 랜덤 |
| **Shooting Star** | 대각선(약 −30°) 그라디언트 꼬리 + 시안 발광 머리, 4~8초 간격 |
| **Nebula Blob** | 큰 유기적 곡선 블롭, `#2B1260 ~ #5B2A9E`, 레이어 2~3겹 |
| **Planets** | 화면 모서리에 크롭되어 걸치게 배치 (프레이밍 역할), 셀 셰이딩 2톤 + 디테일 패턴 |
| **Orbit Ring** | 로고 뒤 얇은 원형 링 (`2px`, `rgba(255,255,255,.35)`) — 포커스 프레임 |

**레이어 순서 (z-index)**
```
0  배경 그라디언트
1  성운 블롭
2  별 / 반짝이
3  유성
4  행성 (모서리 크롭)
5  UI 패널 / 마스코트
6  로고 / CTA
7  모달 / 토스트
```

---

## 7. Motion

| Token | Value | 용도 |
|---|---|---|
| `--ease-bounce` | `cubic-bezier(.34,1.56,.64,1)` | 버튼, 팝업 등장 |
| `--ease-soft` | `cubic-bezier(.4,0,.2,1)` | 페이드, 화면 전환 |
| `--dur-fast` | 120ms | 버튼 press |
| `--dur-base` | 300ms | 호버, 토글 |
| `--dur-slow` | 600ms | 모달, 페이지 진입 |

```css
/* 행성/마스코트 둥둥 */
@keyframes float { 0%,100% { transform: translateY(0) } 50% { transform: translateY(-12px) } }
/* 별 반짝 */
@keyframes twinkle { 0%,100% { opacity:.3; transform:scale(.8) } 50% { opacity:1; transform:scale(1.2) } }
/* 로고 등장 */
@keyframes pop-in { 0% { transform:scale(.3); opacity:0 } 70% { transform:scale(1.08) } 100% { transform:scale(1); opacity:1 } }
/* 유성 */
@keyframes shoot { from { transform: translate(0,0) rotate(-30deg); opacity:1 }
                   to   { transform: translate(-600px,350px) rotate(-30deg); opacity:0 } }
```
- 행성마다 `float` duration을 4~8s로 다르게 → 자연스러운 비동기감
- `prefers-reduced-motion` 시 float/twinkle/shoot 정지

---

## 8. Layout & Pages

### 8-1. Grid
- Desktop: 12 col / max-width 1280 / gutter 24
- Mobile: 4 col / side 16 / gutter 16
- 로고·CTA는 항상 **중앙 정렬**, 장식 요소는 **좌우 대칭에 가깝게** 배치

### 8-2. 권장 페이지 구성
1. **Hero** — 중앙 로고 + 오빗 링 + START 버튼, 모서리 행성 4개, 유성
2. **Game Intro** — 마스코트 + 말풍선, 게임 특징 3개 카드
3. **Planets / Stages** — 가로 스크롤 행성 카드 (잠금 행성은 Moon Gray + 자물쇠)
4. **Characters** — 마스코트 포즈 갤러리
5. **Rewards** — 코인/젬 아이콘 + 프로그레스 바
6. **Footer** — 아이콘 버튼 바(홈/사운드/설정), 별 배경 유지

### 8-3. Do / Don't
| ✅ Do | ❌ Don't |
|---|---|
| 버튼마다 하단 edge + 광택 | 플랫한 사각 버튼 |
| 채도 높은 원색 3~4개를 어두운 배경 위에 | 회색·무채색 위주 UI |
| 굵고 둥근 폰트 | 얇은 세리프/기본 시스템 폰트 |
| 모든 요소에 미세한 움직임 | 완전히 정적인 화면 |
| CTA는 화면당 Yellow 1개 | Yellow 버튼 남발 |

---

## 9. CSS Token 모음 (복붙용)

```css
:root {
  /* Space */
  --space-900:#0E0626; --space-800:#1A0B3D; --space-700:#2B1260;
  --space-600:#3D1A80; --nebula-500:#5B2A9E;
  /* Accents (top / base / edge) */
  --cyan-top:#9BE7FF;    --cyan:#3BB4F5;    --cyan-edge:#1A6FC4;
  --yellow-top:#FFE680;  --yellow:#FFC23D;  --yellow-edge:#E07B12;
  --magenta-top:#F79CFF; --magenta:#D94BF0; --magenta-edge:#8A1FB0;
  --pink-top:#FFA3D1;    --pink:#FF4FA3;    --pink-edge:#C2186B;
  --white-top:#FFFFFF;   --white:#E9E6F7;   --white-edge:#A9A3C9;
  /* Semantic */
  --success:#4DE8B0; --danger:#FF4F7B;
  --text-primary:#FFFFFF; --text-secondary:#C9BFF0;
  /* Type */
  --font-display:'Lilita One','Jua',sans-serif;
  --font-script:'Pacifico','Gaegu',cursive;
  --font-ui:'Fredoka','Jua',sans-serif;
  --font-body:'Nunito','Pretendard',sans-serif;
  /* Shape */
  --r-sm:10px; --r-md:16px; --r-lg:24px; --r-xl:32px; --r-full:999px;
  --depth-edge:6px;
  --shadow-drop:0 10px 20px rgba(14,6,38,.55);
  /* Motion */
  --ease-bounce:cubic-bezier(.34,1.56,.64,1);
  --ease-soft:cubic-bezier(.4,0,.2,1);
  --dur-fast:120ms; --dur-base:300ms; --dur-slow:600ms;
}
```
