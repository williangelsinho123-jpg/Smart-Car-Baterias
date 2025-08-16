
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Smart Car Baterias</title>
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
  /* Reset e fontes */
  * { box-sizing:border-box; margin:0; padding:0; }
  body { font-family:'Roboto', sans-serif; background:#f8f8f8; }

  /* Header */
  header { background:#ff6600; color:white; padding:20px; text-align:center; position:relative; }
  header h1 { margin:0; }
  header p { margin-top:5px; }

  /* Menu flutuante */
  nav { display:flex; justify-content:center; background:#333; position:sticky; top:0; z-index:1000; }
  nav a { color:white; padding:15px 20px; text-decoration:none; transition:0.3s; }
  nav a:hover { background:#555; }

  /* Hero */
  .hero { text-align:center; padding:50px 20px; background:#ffe0cc; animation:fadeIn 1s; }
  .hero h2 { margin-bottom:20px; }
  .whatsapp-btn { display:inline-block; background:#25D366; color:white; padding:10px 20px; border-radius:50px; text-decoration:none; font-weight:bold; margin-top:20px; transition:0.3s; }
  .whatsapp-btn:hover { background:#1ebe57; }

  /* Filtros */
  .filters { text-align:center; margin:20px 0; }
  .filters select { padding:10px; margin:0 5px; border-radius:5px; border:1px solid #ccc; }

  /* Galeria */
  .baterias { display:flex; flex-wrap:wrap; justify-content:center; padding:20px; }
  .bateria-card { background:white; border-radius:10px; box-shadow:0 2px 5px rgba(0,0,0,0.2); margin:10px; padding:20px; width:220px; text-align:center; transition:transform 0.3s, box-shadow 0.3s; cursor:pointer; }
  .bateria-card:hover { transform:translateY(-5px); box-shadow:0 5px 15px rgba(0,0,0,0.3); }
  .bateria-card img { max-width:100%; border-radius:5px; animation:fadeIn 1s; }

  /* Formulário */
  .contact { text-align:center; padding:40px 20px; background:#333; color:white; }
  form { max-width:400px; margin:20px auto; display:flex; flex-direction:column; }
  form input, form select, form textarea { padding:10px; margin:10px 0; border-radius:5px; border:1px solid #ccc; }
  form button { padding:15px; background:#ff6600; color:white; border:none; border-radius:50px; font-weight:bold; cursor:pointer; transition:0.3s; }
  form button:hover { background:#e65c00; }

  /* Footer */
  footer { background:#222; color:white; text-align:center; padding:15px; }

  /* Animações */
  @keyframes fadeIn { from{opacity:0;} to{opacity:1;} }

  /* Responsivo */
  @media(max-width:600px){
    .bateria-card{width:90%;}
    nav { flex-direction:column; }
  }
</style>
</head>
<body>

<header>
  <h1>Smart Car Baterias</h1>
  <p>Av. Internacional, 431, Jd. Santo Antônio, Osasco</p>
</header>

<nav>
  <a href="#baterias">Baterias</a>
  <a href="#contato">Contato</a>
</nav>

<section class="hero">
  <h2>Baterias para todos os tipos de veículos!</h2>
  <p>Entrega e instalação rápida em Osasco e região</p>
  <a class="whatsapp-btn" href="https://wa.me/5511999999999" target="_blank">Fale Conosco no WhatsApp</a>
</section>

<section id="baterias">
  <div class="filters">
    <select id="tipoVeiculo">
      <option value="">Todos os veículos</option>
      <option value="carro">Carro</option>
      <option value="moto">Moto</option>
      <option value="caminhao">Caminhão</option>
    </select>
    <select id="marcaVeiculo">
      <option value="">Todas as marcas</option>
      <option value="chevrolet">Chevrolet</option>
      <option value="ford">Ford</option>
      <option value="volkswagen">Volkswagen</option>
      <option value="honda">Honda</option>
    </select>
  </div>

  <div class="baterias" id="bateriasContainer">
    <div class="bateria-card" data-tipo="carro" data-marca="chevrolet">
      <img src="https://via.placeholder.com/200x150?text=Carro+Chevrolet" alt="Bateria Carro Chevrolet">
      <h3>Carro Chevrolet</h3>
      <p>12V, garantia de 1 ano</p>
    </div>
    <div class="bateria-card" data-tipo="carro" data-marca="ford">
      <img src="https://via.placeholder.com/200x150?text=Carro+Ford" alt="Bateria Carro Ford">
      <h3>Carro Ford</h3>
      <p>12V, durabilidade e performance</p>
    </div>
    <div class="bateria-card" data-tipo="moto" data-marca="honda">
      <img src="https://via.placeholder.com/200x150?text=Moto+Honda" alt="Bateria Moto Honda">
      <h3>Moto Honda</h3>
      <p>12V, ideal para motos</p>
    </div>
    <div class="bateria-card" data-tipo="caminhao" data-marca="volkswagen">
      <img src="https://via.placeholder.com/200x150?text=Caminhão+VW" alt="Bateria Caminhão VW">
      <h3>Caminhão Volkswagen</h3>
      <p>Alta capacidade e resistência</p>
    </div>
  </div>
</section>

<section id="contato" class="contact">
  <h2>Solicite um Orçamento</h2>
  <p>Preencha o formulário e envie direto para nosso WhatsApp</p>

  <form id="formContato">
    <input type="text" name="nome" placeholder="Nome completo" required>
    <input type="tel" name="telefone" placeholder="Telefone" required>
    <select name="veiculo" required>
      <option value="">Tipo de veículo</option>
      <option value="carro">Carro</option>
      <option value="moto">Moto</option>
      <option value="caminhao">Caminhão</option>
    </select>
    <textarea name="mensagem" placeholder="Mensagem" rows="4" required></textarea>
    <button type="submit">Enviar Orçamento</button>
  </form>

  <a class="whatsapp-btn" href="https://wa.me/5511999999999" target="_blank">WhatsApp</a>
</section>

<footer>
  &copy; 2025 Smart Car Baterias - Todos os direitos reservados
</footer>

<script>
  // Filtro de baterias
  const tipoSelect = document.getElementById('tipoVeiculo');
  const marcaSelect = document.getElementById('marcaVeiculo');
  const baterias = document.querySelectorAll('.bateria-card');

  function filtrarBaterias() {
    const tipo = tipoSelect.value;
    const marca = marcaSelect.value;
    baterias.forEach(card => {
      const matchTipo = tipo === "" || card.dataset.tipo === tipo;
      const matchMarca = marca === "" || card.dataset.marca === marca;
      card.style.display = (matchTipo && matchMarca) ? 'block' : 'none';
    });
  }

  tipoSelect.addEventListener('change', filtrarBaterias);
  marcaSelect.addEventListener('change', filtrarBaterias);

  // Formulário envia direto para WhatsApp
  const form = document.getElementById('formContato');
  form.addEventListener('submit', function(e) {
    e.preventDefault();
    const nome = encodeURIComponent(form.nome.value);
    const telefone = encodeURIComponent(form.telefone.value);
    const veiculo = encodeURIComponent(form.veiculo.value);
    const mensagem = encodeURIComponent(form.mensagem.value);

    const textoWhats = `Olá! Meu nome é ${nome}, telefone: ${telefone}, veículo: ${veiculo}. Mensagem: ${mensagem}`;
    const numeroWhats = "5511999999999"; // Substitua pelo seu número
    const url = `https://wa.me/${numeroWhats}?text=${textoWhats}`;
    window.open(url, '_blank');
    form.reset();
  });
</script>

</body>
</html>
