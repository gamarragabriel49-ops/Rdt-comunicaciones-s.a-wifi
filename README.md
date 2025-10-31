<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Escanea el QR | Navega Gratis</title>
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
        }
        
        .container {
            max-width: 1000px;
            width: 100%;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
        }
        
        .left-section, .right-section {
            flex: 1;
            min-width: 300px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 20px;
            text-align: center;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .subtitle {
            font-size: 1.2rem;
            margin-bottom: 30px;
            text-align: center;
            opacity: 0.9;
        }
        
        .qr-container {
            background-color: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            margin-bottom: 20px;
        }
        
        .qr-code {
            width: 250px;
            height: 250px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: #f5f5f5;
            border-radius: 10px;
            font-weight: bold;
            color: #333;
        }
        
        .qr-code img {
            max-width: 100%;
            max-height: 100%;
            border-radius: 10px;
        }
        
        .steps {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 20px;
        }
        
        .step {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .step-number {
            background-color: white;
            color: #2575fc;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }
        
        .login-form {
            background-color: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            width: 100%;
            max-width: 400px;
        }
        
        .login-form h2 {
            color: #333;
            margin-bottom: 20px;
            text-align: center;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: #555;
            font-weight: 500;
        }
        
        .form-group input {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 1rem;
            transition: all 0.3s;
        }
        
        .form-group input:focus {
            outline: none;
            border-color: #2575fc;
            box-shadow: 0 0 0 2px rgba(37, 117, 252, 0.2);
        }
        
        .login-btn {
            width: 100%;
            padding: 12px;
            background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .login-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .footer {
            margin-top: 30px;
            text-align: center;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
                padding: 20px;
            }
            
            h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="left-section">
            <h1>Escanea el QR</h1>
            <p class="subtitle">Logéate y navega gratis</p>
            
            <div class="qr-container">
                <div class="qr-code">
                    <!-- Reemplaza "tu-qr.png" con la ruta de tu archivo QR -->
                    <img src=IMG_20251030_235053.jpg alt="Código QR para login">
                </div>
            </div>
            
            <div class="steps">
                <div class="step">
                    <div class="step-number">1</div>
                    <div>Escanea el código QR con tu dispositivo móvil</div>
                </div>
                <div class="step">
                    <div class="step-number">2</div>
                    <div>Ingresa tus credenciales en la página que se abrirá</div>
                </div>
                <div class="step">
                    <div class="step-number">3</div>
                    <div>¡Disfruta de navegación gratuita!</div>
                </div>
            </div>
        </div>
        
        <div class="right-section">
            <div class="login-form">
                <h2>Iniciar Sesión</h2>
                <form id="loginForm">
                    <div class="form-group">
                        <label for="username">Usuario o Email</label>
                        <input type="text" id="username" name="username" required>
                    </div>
                    <div class="form-group">
                        <label for="password">Contraseña</label>
                        <input type="password" id="password" name="password" required>
                    </div>
                    <button type="submit" class="login-btn">Iniciar Sesión</button>
                </form>
            </div>
        </div>
    </div>
    
    <div class="footer">
        <p>© 2023 Navegación Gratis - Todos los derechos reservados</p>
    </div>

    <script>
        // Manejo del formulario de login
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            
            // Aquí normalmente enviarías los datos a un servidor
            // Por ahora, solo mostraremos una alerta
            alert(`¡Login exitoso! Bienvenido, ${username}. Ahora puedes navegar gratis.`);
            
            // Limpiar el formulario
            document.getElementById('loginForm').reset();
        });
    </script>
</body>
</html>
