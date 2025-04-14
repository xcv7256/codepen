<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>İklim Terimleri Bulmaca</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; background-color: #e9f5ff; }
    h1 { color: #005577; }
    .word-list { margin-top: 20px; }
    canvas { border: 2px solid #005577; margin-top: 20px; }
    .found { text-decoration: line-through; color: green; }
  </style>
</head>
<body>
  <h1>İklim Terimleri Bulmaca</h1>
  <p>Aşağıdaki iklim terimlerini bulabilir misin?</p>
  <div class="word-list" id="words">
    <span>İKLİM</span>, <span>YAĞIŞ</span>, <span>NEM</span>, <span>SICAKLIK</span>,
    <span>KARASELLİK</span>, <span>METEOROLOJİ</span>
  </div>
  <canvas id="puzzleCanvas" width="400" height="400"></canvas>

  <script>
    // Basit kelime yerleştirme ve tespit edilebilirlik örneği
    const words = ["İKLİM", "YAĞIŞ", "NEM", "SICAKLIK", "KARASELLİK", "METEOROLOJİ"];
    const canvas = document.getElementById('puzzleCanvas');
    const ctx = canvas.getContext('2d');

    // Örnek harf ızgarası (daha gelişmiş hale getirilebilir)
    const grid = [
      ['İ','K','L','İ','M','A','B','C'],
      ['Y','A','Ğ','I','Ş','D','E','F'],
      ['N','E','M','G','H','I','J','K'],
      ['S','I','C','A','K','L','I','K'],
      ['L','M','N','O','P','Q','R','S'],
      ['K','A','R','A','S','E','L','L'],
      ['İ','K','T','U','V','W','X','Y'],
      ['Z','M','E','T','E','O','R','O']
    ];

    // Harfleri çiz
    function drawGrid() {
      ctx.font = "20px Arial";
      for (let i = 0; i < grid.length; i++) {
        for (let j = 0; j < grid[i].length; j++) {
          ctx.fillText(grid[i][j], j * 45 + 10, i * 45 + 30);
        }
      }
    }

    drawGrid();
  </script>
</body>
</html>
