<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MV.PROJECT — Правила Medium RP</title>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    font-family: 'Segoe UI', Tahoma, sans-serif;
    background: #0d0d0d;
    color: #d8d8d8;
    line-height: 1.7;
    padding: 20px;
  }
  .container {
    max-width: 1100px;
    margin: 0 auto;
    background: #151515;
    border: 1px solid #2a2a2a;
    border-radius: 12px;
    padding: 40px;
    box-shadow: 0 0 40px rgba(0,0,0,0.8);
  }
  header {
    text-align: center;
    border-bottom: 2px solid #8b0000;
    padding-bottom: 25px;
    margin-bottom: 35px;
  }
  header h1 {
    font-size: 2.4em;
    color: #ff2e2e;
    letter-spacing: 3px;
    text-transform: uppercase;
    text-shadow: 0 0 15px rgba(255,46,46,0.6);
  }
  header p {
    color: #888;
    margin-top: 10px;
    font-size: 0.95em;
    letter-spacing: 1px;
  }
  .version {
    display: inline-block;
    margin-top: 12px;
    padding: 4px 14px;
    background: #8b0000;
    color: #fff;
    border-radius: 20px;
    font-size: 0.8em;
    letter-spacing: 1px;
  }
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
  section {
    margin-bottom: 45px;
    padding-bottom: 25px;
    border-bottom: 1px solid #222;
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
  ul, ol {
    margin: 10px 0 15px 25px;
  }
  li { margin-bottom: 7px; }
  .rule {
    background: #1a1a1a;
    border-left: 4px solid #8b0000;
    padding: 12px 18px;
    margin: 12px 0;
    border-radius: 0 6px 6px 0;
  }
  .rule strong { color: #ff2e2e; }
  .warning {
    background: #1f1010;
    border: 1px solid #8b0000;
    border-left: 5px solid #ff2e2e;
    padding: 15px 20px;
    margin: 15px 0;
    border-radius: 6px;
  }
  .warning strong { color: #ff2e2e; }
  .info {
    background: #10181f;
    border: 1px solid #1e3a5f;
    border-left: 5px solid #3a8bff;
    padding: 15px 20px;
    margin: 15px 0;
    border-radius: 6px;
  }
  .info strong { color: #3a8bff; }
  .ok {
    background: #101f10;
    border: 1px solid #1e5f1e;
    border-left: 5px solid #3aff3a;
    padding: 15px 20px;
    margin: 15px 0;
    border-radius: 6px;
  }
  .ok strong { color: #3aff3a; }
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 15px 0;
    background: #1a1a1a;
    border-radius: 6px;
    overflow: hidden;
    border: 1px solid #2a2a2a;
  }
  th {
    background: #8b0000;
    color: #fff;
    padding: 12px;
    text-align: left;
    font-size: 0.9em;
    text-transform: uppercase;
    letter-spacing: 0.5px;
  }
  td {
    padding: 10px 12px;
    border-bottom: 1px solid #252525;
    font-size: 0.92em;
    color: #c8c8c8;
  }
  tr:last-child td { border-bottom: none; }
  tr:hover td { background: #1f1f1f; }
  footer {
    text-align: center;
    margin-top: 40px;
    padding-top: 25px;
    border-top: 2px solid #8b0000;
    color: #666;
    font-size: 0.85em;
  }
  footer strong { color: #ff2e2e; }
  .badge {
    display: inline-block;
    padding: 2px 10px;
    border-radius: 4px;
    font-size: 0.75em;
    font-weight: bold;
    letter-spacing: 0.5px;
    margin-left: 8px;
  }
  .badge-scp { background: #8b0000; color: #fff; }
  .badge-mtf { background: #1e3a5f; color: #fff; }
  .badge-ci { background: #3a5f1e; color: #fff; }
  .badge-dclass { background: #5f3a1e; color: #fff; }
  .badge-sci { background: #5f1e5f; color: #fff; }
  .badge-staff { background: #ffb400; color: #000; }
</style>
</head>
<body>
<div class="container">

<header>
  <h1>MV.PROJECT</h1>
  <p>MEDIUM ROLEPLAY — ОФИЦИАЛЬНЫЕ ПРАВИЛА СЕРВЕРА</p>
  <span class="version">Версия 2.0 • Обновлено с учётом правок</span>
</header>

<!-- КОДЕКС ИГРОКА -->
<div class="codex">
  <h2>Кодекс игрока</h2>
  <p>Добро пожаловать в <strong>руководство сервера MV.PROJECT</strong>, содержащее основные правила Medium RP, а также необходимые рекомендации для начала игры.</p>
  <p>Присоединяясь к серверу, вы соглашаетесь с данным руководством.</p>
  <p>Незначительно отклоняться от правил допустимо, если это не вредит другим игрокам и RP.</p>
  <p>Не мешайте работе состава проекта, а также игровому опыту других игроков.</p>
  <p class="quote">«Действуй логично и не мешай другим игрокам — так ты автоматически соблюдаешь 80% правил.»</p>
</div>

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

<!-- 1. ОБЩИЕ -->
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

<!-- 2. ROLEPLAY -->
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
  <div class="rule"><strong>2.2.3.</strong> Намеренное破坏 атмосферы: крики в микрофон, музыка, спам.</div>
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

<!-- 3. FEARRP -->
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
  <div class="rule"><strong>3.2.1.</strong> «Я тебя обезоружил» без /me и без согласия — PowerRP.</div>
  <div class="rule"><strong>3.2.2.</strong> «Я тебя убил» без фактического убийства в игре — PowerRP.</div>
  <div class="rule"><strong>3.2.3.</strong> Навязывание романтических, интимных или унизительных сцен — бан от 7 дней.</div>
  <div class="info"><strong>СОВЕТ:</strong> Используйте /me для описания действий. Например: <em>/me пытается обезоружить Д-класса</em> — и ждите реакции.</div>
</section>

<!-- 4. METAGAMING -->
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

<!-- 5. COMBAT -->
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

<!-- 6. SCP -->
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
    <li>Может проходить через стены в «карманное измерение».</li>
    <li>Не может кемпить у выхода из кармана.</li>
    <li>Запрещено убивать сразу после выхода из стены.</li>
    <li><strong>Может убивать всех, кого захочет</strong> — в рамках RP-логики своего персонажа.</li>
    <li><strong>Главная цель — сбежать, а не устроить резню.</strong></li>
    <li>Отсутствует правило «Страх за свою жизнь» — SCP-106 не боится смерти.</li>
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

<!-- 7. MTF -->
<section id="mtf">
  <h2>7. Правила за МОГ <span class="badge badge-mtf">MTF</span></h2>

  <h3>7.1. Общие правила</h3>
  <ul>
    <li>МОГ выполняют <strong>строго свою задачу</strong>, поставленную командиром.</li>
    <li>Приоритет ставит командир — его приказы обязательны.</li>
    <li>У каждой группы свои задачи (штурм, охрана, эвакуация).</li>
    <li>После выполнения всех задач имеют право эвакуировать персонал.</li>
    <li>При коде «Серый» имеют право арестовать весь персонал (кроме руководящего состава).</li>
    <li>МОГ обязаны защищать персонал и containment SCP.</li>
    <li>МОГ не могут убивать Д-класс без приказа или угрозы.</li>
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

  <h3>7.3. Запрещено МОГ</h3>
  <div class="rule"><strong>7.3.1.</strong> Убийство Д-класс без причины.</div>
  <div class="rule"><strong>7.3.2.</strong> Отказ подчиняться командиру.</div>
  <div class="rule"><strong>7.3.3.</strong> Оставление поста без приказа.</div>
  <div class="rule"><strong>7.3.4.</strong> Помощь ПХ или SCP.</div>
  <div class="rule"><strong>7.3.5.</strong> Использование служебного положения в личных целях.</div>
</section>

<!-- 8. CI -->
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

<!-- 9. D-CLASS -->
<section id="dclass">
  <h2>9. Правила за Д-класс <span class="badge badge-dclass">D-CLASS</span></h2>

  <h3>9.1. Общие правила</h3>
  <ul>
    <li>Д-класс — заключённые. Их цель — выжить и сбежать.</li>
    <li>Д-класс подчиняются всем сотрудникам <strong>2 уровня и выше</strong>.</li>
    <li>Соблюдают контракт до НОУС.</li>
    <li>При виде SCP испытывают страх и пытаются сбежать и выжить.</li>
    <li>Могут узнать про SCP, читая документацию в их камерах (импровизация). Для изучения требуется <strong>1 минута</strong>.</li>
    <li>Могут бунтовать, но только при наличии RP-причины.</li>
    <li>Обязаны подчиняться МОГ при угрозе оружием (FearRP).</li>
  </ul>

  <h3>9.2. Запрещено Д-класс</h3>
  <div class="rule"><strong>9.2.1.</strong> Бунт без RP-причины (просто так).</div>
  <div class="rule"><strong>9.2.2.</strong> Убийство других Д-класс без причины.</div>
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

<!-- 10. SCI -->
<section id="sci">
  <h2>10. Правила за учёных <span class="badge badge-sci">SCI</span></h2>

  <h3>10.1. Общие правила</h3>
  <ul>
    <li>Учёные — сотрудники Фонда. Их цель —研究 SCP и выжить.</li>
    <li>Учёные обязаны подчиняться МОГ при эвакуации.</li>
    <li>Учёные могут проводить эксперименты с SCP по RP.</li>
    <li><strong>Знают, как выглядят SCP</strong> и меры противодействия.</li>
    <li>Знают про класс <strong>Кетер ТОЛЬКО КЛАСС ЕВКЛИД = УД</strong>.</li>
    <li>Знают про все существования и противодействия каждого SCP.</li>
    <li><strong>ВЕСЬ НС</strong> — знает все коды, кроме: «Хладное серебро», а также протоколы «Арест персонала» и т.д., связанные с арестом.</li>
    <li>Не знают протоколы, связанные с уничтожением и с «ядеркой».</li>
  </ul>

  <h3>10.2. Запрещено учёным</h3>
  <div class="rule"><strong>10.2.1.</strong> Помощь Д-класс без RP-причины.</div>
  <div class="rule"><strong>10.2.2.</strong> Использование SCP в личных целях.</div>
  <div class="rule"><strong>10.2.3.</strong> Оставление поста без приказа.</div>
  <div class="rule"><strong>10.2.4.</strong> Нарушение протоколов containment.</div>
  <div class="rule"><strong>10.2.5.</strong> Убийство Д-класс без приказа МОГ.</div>
</section>

<!-- 11. STAFF -->
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

<!-- 12. DONATE -->
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

<!-- 13. PUNISH -->
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

<!-- 14. VOICE -->
<section id="voice">
  <h2>14. Голосовой чат</h2>
  <ul>
    <li>Микрофон обязателен для RP-ролей.</li>
    <li>Запрещён спам, посторонние звуки без RP-смысла.</li>
    <li>Запрещено оскорбление по национальному, религиозному признаку.</li>
    <li>Запрещено использование звуковых панелей без RP-причины.</li>
    <li>Запрещено говорить OOC в IC-канале.</li>
    <li><strong>Разрешены разные звуки</strong>, если они подходят для RP: крики «Помогите!», когда за тобой бежит SCP, и т.д. — как в реальной жизни вёл бы себя персонаж.</li>
  </ul>
  <div class="rule"><strong>14.1.</strong> Нарушение голосового чата = мут от 60 минут.</div>
</section>

<!-- 15. DISCORD -->
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

<!-- 16. FINAL -->
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
  <p>Версия правил 2.0</p>
</footer>

</div>
</body>
</html>
