#Solution to css loading performance



<head></head><body><link rel="stylesheet" href="/site-header.css">
  <header>…</header>

  <link rel="stylesheet" href="/article.css">
  <main>…</main>

  <link rel="stylesheet" href="/comment.css">
  <section class="comments">…</section>

  <link rel="stylesheet" href="/about-me.css">
  <section class="about-me">…</section>

  <link rel="stylesheet" href="/site-footer.css">
  <footer>…</footer>
</body>

the different behave between common parallel loading way and this method is that by this mean which defers rendering follow-up parts our project show more human friendly.