# GOLD-KEBAP-IMBISS-<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Gold Kebap & Imbiss</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #fff8f0; color: #333; }
    header { background: goldenrod; color: white; padding: 20px; text-align: center; }
    nav a { margin: 0 15px; color: white; text-decoration: none; font-weight: bold; }
    .menu { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; padding: 20px; }
    .item { background: white; padding: 20px; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); text-align: center; transition: 0.3s; }
    .item:hover { transform: scale(1.05); }
    .item img { width: 100%; height: 180px; object-fit: cover; border-radius: 12px; }
    .item h2 { margin: 15px 0 5px; color: goldenrod; }
    .item p { font-size: 14px; }
    .lieferando-btn {
      display: inline-block; margin: 20px auto; padding: 12px 25px;
      background: #ff8000; color: white; text-decoration: none;
      border-radius: 8px; font-weight: bold;
    }
    .lieferando-btn:hover { background: #e67300; }
    footer { background: goldenrod; color: white; text-align: center; padding: 15px; margin-top: 30px; }
    #events { background:#fff3cd; padding:40px; text-align:center; }
    #event-list { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; margin-top:20px; }
    .event-card { background:white; padding:20px; border-radius:15px; box-shadow:0 4px 10px rgba(0,0,0,0.1); }
  </style>
</head>
<body>
  <header>
    <h1>🌟 Gold Kebap & Imbiss</h1>
    <nav>
      <a href="#">Startseite</a>
      <a href="#menu">Menü</a>
      <a href="#events">Aktionen</a>
      <a href="#kontakt">Kontakt</a>
    </nav>
  </header>

  <!-- Menü -->
  <section id="menu" class="menu">
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Döner" alt="Döner">
      <h2>Döner</h2>
      <p>Klassischer Döner mit Huhn oder Rindfleisch.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Kebab" alt="Kebab">
      <h2>Kebab</h2>
      <p>Gegrillt, scharf oder mild nach Wahl.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Döner+Box" alt="Döner Box">
      <h2>Döner Box</h2>
      <p>Pommes + Döner + Sauce in einer Box.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Lahmacun" alt="Lahmacun">
      <h2>Lahmacun</h2>
      <p>Dünner Teig, frisch belegt mit Kräutern und Fleisch.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Hotdog" alt="Hotdog">
      <h2>Hotdog</h2>
      <p>Würstchen mit Gurken, Ketchup und Mayo.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Bosna" alt="Bosna">
      <h2>Bosna</h2>
      <p>Würzige Bratwurst im Brot – Wiener Klassiker.</p>
    </div>
  </section>

  <!-- Lieferando -->
  <div style="text-align:center;">
    <a href="https://www.lieferando.at/" target="_blank" class="lieferando-btn">
      👉 Jetzt auf Lieferando bestellen
    </a>
  </div>

  <!-- Events -->
  <section id="events">
    <h2 style="color:goldenrod;">🎉 Aktionen & Events</h2>
    <div id="event-list"></div>
  </section>

  <!-- Kontakt -->
  <footer id="kontakt">
    <p>📍 Adresse: Wien, Österreich</p>
    <p>☎ Telefon: +43 660 123 45 67</p>
    <p>Öffnungszeiten: Mo-So 11:00 - 23:00 Uhr</p>
  </footer>

  <!-- Script to load events -->
  <script>
    fetch("events.json")
      .then(response => response.json())
      .then(events => {
        const container = document.getElementById("event-list");
        events.forEach(ev => {
          const card = document.createElement("div");
          card.className = "event-card";
          card.innerHTML = `<h3>${ev.title}</h3><p>${ev.desc}</p><small>${ev.date}</small>`;
          container.appendChild(card);
        });
      });
  </script>
</body>
</html><!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <title>Gold Kebap & Imbiss</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #fff8f0; color: #333; }
    header { background: goldenrod; color: white; padding: 20px; text-align: center; }
    nav a { margin: 0 15px; color: white; text-decoration: none; font-weight: bold; }
    .menu { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; padding: 20px; }
    .item { background: white; padding: 20px; border-radius: 15px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); text-align: center; transition: 0.3s; }
    .item:hover { transform: scale(1.05); }
    .item img { width: 100%; height: 180px; object-fit: cover; border-radius: 12px; }
    .item h2 { margin: 15px 0 5px; color: goldenrod; }
    .item p { font-size: 14px; }
    .lieferando-btn {
      display: inline-block; margin: 20px auto; padding: 12px 25px;
      background: #ff8000; color: white; text-decoration: none;
      border-radius: 8px; font-weight: bold;
    }
    .lieferando-btn:hover { background: #e67300; }
    footer { background: goldenrod; color: white; text-align: center; padding: 15px; margin-top: 30px; }
    #events { background:#fff3cd; padding:40px; text-align:center; }
    #event-list { display:grid; grid-template-columns:repeat(auto-fit,minmax(250px,1fr)); gap:20px; margin-top:20px; }
    .event-card { background:white; padding:20px; border-radius:15px; box-shadow:0 4px 10px rgba(0,0,0,0.1); }
  </style>
</head>
<body>
  <header>
    <h1>🌟 Gold Kebap & Imbiss</h1>
    <nav>
      <a href="#">Startseite</a>
      <a href="#menu">Menü</a>
      <a href="#events">Aktionen</a>
      <a href="#kontakt">Kontakt</a>
    </nav>
  </header>

  <!-- Menü -->
  <section id="menu" class="menu">
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Döner" alt="Döner">
      <h2>Döner</h2>
      <p>Klassischer Döner mit Huhn oder Rindfleisch.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Kebab" alt="Kebab">
      <h2>Kebab</h2>
      <p>Gegrillt, scharf oder mild nach Wahl.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Döner+Box" alt="Döner Box">
      <h2>Döner Box</h2>
      <p>Pommes + Döner + Sauce in einer Box.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Lahmacun" alt="Lahmacun">
      <h2>Lahmacun</h2>
      <p>Dünner Teig, frisch belegt mit Kräutern und Fleisch.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Hotdog" alt="Hotdog">
      <h2>Hotdog</h2>
      <p>Würstchen mit Gurken, Ketchup und Mayo.</p>
    </div>
    <div class="item">
      <img src="https://via.placeholder.com/400x250?text=Bosna" alt="Bosna">
      <h2>Bosna</h2>
      <p>Würzige Bratwurst im Brot – Wiener Klassiker.</p>
    </div>
  </section>

  <!-- Lieferando -->
  <div style="text-align:center;">
    <a href="https://www.lieferando.at/" target="_blank" class="lieferando-btn">
      👉 Jetzt auf Lieferando bestellen
    </a>
  </div>

  <!-- Events -->
  <section id="events">
    <h2 style="color:goldenrod;">🎉 Aktionen & Events</h2>
    <div id="event-list"></div>
  </section>

  <!-- Kontakt -->
  <footer id="kontakt">
    <p>📍 Adresse: Wien, Österreich</p>
    <p>☎ Telefon: +43 660 123 45 67</p>
    <p>Öffnungszeiten: Mo-So 11:00 - 23:00 Uhr</p>
  </footer>

  <!-- Script to load events -->
  <script>
    fetch("events.json")
      .then(response => response.json())
      .then(events => {
        const container = document.getElementById("event-list");
        events.forEach(ev => {
          const card = document.createElement("div");
          card.className = "event-card";
          card.innerHTML = `<h3>${ev.title}</h3><p>${ev.desc}</p><small>${ev.date}</small>`;
          container.appendChild(card);
        });
      });
  </script>
</body>
</html>
