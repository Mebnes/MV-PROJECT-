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

  /* ИСПРАВЛЕННЫЙ БЛОК ПРАВИЛ */
  .rule {
    background: #1f1f1f;
    border-left: 4px solid #ff2e2e;
    padding: 14px 20px;
    margin: 12px 0;
    border-radius: 0 8px 8px 0;
    color: #e8e8e8;
    font-size: 0.95em;
    line-height: 1.6;
    box-shadow: 0 2px 6px rgba(0,0,0,0.4);
    transition: 0.2s;
  }

  .rule:hover {
    background: #252525;
    border-left-color: #ff5555;
  }

  .rule strong {
    color: #ff2e2e;
    font-weight: 700;
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

  /* ИСПРАВЛЕННЫЕ ТАБЛИЦЫ */
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

  tr:hover td {
    background: #262626;
    color: #ffffff;
  }

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

  /* Адаптив для мобильных */
  @media (max-width: 700px) {
    .container { padding: 20px 15px; }
    header h1 { font-size: 1.6em; letter-spacing: 1px; }
    h2 { font-size: 1.2em; }
    h3 { font-size: 1em; }
    th, td { padding: 8px 10px; font-size: 0.85em; }
    nav ul { grid-template-columns: 1fr; }
  }
</style>
