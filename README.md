<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ACE jyosetu</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@400;700&display=swap" rel="stylesheet">
</head>
<body>
  <!-- サイト全体のヘッダー（ロゴ・ナビ） -->
  <header class="site-header">
    <div class="container">
      <div class="logo">ACE</div>
      <nav class="nav">
        <ul>
          <li><a href="#courses">MENU</a></li>
          <li><a href="#features">text</a></li>
          <li><a href="#news">text</a></li>
          <li><a href="#contact" class="btn">お問い合わせ</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- ファーストビュー -->
  <section class="hero">
    <h1></h1>
    <p></p>
    
  </section>

  <!-- 初回お試し体験 -->
  <section class="trial-experience">
    <h2>MENU</h2>
    <p>text text text text text text text text。</p>

    <div class="trial-courses">
      <div class="course">
        <h3>除雪</h3>
        <p>text text text text</p>
        <p class="original-price">¥15,400</p>
        <p class="trial-price">¥5,500</p>
      </div>
      <div class="course">
        <h3>芝刈り</h3>
        <p>text text  text text</p>
        <p class="original-price">¥15,400</p>
        <p class="trial-price">¥7,700</p>
      </div>
    </div>

    <h3 class="TEL">TEL 080-xxxx-xxxx</h3>
  </section>

  <!-- こだわり紹介 -->
  <section class="features">
    <h2>TEXT TEXT TEXT</h2>
    <div class="feature-list">
      <div class="feature">
        <h3>text text text </h3>
        <p>text text text text text text text text text text</p>
      </div>
      <div class="feature">
        <h3>text text</h3>
        <p>text text text text text text text text text text。</p>
      </div>
      <div class="feature">
        <h3>text text</h3>
        <p>text text text text text text text text text text。</p>
      </div>
    </div>
  </section>

  <!-- ニュース -->
  <section class="news">
    <h2>text text</h2>
    <ul>
      <li><span>2025.09.01</span>text text </li>
      <li><span>2025.08.20</span> text text </li>
      <li><span>2025.08.05</span> text text </li>
    </ul>
  </section>

  <!-- フッター -->
  <footer>
    <p>&copy; ACE TOYAMA.</p>
  </footer>

  <!-- 自動横スクロール用スクリプト -->
<!-- <script>
  window.addEventListener('load', () => {
    const container = document.querySelector('.trial-courses');
    let scrollPos = 0;
    let isPaused = false;

    function autoScroll() {
      if (!container) return;

      if (!isPaused) {
        scrollPos += 0.6; // スクロール速度
        if (scrollPos > container.scrollWidth - container.clientWidth) {
          scrollPos = 0; // 末尾まで行ったら先頭に戻る
        }
        container.scrollLeft = scrollPos;
      }

      requestAnimationFrame(autoScroll);
    }

    container.addEventListener('mouseenter', () => isPaused = true);
    container.addEventListener('mouseleave', () => isPaused = false);

    autoScroll();
  });
</script> -->
<script>
  // trial-courses 内でマウスホイールの上下を横スクロールに変換
  const container = document.querySelector('.trial-courses');

  if (container) {
    container.addEventListener('wheel', (e) => {
      // 上下スクロールを横スクロールに変換
      if (e.deltaY !== 0) {
        e.preventDefault(); // 通常の上下スクロールを無効化
        container.scrollLeft += e.deltaY; // 横方向に移動
      }
    });
  }
</script>



</body>
</html>
