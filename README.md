<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Cuidado Ambiental</title>

  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #0d1117;
      color: #e6edf3;
    }

    header {
      background: #161b22;
      padding: 20px;
      text-align: center;
      border-bottom: 2px solid #2ea043;
    }

    h1 {
      color: #2ea043;
      margin: 0;
    }

    nav {
      display: flex;
      justify-content: center;
      gap: 15px;
      padding: 10px;
      background: #0d1117;
    }

    nav button {
      background: #2ea043;
      border: none;
      padding: 10px 15px;
      color: white;
      cursor: pointer;
      border-radius: 5px;
    }

    nav button:hover {
      background: #238636;
    }

    section {
      padding: 20px;
      display: none;
    }

    section.active {
      display: block;
    }

    .card {
      background: #161b22;
      padding: 15px;
      margin: 10px 0;
      border-left: 4px solid #2ea043;
      border-radius: 5px;
    }

    footer {
      text-align: center;
      padding: 15px;
      background: #161b22;
      margin-top: 20px;
      font-size: 14px;
    }
  </style>
</head>

<body>

<header>
  <h1>🌍 Cuidado Ambiental</h1>
  <p>Protejamos el planeta juntos</p>
</header>

<nav>
  <button onclick="mostrar('inicio')">Inicio</button>
  <button onclick="mostrar('problemas')">Problemas</button>
  <button onclick="mostrar('soluciones')">Soluciones</button>
  <button onclick="mostrar('acciones')">Acciones</button>
</nav>

<section id="inicio" class="active">
  <div class="card">
    <h2>¿Por qué es importante?</h2>
    <p>El cuidado ambiental es fundamental para la vida en la Tierra. Nos permite conservar los recursos naturales y garantizar un futuro sostenible.</p>
  </div>

  <div class="card">
    <h2>Impacto humano</h2>
    <p>Las actividades humanas como la contaminación, la deforestación y el consumo excesivo afectan gravemente al planeta.</p>
  </div>
</section>

<section id="problemas">
  <div class="card">
    <h2>🌫 Contaminación</h2>
    <p>El aire, agua y suelo están siendo contaminados por industrias y residuos.</p>
  </div>

  <div class="card">
    <h2>🌳 Deforestación</h2>
    <p>La tala masiva destruye hábitats y reduce la biodiversidad.</p>
  </div>

  <div class="card">
    <h2>🔥 Cambio climático</h2>
    <p>El aumento de gases de efecto invernadero provoca calentamiento global.</p>
  </div>
</section>

<section id="soluciones">
  <div class="card">
    <h2>♻ Reciclaje</h2>
    <p>Separar residuos ayuda a reducir la contaminación.</p>
  </div>

  <div class="card">
    <h2>🔋 Energías renovables</h2>
    <p>Utilizar energía solar y eólica disminuye el impacto ambiental.</p>
  </div>

  <div class="card">
    <h2>🚲 Transporte sostenible</h2>
    <p>Usar bicicleta o transporte público reduce emisiones.</p>
  </div>
</section>

<section id="acciones">
  <div class="card">
    <h2>💡 ¿Qué podés hacer?</h2>
    <ul>
      <li>Apagar luces innecesarias</li>
      <li>Reducir el uso de plástico</li>
      <li>Ahorrar agua</li>
      <li>Plantar árboles</li>
    </ul>
  </div>

  <div class="card">
    <h2>🌱 Calculador ecológico</h2>
    <p>¿Cuántas acciones hiciste hoy?</p>
    <input type="number" id="accionesInput" placeholder="Ej: 3">
    <button onclick="calcularImpacto()">Calcular impacto</button>
    <p id="resultado"></p>
  </div>
</section>

<footer>
  © 2026 - Cuidado Ambiental
</footer>

<script>
  function mostrar(seccion) {
    document.querySelectorAll("section").forEach(sec => {
      sec.classList.remove("active");
    });
    document.getElementById(seccion).classList.add("active");
  }

  function calcularImpacto() {
    let acciones = document.getElementById("accionesInput").value;
    let resultado = document.getElementById("resultado");

    if (acciones > 0) {
      resultado.textContent = "🌍 ¡Buen trabajo! Estás ayudando al planeta.";
    } else {
      resultado.textContent = "⚠ Intenta hacer al menos una acción ecológica hoy.";
    }
  }
</script>

</body>
</html>
