# Історія ChatGPT, Codex і Gemini: фактична база для освітнього курсу

*Станом на 17 листопада 2026 р.*

Головне: ChatGPT (OpenAI, запущений 30 листопада 2022 р.) і Gemini (Google, анонсований 6 грудня 2023 р.; до 8 лютого 2024 р. асистент називався Bard) виросли з одного винаходу — архітектури «трансформер», яку вісім дослідників Google описали у статті «Attention Is All You Need» (arXiv, 12 червня 2017 р.). Codex — це дві різні речі під однією назвою: модель 2021–2023 рр., що працювала в GitHub Copilot, і зовсім новий агент для програмування, який OpenAI випускає з 2025 р.

## TL;DR

- **Спільний корінь і різні шляхи.** Трансформер (Google, 2017) → GPT-1 (2018), GPT-2 (2019), GPT-3 (2020), InstructGPT із навчанням на людських оцінках (2022) → ChatGPT (30.11.2022). У Google той самий корінь дав BERT (2018), LaMDA (2021), PaLM (2022), Bard (2023) і нарешті Gemini (з грудня 2023). Станом на листопад 2026 р. найновіші покоління — GPT-6 (OpenAI) та Gemini 4 Argon (Google).
- **Codex — це два різні продукти.** Codex-модель (серпень 2021 р., стаття arXiv 2107.03374) була «двигуном» GitHub Copilot, а в березні 2023 р. її вимкнули в API. Codex-агент (CLI — квітень 2025, хмарна версія — 16 травня 2025) — новий продукт на інших моделях (codex-1, лінійка GPT-5-Codex), лише з тією самою назвою.
- **Масштаб і обережність із цифрами.** OpenAI повідомила про 1,2 млрд *щотижневих* користувачів ChatGPT (DevDay, 29.09.2026), Google — про понад 1 млрд *щомісячних* користувачів застосунку Gemini (11.08.2026). Ці метрики різні, тож напряму їх порівнювати не можна. Знамените «100 млн користувачів ChatGPT за 2 місяці» — це оцінка дослідження UBS на основі даних Similarweb, яку Reuters поширило 1.02.2023, а не офіційна цифра OpenAI. Кількість параметрів GPT-4 офіційно ніколи не розкривали.

---

## 1. Хронологія (єдина шкала для всіх трьох асистентів)

Позначки: **[офіц.]** — першоджерело компанії або наукова стаття; **[вторин.]** — медіа чи компіляція; **[оцінка]** — неофіційна або розрахункова цифра.

### Передісторія (до 2017)

| Дата | Подія | Джерело |
|---|---|---|
| 1964–1966 | Джозеф Вайценбаум створює ELIZA — програму-співрозмовника, що імітувала психотерапевта; стаття вийшла 1966 р. | Britannica, стаття «ELIZA» [офіц./енцикл.] |
| 2014 (26–27 січня) | Google купує лондонську лабораторію DeepMind; ціну офіційно не розкрито (див. розділ 3) | AFP через phys.org; TechCrunch [вторин.] |
| 11 грудня 2015 | Публічно оголошено про створення OpenAI як некомерційної дослідницької компанії; співголови — Сем Альтман та Ілон Маск, директор із досліджень — Ілля Суцкевер, технічний директор — Ґреґ Брокман | Допис OpenAI «Introducing OpenAI» [офіц.] |
| травень 2016 | Google на конференції I/O оголошує про TPU — власний чип для ШІ, який на той момент уже понад рік працював у її дата-центрах | Матеріали Google I/O 2016 (через енцикл. огляди TPU) [вторин.] |

### Ера трансформера і моделей GPT (2017–2022)

| Дата | Подія | Джерело |
|---|---|---|
| 12 червня 2017 | На arXiv з'являється «Attention Is All You Need» (arXiv 1706.03762); 8 авторів: Ашиш Васвані, Ноам Шазір, Нікі Пармар, Якоб Ушкорайт, Ліон Джонс, Ейдан Ґомес, Лукаш Кайзер, Ілля Полосухін. Робота опублікована у збірнику конференції NIPS 2017 (4–9 грудня 2017) | arXiv 1706.03762; NeurIPS Proceedings [офіц.] |
| 11 червня 2018 | OpenAI публікує GPT-1 («Improving language understanding with unsupervised learning»): поєднання трансформера та попереднього навчання без учителя | Блог OpenAI [офіц.] |
| 11 жовтня 2018 | Google публікує BERT (arXiv 1810.04805) | arXiv [офіц.] |
| 14 лютого 2019 | Анонс GPT-2 (1,5 млрд параметрів, навчена на 8 млн вебсторінок); модель випускали поетапно, повну версію оприлюднили в листопаді 2019 р. | Блог OpenAI «Better language models…» [офіц.] |
| 2019 | Microsoft інвестує в OpenAI 1 млрд доларів | The Verge/Engadget/GeekWire (травень 2020) [вторин.] |
| 19 травня 2020 | Microsoft на Build 2020 представляє суперкомп'ютер в Azure, побудований для OpenAI: понад 285 000 ядер CPU, 10 000 GPU, 400 Гбіт/с мережі на кожен GPU-сервер; за заявою компанії — у топ-5 світу | Microsoft Source [офіц.] |
| 28 травня 2020 | Стаття про GPT-3 «Language Models are Few-Shot Learners» (arXiv 2005.14165): 175 млрд параметрів | arXiv [офіц.] |
| 11 червня 2020 | GPT-3 стає доступною через OpenAI API (закрита бета) | Блог OpenAI «OpenAI API» [офіц.] |
| 18 травня 2021 | Google на I/O анонсує LaMDA — мовну модель для діалогів | Блог Google «LaMDA: our breakthrough conversation technology» [офіц.] |
| 29 червня 2021 | GitHub запускає технічне прев'ю Copilot на основі OpenAI Codex | GitHub Blog [офіц.] |
| 7 липня 2021 | Стаття «Evaluating Large Language Models Trained on Code» (arXiv 2107.03374): Codex розв'язує 28,8% задач нового тесту HumanEval (164 задачі на Python); GPT-3 — 0%. Окрема «виробнича» версія Codex працює в GitHub Copilot | arXiv [офіц.] |
| 10 серпня 2021 | OpenAI відкриває Codex у своєму API (закрита бета) | Компіляція хронології OpenAI (hidekazu-konishi.com) [вторин.] |
| березень 2022 | Стаття про InstructGPT (arXiv 2203.02155): після донавчання на людських оцінках (RLHF) відповіді моделі з 1,3 млрд параметрів люди-оцінювачі обирали частіше, ніж відповіді GPT-3 зі 175 млрд | arXiv; NeurIPS 2022 [офіц.] |
| 4 квітня 2022 | Google Research представляє PaLM — модель на 540 млрд параметрів | Блог Google Research [офіц.] |
| 21 червня 2022 | GitHub Copilot стає загальнодоступним за 10 дол./місяць або 100 дол./рік | TechCrunch; GitHub Blog [офіц./вторин.] |
| **30 листопада 2022** | **OpenAI випускає ChatGPT як безкоштовне «дослідницьке прев'ю» на основі моделей серії GPT-3.5** | Допис OpenAI «Introducing ChatGPT» [офіц.] |

### Гонка асистентів (2023–2024)

| Дата | Подія | Джерело |
|---|---|---|
| січень 2023 | За дослідженням UBS на основі даних Similarweb, ChatGPT «за оцінками» досяг 100 млн щомісячних користувачів у січні 2023 р.; у середньому близько 13 млн унікальних відвідувачів на день — більш ніж удвічі більше, ніж у грудні. Для порівняння, TikTok на це знадобилося близько 9 місяців, Instagram — 2,5 року (Sensor Tower) | Reuters, 1 лютого 2023 (через Engadget, Time, Guardian) [оцінка] |
| 1 лютого 2023 | Запуск платної підписки ChatGPT Plus (20 дол./місяць) | OpenAI; The Guardian [офіц.] |
| 6 лютого 2023 | Сундар Пічаї оголошує Bard — експериментальний розмовний сервіс на основі LaMDA, спершу для обмеженого кола тестувальників | Блог Google «An important next step on our AI journey» [офіц.] |
| 14 березня 2023 | OpenAI представляє GPT-4 — мультимодальну модель (текст + зображення на вході). Технічний звіт свідомо не розкриває архітектуру й розмір моделі | Звіт GPT-4 (arXiv 2303.08774) [офіц.] |
| 21 березня 2023 | Bard відкривають для публіки у США та Великій Британії | Блог Google «Try Bard» [офіц.] |
| 20–23 березня 2023 | OpenAI повідомляє клієнтів про припинення роботи Codex API; моделі code-davinci/code-cushman вимикають 23 березня | Сторінка OpenAI «Deprecations»; Hacker News, 21.03.2023 [офіц./вторин.] |
| 20 квітня 2023 | Google об'єднує Google Brain і DeepMind у Google DeepMind на чолі з Демісом Хассабісом; Джефф Дін стає головним науковцем Google | Блог Пічаї (через SiliconANGLE, The Register, Bloomberg) [офіц./вторин.] |
| 10 травня 2023 | Google на I/O представляє PaLM 2, на якій тепер працює Bard | Блог Google «Introducing PaLM 2» [офіц.] |
| 6 листопада 2023 | Перший DevDay OpenAI: GPT-4 Turbo (контекст 128 тис. токенів), GPTs; Альтман повідомляє про 100 млн *щотижневих* користувачів ChatGPT | OpenAI; The Verge [офіц./вторин.] |
| 17–29 листопада 2023 | Рада директорів OpenAI звільняє Альтмана (17.11). Тимчасовою CEO стає Міра Мураті. 745 із 770 працівників підписують лист із погрозою звільнитися (20.11), серед підписантів — Суцкевер. Домовленість про повернення Альтмана досягнуто 21–22.11, формально він повернувся 29.11 | Fortune, TechCrunch [вторин.] |
| **6 грудня 2023** | **Google анонсує Gemini 1.0 трьох розмірів (Ultra, Pro, Nano) — першу свою «нативно мультимодальну» модель; Bard переходить на Gemini Pro** | Блог Google «Introducing Gemini» [офіц.] |
| 19 грудня 2023 | Технічний звіт Gemini (arXiv 2312.11805) | arXiv [офіц.] |
| 10 січня 2024 | Відкривається GPT Store | OpenAI [офіц.] |
| **8 лютого 2024** | **Bard перейменовано на Gemini; запущено Gemini Advanced із моделлю Ultra 1.0** | Блог Google «Bard becomes Gemini» [офіц.] |
| 15 лютого 2024 | Gemini 1.5 Pro: архітектура «суміш експертів» і контекст до 1 млн токенів | Блог Google [офіц.] |
| 13 травня 2024 | GPT-4o («omni») — одна модель для тексту, звуку й зображень | Допис OpenAI «Hello GPT-4o» [офіц.] |
| 18 липня 2024 | GPT-4o mini замінює GPT-3.5 Turbo в ChatGPT | OpenAI [офіц.] |
| 12 вересня 2024 | o1-preview — перша «міркувальна» модель OpenAI, що «думає» перед відповіддю | OpenAI [офіц.] |
| 9 жовтня 2024 | Деміс Хассабіс і Джон Джампер (Google DeepMind) отримують половину Нобелівської премії з хімії за передбачення структури білків (AlphaFold) | Прес-реліз nobelprize.org [офіц.] |
| 31 жовтня 2024 | Запуск пошуку в ChatGPT | OpenAI [офіц.] |
| грудень 2024 | Gemini 2.0, подана як модель для «ери агентів» | Блог Google (за компіляцією hidekazu-konishi.com) [вторин.] |

### Агенти, «міркування» та нові покоління (2025–2026)

| Дата | Подія | Джерело |
|---|---|---|
| 27 лютого 2025 | GPT-4.5 (дослідницьке прев'ю), згодом знятий з використання | OpenAI; TechCrunch [офіц./вторин.] |
| березень 2025 | Gemini 2.5 Pro — перша «думаюча» модель Gemini | Google (через компіляції) [вторин.] |
| 16 квітня 2025 | o3 та o4-mini; того ж тижня з'являється Codex CLI — агент для програмування з відкритим кодом, що працює в терміналі | OpenAI «Introducing o3 and o4-mini» [офіц.] |
| **16 травня 2025** | **Codex — хмарний агент для програмування в ChatGPT (дослідницьке прев'ю) на моделі codex-1, версії o3, оптимізованій для розробки ПЗ** | OpenAI «Introducing Codex» [офіц.] |
| 3 червня 2025 | Codex стає доступним для користувачів ChatGPT Plus | OpenAI (оновлення до «Introducing Codex», за вторинними оглядами) [вторин.] |
| 7 серпня 2025 | GPT-5: єдина система зі швидкою моделлю, «думаючою» моделлю і маршрутизатором між ними; доступна і безкоштовним користувачам; навчена на суперкомп'ютерах Microsoft Azure | OpenAI «Introducing GPT-5» [офіц.] |
| 15 вересня 2025 | GPT-5-Codex стає основною моделлю Codex | OpenAI (за компіляцією) [вторин.] |
| 6 жовтня 2025 | Codex стає загальнодоступним (DevDay 2025) | OpenAI (за компіляцією) [вторин.] |
| 12 листопада 2025 | GPT-5.1 | OpenAI; Ars Technica [офіц./вторин.] |
| 18 листопада 2025 | Gemini 3 Pro: Google вперше вбудовує нову модель Gemini в Пошук у день випуску; разом із нею виходить платформа для програмування Antigravity | Блог Google «A new era of intelligence with Gemini 3» [офіц.] |
| 11 грудня 2025 | GPT-5.2; за повідомленнями медіа, її випуск прискорив внутрішній «code red» в OpenAI як відповідь на Gemini 3 | TechCrunch, Reuters, CNBC [вторин.] |
| 17 грудня 2025 | Gemini 3 Flash стає моделлю за замовчуванням у застосунку Gemini | TechCrunch [вторин.] |
| 4 лютого 2026 | Застосунок Gemini — понад 750 млн щомісячних користувачів (звіт Alphabet за 4-й квартал 2025 р.) | TechCrunch [вторин.] |
| 5 лютого 2026 | GPT-5.3-Codex; OpenAI називає її своєю «першою моделлю, яка допомогла створити саму себе» | Ars Technica; OpenAI [вторин./офіц.] |
| 13 лютого 2026 | GPT-4o та кілька інших моделей прибирають із ChatGPT (у API GPT-4o лишається) | CNBC, Engadget [вторин.] |
| 19 лютого 2026 | Gemini 3.1 Pro (прев'ю) | Трекер релізів benchlm.ai [вторин.] |
| 27 лютого 2026 | OpenAI повідомляє про 900 млн щотижневих користувачів ChatGPT | OpenAI (через TechCrunch та статистичні огляди) [вторин.] |
| 5 березня 2026 | GPT-5.4 — перша основна модель із вбудованим «керуванням комп'ютером» | OpenAI (за компіляцією) [вторин.] |
| 23 квітня 2026 | GPT-5.5 | CNBC, The Verge [вторин.] |
| 9 липня 2026 | GPT-5.6 з новою схемою назв рівнів: Sol / Terra / Luna | OpenAI (за компіляцією) [вторин.] |
| 22 липня 2026 | Застосунок Gemini — 950 млн щомісячних користувачів (звіт за 2-й квартал 2026 р.) | Блог Google, виступ Пічаї [офіц.] |
| 11 серпня 2026 | Пічаї: застосунок Gemini перетнув позначку 1 млрд щомісячних користувачів | TechCrunch [вторин.] |
| 3 вересня 2026 | GPT-6 Astra — нова флагманська модель OpenAI | Компіляція hidekazu-konishi.com з посиланням на OpenAI [вторин.] |
| 29 вересня 2026 | DevDay 2026: 1,2 млрд щотижневих користувачів ChatGPT | The Verge, Engadget (через огляди) [вторин.] |
| 30 вересня 2026 | Google анонсує Gemini 4 Argon — першу модель покоління Gemini 4; спершу вона доступна обмеженому колу фахівців із кібербезпеки (програма Fairwind) | Блог Google «Gemini 4 Argon: our next era of frontier intelligence» [офіц.] |
| 7 жовтня 2026 | GPT-6 стає основною моделлю чату ChatGPT для всіх тарифів | Компіляції; довідка OpenAI [вторин./офіц.] |
| 13 жовтня 2026 | Gemini 4 Argon стає доступною розробникам і передплатникам Google AI Pro/Ultra в застосунку Gemini | Блог Google [офіц.] |
| 26 жовтня 2026 | GPT-6.1 Terra в API, ChatGPT Work і Codex | Довідка OpenAI «Model Release Notes» [офіц.] |
| 28 жовтня 2026 | Google анонсує Gemini 4 Carbon (поки що не загальнодоступна) | Компіляція hidekazu-konishi.com [вторин.] |

---

## 2. Ключові «машини» та люди

### 2.1. Моделі, системи та інфраструктура

**Трансформер (2017).** Архітектура нейромережі, в основі якої механізм «уваги» (attention): модель зважує, які слова в тексті найважливіші одне для одного. На ній побудовано і GPT («T» у назві означає Transformer), і BERT, LaMDA, PaLM та Gemini. Джерело: arXiv 1706.03762.

**Серія GPT (OpenAI).**

- GPT-1 (2018) — показала, що попереднє навчання на великому обсязі тексту плюс донавчання дає сильну модель.
- GPT-2 (2019) — 1,5 млрд параметрів. OpenAI спочатку не випустила повну версію через ризики зловживань.
- GPT-3 (2020) — 175 млрд параметрів, уміє виконувати завдання за кількома прикладами.
- InstructGPT (2022) — навчання на людських оцінках (RLHF) зробило модель кращою у виконанні інструкцій.
- GPT-3.5 (2022) — основа першого ChatGPT.
- GPT-4 (2023) — мультимодальна; розмір не розкрито.
- GPT-4o (2024) — «omni»: голос, зображення й текст в одній моделі.
- o1/o3 (2024–2025) — «міркувальні» моделі.
- GPT-5 (2025) — об'єднала швидку й «думаючу» лінії.
- GPT-6 (2026).

Джерела: статті arXiv, блог OpenAI, компіляція hidekazu-konishi.com.

**Codex — два значення, які не можна плутати:**

| | Codex-модель (2021–2023) | Codex-агент (з 2025) |
|---|---|---|
| Що це | Мовна модель — нащадок GPT-3, донавчена на публічному коді з GitHub; перетворює опис англійською на код | Агент, який сам виконує завдання з програмування: пише функції, виправляє помилки, запускає тести, пропонує зміни (pull request) в ізольованому хмарному середовищі |
| Ключові дати | Стаття — липень 2021; API — 10.08.2021; вимкнення в API — 23.03.2023 | Codex CLI — 16.04.2025; хмарний Codex — 16.05.2025; загальна доступність — 06.10.2025 |
| Моделі | До 12 млрд параметрів у статті; в API — code-davinci-002, code-cushman-001 | codex-1 (на основі o3), GPT-5-Codex, GPT-5.2-Codex, GPT-5.3-Codex; з GPT-5.5 основні моделі працюють у Codex напряму |
| Де використовували | GitHub Copilot (прев'ю 2021, загальна доступність 2022) | ChatGPT, термінал, редактори коду, GitHub |
| Джерела | arXiv 2107.03374; OpenAI Deprecations; TechCrunch | OpenAI «Introducing Codex»; компіляція hidekazu-konishi.com |

**Ланцюжок моделей Google.** BERT (2018) → LaMDA (2021, діалогова модель) → PaLM (2022, 540 млрд параметрів) → PaLM 2 (2023) → Gemini 1.0 (грудень 2023; розміри Ultra/Pro/Nano, де Nano працює прямо на телефоні Pixel 8 Pro) → 1.5 (2024, контекст до 1–2 млн токенів) → 2.0 (грудень 2024, «агентна ера») → 2.5 (2025, «думаючі» моделі) → 3 (листопад 2025) → 3.1–3.8 (2026) → Gemini 4 Argon (вересень–жовтень 2026). Джерела: блог Google, компіляція hidekazu-konishi.com.

**Bard → Gemini.** Чат-бот Bard анонсували 6.02.2023 (на основі LaMDA), відкрили для публіки 21.03.2023, потім перевели на PaLM 2, а з грудня 2023 р. — на Gemini Pro. 8.02.2024 його перейменували на Gemini. Джерела: блог Google.

**TPU (Tensor Processing Unit).** Спеціалізований чип Google для обчислень нейромереж. Анонсований на I/O у травні 2016 р.; на той момент уже понад рік працював у дата-центрах компанії. Стаття на конференції ISCA 2017 повідомляла про продуктивність у 15–30 разів вищу, ніж у тогочасних CPU та GPU. Джерела: енциклопедичні огляди TPU, що посилаються на Google.

**Суперкомп'ютер Microsoft Azure для OpenAI.** Представлений 19.05.2020: понад 285 000 ядер CPU, 10 000 GPU, 400 Гбіт/с на кожен GPU-сервер. Сем Альтман назвав його «системою мрії» OpenAI. За даними OpenAI, GPT-5 також навчали на суперкомп'ютерах Azure. Джерела: Microsoft Source; OpenAI «Introducing GPT-5».

### 2.2. Люди

| Людина | Роль | Джерело |
|---|---|---|
| Ашиш Васвані, Ноам Шазір (та ще 6 співавторів: Пармар, Ушкорайт, Джонс, Ґомес, Кайзер, Полосухін) | Автори статті про трансформер (2017), на той час працювали в Google Brain / Google Research | arXiv 1706.03762 |
| Сем Альтман | Співголова OpenAI від заснування (2015), згодом CEO. 17.11.2023 був звільнений радою і через кілька днів повернувся | «Introducing OpenAI»; Fortune |
| Ілля Суцкевер | Директор із досліджень, згодом головний науковець OpenAI. Голосував за звільнення Альтмана, а 20.11.2023 публічно пошкодував про це. 14.05.2024 оголосив про відхід з OpenAI; новим головним науковцем став Якуб Пахоцький (Engadget, 15.05.2024; CNBC, 14.05.2024) | «Introducing OpenAI»; TechCrunch; Engadget; CNBC |
| Ґреґ Брокман | Технічний директор OpenAI при заснуванні, потім президент; співавтор статті про Codex. На знак протесту пішов 17.11.2023, повернувся разом з Альтманом | «Introducing OpenAI»; arXiv 2107.03374; Fortune |
| Войцех Заремба | Один із засновників OpenAI (2015); останній автор статті про Codex (2021) | «Introducing OpenAI»; arXiv 2107.03374 |
| Міра Мураті | Технічна директорка OpenAI; тимчасова CEO 17.11.2023. Оголосила про відхід з OpenAI 25.09.2024, після 6,5 року в компанії; того ж дня пішли Боб Макґрю і Баррет Зоф (Axios, Fortune, 25.09.2024) | Fortune; Biography.com; Axios |
| Деміс Хассабіс | Співзасновник DeepMind, з квітня 2023 р. CEO Google DeepMind. Співавтор анонсів Gemini 1.0 і Gemini 3. Нобелівська премія з хімії 2024 р. (разом із Джоном Джампером) | Блог Google; nobelprize.org |
| Сундар Пічаї | CEO Google та Alphabet. Оголосив Bard (2023), об'єднання Brain і DeepMind (2023) і перейменування Bard на Gemini (2024); регулярно повідомляє кількість користувачів Gemini | Блог Google |
| Джефф Дін | Співзасновник Google Brain; з квітня 2023 р. головний науковець Google Research і Google DeepMind | SiliconANGLE; DCD |
| Корай Кавукчуоглу | Технічний директор Google DeepMind і головний архітектор ШІ в Google; співавтор анонсу Gemini 3 (разом із Хассабісом) | Блог Google «Gemini 3» |
| Марк Чен та ін. | Перший автор статті про Codex (2021) | arXiv 2107.03374 |
| Лонг Оуян та ін. | Перший автор статті про InstructGPT (2022) | arXiv 2203.02155 |
| Джозеф Вайценбаум | Автор ELIZA (1964–1966) | Britannica |

> **Примітка про Ноама Шазіра.** У 2021 р. він пішов із Google і разом із Даніелем Де Фрейтасом заснував Character.AI. У серпні 2024 р. повернувся до Google DeepMind за угодою на 2,7 млрд доларів (за Reuters) і став співкерівником Gemini. За повідомленнями Quartz і CNBC (18.06.2026), згодом він перейшов із Google до OpenAI. Отже, його роль у Gemini стосується періоду 2024–2026 рр.

---

## 3. Суперечливі та спірні твердження

1. **«100 млн користувачів ChatGPT за два місяці».**
   - Версія А: близько 100 млн *щомісячних* активних користувачів у січні 2023 р. Це оцінка UBS на основі даних Similarweb, яку 1.02.2023 поширило Reuters. Ще одна оцінка того ж дослідження: 57 млн у грудні 2022 р. (Engadget).
   - Версія Б: перша *офіційна* цифра OpenAI в 100 млн — це *щотижневі* користувачі, і пролунала вона лише 6.11.2023 на DevDay (The Verge).
   - Висновок для курсу: формулювати як «за оцінками аналітиків».

2. **Кількість користувачів у 2026 р.**
   - ChatGPT: 900 млн щотижневих (OpenAI, 27.02.2026) → 1 млрд (серпень 2026) → 1,2 млрд (DevDay, 29.09.2026).
   - Gemini: 750 млн щомісячних (лютий 2026) → 950 млн (липень 2026) → понад 1 млрд (11.08.2026).
   - Метрики різні (щотижневі проти щомісячних), а цифри Google стосуються лише застосунку, без AI Overviews у Пошуку.
   - Дата, коли застосунок ChatGPT досяг 1 млрд щомісячних користувачів, у вторинних джерелах різниться: травень 2026 р. (Sensor Tower, за toolixlab/whizi) або червень 2026 р. (TechCrunch, wisernotify). OpenAI цю метрику офіційно не публікує.

3. **Кількість параметрів GPT-4.** Офіційно не розкрито. Технічний звіт прямо каже, що не містить подробиць про архітектуру, включно з розміром моделі. Цифра «1 трильйон» походить від анонімних джерел Semafor (березень 2023) — це **неофіційна чутка**.

4. **Вартість навчання GPT-4.** Альтман говорив про «понад 100 млн доларів» (за Forbes). Epoch AI оцінює 41–78 млн доларів залежно від методу; Stanford AI Index — близько 78 млн за цінами оренди хмари. Усе це **оцінки**, і рахують їх по-різному.

5. **Коли «помер» Codex-модель.** OpenAI оголосила про це 20.03.2023, а вимкнула 23.03.2023, тобто лише через три дні. Проте сторінка OpenAI Deprecations має ще й другий запис: code-davinci-002 вимкнено 4.01.2024 за повідомленням від 6.07.2023. Крім того, як заміну там тепер вказано gpt-4o, хоча у 2023 р. цієї моделі ще не існувало; тоді рекомендували GPT-3.5-Turbo.

6. **Що вважати «запуском» Codex-агента.** Codex CLI вийшов 16.04.2025, хмарний Codex — 16.05.2025. Медіа й енциклопедії називають датою появи то квітень, то травень 2025 р.

7. **Codex і Copilot.** У статті 2021 р. сказано, що в Copilot працює «окрема виробнича версія Codex», а не та сама модель, що описана в статті. Популярне «Copilot = Codex» — спрощення.

8. **Ціна купівлі DeepMind (2014).** Офіційно не розкрито. Медіа називали «близько 400 млн доларів» (Re/code, Forbes), «понад 500 млн доларів» (The Information, TechCrunch) і «400 млн фунтів» (The Guardian). Частину розбіжностей, ймовірно, спричинила плутанина валют.

9. **Дата заснування OpenAI і хто засновник.** Публічне оголошення датоване 11.12.2015; у Wikipedia зазначено 8.12.2015. В оригінальному дописі Альтман і Маск названі «співголовами», а не засновниками, хоча згодом їх зазвичай називають співзасновниками.

10. **Дата ELIZA.** Britannica в одній статті подає 1964–1966 (період створення), в іншій — 1966 (рік публікації статті). Обидві дати коректні, якщо пояснити різницю.

11. **«Gemini Ultra перевершив людей-експертів на MMLU (90,0%)».** Так стверджує блог Google (6.12.2023). У технічному звіті на arXiv сказано лише про «першу модель, що досягла рівня людини-експерта». Результат 90,0% отримано зі спеціальною методикою CoT@32; за стандартною методикою (5-shot), за вторинними джерелами, — 83,7%, тобто нижче, ніж у GPT-4. Це варто подавати як **маркетингове твердження з застереженням**.

12. **Повернення Альтмана.** Залежно від того, що вважати поверненням, джерела називають 21, 22 або 29 листопада 2023 р.: домовленість у принципі — 21–22.11, формальне відновлення на посаді — 29.11 (Fortune).

13. **Bard: анонс чи запуск.** Анонс і тестування — 6.02.2023, публічний доступ — 21.03.2023.

14. **Дрібні розбіжності в науковій літературі.** У статті про трансформер на NIPS 2017 і в пізнішій версії на arXiv наведено різні показники якості перекладу (BLEU 27,5/41,1 проти 28,4/41,8). OpenAI також згодом виправила розміри малих моделей GPT-2 (117M/345M → 124M/355M); 1,5 млрд для повної моделі залишилося незмінним.

15. **Події 2026 р.** Частина дат 2026 р. (GPT-5.4, GPT-5.6, GPT-6 Astra, Gemini 4 Carbon) взята з якісних компіляцій, що посилаються на офіційні дописи, а не напряму з першоджерел. Офіційна сторінка OpenAI з примітками до релізів блокувала автоматичний доступ. Перед публікацією для підлітків ці дати варто звірити з openai.com і blog.google.

---

## 4. Перелік джерел із посиланнями

### Наукові статті

- Vaswani et al. «Attention Is All You Need» (2017) — https://arxiv.org/abs/1706.03762 · NeurIPS: https://papers.nips.cc/paper/7181-attention-is-all-you-need
- Devlin et al. «BERT» (2018) — https://arxiv.org/abs/1810.04805
- Brown et al. «Language Models are Few-Shot Learners» (GPT-3, 2020) — https://arxiv.org/abs/2005.14165
- Chen et al. «Evaluating Large Language Models Trained on Code» (Codex, 2021) — https://arxiv.org/pdf/2107.03374
- Ouyang et al. «Training language models to follow instructions with human feedback» (InstructGPT, 2022) — https://arxiv.org/pdf/2203.02155 · OpenReview: https://openreview.net/forum?id=TG8KACxEON
- OpenAI «GPT-4 Technical Report» (2023) — https://arxiv.org/pdf/2303.08774v2
- Gemini Team «Gemini: A Family of Highly Capable Multimodal Models» (2023) — https://arxiv.org/abs/2312.11805

### OpenAI

- «Introducing OpenAI» (2015, архівна копія) — https://273ventures.com/pdf/OpenAI_Website_20151211215507.pdf
- «Improving language understanding with unsupervised learning» (GPT-1, 2018) — https://openai.com/index/language-unsupervised/
- «Better language models and their implications» (GPT-2, 2019) — https://openai.com/index/better-language-models/
- «Release Strategies and the Social Impacts of Language Models» (звіт про GPT-2, 2019) — https://cdn.openai.com/GPT_2_August_Report.pdf
- «Introducing Codex» (2025) — https://openai.com/index/introducing-codex/
- «Introducing GPT-5» (2025) — https://openai.com/index/introducing-gpt-5/
- Сторінка «Deprecations» — https://platform.openai.com/docs/deprecations
- «Model Release Notes» — https://help.openai.com/en/articles/9624314-model-release-notes

### Google / Google DeepMind

- «An important next step on our AI journey» (Bard, 2023) — https://blog.google/intl/en-africa/products/explore-get-answers/an-important-next-step-on-our-ai-journey/
- «Introducing Gemini: our largest and most capable AI model» (2023) — https://blog.google/intl/en-mena/company-news/technology/google-gemini-ai/
- «Bard is now Gemini» (2024) — https://blog.google/products-and-platforms/products/gemini/bard-gemini-advanced-app/
- Пічаї про Ultra 1.0 і Gemini Advanced (2024) — https://blog.google/innovation-and-ai/technology/ai/google-gemini-update-sundar-pichai-2024/
- «A new era of intelligence with Gemini 3» (2025) — https://blog.google/intl/en-mena/product-updates/explore-get-answers/gemini-3-launches-in-mena/
- «Gemini 4 Argon: our next era of frontier intelligence» (2026) — https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/
- «Gemini 4 Argon is now available in the Gemini app» (2026) — https://blog.google/innovation-and-ai/products/gemini-app/gemini-4-argon-availability/
- «Gemini 4 Argon is now available for developers» (2026) — https://blog.google/innovation-and-ai/technology/developers-tools/build-with-gemini-4-argon/
- Виступ Пічаї за результатами Alphabet Q2 2026 — https://blog.google/company-news/inside-google/message-ceo/alphabet-earnings-q2-2026/

### Енциклопедії та інші офіційні джерела

- Britannica «ELIZA» — https://www.britannica.com/technology/Eliza
- Britannica «Joseph Weizenbaum» — https://www.britannica.com/biography/Joseph-Weizenbaum
- Microsoft Source про суперкомп'ютер для OpenAI (2020) — https://news.microsoft.com/source/features/ai/openai-azure-supercomputer/
- Нобелівська премія з хімії 2024 (прес-реліз) — https://www.nobelprize.org/prizes/chemistry/2024/press-release/

### Технічні медіа

- TechCrunch: купівля DeepMind (2014) — https://techcrunch.com/2014/01/26/google-deepmind
- Engadget: суперкомп'ютер Azure (2020) — https://www.engadget.com/microsoft-openai-supercomputer-azure-150001119.html
- Engadget: 100 млн користувачів ChatGPT (2023) — https://www.engadget.com/chatgpt-100-million-users-january-130619073.html
- SiliconANGLE: об'єднання DeepMind і Google Brain (2023) — https://siliconangle.com/2023/04/20/google-merges-deepmind-google-brain-ai-research-groups/
- The Register: об'єднання DeepMind і Google Brain (2023) — https://www.theregister.com/2023/04/20/google_brain_deep_mind/
- Fortune: повернення Альтмана (2023) — https://fortune.com/2023/11/29/sam-altman-officially-reinstated-openai-ceo-board-bret-taylor
- Forbes: вартість навчання моделей (2024) — https://www.forbes.com/sites/katharinabuchholz/2024/08/23/the-extreme-cost-of-training-ai-models/
- TechCrunch: Gemini — 750 млн користувачів (2026) — https://techcrunch.com/2026/02/04/googles-gemini-app-has-surpassed-750m-monthly-active-users/
- TechCrunch: Gemini — 1 млрд користувачів (2026) — https://techcrunch.com/2026/08/11/googles-gemini-app-surges-to-one-billion-users/

### Компіляції та вторинні довідники (для звірки, не як першоджерело)

- Хронологія моделей OpenAI (hidekazu-konishi.com) — https://hidekazu-konishi.com/entry/openai_gpt_model_release_timeline.html
- Хронологія моделей Gemini (hidekazu-konishi.com) — https://hidekazu-konishi.com/entry/google_gemini_model_release_timeline.html
- Wikipedia «Removal of Sam Altman from OpenAI» — https://en.wikipedia.org/wiki/Removal_of_Sam_Altman_from_OpenAI
- Wikipedia «OpenAI Codex» — https://en.wikipedia.org/wiki/OpenAI_Codex

### Згадані у звіті, але без перевіреного посилання

Ці дописи названо у хронології, проте пряме посилання на них у ході дослідження не збиралося. Їх варто знайти й додати перед публікацією: OpenAI «OpenAI API» (2020), «Introducing ChatGPT» (2022), «Hello GPT-4o» (2024), «Introducing o3 and o4-mini» (2025); Google «LaMDA: our breakthrough conversation technology» (2021), «Try Bard» (2023), «Introducing PaLM 2» (2023), блог Google Research про PaLM (2022); GitHub Blog «Introducing GitHub Copilot» (2021) і «GitHub Copilot is generally available» (2022).

---

## 5. Як можна поділити матеріал на 5 коротких статей для підлітків

1. **«Від ELIZA до трансформера»** — як комп'ютери вчилися говорити і чому стаття 2017 р. «Увага — це все, що потрібно» змінила все.
2. **«Як народився ChatGPT»** — GPT-1→3, навчання на людських оцінках і запуск 30 листопада 2022 р., що за 2 місяці (за оцінками аналітиків) зібрав 100 млн людей.
3. **«Дві історії Codex»** — модель, що підказувала код у Copilot (2021–2023), і новий агент-програміст (з 2025 р.): чому одна назва — це два різні продукти.
4. **«Відповідь Google: від Bard до Gemini»** — DeepMind, TPU, LaMDA і PaLM, об'єднання лабораторій 2023 р., Gemini і Нобелівська премія Хассабіса.
5. **«Гонка триває: 2024–2026 і як перевіряти цифри»** — GPT-4o→GPT-6, Gemini 1.5→4, мільярд користувачів і чому важливо розрізняти офіційні дані, оцінки та чутки.
