<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Red Gratuita Argentina - Escanea el QR</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #74ACDF 0%, #FFFFFF 50%, #74ACDF 100%);
            color: #333;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 20px;
            text-align: center;
        }
        
        .container {
            max-width: 900px;
            width: 100%;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            border: 2px solid #74ACDF;
            position: relative;
            overflow: hidden;
        }
        
        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 10px;
            background: linear-gradient(90deg, #74ACDF 0%, #FFFFFF 50%, #74ACDF 100%);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: #333;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.1);
        }
        
        .subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            font-weight: 500;
            color: #74ACDF;
        }
        
        .highlight {
            color: #74ACDF;
            font-weight: bold;
        }
        
        .argentina-flag {
            display: flex;
            justify-content: center;
            margin: 20px 0;
            height: 20px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        .flag-stripe {
            height: 100%;
            flex: 1;
        }
        
        .flag-blue {
            background-color: #74ACDF;
        }
        
        .flag-white {
            background-color: white;
        }
        
        .sun-flag {
            position: absolute;
            top: 15px;
            right: 15px;
            width: 40px;
            height: 40px;
            color: #F6B40E;
            font-size: 24px;
        }
        
        .qr-container {
            margin: 30px auto;
            width: 280px;
            height: 280px;
            background: white;
            border-radius: 20px;
            padding: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            border: 2px solid #74ACDF;
        }
        
        .qr-container::before {
            content: '';
            position: absolute;
            width: 150%;
            height: 150%;
            background: conic-gradient(
                #74ACDF, #FFFFFF, #74ACDF, #FFFFFF, 
                #74ACDF, #FFFFFF, #74ACDF, #FFFFFF
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
            border: 1px solid #74ACDF;
            overflow: hidden;
        }
        
        .qr-code img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 8px;
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
            background: rgba(116, 172, 223, 0.1);
            padding: 20px;
            border-radius: 15px;
            border: 1px solid #74ACDF;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .step:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(116, 172, 223, 0.2);
        }
        
        .step-number {
            display: inline-block;
            width: 40px;
            height: 40px;
            background: #74ACDF;
            border-radius: 50%;
            line-height: 40px;
            margin-bottom: 15px;
            font-weight: bold;
            color: white;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }
        
        .step h3 {
            color: #74ACDF;
            margin-bottom: 10px;
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
            background: rgba(116, 172, 223, 0.15);
            padding: 10px 20px;
            border-radius: 50px;
            font-size: 0.9rem;
            color: #333;
            border: 1px solid #74ACDF;
        }
        
        .feature i {
            margin-right: 8px;
            font-size: 1.2rem;
            color: #74ACDF;
        }
        
        .footer {
            margin-top: 40px;
            font-size: 0.9rem;
            color: #666;
        }
        
        .footer p {
            margin-bottom: 10px;
        }
        
        .argentina-icon {
            color: #74ACDF;
            margin: 0 5px;
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
        <div class="sun-flag">
            <i class="fas fa-sun"></i>
        </div>
        
        <h1>¡Conéctate a Internet <span class="highlight">GRATIS</span>!</h1>
        <p class="subtitle">Escanea el QR y navegá por la red totalmente gratis siguiendo estos pasos</p>
        
        <div class="argentina-flag">
            <div class="flag-stripe flag-blue"></div>
            <div class="flag-stripe flag-white"></div>
            <div class="flag-stripe flag-blue"></div>
        </div>
        
        <div class="qr-container">
            <div class="qr-code">
                <!-- AQUÍ VA TU CÓDIGO QR -->
                <img src="https://github.com/user-attachments/assets/15c79d93-f504-4941-8c45-59fa8fd44041" alt="Código QR para red gratuita">
            </div>
        </div>
        
        <div class="steps">
            <div class="step">
                <div class="step-number">1</div>
                <h3>Escaneá el código QR</h3>
                <p>Abrí la cámara de tu teléfono y apuntá hacia el código QR</p>
            </div>
            
            <div class="step">
                <div class="step-number">2</div>
                <h3>Seguí el enlace</h3>
                <p>Hacé clic en el enlace que aparece después de escanear</p>
            </div>
            
            <div class="step">
                <div class="step-number">3</div>
                <h3>¡Disfrutá!</h3>
                <p>Conectate a nuestra red rápida, segura y exclusiva</p>
            </div>
        </div>
        
        <div class="features">
            <div class="feature">
                <i class="fas fa-bolt"></i> Red Rápida
            </div>
            <div class="feature">
                <i class="fas fa-shield-alt"></i> Conexión Segura
            </div>
            <div class="feature">
                <i class="fas fa-crown"></i> Acceso Exclusivo
            </div>
        </div>
        
        <div class="footer">
            <p>Conectate ahora y disfrutá de navegación ilimitada <i class="fas fa-wifi argentina-icon"></i></p>
            <p>Red gratuita para todos los argentinos <i class="fas fa-flag argentina-icon"></i></p>
        </div>
    </div>
</body>
</html>
