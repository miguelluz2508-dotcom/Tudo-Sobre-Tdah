<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site com Interface</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .checkbox-container {
            margin-bottom: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:disabled {
            background-color: #ccc;
            cursor: not-allowed;
        }
        .interface {
            display: none;
            margin-top: 20px;
        }
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }
        .tab-button {
            padding: 10px 20px;
            background: #ddd;
            border: none;
            cursor: pointer;
            margin: 0 5px;
        }
        .tab-button.active {
            background: #007bff;
            color: white;
        }
        .tab-content {
            display: none;
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .tab-content.active {
            display: block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Bem-vindo ao Meu Site</h1>
        <div class="checkbox-container">
            <label>
                <input type="checkbox" id="agree"> Marque esta caixinha para liberar o botão
            </label>
        </div>
        <button id="enter" disabled>Entrar na Interface</button>
        
        <div class="interface" id="interface">
            <div class="tabs">
                <button class="tab-button active" data-tab="sensi">Sensi</button>
                <button class="tab-button" data-tab="metodo">Metodo</button>
                <button class="tab-button" data-tab="dpi">Dpi</button>
                <button class="tab-button" data-tab="hud">Hud</button>
            </div>
            
            <div id="sensi" class="tab-content active">
                <h2>Sensi</h2>
                <p>Aqui você pode configurar a sensibilidade do mouse. Exemplo: Ajuste para 1.5 para jogos de tiro.</p>
                <!-- Adicione mais conteúdo aqui, como inputs ou sliders -->
            </div>
            
            <div id="metodo" class="tab-content">
                <h2>Metodo</h2>
                <p>Escolha o método de mira. Exemplo: Método 1 para precisão, Método 2 para velocidade.</p>
                <!-- Adicione mais conteúdo aqui -->
            </div>
            
            <div id="dpi" class="tab-content">
                <h2>Dpi</h2>
                <p>Configure os DPI do mouse. Exemplo: 800 DPI para jogos FPS.</p>
                <!-- Adicione mais conteúdo aqui -->
            </div>
            
            <div id="hud" class="tab-content">
                <h2>Hud</h2>
                <p>Personalize o HUD. Exemplo: Ative overlays para informações em tempo real.</p>
                <!-- Adicione mais conteúdo aqui -->
            </div>
        </div>
    </div>

    <script>
        // Referências aos elementos
        const agreeCheckbox = document.getElementById('agree');
        const enterButton = document.getElementById('enter');
        const interfaceDiv = document.getElementById('interface');
        const tabButtons = document.querySelectorAll('.tab-button');
        const tabContents = document.querySelectorAll('.tab-content');

        // Habilita o botão quando a checkbox é marcada
        agreeCheckbox.addEventListener('change', () => {
            enterButton.disabled = !agreeCheckbox.checked;
        });

        // Mostra a interface ao clicar no botão
        enterButton.addEventListener('click', () => {
            interfaceDiv.style.display = 'block';
        });

        // Funcionalidade das abas
        tabButtons.forEach(button => {
            button.addEventListener('click', () => {
                // Remove a classe 'active' de todos os botões e conteúdos
                tabButtons.forEach(btn => btn.classList.remove('active'));
                tabContents.forEach(content => content.classList.remove('active'));
                
                // Adiciona 'active' ao botão clicado e ao conteúdo correspondente
                button.classList.add('active');
                const tabId = button.getAttribute('data-tab');
                document.getElementById(tabId).classList.add('active');
            });
        });
    </script>
</body>
</html>
