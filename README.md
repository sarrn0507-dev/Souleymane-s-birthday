<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Joyeux Anniversaire Soupou nene 🎉</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff7eb9, #ff758c);
      color: white;
      text-align: center;
    }
    section {
      padding: 60px 20px;
      max-width: 800px;
      margin: auto;
    }
    h1, h2 {
      margin-bottom: 20px;
    }
    p {
      font-size: 18px;
      line-height: 1.6;
    }
    .card {
      background: rgba(255, 255, 255, 0.15);
      padding: 30px;
      border-radius: 15px;
      margin-top: 30px;
    }
    button {
      margin-top: 30px;
      padding: 15px 30px;
      font-size: 18px;
      border: none;
      border-radius: 30px;
      background: #ffcc70;
      cursor: pointer;
    }
    button:hover {
      background: #ffd98e;
    }
    #bisous, #secret, #blague {
      margin-top: 30px;
      font-size: 22px;
    }
    footer {
      margin-top: 50px;
      font-size: 14px;
      opacity: 0.8;
    }
  </style>
</head>
<body>

  <!-- Accueil -->
  <section>
    <h1>🎉 Joyeux 19 ans, Soupou nene ! 🎉</h1>
    <p>19 ans et déjà un maître du rire et des bons moments !</p>
    <button onclick="scrollToNext()">Commence la surprise !</button>
  </section>

  <!-- Messages drôles -->
  <section class="card" id="section-blague">
    <h2>Messages drôles 😄</h2>
    <p id="blague">À 19 ans, tu réussis toujours à nous faire éclater de rire !</p>
    <button onclick="changerBlague()">Encore une surprise !</button>
  </section>

  <!-- Défis interactifs -->
  <section class="card">
    <h2>Défis interactifs 🎮</h2>
    <p>Quiz rigolo : Qui est le plus… ?</p>
    <button onclick="alert('Bien joué ! Tu es imbattable 😎')">Moi</button>
    <button onclick="alert('Haha, tu as choisi lui ! Pas mal 😄')">Soupou nene</button>
    <p>Ou lance un feu d’artifice 🎆</p>
    <button onclick="lancerFeu()">🎆 Feu d’artifice !</button>
    <div id="feu" style="margin-top:20px;font-size:30px;"></div>
  </section>

  <!-- 19 bisous animés -->
  <section class="card">
    <h2>19 bisous pour tes 19 ans 💋</h2>
    <button onclick="showBisous()">Clique pour recevoir tes bisous 🎁</button>
    <div id="bisous"></div>
  </section>

  <!-- Message final émotionnel -->
  <section class="card">
    <button onclick="showSecret()">Clique pour la surprise finale ✨</button>
    <div id="secret">
      <p>
        Soupou nene, je te souhaite tout le bonheur du monde 💙<br>
        Je suis tellement fière de toi : tu es devenu mature, réfléchi et responsable.<br>
        Je t’admire pour tout ce que tu es et tout ce que tu accomplis chaque jour.<br>
        Tu comptes énormément pour moi, et je suis vraiment heureuse de t’avoir dans ma vie.<br>
        Joyeux 19 ans, mon ami légendaire 🎂✨
      </p>
    </div>
  </section>

  <footer>
    Fait avec le cœur pour Soupou nene 💖
  </footer>

  <script>
    // Scroll vers la section suivante
    function scrollToNext() {
      document.getElementById("section-blague").scrollIntoView({behavior: "smooth"});
    }

    // Messages drôles
    const blagues = [
      "À 19 ans, tu réussis toujours à nous faire éclater de rire !",
      "Tes blagues sont toujours les meilleures 😄",
      "Le roi du rire est parmi nous !",
      "Tu transformes chaque moment en fou rire 😂"
    ];
    let blagueIndex = 0;
    function changerBlague() {
      blagueIndex = (blagueIndex + 1) % blagues.length;
      document.getElementById("blague").innerText = blagues[blagueIndex];
    }

    // Feu d’artifice simple
    function lancerFeu() {
      const feu = document.getElementById("feu");
      feu.innerHTML = "🎆🎇✨🎆🎇✨";
      setTimeout(()=>feu.innerHTML="",1000);
    }

    // Bisous animés
    const bisousDiv = document.getElementById("bisous");
    let countBisous = 0;
    const maxBisous = 19;
    function showBisous() {
      bisousDiv.innerHTML = "";
      countBisous = 0;
      const interval = setInterval(() => {
        if(countBisous < maxBisous) {
          bisousDiv.innerHTML += "💋";
          countBisous++;
        } else {
          clearInterval(interval);
        }
      }, 200);
    }

    // Surprise finale
    function showSecret() {
      document.getElementById("secret").style.display = "block";
      document.getElementById("secret").scrollIntoView({behavior: "smooth"});
    }
  </script>

</body>
</html>
