<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Cinema Heaven</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      background: #111;
      color: white;
      font-family: Arial, sans-serif;
    }

    header {
      background: #181818;
      padding: 18px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .logo {
      font-size: 22px;
      font-weight: bold;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 12px;
      font-size: 14px;
    }

    .hero {
      padding: 70px 20px;
      text-align: center;
      background: linear-gradient(#0008, #000),
                  url("https://images.unsplash.com/photo-1489599849927-2ee91cede3ba")
                  center/cover;
    }

    .hero h1 {
      font-size: 40px;
      margin-bottom: 12px;
    }

    .hero p {
      color: #ddd;
      margin-bottom: 20px;
    }

    .search {
      width: 90%;
      max-width: 500px;
      padding: 14px;
      border: none;
      border-radius: 8px;
      font-size: 16px;
    }

    section {
      padding: 25px 15px;
    }

    section h2 {
      margin-bottom: 18px;
    }

    .movies {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 15px;
    }

    .card {
      background: #1d1d1d;
      border-radius: 10px;
      overflow: hidden;
    }

    .card img {
      width: 100%;
      height: 230px;
      object-fit: cover;
    }

    .card-content {
      padding: 12px;
    }

    .card h3 {
      font-size: 16px;
      margin-bottom: 6px;
    }

    .card p {
      color: #aaa;
      font-size: 13px;
    }

    .watch {
      display: inline-block;
      margin-top: 10px;
      background: #e50914;
      color: white;
      padding: 8px 12px;
      border-radius: 5px;
      text-decoration: none;
      font-size: 13px;
    }

    footer {
      text-align: center;
      padding: 25px;
      color: #888;
      background: #181818;
      margin-top: 20px;
    }
  </style>
</head>

<body>

  <header>
    <div class="logo">🎬 Cinema Heaven</div>

    <nav>
      <a href="#">Home</a>
      <a href="#movies">Movies</a>
      <a href="#series">Series</a>
      <a href="#anime">Anime</a>
    </nav>
  </header>

  <div class="hero">
    <h1>Welcome to Cinema Heaven</h1>
    <p>Movies • Web Series • Anime</p>

    <input
      class="search"
      type="text"
      placeholder="Search movies..."
      onkeyup="searchMovies()"
      id="searchBox">
  </div>

  <section id="movies">
    <h2>🔥 Latest Movies</h2>

    <div class="movies" id="movieList">

      <div class="card">
        <img src="https://via.placeholder.com/500x700?text=Movie+1">
        <div class="card-content">
          <h3>Movie Name 1</h3>
          <p>2026 • Action</p>
          <a href="#" class="watch">Watch Now</a>
        </div>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/500x700?text=Movie+2">
        <div class="card-content">
          <h3>Movie Name 2</h3>
          <p>2026 • Adventure</p>
          <a href="#" class="watch">Watch Now</a>
        </div>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/500x700?text=Movie+3">
        <div class="card-content">
          <h3>Movie Name 3</h3>
          <p>2026 • Drama</p>
          <a href="#" class="watch">Watch Now</a>
        </div>
      </div>

      <div class="card">
        <img src="https://via.placeholder.com/500x700?text=Movie+4">
        <div class="card-content">
          <h3>Movie Name 4</h3>
          <p>2026 • Comedy</p>
          <a href="#" class="watch">Watch Now</a>
        </div>
      </div>

    </div>
  </section>

  <section id="series">
    <h2>📺 Web Series</h2>
    <p>Web series section coming soon...</p>
  </section>

  <section id="anime">
    <h2>🍿 Anime</h2>
    <p>Anime section coming soon...</p>
  </section>

  <footer>
    © 2026 Cinema Heaven
  </footer>

  <script>
    function searchMovies() {
      let input = document
        .getElementById("searchBox")
        .value
        .toLowerCase();

      let cards = document.querySelectorAll(".card");

      cards.forEach(card => {
        let title = card
          .querySelector("h3")
          .innerText
          .toLowerCase();

        card.style.display =
          title.includes(input) ? "block" : "none";
      });
    }
  </script>

</body>
</html>
