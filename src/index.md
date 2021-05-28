<!doctype html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Новости">
  <meta name="keywords" content="news,новости">
  <meta name="author" content="Uladzimir Osipchyk">
  <title>News</title>
  <link rel="shortcut icon" href="<%= require('./images/news-icon.png').default %>" type="image/x-icon">
  <link rel="stylesheet" href="<%= htmlWebpackPlugin.files.css %>">
</head>
<body class="root">
<div class="root__container">
  <header class="header">
    <a class="logo" href="src/index.md">News App</a>
  </header>
  <section class="cover">
    <div class="cover__content">
      <h1 class="cover__title">World News</h1>
      <p class="cover__paragraph">Search by Topic</p>
    </div>
    <form class="form" novalidate>
      <input class="form__input" placeholder="Input the topic" required>
      <span class="form__error"></span>
      <button type="submit" class="form__button">Search</button>
    </form>
  </section>
</div>
<section class="search-result" id="preloader">
  <div class="preloader"></div>
  <h2 class="search-result__paragraph">Searching...</h2>
</section>
<section class="search-result" id="not-found">
  <div class="search-result__not-found"></div>
  <h2 class="search-result__title"></h2>
  <p class="search-result__paragraph"></p>
</section>
<main class="search-result" id="cards">
  <div class="cards">
    <h2 class="cards__title">Search Results</h2>
  </div>
  <ul class="cards-items">
  </ul>
  <button class="cards__button">Show more</button>
</main>
<footer class="footer">
  <p class="footer__copyright"></p>
</footer>
<script src="<%= htmlWebpackPlugin.files.js %>"></script>
</body>
</html>