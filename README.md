<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README Rosa & Preto ✨</title>
    <style>
        body {
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 50%, #2d1b2e 100%);
            margin: 0;
            padding: 20px;
            min-height: 100vh;
            color: #ffffff;
        }
        
        .readme-container {
            max-width: 900px;
            margin: 0 auto;
            background: rgba(20, 20, 20, 0.95);
            border-radius: 25px;
            padding: 50px;
            box-shadow: 0 25px 50px rgba(255, 20, 147, 0.1);
            border: 1px solid rgba(255, 20, 147, 0.2);
            backdrop-filter: blur(10px);
        }
        
        .header {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .title {
            font-size: 3.5rem;
            font-weight: bold;
            background: linear-gradient(45deg, #ff1493, #ff69b4, #ffc0cb, #ff1493);
            background-size: 300% 300%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            animation: gradientShift 4s ease-in-out infinite;
            margin-bottom: 20px;
            text-shadow: 0 0 30px rgba(255, 20, 147, 0.5);
        }
        
        @keyframes gradientShift {
            0%, 100% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
        }
        
        .subtitle {
            font-size: 1.3rem;
            color: #ff69b4;
            margin-bottom: 30px;
            font-weight: 300;
        }
        
        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }
        
        .floating-heart {
            position: absolute;
            color: #ff1493;
            font-size: 1.5rem;
            animation: float 6s ease-in-out infinite;
            opacity: 0.7;
        }
        
        .floating-heart:nth-child(1) { top: 10%; left: 10%; animation-delay: 0s; }
        .floating-heart:nth-child(2) { top: 20%; right: 15%; animation-delay: 2s; }
        .floating-heart:nth-child(3) { bottom: 30%; left: 20%; animation-delay: 4s; }
        .floating-heart:nth-child(4) { bottom: 10%; right: 10%; animation-delay: 1s; }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            33% { transform: translateY(-20px) rotate(5deg); }
            66% { transform: translateY(10px) rotate(-3deg); }
        }
        
        .section {
            margin-bottom: 45px;
            position: relative;
        }
        
        .section-title {
            font-size: 1.8rem;
            font-weight: 600;
            color: #ff69b4;
            margin-bottom: 25px;
            text-align: center;
            position: relative;
        }
        
        .section-title::before,
        .section-title::after {
            content: '✨';
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            color: #ff1493;
            animation: sparkle 2s ease-in-out infinite;
        }
        
        .section-title::before { left: -40px; }
        .section-title::after { right: -40px; animation-delay: 1s; }
        
        .section-content {
            background: linear-gradient(135deg, rgba(255, 20, 147, 0.1) 0%, rgba(0, 0, 0, 0.3) 100%);
            padding: 30px;
            border-radius: 20px;
            border: 1px solid rgba(255, 105, 180, 0.3);
            backdrop-filter: blur(5px);
        }
        
        .skill-list {
            list-style: none;
            padding: 0;
            margin: 20px 0;
        }
        
        .skill-item {
            margin: 15px 0;
            padding: 12px 0;
            color: #ffffff;
            font-size: 1.1rem;
            transition: transform 0.3s ease;
        }
        
        .skill-item:hover {
            transform: translateX(10px);
            color: #ff69b4;
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 20px;
            margin-top: 25px;
        }
        
        .tech-item {
            background: linear-gradient(135deg, rgba(255, 20, 147, 0.2), rgba(0, 0, 0, 0.5));
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(255, 105, 180, 0.3);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .tech-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 30px rgba(255, 20, 147, 0.3);
        }
        
        .tech-icon {
            font-size: 2.5rem;
            margin-bottom: 10px;
            display: block;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 25px;
            margin-top: 25px;
        }
        
        .stat-card {
            background: linear-gradient(135deg, rgba(255, 20, 147, 0.15), rgba(0, 0, 0, 0.4));
            padding: 25px;
            border-radius: 20px;
            text-align: center;
            border: 1px solid rgba(255, 105, 180, 0.4);
            transition: transform 0.3s ease;
        }
        
        .stat-card:hover {
            transform: scale(1.05);
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #ff1493;
            margin-bottom: 10px;
        }
        
        .stat-label {
            color: #ff69b4;
            font-weight: 500;
        }
        
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 25px;
            flex-wrap: wrap;
            margin-top: 25px;
        }
        
        .contact-link {
            background: linear-gradient(45deg, #ff1493, #ff69b4);
            color: white;
            padding: 15px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 2px solid transparent;
        }
        
        .contact-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(255, 20, 147, 0.4);
            border-color: #ff69b4;
        }
        
        .quote-section {
            text-align: center;
            background: linear-gradient(135deg, rgba(255, 20, 147, 0.1), rgba(0, 0, 0, 0.2));
            padding: 30px;
            border-radius: 20px;
            border: 1px solid rgba(255, 105, 180, 0.3);
            margin: 40px 0;
        }
        
        .quote {
            font-size: 1.3rem;
            font-style: italic;
            color: #ff69b4;
            margin-bottom: 15px;
        }
        
        .footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 2px solid rgba(255, 105, 180, 0.3);
            color: #ff69b4;
        }
        
        .sparkle {
            animation: sparkle 2s ease-in-out infinite;
        }
        
        @keyframes sparkle {
            0%, 100% { opacity: 1; transform: scale(1); }
            50% { opacity: 0.5; transform: scale(1.2); }
        }
        
        .progress-bar {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            overflow: hidden;
            margin: 10px 0;
        }
        
        .progress-fill {
            height: 8px;
            background: linear-gradient(90deg, #ff1493, #ff69b4);
            border-radius: 10px;
            animation: progressLoad 2s ease-out;
        }
        
        @keyframes progressLoad {
            from { width: 0%; }
        }
        
        .current-focus {
            background: linear-gradient(135deg, rgba(255, 20, 147, 0.2), rgba(0, 0, 0, 0.3));
            padding: 25px;
            border-radius: 15px;
            border-left: 5px solid #ff1493;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <div class="readme-container">
        <div class="floating-elements">
            <div class="floating-heart">💖</div>
            <div class="floating-heart">✨</div>
            <div class="floating-heart">🌸</div>
            <div class="floating-heart">💫</div>
        </div>
        
        <div class="header">
            <h1 class="title">✨ Olá, mundo! ✨</h1>
            <p class="subtitle">Estudante de Sistemas de Informação apaixonada por tecnologia 💖</p>
        </div>

        <div class="quote-section">
            <div class="quote">"O código é poesia em movimento, cada linha uma nova possibilidade"</div>
            <div style="color: #ff1493;">~ Desenvolvendo sonhos em bytes ~</div>
        </div>

        <div class="section">
            <h2 class="section-title">Sobre Mim</h2>
            <div class="section-content">
                <p>Olá! Sou uma estudante apaixonada por tecnologia, sempre em busca de novos desafios e aprendizados. Acredito que a programação é uma forma de arte que nos permite criar soluções incríveis para o mundo! 🌟</p>
                
                <div class="current-focus">
                    <h4 style="color: #ff69b4; margin-top: 0;">🎯 Foco Atual</h4>
                    <p>Mergulhando fundo no desenvolvimento web front-end e explorando o fascinante mundo da inteligência artificial!</p>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">Habilidades & Ferramentas</h2>
            <div class="section-content">
                <p>Estou constantemente aprendendo e explorando diversas tecnologias:</p>
                
                <div class="tech-grid">
                    <div class="tech-item">
                        <span class="tech-icon">🐍</span>
                        <div>Python</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 75%;"></div>
                        </div>
                    </div>
                    <div class="tech-item">
                        <span class="tech-icon">⚡</span>
                        <div>JavaScript</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 70%;"></div>
                        </div>
                    </div>
                    <div class="tech-item">
                        <span class="tech-icon">☕</span>
                        <div>Java</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 65%;"></div>
                        </div>
                    </div>
                    <div class="tech-item">
                        <span class="tech-icon">⚙️</span>
                        <div>C++</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 60%;"></div>
                        </div>
                    </div>
                    <div class="tech-item">
                        <span class="tech-icon">🎨</span>
                        <div>HTML/CSS</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 80%;"></div>
                        </div>
                    </div>
                    <div class="tech-item">
                        <span class="tech-icon">📝</span>
                        <div>LaTeX</div>
                        <div class="progress-bar">
                            <div class="progress-fill" style="width: 55%;"></div>
                        </div>
                    </div>
                </div>
                
                <ul class="skill-list">
                    <li class="skill-item">╰┈➤ <strong>Conceitos:</strong> Lógica de programação, Estruturas de dados, Algoritmos</li>
                    <li class="skill-item">╰┈➤ <strong>Ferramentas:</strong> Git, VS Code, Pacote Office, Figma</li>
                    <li class="skill-item">╰┈➤ <strong>Interesses:</strong> Desenvolvimento web, UX/UI, IA, Análise de dados, Redes</li>
                </ul>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">Estatísticas GitHub</h2>
            <div class="section-content">
                <div class="stats-container">
                    <div class="stat-card">
                        <div class="stat-number">25+</div>
                        <div class="stat-label">Repositórios</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">500+</div>
                        <div class="stat-label">Commits</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">8</div>
                        <div class="stat-label">Linguagens</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">∞</div>
                        <div class="stat-label">Café consumido</div>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">Projetos em Destaque</h2>
            <div class="section-content">
                <div class="tech-grid">
                    <div class="tech-item">
                        <span class="tech-icon">🌐</span>
                        <div><strong>Portfolio Web</strong></div>
                        <div style="font-size: 0.9rem; color: #ff69b4; margin-top: 8px;">HTML, CSS, JavaScript</div>
                    </div>
                    <div class="tech-item">
                        <span class="tech-icon">📊</span>
                        <div><strong>Análise de Dados</strong></div>
                        <div style="font-size: 0.9rem; color: #ff69b4; margin-top: 8px;">Python, Pandas, Matplotlib</div>
                    </div>
                    <div class="tech-item">
                        <span class="tech-icon">🎮</span>
                        <div><strong>Jogo em Java</strong></div>
                        <div style="font-size: 0.9rem; color: #ff69b4; margin-top: 8px;">Java, Swing, POO</div>
                    </div>
                </div>
            </div>
        </div>

        <div class="section">
            <h2 class="section-title">Contato & Conexões</h2>
            <div class="section-content">
                <ul class="skill-list">
                    <li class="skill-item">╰┈➤ <strong>Lattes:</strong> <a href="http://lattes.cnpq.br/" target="_blank" rel="noopener noreferrer" style="color: #ff69b4;">http://lattes.cnpq.br/</a></li>
                    <li class="skill-item">╰┈➤ <strong>E-mail:</strong> <a href="mailto:fragosoamabile2017@gmail.com" style="color: #ff69b4;">fragosoamabile2017@gmail.com</a></li>
                </ul>
                
                <div class="contact-links">
                    <a href="mailto:fragosoamabile2017@gmail.com" class="contact-link">📧 Email</a>
                    <a href="http://lattes.cnpq.br/" target="_blank" rel="noopener noreferrer" class="contact-link">📄 Lattes</a>
                    <a href="#" class="contact-link">💼 LinkedIn</a>
                    <a href="#" class="contact-link">🐱 GitHub</a>
                </div>
            </div>
        </div>

        <div class="footer">
            <p class="sparkle">✨ "Transformando café em código, uma linha por vez" ✨</p>
            <p>Feito com 💖 e muito amor pela programação</p>
            <p style="font-size: 0.9rem; margin-top: 15px;">🌸 Sempre aberta para colaborações e novos desafios! 🌸</p>
        </div>
    </div>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'984b0458c2e0f610',t:'MTc1ODgwODUwMy4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
