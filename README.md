<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Internet Gratis - Escanea el QR</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
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
            background: rgba(0, 0, 0, 0.7);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
            margin: 20px;
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }
        
        p {
            font-size: 1.2rem;
            margin-bottom: 30px;
            line-height: 1.6;
        }
        
        .qr-container {
            background: white;
            border-radius: 15px;
            padding: 20px;
            display: inline-block;
            margin: 20px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .qr-code {
            width: 250px;
            height: 250px;
            background: #f0f0f0;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 10px;
            margin: 0 auto;
            font-weight: bold;
            color: #333;
            position: relative;
            overflow: hidden;
        }
        
        .qr-code::before {
            content: "";
            position: absolute;
            width: 100%;
            height: 100%;
            background: 
                linear-gradient(45deg, transparent 45%, #333 45%, #333 55%, transparent 55%),
                linear-gradient(-45deg, transparent 45%, #333 45%, #333 55%, transparent 55%);
            background-size: 20px 20px;
        }
        
        .qr-code::after {
            content: "CÓDIGO QR DE EJEMPLO";
            position: absolute;
            background: white;
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 0.8rem;
            bottom: 10px;
        }
        
        .instructions {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 20px;
            margin: 30px 0;
            text-align: left;
        }
        
        .instructions h2 {
            margin-bottom: 15px;
            text-align: center;
        }
        
        .instructions ol {
            padding-left: 20px;
        }
        
        .instructions li {
            margin-bottom: 10px;
            line-height: 1.5;
        }
        
        .features {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 20px;
            margin: 30px 0;
        }
        
        .feature {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            padding: 15px;
            width: 180px;
            transition: transform 0.3s;
        }
        
        .feature:hover {
            transform: translateY(-5px);
        }
        
        .feature i {
            font-size: 2rem;
            margin-bottom: 10px;
            display: block;
        }
        
        .footer {
            margin-top: 30px;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        @media (max-width: 600px) {
            h1 {
                font-size: 2rem;
            }
            
            p {
                font-size: 1rem;
            }
            
            .qr-code {
                width: 200px;
                height: 200px;
            }
            
            .container {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>¡Navega Gratis por Internet!</h1>
        <p>Escanea el código QR con tu teléfono para acceder a internet gratuito de forma inmediata y segura.</p>
        
        <div class="qr-container">
            <div class="qr-code">
                <!-- Aquí iría el código QR real -->
            </div>
        </div>
        
        <div class="instructions">
            <h2>¿Cómo funciona?</h2>
            <ol>
                <li>Abre la aplicación de cámara o un escáner QR en tu teléfono</li>
                <li>Enfoca el código QR que aparece arriba</li>
                <li>Sigue el enlace que aparece en tu pantalla</li>
                <li>¡Disfruta de navegación gratuita!</li>
            </ol>
        </div>
        
        <div class="features">
            <div class="feature">
                <i>🚀</i>
                <h3>Rápido</h3>
                <p>Conexión de alta velocidad</p>
            </div>
            <div class="feature">
                <i>🔒</i>
                <h3>Seguro</h3>
                <p>Conexión cifrada</p>
            </div>
            <div class="feature">
                <i>📱</i>
                <h3>Fácil</h3>
                <p>Acceso con un solo escaneo</p>
            </div>
        </div>
        
        <div class="footer">
            <p>Este servicio es proporcionado de forma gratuita. No se requieren registros.</p>
        </div>
    </div>
</body>
</html>
