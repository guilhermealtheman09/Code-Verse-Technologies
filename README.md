<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Codeverse Technologies</title>
  <style>
    :root {
      --primary: #003366;
      --secondary: #00bcd4;
      --background: #f4f8fb;
      --text-dark: #1a1a1a;
      --white: #ffffff;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--background);
      color: var(--text-dark);
    }

    header {
      background-color: var(--primary);
      color: var(--white);
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 999;
    }

    header h1 {
      font-size: 1.5em;
      margin: 0;
    }

    nav a {
      color: var(--white);
      text-decoration: none;
      margin-left: 20px;
      font-weight: bold;
      transition: color 0.3s;
      cursor: pointer;
    }

    nav a:hover {
      color: var(--secondary);
    }

    .btn {
      background: var(--secondary);
      color: var(--white);
      padding: 12px 28px;
      border: none;
      border-radius: 25px;
      text-decoration: none;
      font-weight: bold;
      transition: background 0.3s;
      display: inline-block;
      cursor: pointer;
    }

    .btn:hover {
      background: #0097a7;
    }

    .section {
      display: none;
      padding: 60px 20px;
      max-width: 1000px;
      margin: auto;
      animation: fadeIn 0.4s ease-in-out;
    }

    .section.active {
      display: block;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .hero {
      background: linear-gradient(to right, #003366, #0066cc);
      color: var(--white);
      text-align: center;
      padding: 100px 20px;
    }

    .hero h2 {
      font-size: 2.8em;
      margin-bottom: 20px;
    }

    .hero p {
      font-size: 1.2em;
      margin-bottom: 30px;
    }

    form {
      display: flex;
      flex-direction: column;
    }

    input, textarea, select {
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 1em;
    }

    footer {
      background-color: var(--primary);
      color: white;
      text-align: center;
      padding: 20px;
    }

    @media (max-width: 768px) {
      header {
        flex-direction: column;
        align-items: flex-start;
      }

      nav {
        margin-top: 10px;
      }

      nav a {
        display: block;
        margin: 10px 0;
      }

      .hero h2 {
        font-size: 2em;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Codeverse Technologies</h1>
    <nav>
      <a onclick="showSection('sobre')">Sobre</a>
      <a onclick="showSection('servicos')">Serviços</a>
      <a onclick="showSection('orcamento')">Orçamento</a>
      <a onclick="showSection('cadastro')">Cadastro</a>
      <a onclick="showSection('contato')">Contato</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Soluções SAP sob medida</h2>
    <p>Consultoria e tecnologia para empresas que querem crescer com eficiência.</p>
    <button class="btn" onclick="showSection('orcamento')">Solicite um Orçamento</button>
  </section>

  <section id="sobre" class="section">
    <h3>Quem Somos</h3>
    <p>
      A <strong>Codeverse Technologies</strong> é uma empresa de tecnologia especializada na transformação digital de negócios por meio de soluções SAP S/4HANA e SAP BTP (Business Technology Platform). Com uma equipe experiente e comprometida com resultados, oferecemos consultoria estratégica, desenvolvimento personalizado e integração entre sistemas. Nossa missão é impulsionar empresas a atingirem seu máximo potencial com inovação, eficiência e escalabilidade.
    </p>
  </section>

  <section id="servicos" class="section">
    <h3>Nossos Serviços</h3>
    <ul>
      <li>Consultoria SAP S/4HANA</li>
      <li>Suporte técnico e manutenção</li>
      <li>Integrações entre sistemas</li>
      <li>Desenvolvimento de soluções customizadas</li>
      <li>Treinamentos e capacitações corporativas</li>
    </ul>
  </section>

  <section id="orcamento" class="section">
    <h3>Solicite um Orçamento</h3>
    <form onsubmit="enviarOrcamento(event)">
      <input type="text" name="nome" placeholder="Nome completo" required>
      <input type="email" name="email" placeholder="E-mail" required id="orcamento-email">
      <input type="text" name="empresa" placeholder="Nome da empresa" required>
      <input type="tel" name="telefone" placeholder="Telefone para contato" required>
      <select name="servico" required>
        <option value="">Selecione um serviço</option>
        <option value="consultoria">Consultoria SAP S/4HANA</option>
        <option value="suporte">Suporte técnico</option>
        <option value="integracoes">Integrações de sistemas</option>
        <option value="customizado">Soluções customizadas</option>
        <option value="treinamento">Treinamentos corporativos</option>
      </select>
      <textarea name="detalhes" rows="5" placeholder="Descreva o que sua empresa precisa..."></textarea>
      <button type="submit" class="btn">Solicitar Orçamento</button>
    </form>
  </section>

  <section id="cadastro" class="section">
    <h3>Cadastro de Interesse</h3>
    <form>
      <input type="text" name="nome" placeholder="Nome completo" required>
      <input type="email" name="email" placeholder="E-mail" required>
      <input type="text" name="empresa" placeholder="Empresa (opcional)">
      <textarea name="mensagem" rows="5" placeholder="Descreva sua necessidade ou dúvida..."></textarea>
      <button type="submit" class="btn">Enviar Cadastro</button>
    </form>
  </section>

  <section id="contato" class="section">
    <h3>Contato</h3>
    <p>📞 Telefone: (11) 3948-9823</p>
    <p>📧 E-mail: contato@codeverse.com.br</p>
    <p>📍 Endereço: Av. Inovação, 1010 – São Paulo, SP</p>
  </section>

  <section id="confirmacao" class="section">
    <h3>Orçamento em Andamento</h3>
    <p>Recebemos sua solicitação e estamos trabalhando nela.</p>
    <p>Em breve entraremos em contato pelo e-mail: <strong id="email-confirmado"></strong></p>
  </section>

  <footer>
    <p>&copy; 2025 Codeverse Technologies. Todos os direitos reservados.</p>
  </footer>

  <script>
    function showSection(id) {
      const sections = document.querySelectorAll('.section');
      sections.forEach(section => section.classList.remove('active'));
      document.getElementById(id).classList.add('active');
      window.scrollTo(0, 0);
    }

    function enviarOrcamento(event) {
      event.preventDefault();
      const email = document.getElementById('orcamento-email').value;
      document.getElementById('email-confirmado').textContent = email;
      showSection('confirmacao');
    }

    window.onload = () => showSection('sobre');
  </script>

</body>
</html>
