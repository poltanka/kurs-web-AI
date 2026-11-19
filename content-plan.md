# Контент-план: 5 статей для розділу «Статті» на сайті «ШІ-майстерня»

*Основа: звіт research-report.md (історія ChatGPT, Codex і Gemini, станом на 17.11.2026)*

**Принцип порядку:** кожна стаття спирається на попередню. Спочатку ідея розмовної машини (без техніки), далі одна компанія, потім друга, після неї складніша тема (код і агенти) і наприкінці критичне мислення щодо цифр і новин.

**Принцип без повторів:** кожна тема має одну «домівку». В інших статтях вона згадується одним реченням із посиланням на свою статтю (див. таблицю в кінці).

---

## 1. До ChatGPT: як комп'ютери вчилися розмовляти

- **Порядок:** 1
- **Ключова думка:** Перші чат-боти працювали за готовими сценаріями, а у 2017 р. архітектура «трансформер» навчила машини виводити закономірності мови з величезних обсягів тексту.
- **Аудиторія:** 14–18 років, без жодних знань про ШІ. Це вхідна стаття розділу.
- **Охоплює:** ELIZA (1964–1966) і «ефект ELIZA»; чому сценарій ≠ розуміння; стаття «Attention Is All You Need» (2017) як поворотний момент. Механізм «уваги» пояснюємо на побутовому прикладі, без формул.
- **Джерела:**
  - Britannica «ELIZA» — https://www.britannica.com/technology/Eliza
  - Britannica «Joseph Weizenbaum» — https://www.britannica.com/biography/Joseph-Weizenbaum
  - arXiv 1706.03762 — https://arxiv.org/abs/1706.03762
  - NeurIPS Proceedings — https://papers.nips.cc/paper/7181-attention-is-all-you-need
- **Обсяг:** 600–700 слів.

## 2. Як народився ChatGPT

- **Порядок:** 2
- **Ключова думка:** ChatGPT з'явився завдяки двом крокам: моделі GPT ставали дедалі більшими, а потім їх донавчили на оцінках людей, щоб вони виконували прохання.
- **Аудиторія:** 14–18 років; читачі, які вже користуються ChatGPT, але не знають, звідки він узявся.
- **Охоплює:** заснування OpenAI (2015); GPT-1 → GPT-2 → GPT-3 (зростання параметрів простими порівняннями); InstructGPT і навчання на людських оцінках (RLHF); суперкомп'ютер Azure; запуск 30.11.2022. Про популярність — одне речення «за оцінками аналітиків» із посиланням на статтю 5.
- **Джерела:**
  - «Introducing OpenAI» (архів) — https://273ventures.com/pdf/OpenAI_Website_20151211215507.pdf
  - Блог OpenAI про GPT-1 — https://openai.com/index/language-unsupervised/
  - Блог OpenAI про GPT-2 — https://openai.com/index/better-language-models/
  - arXiv 2005.14165 (GPT-3) — https://arxiv.org/abs/2005.14165
  - arXiv 2203.02155 (InstructGPT) — https://arxiv.org/pdf/2203.02155
  - Microsoft Source (суперкомп'ютер) — https://news.microsoft.com/source/features/ai/openai-azure-supercomputer/
  - ⚠️ «Introducing ChatGPT» — посилання ще треба знайти.
- **Обсяг:** 750–850 слів.

## 3. Від Bard до Gemini: відповідь Google

- **Порядок:** 3
- **Ключова думка:** Google винайшла трансформер, але першим масовим чат-ботом став ChatGPT, тож компанія об'єднала свої лабораторії й побудувала Gemini — модель, що з самого початку працює і з текстом, і з зображеннями, і зі звуком.
- **Аудиторія:** 14–18 років; користувачі Android і сервісів Google, яким цікаво, чим Gemini відрізняється від ChatGPT.
- **Охоплює:** DeepMind і TPU (власні чипи); LaMDA і PaLM; Bard (2023); об'єднання Google Brain і DeepMind; Gemini 1.0 (Ultra/Pro/Nano); перейменування Bard → Gemini (2024); мультимодальність; Нобелівська премія Хассабіса як приклад ШІ в науці.
- **Джерела:**
  - TechCrunch (купівля DeepMind) — https://techcrunch.com/2014/01/26/google-deepmind
  - Блог Google про Bard — https://blog.google/intl/en-africa/products/explore-get-answers/an-important-next-step-on-our-ai-journey/
  - Блог Google «Introducing Gemini» — https://blog.google/intl/en-mena/company-news/technology/google-gemini-ai/
  - Блог Google «Bard is now Gemini» — https://blog.google/products-and-platforms/products/gemini/bard-gemini-advanced-app/
  - SiliconANGLE (об'єднання) — https://siliconangle.com/2023/04/20/google-merges-deepmind-google-brain-ai-research-groups/
  - The Register (об'єднання) — https://www.theregister.com/2023/04/20/google_brain_deep_mind/
  - arXiv 2312.11805 — https://arxiv.org/abs/2312.11805
  - nobelprize.org — https://www.nobelprize.org/prizes/chemistry/2024/press-release/
  - ⚠️ Блоги Google про LaMDA і PaLM — посилання ще треба знайти.
- **Обсяг:** 750–850 слів.

## 4. Codex: одна назва — два різні помічники

- **Порядок:** 4
- **Ключова думка:** Під назвою Codex OpenAI випустила два різні продукти: модель-підказувача коду (2021–2023) і агента, який сам виконує завдання з програмування (з 2025), і різниця між ними показує, як ШІ перейшов від порад до дій.
- **Аудиторія:** 15–18 років; ті, хто цікавиться програмуванням. Статтю можна читати без досвіду кодування.
- **Охоплює:** порівняльна таблиця двох Codex; GitHub Copilot як «автодоповнення» коду; тест HumanEval простими словами; чому стару модель вимкнули у 2023 р.; що таке ШІ-агент; коротке «що агент може, а що варто перевіряти людині».
- **Джерела:**
  - arXiv 2107.03374 — https://arxiv.org/pdf/2107.03374
  - OpenAI «Deprecations» — https://platform.openai.com/docs/deprecations
  - OpenAI «Introducing Codex» — https://openai.com/index/introducing-codex/
  - Хронологія hidekazu-konishi.com (для звірки) — https://hidekazu-konishi.com/entry/openai_gpt_model_release_timeline.html
  - Wikipedia «OpenAI Codex» (вторинне) — https://en.wikipedia.org/wiki/OpenAI_Codex
  - ⚠️ GitHub Blog про Copilot (2021, 2022) — посилання ще треба знайти.
- **Обсяг:** 800–900 слів.

## 5. Мільярд користувачів і інші цифри: як читати новини про ШІ

- **Порядок:** 5
- **Ключова думка:** Цифри про ШІ бувають офіційними, оціночними або взагалі чутками, і щоб правильно їх розуміти, треба перевіряти, хто й що саме виміряв.
- **Аудиторія:** 16–18 років; найскладніша стаття розділу, бо спирається на попередні чотири.
- **Охоплює:** короткий огляд 2024–2026 (GPT-4o → GPT-6, Gemini 1.5 → Gemini 4 Argon) — лише як фон; кейс «100 млн за 2 місяці» (оцінка UBS проти офіційних даних OpenAI); тижневі й місячні користувачі (ChatGPT 1,2 млрд проти Gemini 1 млрд); нерозкриті параметри GPT-4 і вартість навчання; маркетинговий результат Gemini Ultra на MMLU. Наприкінці — чекліст із 4–5 питань для перевірки новини.
- **Джерела:**
  - Звіт GPT-4 (arXiv 2303.08774) — https://arxiv.org/pdf/2303.08774v2
  - Engadget (100 млн) — https://www.engadget.com/chatgpt-100-million-users-january-130619073.html
  - TechCrunch (Gemini — 750 млн) — https://techcrunch.com/2026/02/04/googles-gemini-app-has-surpassed-750m-monthly-active-users/
  - TechCrunch (Gemini — 1 млрд) — https://techcrunch.com/2026/08/11/googles-gemini-app-surges-to-one-billion-users/
  - Блог Google Q2 2026 — https://blog.google/company-news/inside-google/message-ceo/alphabet-earnings-q2-2026/
  - Forbes (вартість навчання) — https://www.forbes.com/sites/katharinabuchholz/2024/08/23/the-extreme-cost-of-training-ai-models/
  - Блог Google «Introducing Gemini» і arXiv 2312.11805 (для кейсу MMLU)
  - Розділ 3 звіту research-report.md
  - ⚠️ Дати 2026 р. (GPT-5.4, GPT-6 Astra, Gemini 4 Carbon) звірити з openai.com і blog.google.
- **Обсяг:** 800–900 слів.

---

## Розподіл тем (щоб не повторюватись)

| Тема | Де розкрита | Де лише згадується |
|---|---|---|
| Трансформер | 1 | 2, 3 |
| Навчання на людських оцінках (RLHF) | 2 | — |
| Суперкомп'ютер Azure / TPU | 2 / 3 | — |
| Мультимодальність | 3 | 5 |
| GitHub Copilot, агенти | 4 | 5 |
| 100 млн користувачів, порівняння аудиторій | 5 | 2 |
| Моделі 2024–2026 | 5 | 3, 4 |
| Звільнення Альтмана (2023) | не входить: не стосується лінії «як працює й розвивається ШІ» | — |

Це план для української версії. Англійську, ймовірно, варто готувати окремо як адаптацію, а не дослівний переклад.
