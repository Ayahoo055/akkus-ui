<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>akkus-ui - Dokümantasyon</title>
  <link rel="stylesheet" href="style.css"> <!-- Senin kütüphanen burada yüklenir -->
  <style>
    body { font-family: system-ui, sans-serif; max-width: 900px; margin: 40px auto; padding: 20px; line-height: 1.6; }
    h1, h2, h3 { color: #333; }
    .preview { border: 1px solid #e0e0e0; padding: 24px; margin: 20px 0; border-radius: 8px; background: #f9f9f9; }
    pre { background: #f5f5f5; padding: 16px; border-radius: 6px; overflow-x: auto; position: relative; }
    .copy-btn { background: #6366f1; color: white; border: none; padding: 8px 16px; border-radius: 6px; cursor: pointer; margin-top: 8px; }
    .copy-btn:hover { background: #4f46e5; }
  </style>
</head>
<body>

  <h1>akkus-ui</h1>
  <p>Kendi Bootstrap benzeri UI kütüphanem. Sadece class'ları kopyala-yapıştır!</p>

  <h2>Kullanım</h2>
  <pre><code>&lt;link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Ayahoo055/akkus-ui/style.css"&gt;</code></pre>

  <h2>Buton Örnekleri</h2>

  <div class="preview">
    <h3>Primary Buton</h3>
    <button class="akkus-btn primary">Birincil Buton</button>
  </div>

  <pre><code id="primary-code">&lt;button class="akkus-btn primary"&gt;Birincil Buton&lt;/button&gt;</code></pre>
  <button class="copy-btn" onclick="copyToClipboard('primary-code', this)">Kodu Kopyala</button>

  <div class="preview" style="margin-top: 30px;">
    <h3>Secondary Buton</h3>
    <button class="akkus-btn secondary">İkincil Buton</button>
  </div>

  <pre><code id="secondary-code">&lt;button class="akkus-btn secondary"&gt;İkincil Buton&lt;/button&gt;</code></pre>
  <button class="copy-btn" onclick="copyToClipboard('secondary-code', this)">Kodu Kopyala</button>

  <script>
    function copyToClipboard(id, btn) {
      const code = document.getElementById(id).innerText;
      navigator.clipboard.writeText(code);
      btn.innerText = 'Kopyalandı!';
      setTimeout(() => { btn.innerText = 'Kodu Kopyala'; }, 2000);
    }
  </script>

</body>
</html>
