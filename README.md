# valentine-surprise
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Valentine Surprise ❤️</title>
  <style>
    * { box-sizing: border-box; }
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      color: #4a1c1c;
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }
    .card {
      background: rgba(255,255,255,0.95);
      max-width: 420px;
      width: 90%;
      padding: 28px;
      border-radius: 22px;
      text-align: center;
      box-shadow: 0 15px 40px rgba(0,0,0,0.2);
      animation: fadeIn 1.2s ease;
    }
    h1 { margin-top: 0; }
    p { line-height: 1.6; }
    .heart { font-size: 3rem; animation: beat 1s infinite; }
    button {
      padding: 12px 22px;
      border: none;
      border-radius: 30px;
      font-size: 1rem;
      cursor: pointer;
      margin: 8px;
      transition: all 0.2s ease;
    }
    .yes {
      background: #ff4d6d;
      color: white;
    }
    .no {
      background: #ccc;
      color: #555;
      position: absolute;
    }
    button:hover { transform: scale(1.05); }
    .hidden { display: none; }
    .name { font-weight: bold; }
    @keyframes beat {
      0%,100%{transform:scale(1);}50%{transform:scale(1.2);} }
    @keyframes fadeIn {
      from{opacity:0;transform:translateY(20px);}to{opacity:1;transform:translateY(0);} }
  </style>
</head>
<body>

  <!-- Slide 1 -->
  <div class="card" id="slide1">
    <div class="heart">❤️</div>
    <h1>Hai Sayang 💕</h1>
    <p>Mau gak jadi Valentine aku hari ini?</p>
    <button class="yes" onclick="nextSlide()">YES 😍</button>
    <button class="no" id="noBtn">NO 🙃</button>
  </div>

  <!-- Slide 2 -->
    <!-- Slide 2 -->
  <div class="card hidden" id="slide2">
    <div class="heart">💖</div>
    <h1>Happy Valentine</h1>
    <p>Hai <span class="name">Nadiaaaa Sayang</span> 🤍</p>

    <img src="foto1.jpg" alt="Foto Nadia" style="width:100%;border-radius:16px;margin:12px 0;">
    <img src="foto2.jpg" alt="Foto Kita" style="width:100%;border-radius:16px;margin:12px 0;">

    <p>
      Aku tau aku kadang ngeselin,
      suka bikin kamu kesel,
      kadang juga kurang peka 😅
    </p>
    <p>
      Maafin aku ya sayang…
      bukan karena aku nggak peduli,
      tapi karena aku masih belajar
      jadi pasangan yang lebih baik buat kamu.
    </p>
    <p>
      Tapi satu hal yang pasti,
      aku beneran sayang kamu 💕
      dari senyum kamu,
      dari juteknya kamu,
      bahkan dari diemnya kamu juga 😆
    </p>
    <p class="name">Happy Valentine ya sayang ❤️</p>
    <p class="name">- Dari aku yang selalu pilih kamu</p>
  </div>
    <h1>Happy Valentine</h1>
    <p>Hai <span class="name">[Nama Pacar]</span>,</p>
    <p>
      Makasih ya sudah memilih <b>YES</b> 🤍
      Website kecil ini aku buat khusus buat kamu.
      Kamu itu penting banget buat aku,
      lebih dari yang bisa aku jelasin dengan kata-kata.
    </p>
    <p class="name">- Dari aku yang sayang kamu</p>
  </div>

  <script>
    const noBtn = document.getElementById('noBtn');

    noBtn.addEventListener('mouseover', () => {
      const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
      const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);
      noBtn.style.left = x + 'px';
      noBtn.style.top = y + 'px';
    });

    function nextSlide() {
      document.getElementById('slide1').classList.add('hidden');
      document.getElementById('slide2').classList.remove('hidden');
    }
  </script>

</body>
</html>
