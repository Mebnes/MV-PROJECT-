<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="MV.PROJECT — официальные правила сервера Medium RP (SCP:SL). Версия 2.7">
<meta name="theme-color" content="#8b0000">
<title>MV.PROJECT — Правила Medium RP</title>
<style>
  /* СБРОС И БАЗОВЫЕ СТИЛИ */
  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Segoe UI', Tahoma, sans-serif;
    background: #0d0d0d;
    color: #d8d8d8;
    line-height: 1.7;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ЗАГОЛОВОК И ПОИСК (ПРАВЫЙ ВЕРХНИЙ УГОЛ) */
  .sticky-header {
    position: sticky;
    top: 0;
    background: #0d0d0d;
    z-index: 100;
    padding: 20px 30px;
    border-bottom: 2px solid #8b0000;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.5);
  }

  .header-text h1 {
    font-size: 1.8em;
    color: #ff2e2e;
    letter-spacing: 2px;
    text-transform: uppercase;
    text-shadow: 0 0 15px rgba(255,46,46,0.6);
    line-height: 1.2;
  }

  .header-text p {
    color: #888;
    margin-top: 5px;
    font-size: 0.85em;
    letter-spacing: 1px;
  }

  .version {
    display: inline-block;
    margin-top: 8px;
    padding: 3px 12px;
    background: #8b0000;
    color: #fff;
    border-radius: 20px;
    font-size: 0.75em;
    letter-spacing: 1px;
  }

  /* ПОИСК */
  .search-box {
    width: 320px;
    flex-shrink: 0;
    background: #1a1a1a;
    border: 1px solid #2a2a2a;
    border-radius: 8px;
    padding: 12px 15px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.4);
  }

  .search-box label {
    display: block;
    color: #ff2e2e;
    font-size: 0.75em;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: 6px;
    font-weight: 600;
  }

  .search-box input {
    width: 100%;
    padding: 10px 12px;
    background: #0d0d0d;
    border: 1px solid #333;
    border-radius: 6px;
    color: #e0e0e0;
    font-size: 0.9em;
    outline: none;
    transition: border-color 0.2s;
  }

  .search-box input:focus {
    border-color: #ff2e2e;
    box-shadow: 0 0 10px rgba(255,46,46,0.3);
  }

  .search-box .hint {
    color: #666;
    font-size: 0.7em;
    margin-top: 6px;
  }

  /* ОСНОВНОЙ КОНТЕНТ */
  .main-content {
    padding: 30px 40px;
    width: 100%;
    max-width: 100%;
    animation: fadeIn 0.3s ease-in;
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* НАВИГАЦИЯ (ВЕРХНЯЯ) */
  nav {
    background: #1a1a1a;
    border: 1px solid #2a2a2a;
    border-radius: 8px;
    padding: 20px;
    margin-bottom: 35px;
  }

  nav h3 {
    color: #ff2e2e;
    margin-bottom: 12px;
    font-size: 1em;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  nav ul {
    list-style: none;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 8px;
  }

  nav a {
    color: #b0b0b0;
    text-decoration: none;
    font-size: 0.9em;
    transition: 0.2s;
    display: block;
    padding: 5px 10px;
    border-left: 3px solid transparent;
  }

  nav a:hover {
    color: #ff2e2e;
    border-left: 3px solid #ff2e2e;
    background: #1f1f1f;
  }

  /* ДИСКЛЕЙМЕР */
  .disclaimer {
    background: #2a1010;
    border: 1px solid #8b0000;
    border-left: 5px solid #ff2e2e;
    padding: 16px 22px;
    margin-bottom: 30px;
    border-radius: 8px;
    color: #f0d0d0;
    font-size: 0.95em;
    box-shadow: 0 2px 8px rgba(139,0,0,0.3);
  }

  .disclaimer strong { color: #ff5555; }

  /* БЛОКИ КОДЕКСА */
  .codex {
    background: linear-gradient(135deg, #1a1a1a, #1f1f1f);
    border: 2px solid #ff2e2e;
    border-radius: 10px;
    padding: 25px 30px;
    margin-bottom: 35px;
    text-align: center;
  }

  .codex h2 {
    color: #ff2e2e;
    font-size: 1.4em;
    margin-bottom: 15px;
    text-transform: uppercase;
    letter-spacing: 2px;
    border: none;
    padding: 0;
  }

  .codex p {
    color: #c0c0c0;
    font-size: 0.95em;
    margin-bottom: 10px;
  }

  .codex .quote {
    color: #ffb400;
    font-style: italic;
    margin-top: 15px;
    font-size: 0.9em;
  }

  section {
    margin-bottom: 45px;
    padding-bottom: 25px;
    border-bottom: 1px solid #222;
    scroll-margin-top: 100px;
  }

  section:last-child { border-bottom: none; }

  h2 {
    color: #ff2e2e;
    font-size: 1.6em;
    margin-bottom: 18px;
    padding-left: 15px;
    border-left: 5px solid #8b0000;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  h3 {
    color: #ffb400;
    font-size: 1.15em;
    margin: 22px 0 12px;
    letter-spacing: 0.5px;
  }

  h4 {
    color: #e0e0e0;
    font-size: 1em;
    margin: 16px 0 8px;
  }

  p { margin-bottom: 10px; }

  ul, ol { margin: 10px 0 15px 25px; }

  li { margin-bottom: 7px; }

  /* БЛОКИ ПРАВИЛ */
  .rule, .warning, .info, .ok, .mtf-card, .protocol-card, .codex, .search-box, .disclaimer, .classic-protocol {
    height: auto !important;
    min-height: fit-content;
    overflow: visible;
    word-wrap: break-word;
    overflow-wrap: break-word;
  }

  .rule {
    display: block;
    width: 100%;
    background: #202020;
    border: 1px solid #2e2e2e;
    border-left: 5px solid #ff2e2e;
    padding: 14px 20px;
    margin: 12px 0;
    border-radius: 6px;
    color: #ffffff;
    font-size: 0.95em;
    line-height: 1.7;
    box-shadow: 0 3px 10px rgba(0,0,0,0.6);
    transition: background 0.2s, border-left-color 0.2s;
  }

  .rule:hover {
    background: #262626;
    border-left-color: #ff5555;
  }

  .rule strong {
    color: #ff2e2e;
    font-weight: 700;
    margin-right: 6px;
  }

  .warning {
    background: #2a1010;
    border: 1px solid #8b0000;
    border-left: 5px solid #ff2e2e;
    padding: 16px 22px;
    margin: 18px 0;
    border-radius: 8px;
    color: #f0d0d0;
    box-shadow: 0 2px 8px rgba(139,0,0,0.3);
  }

  .warning strong { color: #ff5555; }

  .info {
    background: #101a26;
    border: 1px solid #1e3a5f;
    border-left: 5px solid #3a8bff;
    padding: 16px 22px;
    margin: 18px 0;
    border-radius: 8px;
    color: #d0e0f0;
    box-shadow: 0 2px 8px rgba(58,139,255,0.15);
  }

  .info strong { color: #3a8bff; }

  .ok {
    background: #102010;
    border: 1px solid #1e5f1e;
    border-left: 5px solid #3aff3a;
    padding: 16px 22px;
    margin: 18px 0;
    border-radius: 8px;
    color: #d0f0d0;
    box-shadow: 0 2px 8px rgba(58,255,58,0.15);
  }

  .ok strong { color: #3aff3a; }

  .warning ul { margin-top: 10px; margin-bottom: 0; }

  /* ТАБЛИЦЫ */
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 18px 0;
    background: #1a1a1a;
    border-radius: 8px;
    overflow: hidden;
    border: 1px solid #2a2a2a;
    box-shadow: 0 2px 10px rgba(0,0,0,0.5);
  }

  th {
    background: #8b0000;
    color: #ffffff;
    padding: 14px 16px;
    text-align: left;
    font-size: 0.9em;
    text-transform: uppercase;
    letter-spacing: 1px;
    font-weight: 700;
    border-bottom: 2px solid #ff2e2e;
  }

  td {
    padding: 12px 16px;
    border-bottom: 1px solid #252525;
    font-size: 0.95em;
    color: #e0e0e0;
    background: #1a1a1a;
  }

  tr:last-child td { border-bottom: none; }
  tr:nth-child(even) td { background: #1e1e1e; }
  tr:hover td { background: #262626; color: #ffffff; }

  footer {
    text-align: center;
    margin-top: 40px;
    padding-top: 25px;
    border-top: 2px solid #8b0000;
    color: #666;
    font-size: 0.85em;
    padding-bottom: 20px;
  }

  footer strong { color: #ff2e2e; }

  /* БЕЙДЖИ */
  .badge {
    display: inline-block;
    padding: 3px 12px;
    border-radius: 4px;
    font-size: 0.75em;
    font-weight: bold;
    letter-spacing: 0.5px;
    margin-left: 8px;
    vertical-align: middle;
  }

  .badge-scp { background: #8b0000; color: #fff; }
  .badge-mtf { background: #1e3a5f; color: #fff; }
  .badge-ci { background: #3a5f1e; color: #fff; }
  .badge-dclass { background: #5f3a1e; color: #fff; }
  .badge-sci { background: #5f1e5f; color: #fff; }
  .badge-staff { background: #ffb400; color: #000; }

  /* РАСКРЫВАЮЩИЕСЯ БЛОКИ */
  details.mtf-card,
  details.protocol-card {
    background: #141a24;
    border: 1px solid #1e3a5f;
    border-left: 5px solid #3a8bff;
    border-radius: 8px;
    padding: 0;
    margin: 12px 0;
    box-shadow: 0 2px 8px rgba(0,0,0,0.4);
    overflow: hidden;
  }

  details.mtf-card summary,
  details.protocol-card summary {
    padding: 14px 20px;
    cursor: pointer;
    font-weight: 600;
    color: #7fbfff;
    list-style: none;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #141a24;
    border-bottom: 1px solid transparent;
    transition: background 0.2s;
  }

  details.mtf-card summary::-webkit-details-marker,
  details.protocol-card summary::-webkit-details-marker {
    display: none;
  }

  details.mtf-card summary::after,
  details.protocol-card summary::after {
    content: "▼";
    font-size: 0.8em;
    color: #3a8bff;
    transition: transform 0.2s;
  }

  details[open].mtf-card summary::after,
  details[open].protocol-card summary::after {
    transform: rotate(180deg);
  }

  details.mtf-card[open] summary,
  details.protocol-card[open] summary {
    border-bottom: 1px solid #1e3a5f;
  }

  details.mtf-card .content,
  details.protocol-card .content {
    padding: 16px 20px;
  }

  .mtf-card h4 {
    color: #7fbfff;
    margin-top: 0;
    margin-bottom: 8px;
    font-size: 1.05em;
  }

  .mtf-card .role {
    color: #ffb400;
    font-size: 0.85em;
    font-style: italic;
    margin-bottom: 8px;
    display: block;
  }

  .mtf-card p {
    color: #d0d8e0;
    font-size: 0.92em;
    margin-bottom: 6px;
  }

  /* ЦВЕТНЫЕ БЕЙДЖИ КОДОВ */
  .code-badge {
    display: inline-block;
    padding: 3px 10px;
    border-radius: 4px;
    font-size: 0.8em;
    font-weight: bold;
    margin-right: 8px;
  }

  .code-green { background: #1e5f1e; color: #90ff90; }
  .code-yellow { background: #5f5f1e; color: #ffff90; }
  .code-orange { background: #5f3a1e; color: #ffb070; }
  .code-red { background: #5f1e1e; color: #ff8080; }
  .code-black { background: #0a0a0a; color: #cccccc; border: 1px solid #444; }
  .code-gray { background: #3a3a3a; color: #d0d0d0; }
  .code-blue { background: #1e3a5f; color: #90c0ff; }
  .code-white { background: #d0d0d0; color: #000; }
  .code-purple { background: #5f1e5f; color: #e090ff; }

  /* КЛАССИКА (ПРОТОКОЛ) */
  .classic-protocol {
    background: #1a1a1a;
    border: 1px solid #2a2a2a;
    border-top: 4px solid #ff2e2e;
    border-radius: 8px;
    padding: 20px 25px;
    margin: 20px 0;
    box-shadow: 0 4px 12px rgba(0,0,0,0.5);
  }

  .classic-protocol h3 {
    color: #ff2e2e;
    font-size: 1.2em;
    margin-bottom: 12px;
    padding-bottom: 8px;
    border-bottom: 1px solid #2a2a2a;
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .classic-protocol p {
    color: #c0c0c0;
    margin-bottom: 15px;
    font-size: 0.95em;
  }

  .classic-protocol ul {
    list-style: none;
    margin-left: 0;
  }

  .classic-protocol > ul > li {
    margin-bottom: 12px;
  }

  .classic-protocol > ul > li > strong {
    color: #ffb400;
    display: block;
    margin-bottom: 6px;
    font-size: 1em;
  }

  .classic-protocol ul ul {
    margin-top: 6px;
    margin-left: 20px;
    list-style-type: disc;
  }

  .classic-protocol ul ul li {
    color: #b0b0b0;
    font-size: 0.92em;
    margin-bottom: 6px;
  }

  .classic-protocol ul ul li::marker {
    color: #ff2e2e;
  }

  /* АДАПТИВНОСТЬ */
  @media (max-width: 1024px) {
    .sticky-header {
      flex-direction: column;
      align-items: flex-start;
    }
    .search-box { width: 100%; }
  }

  @media (max-width: 700px) {
    .main-content { padding: 15px 10px; }
    .header-text h1 { font-size: 1.4em; letter-spacing: 1px; }
    h2 { font-size: 1.2em; }
    h3 { font-size: 1em; }
    th, td { padding: 8px 10px; font-size: 0.85em; }
    nav ul { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<!-- ЗАГОЛОВОК И ПОИСК -->
<header class="sticky-header">
  <div class="header-text">
    <h1>MV.PROJECT</h1>
    <p>MEDIUM ROLEPLAY — ОФИЦИАЛЬНЫЕ ПРАВИЛА СЕРВЕРА • Комплекс Зона 02</p>
    <span class="version">Версия 2.7 • Расширенный раздел МОГ, коды и протоколы</span>
  </div>
  <div class="search-box">
    <label for="searchInput">🔍 Поиск по правилам</label>
    <input type="text" id="searchInput" placeholder="Введите слово или фразу..." autocomplete="off">
    <div class="hint">Начните вводить текст — разделы, не содержащие совпадений, будут скрыты.</div>
  </div>
</header>

<!-- ОСНОВНОЙ КОНТЕНТ -->
<main class="main-content">

  <!-- НАВИГАЦИЯ (ВЕРХНЯЯ) -->
  <nav>
    <h3>Навигация по разделам</h3>
    <ul>
      <li><a href="#general">1. Общие положения</a></li>
      <li><a href="#rp">2. Основы RolePlay</a></li>
      <li><a href="#fearrp">3. FearRP и PowerRP</a></li>
      <li><a href="#meta">4. MetaGaming и PowerGaming</a></li>
      <li><a href="#combat">5. Боевые правила</a></li>
      <li><a href="#scp">6. Правила за SCP</a></li>
      <li><a href="#mtf">7. Правила за МОГ</a></li>
      <li><a href="#ci">8. Правила за ПХ</a></li>
      <li><a href="#dclass">9. Правила за Д-класс</a></li>
      <li><a href="#sci">10. Правила за учёных</a></li>
      <li><a href="#staff">11. Правила для стаффа</a></li>
      <li><a href="#donate">12. Донат и поддержка</a></li>
      <li><a href="#punish">13. Система наказаний</a></li>
      <li><a href="#voice">14. Голосовой чат</a></li>
      <li><a href="#discord">15. Discord-правила</a></li>
      <li><a href="#final">16. Заключительные положения</a></li>
    </ul>
  </nav>

  <div class="disclaimer">
    <strong>ВНИМАНИЕ:</strong> Проект MV.PROJECT имеет собственный лор и не относится к официальному SCP Foundation. Все события, объекты и персонажи являются вымышленными и созданы исключительно для игровых целей в рамках ролевого сервера.
  </div>

  <div class="codex">
    <h2>Кодекс игрока</h2>
    <p>Добро пожаловать в <strong>руководство сервера MV.PROJECT</strong>, содержащее основные правила Medium RP, а также необходимые рекомендации для начала игры.</p>
    <p>Присоединяясь к серверу, вы соглашаетесь с данным руководством.</p>
    <p>Незначительно отклоняться от правил допустимо, если это не вредит другим игрокам и RP.</p>
    <p>Не мешайте работе состава проекта, а также игровому опыту других игроков.</p>
    <p class="quote">«Действуй логично и не мешай другим игрокам — так ты автоматически соблюдаешь 80% правил.»</p>
  </div>

  <section id="general">
    <h2>1. Общие положения</h2>
    <p>Настоящие правила действуют на всех серверах проекта <strong>MV.PROJECT</strong> и в связанных с ним сообществах (Discord, VK, Telegram).</p>
    <div class="rule"><strong>1.1.</strong> Незнание правил не освобождает от ответственности. Каждый игрок обязан ознакомиться с ними перед входом на сервер.</div>
    <div class="rule"><strong>1.2.</strong> Администрация вправе изменять правила без предварительного уведомления. Актуальная версия всегда закреплена в Discord.</div>
    <div class="rule"><strong>1.3.</strong> Решения администрации обязательны к исполнению. Оспаривание происходит только через апелляцию в Discord.</div>
    <div class="rule"><strong>1.4.</strong> Регистрируясь на сервере, вы автоматически соглашаетесь с данными правилами.</div>
    <div class="rule"><strong>1.5.</strong> Возрастное ограничение: <strong>13+</strong>. Игроки младше могут быть удалены без объяснения причин.</div>
    <div class="warning"><strong>ВАЖНО:</strong> Незнание правил, «я новенький», «я не читал» — не являются оправданием. Наказание выносится по факту нарушения.</div>
  </section>

  <section id="rp">
    <h2>2. Основы RolePlay</h2>
    <p>Medium RP — это баланс между серьёзной игрой и свободой действий. Вы играете роль, а не себя.</p>

    <h3>2.1. Обязательные элементы RP</h3>
    <ul>
      <li>Отыгрыш персонажа в рамках его роли (учёный, Д-класс, МОГ, ПХ, SCP).</li>
      <li>Использование RP-имён вместо ников Steam.</li>
      <li>Реакция на события в мире: сирены, выстрелы, трупы, SCP.</li>
      <li>Соблюдение иерархии: приказы старших по званию обязательны.</li>
    </ul>

    <h3>2.2. Что запрещено</h3>
    <div class="rule"><strong>2.2.1.</strong> Выход из роли (Break Character) без крайней необходимости.</div>
    <div class="rule"><strong>2.2.2.</strong> Использование OOC-информации в IC-целях.</div>
    <div class="rule"><strong>2.2.3.</strong> Намеренное разрушение атмосферы: крики в микрофон, музыка, спам.</div>
    <div class="rule"><strong>2.2.4.</strong> Игра за роль, которая вам не выдана (самопровозглашение командира МОГ и т.д.).</div>
    <div class="rule"><strong>2.2.5.</strong> Отказ от RP без веской причины.</div>

    <h3>2.3. RP-имена</h3>
    <table>
      <tr><th>Роль</th><th>Формат имени</th><th>Пример</th></tr>
      <tr><td>Д-класс</td><td>Д-XXXX</td><td>Д-7341</td></tr>
      <tr><td>Учёный</td><td>Имя Фамилия</td><td>Алексей Волков</td></tr>
      <tr><td>МОГ</td><td>Звание Фамилия</td><td>Сержант Кравцов</td></tr>
      <tr><td>ПХ</td><td>Позывной</td><td>Гроза-1</td></tr>
      <tr><td>SCP</td><td>SCP-XXX</td><td>SCP-173</td></tr>
    </table>
    <div class="warning"><strong>ЗАПРЕЩЕНО:</strong> имена с оскорблениями, политикой, рекламой, цифрами вместо имени (кроме Д-класса), копирование имён известных личностей.</div>
  </section>

  <section id="fearrp">
    <h2>3. FearRP и PowerRP</h2>

    <h3>3.1. FearRP — страх за жизнь</h3>
    <p>Ваш персонаж боится смерти. Если на вас наставили оружие — вы подчиняетесь.</p>
    <ul>
      <li>При угрозе оружием в упор — выполнять требования.</li>
      <li>Не бежать от вооружённого противника без укрытия.</li>
      <li>Не атаковать, если у вас нет шанса выжить.</li>
      <li>При ранении — отыгрывать боль, хромать, просить помощи.</li>
    </ul>
    <div class="rule"><strong>3.1.1.</strong> Нарушение FearRP = наказание от 60 минут до 1 дня мута.</div>

    <h3>3.2. PowerRP — навязывание действий</h3>
    <p>Запрещено навязывать другому игроку действия, которые он не может отменить.</p>
    <div class="rule"><strong>3.2.1.</strong> «Я тебя обезоружил» без отыгрыша голосом и без согласия — PowerRP.</div>
    <div class="rule"><strong>3.2.2.</strong> «Я тебя убил» без фактического убийства в игре — PowerRP.</div>
    <div class="rule"><strong>3.2.3.</strong> Навязывание романтических, интимных или унизительных сцен — бан от 7 дней.</div>
    <div class="info"><strong>СОВЕТ:</strong> Отыгрывайте действия <strong>голосом</strong> — например: <em>«Надеваю наручники на Д-класса перед собой»</em>, <em>«Достаю пистолет и направляю на учёного»</em>. Просто озвучивайте, что делает ваш персонаж, и ждите реакции другого игрока.</div>
  </section>

  <section id="meta">
    <h2>4. MetaGaming и PowerGaming</h2>

    <h3>4.1. MetaGaming</h3>
    <p>Использование информации, которую ваш персонаж не мог получить в игре.</p>
    <ul>
      <li>Discord, стрим, голосовой чат вне игры — не источник IC-информации.</li>
      <li>Если вы умерли — вы не знаете, что произошло после.</li>
      <li>Нельзя сообщать союзникам координаты врага, увиденные в спектаторе.</li>
    </ul>
    <div class="rule"><strong>4.1.1.</strong> MetaGaming = мут 120 минут + предупреждение.</div>

    <h3>4.2. PowerGaming</h3>
    <p>Использование игровых механик для получения преимущества, которое невозможно в реальной жизни.</p>
    <ul>
      <li>Прыжки через заборы в бою без причины.</li>
      <li>Стрельба с двух рук одновременно.</li>
      <li>Использование багов карты.</li>
      <li>Мгновенное перезаряжание через эксплойт.</li>
    </ul>
    <div class="rule"><strong>4.2.1.</strong> PowerGaming = кик, при повторе — бан 1 день.</div>
  </section>

  <section id="combat">
    <h2>5. Боевые правила</h2>

    <h3>5.1. Общие боевые правила</h3>
    <ul>
      <li>KOS (Kill on Sight) запрещён вне зон конфликта.</li>
      <li>TeamKill (убийство союзника) — бан от 1 дня.</li>
      <li>Стрельба без предупреждения запрещена, кроме самообороны.</li>
      <li>Добивание раненых без RP-причины — нарушение.</li>
    </ul>

    <h3>5.2. Зоны конфликта</h3>
    <table>
      <tr><th>Зона</th><th>Правила</th></tr>
      <tr><td>КПП</td><td>Стрельба разрешена при нарушении периметра</td></tr>
      <tr><td>Зона-914</td><td>Бой разрешён только при конфликте за SCP</td></tr>
      <tr><td>Тяжёлая зона</td><td>Свободный бой между фракциями</td></tr>
      <tr><td>Лёгкая зона</td><td>Бой только при объявленной тревоге</td></tr>
      <tr><td>Выход</td><td>Бой разрешён всем фракциям</td></tr>
    </table>

    <h3>5.3. Запрещено в бою</h3>
    <div class="rule"><strong>5.3.1.</strong> Стрельба по своим без причины (TK).</div>
    <div class="rule"><strong>5.3.2.</strong> Использование читов, макросов, аимбота — перманентный бан.</div>
    <div class="rule"><strong>5.3.3.</strong> Кемпинг на респавне врага.</div>
    <div class="rule"><strong>5.3.4.</strong> Убийство сдавшихся без RP-причины.</div>
    <div class="rule"><strong>5.3.5.</strong> Стрельба через стены и текстуры.</div>
  </section>

  <section id="scp">
    <h2>6. Правила за SCP <span class="badge badge-scp">SCP</span></h2>

    <h3>6.1. Общие правила для всех SCP</h3>
    <ul>
      <li>SCP обязаны отыгрывать свою природу: агрессию, страх, голод.</li>
      <li>SCP не обязаны подчиняться людям, кроме SCP-049 и подобных разумных.</li>
      <li>SCP не могут использовать голосовой чат, кроме разумных SCP (049, 035).</li>
      <li>SCP не могут объединяться с людьми против других SCP без RP-причины.</li>
    </ul>

    <h3>6.2. Индивидуальные правила</h3>

    <h4>SCP-173 «Статуя»</h4>
    <ul>
      <li>Двигается только когда на него не смотрят.</li>
      <li>Не может открывать двери (кроме лифтов).</li>
      <li>Запрещено моргать в игре для обхода механики.</li>
    </ul>

    <h4>SCP-096 «Застенчивый»</h4>
    <ul>
      <li>Атакует только того, кто видел его лицо.</li>
      <li>Не может атаковать, если никто не смотрит.</li>
      <li>Запрещено намеренно показывать лицо через баги.</li>
    </ul>

    <h4>SCP-049 «Чумной Доктор»</h4>
    <ul>
      <li>Может говорить, но только по RP-теме «исцеления».</li>
      <li>Не может атаковать без попытки «исцелить».</li>
      <li>Созданные зомби подчиняются 049.</li>
    </ul>

    <h4>SCP-106 «Старик»</h4>
    <ul>
      <li>Может проходить сквозь стены, уходя в «карманное измерение».</li>
      <li>Не может кемпить у выхода из карманного измерения.</li>
      <li>Запрещено убивать сразу после выхода из стены.</li>
      <li><strong>Может убивать любых игроков</strong> — в рамках RP-логики своего персонажа.</li>
      <li><strong>Главная цель — сбежать, а не устроить резню.</strong></li>
      <li>Правило «Страх за свою жизнь» на него не распространяется — SCP-106 не боится смерти.</li>
    </ul>

    <h4>SCP-035 «Маска»</h4>
    <ul>
      <li>Может говорить и убеждать.</li>
      <li>Запрещено использовать маску для метагейма.</li>
      <li>Без носителя не может атаковать физически.</li>
    </ul>

    <h4>SCP-939 «Собаки»</h4>
    <ul>
      <li>Могут имитировать голоса людей.</li>
      <li>Не могут говорить осмысленно.</li>
      <li>Запрещено использовать голосовой чат для обмана вне RP.</li>
    </ul>

    <h3>6.3. Запрещено всем SCP</h3>
    <div class="rule"><strong>6.3.1.</strong> TeamKill между SCP.</div>
    <div class="rule"><strong>6.3.2.</strong> Кемпинг у выхода/респавна людей.</div>
    <div class="rule"><strong>6.3.3.</strong> Игнорирование своей роли.</div>
    <div class="rule"><strong>6.3.4.</strong> Использование багов карты для преимущества.</div>
  </section>

  <!-- РАСШИРЕННЫЙ РАЗДЕЛ МОГ -->
  <section id="mtf">
    <h2>7. Правила за МОГ <span class="badge badge-mtf">MTF</span></h2>

    <h3>7.1. Общие правила</h3>
    <ul>
      <li>МОГ выполняют <strong>строго свою задачу</strong>, поставленную командиром.</li>
      <li>Приоритеты определяет командир — его приказы обязательны.</li>
      <li>У каждой группы свои задачи (штурм, охрана, эвакуация).</li>
      <li>После выполнения всех задач имеют право эвакуировать персонал.</li>
      <li>При коде «Серый» имеют право арестовать весь персонал (кроме руководящего состава).</li>
      <li>МОГ обязаны защищать персонал и обеспечивать сдерживание SCP.</li>
      <li>МОГ не могут убивать Д-класса без приказа или угрозы.</li>
    </ul>

    <h3>7.2. Иерархия</h3>
    <table>
      <tr><th>Звание</th><th>Права</th></tr>
      <tr><td>Рядовой</td><td>Выполняет приказы</td></tr>
      <tr><td>Сержант</td><td>Командует отрядом до 4 человек</td></tr>
      <tr><td>Лейтенант</td><td>Командует взводом</td></tr>
      <tr><td>Капитан</td><td>Командует операцией</td></tr>
      <tr><td>Командир</td><td>Полный контроль над МОГ</td></tr>
    </table>

    <!-- БЛОК КЛАССИКА -->
    <div class="classic-protocol">
      <h3>7.2.1 | Классика</h3>
      <p>Протокол, объявляемый в случае массового нарушения условий контракта персоналом класса D.</p>
      <ul>
        <li>
          <strong>Основания для активации:</strong>
          <ul>
            <li>Подтверждено, что один или несколько представителей D-Класса вооружены и проявляют агрессию к сотрудникам Фонда.</li>
            <li>D-Класс сотрудничает с враждебными структурами, препятствует операциям Фонда или угрожает интересам организации.</li>
            <li>D-Класс получил доступ к информации выше его уровня допуска (2+).</li>
            <li>Зафиксировано массовое использование SCP-Объектов персоналом класса D.</li>
            <li>Контроль над D-Классом утерян.</li>
          </ul>
        </li>
        <li>
          <strong>Последствия:</strong>
          <ul>
            <li>Все военизированные единицы комплекса получают полномочия на ликвидацию всего несвязанного персонала класса D и/или D-Класса без сопровождения сотрудников Фонда, без предупреждения.</li>
          </ul>
        </li>
      </ul>
    </div>

    <h3>7.3. Коды тревоги C.A.S.S.I.E.</h3>
    <p>Коды объявляются через C.A.S.S.I.E. и определяют режим работы всего комплекса.</p>
    <table>
      <tr><th>Код</th><th>Название</th><th>Описание</th></tr>
      <tr><td><span class="code-badge code-green">🟢</span> Код Зелёный</td><td>Норма</td><td>Комплекс работает в штатном режиме. Все SCP в камерах.</td></tr>
      <tr><td><span class="code-badge code-yellow">🟡</span> Код Жёлтый</td><td>Повышенная готовность</td><td>Обнаружены подозрительные лица или мелкие нарушения. МОГ патрулирует.</td></tr>
      <tr><td><span class="code-badge code-orange">🟠</span> Код Оранжевый</td><td>Угроза SCP</td><td>Один или несколько SCP сбежали. Начинается операция по сдерживанию.</td></tr>
      <tr><td><span class="code-badge code-red">🔴</span> Код Красный</td><td>Критическая угроза</td><td>Массовый побег SCP. Эвакуация персонала. Все МОГ мобилизованы.</td></tr>
      <tr><td><span class="code-badge code-gray">⬛</span> Код Серый</td><td>Внутренняя угроза</td><td>Бунт, саботаж, предательство. Арест всего персонала ниже руководящего состава.</td></tr>
      <tr><td><span class="code-badge code-black">⬛</span> Код Чёрный</td><td>Полная изоляция</td><td>Утечка класса Кетер. Комплекс изолирован. Внешние МОГ не входят.</td></tr>
      <tr><td><span class="code-badge code-blue">🔵</span> Код Синий</td><td>Аномалия в C.A.S.S.I.E.</td><td>Сбои в системе оповещения. Возможен взлом. Действовать по протоколу.</td></tr>
      <tr><td><span class="code-badge code-white">⚪</span> Код Белый</td><td>Учения</td><td>Тренировочная тревога. Реальные угрозы отсутствуют.</td></tr>
      <tr><td><span class="code-badge code-purple">🟣</span> Код Пурпурный</td><td>Пространственная аномалия</td><td>Обнаружена пространственная аномалия. Активирован протокол изоляции.</td></tr>
      <tr><td><span class="code-badge code-blue">💧</span> Код Чистый</td><td>Блокировка</td><td>Комплекс введён в режим блокировки «Чистый». Внеплановая проверка безопасности.</td></tr>
      <tr><td><span class="code-badge code-black">🌀</span> Код Супер-Чистый</td><td>Неизвестность</td><td>Объявлен код «Супер-Чистый». Оно уже здесь. Не смотрите.</td></tr>
      <tr><td><span class="code-badge code-red">🩸</span> Код Алый</td><td>Конец света класса DK</td><td>Объявлен КОД АЛЫЙ. Конец света класса «DK». Не покидайте крыло «ПАУК».</td></tr>
      <tr><td><span class="code-badge code-black">❄️</span> Хладное серебро</td><td>Совершенно секретно</td><td>Протокол «Хладное серебро». Информация засекречена.</td></tr>
    </table>

    <h3>7.4. Оперативные группы и их специализация</h3>
    <p>Каждая МОГ имеет свою специализацию. Невыполнение профильной задачи = нарушение. <strong>Нажмите на группу, чтобы раскрыть подробности.</strong></p>

    <details class="mtf-card">
      <summary>Альфа-1 «Багряная десница»</summary>
      <div class="content">
        <span class="role">Элитное подразделение ОВО (Отдел внутренней безопасности)</span>
        <p>Задачи: нейтрализация аномальных угроз высшего приоритета, защита руководства Фонда, борьба с предателями.</p>
        <p>Особенности: работают под прямым надзором ОВО, имеют право игнорировать приказы обычных командиров.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Альфа-2 «Посыльные»</summary>
      <div class="content">
        <span class="role">Вспомогательное подразделение</span>
        <p>Задачи: доставка приказов, сопровождение VIP-персон, связь между секторами.</p>
        <p>Особенности: входят через гермоворота Браво, обязаны проверять документы у всех.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Бета-7 «Шляпные болванчики»</summary>
      <div class="content">
        <span class="role">Биологическая защита</span>
        <p>Задачи: сдерживание биологических аномалий, дезинфекция, карантин.</p>
        <p>Особенности: работают в защитных костюмах, не вступают в бой без необходимости.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Эта-10 «Не вижу зла»</summary>
      <div class="content">
        <span class="role">Меметические и когнитивные угрозы</span>
        <p>Задачи: сдерживание меметических SCP (SCP-268 и др.), защита разума персонала.</p>
        <p>Особенности: работают в спецшлемах, избегают визуального контакта с аномалиями.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Эта-11 «Дикие твари»</summary>
      <div class="content">
        <span class="role">Звуковые аномалии</span>
        <p>Задачи: сдерживание SCP, связанных со звуком, вибрацией, акустикой.</p>
        <p>Особенности: используют звукоизоляцию, работают в тишине.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Эпсилон-11 «Девятихвостая лиса»</summary>
      <div class="content">
        <span class="role">Внутренняя безопасность</span>
        <p>Задачи: подавление массовых побегов SCP, эвакуация выживших, восстановление контроля над комплексом.</p>
        <p>Особенности: элитное подразделение, подчиняется ОВО. Имеет расширенные полномочия.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Кси-13 «Следуйте за нами»</summary>
      <div class="content">
        <span class="role">Быстрое реагирование</span>
        <p>Задачи: первыми прибывают на место происшествия, зачищают сектор до подхода основных сил.</p>
        <p>Особенности: малочисленны, но мобильны.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Лямбда-5 «Белые кролики»</summary>
      <div class="content">
        <span class="role">Разведка и тестирование</span>
        <p>Задачи: тестирование аномалий, разведка неизвестных зон, сбор данных.</p>
        <p>Особенности: работают с SCP, часто первыми вступают в контакт.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Лима-5 «Травма Тим»</summary>
      <div class="content">
        <span class="role">Медицинская эвакуация</span>
        <p>Задачи: эвакуация раненых, оказание первой помощи, сопровождение выживших.</p>
        <p>Особенности: работают в тылу, не вступают в бой без необходимости.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Ню-7 «Удар молота»</summary>
      <div class="content">
        <span class="role">Тяжёлая пехота</span>
        <p>Задачи: зачистка внутренних секторов, уничтожение неавторизованного персонала, охрана периметра.</p>
        <p>Особенности: имеют тяжёлое вооружение. Могут действовать по протоколу «зачистка всего живого».</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Ню-8 «Армия Унгуда»</summary>
      <div class="content">
        <span class="role">Зачистка секторов</span>
        <p>Задачи: зачистка секторов от угроз, поддержка других МОГ.</p>
        <p>Особенности: работают в условиях повышенной опасности.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Омега-1 «Шуйца Закона»</summary>
      <div class="content">
        <span class="role">Правоприменение</span>
        <p>Задачи: арест нарушителей, охрана руководства, соблюдение законов Фонда.</p>
        <p>Особенности: весь персонал обязан следовать их приказам.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Омега-16 «Новое командование»</summary>
      <div class="content">
        <span class="role">Кризисное управление</span>
        <p>Задачи: берут на себя командование при потере связи с ЦОК, восстанавливают порядок.</p>
        <p>Особенности: обладают правами временного командира.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Ро-9 «Техподдержка»</summary>
      <div class="content">
        <span class="role">Инженерные работы</span>
        <p>Задачи: ремонт систем комплекса, восстановление гермоворот, наладка оборудования.</p>
        <p>Особенности: работают совместно с инженерами Фонда.</p>
      </div>
    </details>

    <details class="mtf-card">
      <summary>Сиерра-9</summary>
      <div class="content">
        <span class="role">Нейтрализация неавторизованного персонала</span>
        <p>Задачи: уничтожение врагов Фонда, защита комплекса от внешних угроз.</p>
        <p>Особенности: работают в агрессивном режиме.</p>
      </div>
    </details>

    <h3>7.5. Протоколы и задачи МОГ</h3>
    <table>
      <tr><th>Протокол</th><th>Описание</th></tr>
      <tr><td>Зачистка сектора</td><td>Полное уничтожение всех угроз в указанной зоне</td></tr>
      <tr><td>Задержание</td><td>Арест подозрительных лиц и доставка на допрос</td></tr>
      <tr><td>Эвакуация</td><td>Вывод персонала из опасной зоны</td></tr>
      <tr><td>Сдерживание</td><td>Возврат SCP в камеру или изоляция</td></tr>
      <tr><td>Нейтрализация</td><td>Уничтожение SCP (только с разрешения ЦОК)</td></tr>
      <tr><td>Сканирование</td><td>Перекличка персонала через камеры</td></tr>
    </table>

    <h3>7.6. Запрещено МОГ</h3>
    <div class="rule"><strong>7.6.1.</strong> Убийство Д-класса без причины.</div>
    <div class="rule"><strong>7.6.2.</strong> Отказ подчиняться командиру.</div>
    <div class="rule"><strong>7.6.3.</strong> Оставление поста без приказа.</div>
    <div class="rule"><strong>7.6.4.</strong> Помощь ПХ или SCP.</div>
    <div class="rule"><strong>7.6.5.</strong> Использование служебного положения в личных целях.</div>
    <div class="rule"><strong>7.6.6.</strong> Игнорирование профильной задачи (например, Ню-7 занимается спасением вместо зачистки).</div>
    <div class="rule"><strong>7.6.7.</strong> Абуз доступом к системам комплекса (ядерка, ворота, тесла).</div>
    <div class="rule"><strong>7.6.8.</strong> Самовольная активация кода тревоги без причины.</div>

    <div class="warning"><strong>ВАЖНО:</strong> Командир МОГ несёт ответственность за весь состав. Если боец нарушает правила — командир получает выговор.</div>

    <h3>7.7. Протоколы C.A.S.S.I.E.</h3>
    <p>Ниже перечислены специальные протоколы, которые могут быть активированы через C.A.S.S.I.E. Нажмите, чтобы раскрыть подробности.</p>

    <details class="protocol-card">
      <summary>Протокол «Рука мертвеца»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Удаленный доступ получен. Режим ожидания… Команда получена. Начало сканирования… Сканирование завершено. Высылаю информацию… Информация отправлена. Режим ожидания… Команда получена. Протокол “Рука мертвеца” активирован. Алгоритм чрезвычайной детонации Омега боеголовки запущен. Подземная и наземная части комплекса будут подорваны через 90 секунд.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Демонтаж»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Запрос принят. Активирован протокол "Демонтаж". Арест всех.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Лима»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Протокол "Лима" Активирован. SCP-914 и SCP-330 в Лёгкой зоне содержания будут ЗАБЛОКИРОВАНЫ.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Лезвие»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Протокол “Лезвие” активирован. Ликвидация.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Тяжёлое решение»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Протокол “Тяжёлое решение” активирован. Врата Альфа и Браво открыты. Боеголовка детонирует через 90 секунд.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Вердикт»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Запрос принят. Активирован протокол "Вердикт". Весь Класс Д разрешено ликвидировать.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Железный занавес»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Персонал Безопасности комплекса был уничтожен. Активирован протокол "Железный занавес". Пропускной пункт в входную зону будет заблокирован до прибытия Отряда МОГ.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Уборка»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩🟦 Работы окончена</p>
        <p><strong>Текст:</strong> Внимание всем оперативникам МОГ. По решению операторов Штаба-04, активируется протокол "Уборка" для ликвидации SCP-###. После ликвидации объекта, эвакуируйте MICRO-HID и продолжайте операцию.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Откат»</summary>
      <div class="content">
        <p><strong>Статус:</strong> ⬛ Работы нет текста</p>
        <p><strong>Текст:</strong> ПРОТОКОЛ Откат.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Тайна»</summary>
      <div class="content">
        <p><strong>Статус:</strong> ⬛ Работы нет текста</p>
        <p><strong>Текст:</strong> ПРОТОКОЛ Тайна.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Очищение»</summary>
      <div class="content">
        <p><strong>Статус:</strong> ⬛ Работы нет текста</p>
        <p><strong>Текст:</strong> ПРОТОКОЛ Очищение.</p>
      </div>
    </details>

    <details class="protocol-card">
      <summary>Протокол «Катаракт»</summary>
      <div class="content">
        <p><strong>Статус:</strong> 🟩 Работы окончена</p>
        <p><strong>Текст:</strong> Запрос принят. Активирован протокол "Катаракт". Уровень-1. Блокировка КПП легкой зоны содержания.</p>
      </div>
    </details>
  </section>

  <section id="ci">
    <h2>8. Правила за ПХ <span class="badge badge-ci">CI</span></h2>

    <h3>8.1. Общие правила</h3>
    <ul>
      <li>ПХ — враги Фонда. Их цель — захват SCP и уничтожение МОГ.</li>
      <li>ПХ обязаны подчиняться командиру.</li>
      <li>ПХ могут брать заложников и вести переговоры.</li>
      <li><strong>Главная задача</strong> — кража Карманных SCP.</li>
      <li>Имеют право на ликвидацию сотрудников <strong>ниже 3-го уровня</strong> (зависит от приказа командира).</li>
      <li>Могут брать в плен по своему желанию (зависит от приказа командира).</li>
      <li>Стратегия: «Вошли и вышли», а не начинать стрельбу по громкой.</li>
      <li>Если командир погиб — весь состав обязан дождаться подмоги. Разрешено покинуть участок в случае огромных потерь и ждать подкрепления.</li>
    </ul>

    <h3>8.2. Запрещено ПХ</h3>
    <div class="rule"><strong>8.2.1.</strong> Убийство своих без причины.</div>
    <div class="rule"><strong>8.2.2.</strong> Союз с МОГ против SCP.</div>
    <div class="rule"><strong>8.2.3.</strong> Кемпинг на респавне Фонда.</div>
    <div class="rule"><strong>8.2.4.</strong> Игнорирование приказов командира.</div>
    <div class="rule"><strong>8.2.5.</strong> Убийство заложников без RP-причины.</div>
  </section>

  <section id="dclass">
    <h2>9. Правила за Д-класс <span class="badge badge-dclass">D-CLASS</span></h2>

    <h3>9.1. Общие правила</h3>
    <ul>
      <li>Д-класс — заключённые. Их цель — выжить и сбежать.</li>
      <li>Д-класс подчиняются всем сотрудникам <strong>2 уровня и выше</strong>.</li>
      <li>Соблюдают контракт с Фондом до побега.</li>
      <li>При виде SCP испытывают страх и пытаются сбежать и выжить.</li>
      <li>Могут узнать про SCP, читая документацию в их камерах (импровизация). Для изучения требуется <strong>1 минута</strong>.</li>
      <li>Могут бунтовать, но только при наличии RP-причины.</li>
      <li>Обязаны подчиняться МОГ при угрозе оружием (FearRP).</li>
    </ul>

    <h3>9.2. Запрещено Д-класс</h3>
    <div class="rule"><strong>9.2.1.</strong> Бунт без RP-причины (просто так).</div>
    <div class="rule"><strong>9.2.2.</strong> Убийство других заключённых Д-класса без причины.</div>
    <div class="rule"><strong>9.2.3.</strong> Помощь SCP без RP-причины.</div>
    <div class="rule"><strong>9.2.4.</strong> Использование читов и багов.</div>
    <div class="rule"><strong>9.2.5.</strong> Нарушение FearRP при угрозе оружием.</div>

    <h3>9.3. Побег</h3>
    <ul>
      <li>Побег разрешён при наличии возможности.</li>
      <li>Запрещено кемпить выход после побега.</li>
      <li>После побега Д-класс может стать ПХ (по RP).</li>
    </ul>
  </section>

  <section id="sci">
    <h2>10. Правила за учёных <span class="badge badge-sci">SCI</span></h2>

    <h3>10.1. Общие правила</h3>
    <ul>
      <li>Учёные — сотрудники Фонда. Их цель — изучение SCP и выживание.</li>
      <li>Учёные обязаны подчиняться МОГ при эвакуации.</li>
      <li>Учёные могут проводить эксперименты с SCP по RP.</li>
      <li>Знают, как выглядят все SCP, и базовые меры противодействия им.</li>
      <li>Знают классификацию SCP: Безопасный, Евклид, Кетер.</li>
      <li>Знают о существовании всех SCP и о способах противодействия каждому из них.</li>
      <li><strong>Весь научный состав (НС)</strong> знает все коды, кроме «Хладное серебро», а также протоколы «Арест персонала» и другие, связанные с арестом.</li>
      <li>Не знают протоколы, связанные с уничтожением SCP и с «ядеркой» (детонацией комплекса).</li>
    </ul>

    <h3>10.2. Запрещено учёным</h3>
    <div class="rule"><strong>10.2.1.</strong> Помощь Д-классу без RP-причины.</div>
    <div class="rule"><strong>10.2.2.</strong> Использование SCP в личных целях.</div>
    <div class="rule"><strong>10.2.3.</strong> Оставление поста без приказа.</div>
    <div class="rule"><strong>10.2.4.</strong> Нарушение протоколов сдерживания.</div>
    <div class="rule"><strong>10.2.5.</strong> Убийство Д-класса без приказа МОГ.</div>
  </section>

  <section id="staff">
    <h2>11. Правила для стаффа <span class="badge badge-staff">STAFF</span></h2>

    <h3>11.1. Общие правила</h3>
    <ul>
      <li>Стафф — лицо проекта. Ведите себя достойно.</li>
      <li>Стафф не имеет права использовать права в личных целях.</li>
      <li>Стафф обязан соблюдать те же правила, что и игроки.</li>
      <li>При первых нарушениях — <strong>выговор</strong>.</li>
      <li><strong>Повторная заявка на «админа»</strong> — только через <strong>2 дня</strong> после отказа. Если подана раньше — моментальный отказ.</li>
    </ul>

    <h3>11.2. Запрещено стаффу</h3>
    <div class="rule"><strong>11.2.1.</strong> Абуз правами (noclip, godmode, teleport без причины).</div>
    <div class="rule"><strong>11.2.2.</strong> Выдача наказаний без доказательств.</div>
    <div class="rule"><strong>11.2.3.</strong> Снятие наказаний за услуги или по дружбе.</div>
    <div class="rule"><strong>11.2.4.</strong> Участие в RP с использованием админ-прав.</div>
    <div class="rule"><strong>11.2.5.</strong> Разглашение внутренней информации проекта.</div>
    <div class="rule"><strong>11.2.6.</strong> Оскорбление игроков в любой форме.</div>

    <h3>11.3. Наказания для стаффа</h3>
    <table>
      <tr><th>Нарушение</th><th>Наказание</th></tr>
      <tr><td>Абуз правами</td><td>Уволен + ЧСА</td></tr>
      <tr><td>Выдача наказаний без причины</td><td>Выговор → снятие</td></tr>
      <tr><td>Оскорбление игроков</td><td>Выговор + снятие</td></tr>
      <tr><td>Разглашение информации</td><td>Перм. бан + ЧСС + ЧСА</td></tr>
    </table>
    <div class="warning"><strong>ВАЖНО:</strong> За абуз правами — снятие с поста без возврата средств. Апелляция подаётся в течение 24 часов, решение руководства окончательное.</div>
    <div class="info"><strong>КОМАНДА В DISCORD:</strong> <code>!Warn "Имя пользователя"</code> — сохраняется как выговор. Выговор снимается автоматически через <strong>1 неделю</strong>.</div>
  </section>

  <section id="donate">
    <h2>12. Донат и поддержка</h2>

    <h3>12.1. Общие положения</h3>
    <ul>
      <li>Донат — <strong>добровольная поддержка проекта</strong>.</li>
      <li>Донат <strong>не даёт права нарушать правила</strong>.</li>
      <li>Донат не гарантирует пост в стаффе.</li>
      <li>Возврат средств не предусмотрен.</li>
    </ul>

    <h3>12.2. Привилегии</h3>
    <table>
      <tr><th>Уровень</th><th>Привилегии</th></tr>
      <tr><td>VIP</td><td>Цветной ник, приоритет входа</td></tr>
      <tr><td>Premium</td><td>+2 слота, кастомные фразы CASSIE</td></tr>
      <tr><td>Elite</td><td>+5 слотов, доступ к ивентам</td></tr>
      <tr><td>Support</td><td>Ускоренное рассмотрение заявки на хелпера</td></tr>
    </table>

    <div class="warning">
      <strong>ВНИМАНИЕ:</strong>
      <ul>
        <li>Возврат средств за снятие с поста не предусмотрен.</li>
        <li>За абуз правами — снятие без возврата.</li>
        <li>Донат не гарантирует пост в стаффе — только ускоряет рассмотрение.</li>
        <li>Оплата означает согласие с уставом команды.</li>
      </ul>
    </div>
  </section>

  <section id="punish">
    <h2>13. Система наказаний</h2>

    <h3>13.1. Виды наказаний</h3>
    <table>
      <tr><th>Наказание</th><th>Срок</th><th>Когда применяется</th></tr>
      <tr><td>Warn</td><td>—</td><td>Мелкие нарушения</td></tr>
      <tr><td>Mute</td><td>60–1440 мин</td><td>Нарушение голосового чата</td></tr>
      <tr><td>Kick</td><td>—</td><td>Повторное мелкое нарушение</td></tr>
      <tr><td>Ban 1 день</td><td>24 ч</td><td>Среднее нарушение</td></tr>
      <tr><td>Ban 7 дней</td><td>168 ч</td><td>Серьёзное нарушение</td></tr>
      <tr><td>Ban 30 дней</td><td>720 ч</td><td>Очень серьёзное нарушение</td></tr>
      <tr><td>PermBan</td><td>Навсегда</td><td>Читы, угрозы, реклама</td></tr>
    </table>

    <h3>13.2. Лимит варнов</h3>
    <ul>
      <li>Обычный игрок: <strong>3 варна в месяц</strong>.</li>
      <li>Донатер: <strong>4 варна в месяц</strong>.</li>
      <li>Поддерживающий стафф: <strong>5 варнов в месяц</strong>.</li>
      <li>Превышение лимита — автоматический бан.</li>
    </ul>

    <h3>13.3. Апелляция</h3>
    <ul>
      <li>Подаётся в Discord в канале #апелляции.</li>
      <li>Срок рассмотрения: до 48 часов.</li>
      <li>Решение руководства окончательное.</li>
    </ul>
  </section>

  <section id="voice">
    <h2>14. Голосовой чат</h2>
    <ul>
      <li>Микрофон обязателен для RP-ролей.</li>
      <li>Запрещён спам, посторонние звуки без RP-смысла.</li>
      <li>Запрещено оскорбление по национальному, религиозному признаку.</li>
      <li>Запрещено использование звуковых панелей без RP-причины.</li>
      <li>Запрещено говорить OOC в IC-канале.</li>
      <li><strong>Разрешены разные звуки</strong>, если они подходят для RP: крики «Помогите!», когда за тобой бежит SCP, и т.д. — как в реальной жизни вёл бы себя персонаж.</li>
      <li><strong>Отыгрыш действий голосом:</strong> игрок озвучивает, что делает его персонаж. Примеры: «Надеваю наручники на Д-класса перед собой», «Достаю пистолет и направляю на учёного», «Обыскиваю тело». Это делает RP живее и атмосфернее.</li>
    </ul>
    <div class="rule"><strong>14.1.</strong> Нарушение голосового чата = мут от 60 минут.</div>
  </section>

  <section id="discord">
    <h2>15. Discord-правила</h2>
    <ul>
      <li>Запрещён спам, флуд, капс.</li>
      <li>Запрещены оскорбления, травля, токсичность.</li>
      <li>Запрещена реклама других проектов.</li>
      <li>Запрещено распространение NSFW, шок-контента.</li>
      <li>Запрещено разглашение личной информации.</li>
      <li>Запрещено обсуждать политику и религию.</li>
      <li>Подчиняйтесь указаниям модерации.</li>
    </ul>
    <div class="warning"><strong>ВАЖНО:</strong> Нарушение Discord-правил = мут/бан в Discord и на сервере. <strong>При первых нарушениях — выговор.</strong></div>
  </section>

  <section id="final">
    <h2>16. Заключительные положения</h2>
    <ul>
      <li>Правила действуют на всех серверах MV.PROJECT.</li>
      <li>Администрация вправе трактовать правила по своему усмотрению.</li>
      <li>Незнание правил не освобождает от ответственности.</li>
      <li>Актуальная версия правил всегда в Discord.</li>
      <li>Играя на сервере, вы соглашаетесь с данными правилами.</li>
    </ul>
    <div class="ok"><strong>СПАСИБО ЗА ИГРУ НА MV.PROJECT!</strong> Соблюдайте правила — и RP будет интересным для всех.</div>
  </section>

  <footer>
    <p><strong>MV.PROJECT</strong> — Medium RP SCP:SL</p>
    <p>© 2026 MV.PROJECT. Все права защищены.</p>
    <p>Версия правил 2.7</p>
  </footer>

</main>

<script>
  // Поиск по правилам
  document.addEventListener('DOMContentLoaded', function () {
    const searchInput = document.getElementById('searchInput');
    const sections = document.querySelectorAll('section');

    searchInput.addEventListener('input', function () {
      const query = this.value.toLowerCase().trim();

      sections.forEach(function (section) {
        if (!query) {
          section.style.display = '';
          return;
        }
        const text = section.textContent.toLowerCase();
        section.style.display = text.includes(query) ? '' : 'none';
      });
    });
  });
</script>
</body>
</html>
