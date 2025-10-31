<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Red Gratuita - Escanea el QR</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            text-align: center;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            font-weight: 300;
        }
        
        .highlight {
            background: linear-gradient(90deg, #ff8a00, #e52e71);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: bold;
        }
        
        .qr-container {
            margin: 30px auto;
            width: 280px;
            height: 280px;
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
        
        .qr-container::before {
            content: '';
            position: absolute;
            width: 150%;
            height: 150%;
            background: conic-gradient(
                #ff0000, #ff9900, #ffff00, #00ff00, 
                #00ffff, #0000ff, #9900ff, #ff00ff, #ff0000
            );
            animation: rotate 4s linear infinite;
            z-index: 0;
        }
        
        .qr-container::after {
            content: '';
            position: absolute;
            width: 270px;
            height: 270px;
            background: white;
            border-radius: 15px;
            z-index: 1;
        }
        
        .qr-code {
            width: 240px;
            height: 240px;
            z-index: 2;
            position: relative;
            border-radius: 10px;
            background: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            color: #333;
            font-size: 1.2rem;
        }
        
        .steps {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 40px 0;
        }
        
        .step {
            flex: 1;
            min-width: 200px;
            background: rgba(255, 255, 255, 0.15);
            padding: 20px;
            border-radius: 15px;
            backdrop-filter: blur(5px);
            transition: transform 0.3s ease;
        }
        
        .step:hover {
            transform: translateY(-5px);
        }
        
        .step-number {
            display: inline-block;
            width: 40px;
            height: 40px;
            background: linear-gradient(45deg, #ff8a00, #e52e71);
            border-radius: 50%;
            line-height: 40px;
            margin-bottom: 15px;
            font-weight: bold;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        
        .features {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        .feature {
            display: flex;
            align-items: center;
            background: rgba(255, 255, 255, 0.1);
            padding: 10px 20px;
            border-radius: 50px;
            font-size: 0.9rem;
        }
        
        .feature i {
            margin-right: 8px;
            font-size: 1.2rem;
        }
        
        .footer {
            margin-top: 40px;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        @keyframes rotate {
            from {
                transform: rotate(0deg);
            }
            to {
                transform: rotate(360deg);
            }
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            
            .subtitle {
                font-size: 1.2rem;
            }
            
            .qr-container {
                width: 250px;
                height: 250px;
            }
            
            .qr-code {
                width: 210px;
                height: 210px;
            }
            
            .step {
                min-width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¡Conéctate a Internet <span class="highlight">GRATIS</span>!</h1>
        <p class="subtitle">Escanea el QR y podrás navegar por la red totalmente gratis siguiendo estos pasos</p>
        
        <div class="qr-container">
            <div class="qr-code">
                <!-- Aquí iría el código QR real -->
                <div style="text-align: center;">
                    <div style="font-size: 3rem; margin-bottom: 10px;">📱</div>
                    <div>Escanea con tu cámara</div>
                </div>
            </div>
        </div>
        
        <div class="steps">
            <div class="step">
                <div class="step-number">1</div>
                <h3>Escanea el código QR</h3>
                <p>Abre la cámara de tu teléfono y apunta hacia el código QR</p>
            </div>
            
            <div class="step">
                <div class="step-number">2</div>
                <h3>Sigue el enlace</h3>
                <p>Haz clic en el enlace que aparece después de escanear</p>
            </div>
            
            <div class="step">
                <div class="step-number">3</div>
                <h3>¡Disfruta!</h3>
                <p>Conéctate a nuestra red rápida, segura y exclusiva</p>
            </div>
        </div>
        
        <div class="features">
            <div class="feature">
                <i>⚡</i> Red Rápida
            </div>
            <div class="feature">
                <i>🔒</i> Conexión Segura
            </div>
            <div class="feature">
                <i>👑</i> Acceso Exclusivo
            </div>
        </div>
        
        <div class="footer">
            <p>Conéctate ahora y disfruta de navegación ilimitada</p>
        </div>
    </div>
</body>
</html>
