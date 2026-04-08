[projeto notesvets.html](https://github.com/user-attachments/files/26581660/projeto.notesvets.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>NotesVets · Diversão em Patas</title>
    <!-- Fontes divertidas e ícones -->
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Quicksand', sans-serif;
            background-color: #f0f9f4;
            color: #2c4a3e;
            scroll-behavior: smooth;
        }

        /* NOVAS CORES: Verde claro + Azul */
        :root {
            --verde-claro: #6fbf8a;
            --verde-escuro: #3a7c5c;
            --azul-claro: #7bc5d9;
            --azul-escuro: #2c7da0;
            --azul-suave: #d4eef5;
            --verde-suave: #e0f5e8;
            --sombra: 0 8px 20px rgba(0,0,0,0.05);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 24px;
        }

        /* header */
        header {
            background-color: white;
            box-shadow: 0 2px 12px rgba(0,0,0,0.03);
            position: sticky;
            top: 0;
            z-index: 100;
            backdrop-filter: blur(2px);
            background-color: rgba(255, 255, 255, 0.95);
        }

        .navbar {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            padding: 16px 0;
        }

        .logo {
            display: flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
        }

        .logo img {
            height: 50px;
            width: auto;
        }

        .logo span {
            color: var(--azul-claro);
            font-size: 0.9rem;
            font-weight: 600;
        }

        .nav-links {
            display: flex;
            gap: 28px;
            flex-wrap: wrap;
        }

        .nav-links a {
            text-decoration: none;
            font-weight: 600;
            color: #2c4a3e;
            transition: 0.2s;
        }

        .nav-links a:hover {
            color: var(--azul-claro);
            transform: scale(1.02);
        }

        .btn-whatsapp-nav {
            background-color: #25d366;
            padding: 8px 20px;
            border-radius: 40px;
            color: white !important;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        /* seção hero */
        .hero {
            background: linear-gradient(120deg, var(--verde-suave), var(--azul-suave));
            padding: 60px 0;
            border-radius: 0 0 60px 60px;
        }

        .hero-grid {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }

        .hero-text {
            flex: 1;
        }

        .hero-text h2 {
            font-size: 2.8rem;
            font-weight: 700;
            color: var(--verde-escuro);
        }

        .hero-text p {
            font-size: 1.2rem;
            margin: 20px 0;
        }

        .hero-img {
            flex: 1;
            text-align: center;
        }

        .hero-img img {
            max-width: 100%;
            border-radius: 20px;
            box-shadow: var(--sombra);
        }

        /* botões */
        .btn {
            display: inline-block;
            background-color: var(--azul-claro);
            color: white;
            padding: 12px 28px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            transition: 0.2s;
            border: none;
            cursor: pointer;
            font-family: 'Quicksand', sans-serif;
        }

        .btn:hover {
            background-color: var(--azul-escuro);
            transform: translateY(-3px);
        }

        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--azul-claro);
            color: var(--azul-claro);
        }

        /* serviços */
        .section {
            padding: 70px 0;
        }

        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 48px;
            position: relative;
            color: var(--verde-escuro);
        }

        .section-title:after {
            content: "🐾";
            display: block;
            font-size: 2rem;
            opacity: 0.6;
        }

        .cards {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
        }

        .card {
            background: white;
            border-radius: 40px;
            padding: 30px 20px;
            text-align: center;
            flex: 1 1 240px;
            box-shadow: var(--sombra);
            transition: 0.2s;
            border-bottom: 5px solid var(--azul-claro);
        }

        .card i {
            font-size: 3rem;
            color: var(--verde-claro);
            margin-bottom: 20px;
        }

        .card h3 {
            margin-bottom: 12px;
            color: var(--verde-escuro);
        }

        .card:hover {
            transform: translateY(-8px);
        }

        /* Destaque para o card de consultas com a domicílio */
        .card-consulta {
            position: relative;
        }

        .badge-domicilio {
            display: inline-block;
            background-color: var(--azul-claro);
            color: white;
            font-size: 0.8rem;
            padding: 4px 12px;
            border-radius: 30px;
            margin-top: 10px;
            font-weight: 600;
        }

        /* galeria do ambiente */
        .galeria {
            background-color: var(--verde-suave);
            border-radius: 70px;
        }

        .grid-fotos {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .grid-fotos img {
            width: 100%;
            height: 220px;
            object-fit: cover;
            border-radius: 32px;
            box-shadow: var(--sombra);
            transition: 0.2s;
        }

        .grid-fotos img:hover {
            transform: scale(1.02);
        }

        /* depoimentos */
        .depoimentos-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }

        .depoimento {
            background: white;
            padding: 24px;
            border-radius: 32px;
            flex: 1;
            font-style: italic;
            border-left: 8px solid var(--azul-claro);
        }

        /* formulário de reserva hospedagem */
        .reserva-box {
            background: white;
            border-radius: 60px;
            padding: 40px;
            box-shadow: var(--sombra);
            max-width: 800px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            font-weight: 600;
            display: block;
            margin-bottom: 8px;
        }

        input, select, textarea {
            width: 100%;
            padding: 14px 18px;
            border-radius: 40px;
            border: 1px solid var(--azul-claro);
            background-color: #fffbf5;
            font-family: 'Quicksand', sans-serif;
        }

        .whatsapp-btn-submit {
            background-color: #25d366;
            width: 100%;
            font-size: 1.1rem;
        }

        .info-extra {
            text-align: center;
            margin-top: 20px;
            font-size: 0.9rem;
        }

        footer {
            background-color: var(--verde-suave);
            text-align: center;
            padding: 30px 0;
            border-radius: 40px 40px 0 0;
            margin-top: 50px;
        }

        @media (max-width: 760px) {
            .navbar {
                flex-direction: column;
                gap: 12px;
                text-align: center;
            }
            .hero-text h2 {
                font-size: 2rem;
            }
            .logo {
                justify-content: center;
            }
        }
    </style>
</head>
<body>

<header>
    <div class="container">
        <div class="navbar">
            <div class="logo">
                <img src="imagens/logo.png" alt="NotesVets 
                <span>Diversão em Patas · Hotel · Creche · Consultas</span>
            </div>
            <div class="nav-links">
                <a href="#servicos">Serviços</a>
                <a href="#ambiente">Ambiente</a>
                <a href="#resultados">Resultados</a>
                <a href="#hospedagem">Hospedagem</a>
                <a href="#contato" class="btn-whatsapp-nav"><i class="fab fa-whatsapp"></i> WhatsApp</a>
            </div>
        </div>
    </div>
</header>

<main>
    <!-- HERO -->
    <section class="hero">
        <div class="container hero-grid">
            <div class="hero-text">
                <h2>🐕 Diversão em Patas</h2>
                <p>Hotelzinho com supervisão veterinária, creche animada, adestramento positivo e consultas veterinárias (inclusive a domicílio!). Aqui seu melhor amigo é tratado como família!</p>
                <a href="#hospedagem" class="btn"><i class="fas fa-calendar-check"></i> Reservar Hospedagem</a>
                <a href="#contato" class="btn btn-outline" style="margin-left: 12px;"><i class="fab fa-whatsapp"></i> Falar com equipe</a>
            </div>
            <div class="hero-img">
                <img src="https://placehold.co/500x400/A8E6CF/2c4a3e?text=Cachorros+felizes+🐕‍🦺🐩" alt="Cães felizes no hotel">
                <p style="font-size: 0.7rem; margin-top: 8px;">🐾 momentos reais no NotesVets</p>
            </div>
        </div>
    </section>

    <!-- SERVIÇOS -->
    <section id="servicos" class="section">
        <div class="container">
            <div class="section-title">Nossos serviços 💚</div>
            <div class="cards">
                <div class="card"><i class="fas fa-home"></i><h3>Hospedagem</h3><p>24h com monitoramento, camas fofinhas e rotina de passeios.</p></div>
                <div class="card"><i class="fas fa-paw"></i><h3>Creche</h3><p>Socialização, brincadeiras e muito carinho durante o dia.</p></div>
                <div class="card"><i class="fas fa-dog"></i><h3>Adestramento</h3><p>Positivo e personalizado: comandos, ansiedade e comportamento.</p></div>
                <div class="card card-consulta">
                    <i class="fas fa-stethoscope"></i>
                    <h3>Consultas Veterinárias</h3>
                    <p>Atendimento clínico completo e preventivo.</p>
                    <span class="badge-domicilio"><i class="fas fa-home"></i> a domicílio também!</span>
                </div>
                <div class="card"><i class="fas fa-walking"></i><h3>Passeios</h3><p>Guiados por profissionais, enriquecimento ambiental.</p></div>
                <div class="card"><i class="fas fa-bath"></i><h3>Banho & Tosa</h3><p>Higiene e conforto com produtos específicos.</p></div>
            </div>
        </div>
    </section>

    <!-- AMBIENTE -->
    <section id="ambiente" class="section galeria">
        <div class="container">
            <div class="section-title">🐕 Nosso espaço divertido e seguro</div>
            <div class="grid-fotos">
                <img src="https://placehold.co/400x300/A8E6CF/2c4a3e?text=Área+externa+gramada" alt="Área externa">
                <img src="https://placehold.co/400x300/7BC5D9/2c4a3e?text=Sala+de+brinquedos" alt="Brinquedoteca pet">
                <img src="https://placehold.co/400x300/A8E6CF/2c4a3e?text=Quartinho+aconchegante" alt="Quarto individual">
                <img src="https://placehold.co/400x300/7BC5D9/2c4a3e?text=Consultório+veterinário" alt="Consultório">
            </div>
            <p style="text-align: center; margin-top: 28px;">🏡 Câmeras em tempo real · Higienização diária · Supervisão veterinária 24/7</p>
        </div>
    </section>

    <!-- RESULTADOS e Feedbacks -->
    <section id="resultados" class="section">
        <div class="container">
            <div class="section-title">Resultados que viram rabinho feliz 🐾</div>
            <div class="depoimentos-grid">
                <div class="depoimento">
                    <i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i>
                    <p>"Meu Thor voltou da creche mais calmo e sociável! O adestramento fez toda diferença. Ambiente muito alegre."</p>
                    <strong>— Mariana (Bella e Thor)</strong>
                </div>
                <div class="depoimento">
                    <i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i>
                    <p>"Hospedagem nota 10! Enquanto viajávamos, recebíamos fotos e vídeos. Equipe veterinária sempre atenta."</p>
                    <strong>— Ricardo & Luna</strong>
                </div>
                <div class="depoimento">
                    <i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i><i class="fas fa-star" style="color: #7bc5d9;"></i>
                    <p>"Além do atendimento clínico impecável, o hotelzinho tem brinquedos e piscininha. Meu cachorro não quer ir embora!"</p>
                    <strong>— Camila (Bob)</strong>
                </div>
            </div>
        </div>
    </section>

    <!-- HOSPEDAGEM - FECHAR SERVIÇO -->
    <section id="hospedagem" class="section" style="background-color: #e8f4f0;">
        <div class="container">
            <div class="section-title">📅 Reserve a hospedagem do seu melhor amigo</div>
            <div class="reserva-box">
                <p style="margin-bottom: 20px;"><i class="fas fa-shield-alt"></i> Preencha os dados e finalizamos pelo WhatsApp com segurança e rapidez!</p>
                <form id="formReserva">
                    <div class="form-group">
                        <label>Nome do tutor:</label>
                        <input type="text" id="nomeTutor" placeholder="Seu nome completo" required>
                    </div>
                    <div class="form-group">
                        <label>Nome do pet 🐕:</label>
                        <input type="text" id="nomePet" placeholder="Ex: Thor, Luna, Mel" required>
                    </div>
                    <div class="form-group">
                        <label>Data de entrada:</label>
                        <input type="date" id="dataInicio" required>
                    </div>
                    <div class="form-group">
                        <label>Data de saída:</label>
                        <input type="date" id="dataFim" required>
                    </div>
                    <div class="form-group">
                        <label>Necessidades especiais (medicação, alimentação, etc):</label>
                        <textarea rows="2" id="obs" placeholder="Ex: ração específica, remédio às 20h..."></textarea>
                    </div>
                    <div class="form-group">
                        <label>Seu WhatsApp (com DDD):</label>
                        <input type="tel" id="whatsapp" placeholder="(11) 99999-1234" required>
                    </div>
                    <button type="button" id="btnFinalizarReserva" class="btn whatsapp-btn-submit"><i class="fab fa-whatsapp"></i> Finalizar reserva pelo WhatsApp</button>
                </form>
                <div class="info-extra">
                    <p>🔒 Após clicar, você será redirecionado ao WhatsApp com uma pré-reserva. Nossa equipe confirma disponibilidade e envia valores.</p>
                    <p>🏆 <strong>Supervisão veterinária inclusa em todas as diárias!</strong></p>
                </div>
            </div>
        </div>
    </section>

    <!-- CONTATO FINAL -->
    <section id="contato" class="section">
        <div class="container" style="text-align: center;">
            <div class="section-title">📍 Estamos prontos para te atender</div>
            <p style="font-size: 1.2rem;"><i class="fab fa-whatsapp"></i> <strong>WhatsApp:</strong> (11) 91234-5678 (clique no botão abaixo)</p>
            <p><i class="fas fa-map-marker-alt"></i> Av. dos Pets, 777 - Bairro Alegria | SP</p>
            <p><i class="fas fa-clock"></i> Hotel e creche: 24h | Consultas: seg-sáb 8h-19h (inclusive a domicílio)</p>
            <div style="margin-top: 30px;">
                <a href="https://wa.me/5511912345678?text=Olá%20NotesVets!%20Vi%20o%20site%20e%20gostaria%20de%20mais%20informações%20sobre%20hospedagem%20e%20serviços." target="_blank" class="btn" style="background-color: #25d366;"><i class="fab fa-whatsapp"></i> Conversar agora</a>
                <a href="#hospedagem" class="btn btn-outline" style="margin-left: 15px;"><i class="fas fa-calendar-alt"></i> Reservar hospedagem</a>
            </div>
        </div>
    </section>
</main>

<footer>
    <div class="container">
        <p>🐾 NotesVets · Diversão em Patas · Cuidado que transforma medo em alegria 🐾</p>
        <p><i class="fab fa-instagram"></i> @notesvets · <i class="fab fa-whatsapp"></i> (11) 91234-5678</p>
        <small>© 2026 · Hotel, Creche & Consultas Veterinárias (a domicílio disponível)</small>
    </div>
</footer>

<script>
    // Botão de reserva via WhatsApp
    document.getElementById('btnFinalizarReserva').addEventListener('click', function() {
        const nomeTutor = document.getElementById('nomeTutor').value.trim();
        const nomePet = document.getElementById('nomePet').value.trim();
        const dataInicio = document.getElementById('dataInicio').value;
        const dataFim = document.getElementById('dataFim').value;
        const obs = document.getElementById('obs').value.trim();
        let whatsapp = document.getElementById('whatsapp').value.trim();

        if (!nomeTutor || !nomePet || !dataInicio || !dataFim || !whatsapp) {
            alert("🐶 Por favor, preencha todos os campos obrigatórios: tutor, pet, datas e seu WhatsApp.");
            return;
        }

        if (new Date(dataInicio) > new Date(dataFim)) {
            alert("A data de saída precisa ser depois da data de entrada 🗓️");
            return;
        }

        whatsapp = whatsapp.replace(/\D/g, '');
        if (whatsapp.length < 10 || whatsapp.length > 13) {
            alert("Por favor, insira um número de WhatsApp válido com DDD (ex: 11999991234)");
            return;
        }

        const numeroNegocio = "5511912345678";

        let mensagem = `🐕 *NOVA RESERVA - NOTESVETS* 🐕%0A%0A`;
        mensagem += `*Tutor(a):* ${nomeTutor}%0A`;
        mensagem += `*Pet:* ${nomePet}%0A`;
        mensagem += `*Entrada:* ${dataInicio}%0A`;
        mensagem += `*Saída:* ${dataFim}%0A`;
        if (obs) mensagem += `*Observações:* ${obs}%0A`;
        mensagem += `*WhatsApp tutor:* ${whatsapp}%0A%0A`;
        mensagem += `Gostaria de confirmar disponibilidade e valores. Aguardo contato. 🐾`;

        const urlWhats = `https://wa.me/${numeroNegocio}?text=${mensagem}`;
        window.open(urlWhats, '_blank');
    });
</script>
</body>
</html>
