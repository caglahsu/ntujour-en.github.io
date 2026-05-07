# Change Log — Graduate Institute of Journalism, NTU (English Website)

> **Rule:** Every time a prompt is used to revise the code, record the entry here with:
> `## [YYYY-MM-DD HH:MM TST] — Brief title`
> followed by the prompt summary and files changed.
> Time zone: Taiwan Standard Time (TST, UTC+8).

---

## [2026-05-07 ~15:20 TST] — Initial website build

**Prompt summary:**
> 「我現在想要架設一個一頁式的英文版網頁，其中文版網頁為：https://ntujour.github.io/ （視覺風格參考）。英文資訊請參考：https://webpageprodvm.ntu.edu.tw/Journalism/Default.aspx。這個頁面會有以下資訊：簡短的 Introduction、新聞所 news、新聞所教師（full-time 專任教師需額外有連結，建立一個新的頁面）」

**Actions taken:**
- Fetched content from `ntujour.github.io` and `webpageprodvm.ntu.edu.tw/Journalism/` to gather design references, English content, faculty info, and news items.
- Fetched all 7 full-time faculty profile pages from the NTU official site.
- Created `css/style.css` — full stylesheet with dark-blue NTU color scheme (initial draft, later revised).
- Created `index.html` — one-page site with: site banner, sticky nav, hero section, Introduction (with pillar cards and stats), News (5 cards), Faculty grid (7 cards).
- Created 7 faculty profile pages under `faculty/`:
  - `ji-lung-hsieh.html`
  - `lih-yun-lin.html`
  - `chen-ling-hung.html`
  - `adrian-rauchfleisch.html`
  - `hui-ju-tsai.html`
  - `i-i-chan.html`
  - `lokman-tsui.html`

**Files created:** `css/style.css`, `index.html`, `faculty/ji-lung-hsieh.html`, `faculty/lih-yun-lin.html`, `faculty/chen-ling-hung.html`, `faculty/adrian-rauchfleisch.html`, `faculty/hui-ju-tsai.html`, `faculty/i-i-chan.html`, `faculty/lokman-tsui.html`

---

## [2026-05-07 ~15:34 TST] — Color scheme & banner redesign to match ntujour.github.io

**Prompt summary:**
> 「我的配色要和 https://ntujour.github.io/ 的配色一模一樣！還有最頂端的 bar 也要一樣！」

**Actions taken:**
- Fetched raw HTML source of `ntujour.github.io` via `curl` to obtain exact class names and structure.
- Fetched `ntujour.github.io/css/site-common.css` to extract exact color values.
- Fetched `ntujour.github.io/js/load-banner.js` to understand dynamic banner rendering.
- Identified the correct color palette:
  - Nav background: `#671919` (maroon)
  - Active/hover nav text: `#efa22a` (gold)
  - Footer background: `#3e0f0f` (dark maroon)
  - Banner background: `#f5f5f5` (light gray) with decorative images
- Rewrote `css/style.css` completely with the new color variables and banner styles.
- Updated `index.html`: replaced dark-blue `.topbar` + `.navbar` with light-gray `.site-banner` + maroon `.site-nav`; moved 中文 language link into nav; fixed scroll-spy offset calculation.
- Updated all 7 faculty pages via Python batch script: replaced `.topbar` + `.navbar` blocks with the new `.site-banner` + `.site-nav` structure.

**Files modified:** `css/style.css`, `index.html`, `faculty/ji-lung-hsieh.html`, `faculty/lih-yun-lin.html`, `faculty/chen-ling-hung.html`, `faculty/adrian-rauchfleisch.html`, `faculty/hui-ju-tsai.html`, `faculty/i-i-chan.html`, `faculty/lokman-tsui.html`

---

## [2026-05-07 ~15:40 TST] — Project review and documentation

**Prompt summary:**
> 「Please review whole project, and save the record as INSTRUCTION.md, and generate another LOG.md used to record each operation. And note a rule on INSTRUCTION.md, each time when using prompt to revise the code, please record each prompt's date and time.」

**Actions taken:**
- Reviewed full project file structure and all source files.
- Created `INSTRUCTION.md` with: project overview, file structure, design system (colors, typography, layout), banner/nav spec, content update guide, deployment notes, external dependencies, and the logging rule.
- Created `LOG.md` (this file) with retrospective entries for all previous sessions and the logging rule explanation.

**Files created:** `INSTRUCTION.md`, `LOG.md`

---

<!-- Template for future entries:

## [YYYY-MM-DD HH:MM TST] — Short title

**Prompt summary:**
> 「...」

**Actions taken:**
- ...

**Files modified/created:** ...

-->
