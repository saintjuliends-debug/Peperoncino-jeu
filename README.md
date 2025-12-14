# Peperoncino-jeu
Jeu cadeau interactif pour restaurant (type BoxMysteryGift). Page web gratuite en HTML / CSS / JavaScript permettant aux clients de découvrir un cadeau aléatoire (réduction, dessert, boisson). Idéal pour utilisation via QR code en restaurant.

<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cadeau Mystère - Peperoncino</title>

  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #1c1c1c, #3a3a3a);
      color: white;
      text-align: center;
      padding: 30px;
    }

    .box {
      max-width: 400px;
      margin: auto;
      background: #111;
      border-radius: 15px;
      padding: 25px;
      box-shadow: 0 0 20px rgba(0,0,0,0.6);
    }

    h1 {
      margin-bottom: 10px;
    }

    button {
      background: #e63946;
      color: white;
      border: none;
      padding: 15px 25px;
      font-size: 18px;
      border-radius: 10px;
      cursor: pointer;
      margin-top: 20px;
    }

    button:hover {
      background: #ff4d5a;
    }

    #resultat {
      margin-top: 25px;
      font-size: 20px;
      font-weight: bold;
    }

    .conditions {
      font-size: 12px;
      opacity: 0.7;
      margin-top: 20px;
    }
  </style>
</head>

<body>

  <div class="box">
    <h1>🎁 Cadeau Mystère</h1>
    <p>Bienvenue chez <strong>Peperoncino</strong><br>
    Cliquez pour découvrir votre cadeau !</p>

    <button onclick="tirage()">Découvrir mon cadeau</button>

    <div id="resultat"></div>

    <div class="conditions">
      Offre valable une seule fois par table.<br>
      Présenter ce cadeau au serveur.
    </div>
  </div>

  <script>
    const cadeaux = [
      "🎉 10% de réduction sur la note",
      "🍰 1 dessert maison offert",
      "🍹 1 cocktail sans alcool offert"
    ];

    function tirage() {
      const hasard = Math.floor(Math.random() * cadeaux.length);
      document.getElementById("resultat").innerText = cadeaux[hasard];
    }
  </script>

</body>
</html>
