<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WiFi Gratis | Escanea y Conéctate</title>
    <style>
        :root {
            --primary: #3498db;
            --secondary: #2ecc71;
            --dark: #2c3e50;
            --light: #ecf0f1;
            --accent: #e74c3c;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: var(--dark);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }
        
        .container {
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            width: 100%;
            max-width: 900px;
            overflow: hidden;
            margin: 20px 0;
        }
        
        header {
            background-color: var(--dark);
            color: white;
            padding: 20px;
            text-align: center;
        }
        
        header h1 {
            font-size: 2.2rem;
            margin-bottom: 10px;
        }
        
        header p {
            font-size: 1.1rem;
            opacity: 0.9;
        }
        
        .content {
            display: flex;
            flex-wrap: wrap;
            padding: 30px;
        }
        
        .qr-section {
            flex: 1;
            min-width: 300px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        .qr-code {
            width: 250px;
            height: 250px;
            background-color: #f5f5f5;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            border: 2px dashed var(--primary);
            position: relative;
            overflow: hidden;
        }
        
        .qr-code::before {
            content: "";
            position: absolute;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(45deg, transparent 49%, var(--primary) 49%, var(--primary) 51%, transparent 51%),
                linear-gradient(-45deg, transparent 49%, var(--primary) 49%, var(--primary) 51%, transparent 51%);
            background-size: 20px 20px;
            opacity: 0.1;
        }
        
        .qr-code img {
            width: 90%;
            height: 90%;
            object-fit: contain;
            border-radius: 5px;
        }
        
        .instructions {
            flex: 1;
            min-width: 300px;
            padding: 20px;
        }
        
        .instructions h2 {
            color: var(--primary);
            margin-bottom: 20px;
            font-size: 1.8rem;
        }
        
        .step {
            display: flex;
            margin-bottom: 25px;
            align-items: flex-start;
        }
        
        .step-number {
            background-color: var(--primary);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            flex-shrink: 0;
            font-weight: bold;
        }
        
        .step-content h3 {
            margin-bottom: 5px;
            color: var(--dark);
        }
        
        .features {
            background-color: var(--light);
            padding: 30px;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }
        
        .feature {
            text-align: center;
            padding: 15px;
            max-width: 200px;
        }
        
        .feature i {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 15px;
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 20px;
            font-size: 0.9rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            margin-top: 15px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #27ae60;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        @media (max-width: 768px) {
            .content {
                flex-direction: column;
            }
            
            .qr-section, .instructions {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>WiFi Gratis</h1>
            <p>Escanea el código QR y conéctate a nuestra red</p>
        </header>
        
        <div class="content">
            <div class="qr-section">
                <div class="qr-code">
                    <!-- TU CÓDIGO QR DE GITHUB -->
                    <img src="https://github.com/user-attachments/assets/15c79d93-f504-4941-8c45-59fa8fd44041" alt="Código QR para WiFi gratis">
                </div>
                <p>Escanea este código con tu teléfono</p>
                <button class="btn" id="generateQR">Generar Nuevo Código</button>
            </div>
            
            <div class="instructions">
                <h2>Cómo Conectarse</h2>
                
                <div class="step">
                    <div class="step-number">1</div>
                    <div class="step-content">
                        <h3>Abre la cámara de tu teléfono</h3>
                        <p>Usa la aplicación de cámara o un escáner QR para escanear el código.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">2</div>
                    <div class="step-content">
                        <h3>Sigue el enlace</h3>
                        <p>Al escanear el código, se abrirá una página de inicio de sesión.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">3</div>
                    <div class="step-content">
                        <h3>Inicia sesión</h3>
                        <p>Completa el formulario con tus datos o inicia sesión con redes sociales.</p>
                    </div>
                </div>
                
                <div class="step">
                    <div class="step-number">4</div>
                    <div class="step-content">
                        <h3>¡Disfruta del WiFi!</h3>
                        <p>Una vez autenticado, tendrás acceso gratuito a nuestra red WiFi.</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="features">
            <div class="feature">
                <i>⚡</i>
                <h3>Alta Velocidad</h3>
                <p>Conexión rápida y estable para todas tus necesidades.</p>
            </div>
            
            <div class="feature">
                <i>🔒</i>
                <h3>Conexión Segura</h3>
                <p>Tu privacidad está protegida con nuestra red segura.</p>
            </div>
            
            <div class="feature">
                <i>🆓</i>
                <h3>Completamente Gratis</h3>
                <p>Sin costos ocultos ni límites de tiempo.</p>
            </div>
        </div>
        
        <footer>
            <p>© 2023 WiFi Gratis - Todos los derechos reservados</p>
            <p>Para asistencia, contacta a nuestro equipo de soporte.</p>
        </footer>
    </div>

    <script>
        document.getElementById('generateQR').addEventListener('click', function() {
            alert('En una implementación real, aquí se generaría un nuevo código QR. Para este ejemplo, el código QR permanece igual.');
        });
        
        // Simulación de temporizador de sesión
        let timeLeft = 60 * 60; // 60 minutos en segundos
        const timerElement = document.createElement('div');
        timerElement.style.cssText = `
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--dark);
            color: white;
            padding: 10px 15px;
            border-radius: 5px;
            font-size: 0.9rem;
            box-shadow: 0 3px 10px rgba(0,0,0,0.2);
        `;
        document.body.appendChild(timerElement);
        
        function updateTimer() {
            const minutes = Math.floor(timeLeft / 60);
            const seconds = timeLeft % 60;
            timerElement.textContent = Sesión activa: ${minutes}:${seconds < 10 ? '0' : ''}${seconds};
            
            if (timeLeft > 0) {
                timeLeft--;
                setTimeout(updateTimer, 1000);
            } else {
                timerElement.textContent = 'Sesión expirada';
                timerElement.style.background = 'var(--accent)';
            }
        }
        
        updateTimer();
    </script>
</body>
</html>
