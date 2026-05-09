# Alberto2024.github.io

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Autenticando...</title>
    <style>
        body { font-family: sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; }
        .loader { border: 4px solid #f3f3f3; border-top: 4px solid #3498db; border-radius: 50%; width: 30px; height: 30px; animation: spin 2s linear infinite; }
        @keyframes spin { 0% { transform: rotate(0deg); } 100% { transform: rotate(360deg); } }
    </style>
</head>
<body>
    <div style="text-align: center;">
        <div class="loader" style="margin: 0 auto 20px;"></div>
        <p>Conectando con tu Asistente de IA...</p>
    </div>

    <script>
        // Capturamos los datos que Google envía en la URL
        const params = new URLSearchParams(window.location.search);
        const code = params.get('code');
        const error = params.get('error');

        if (code) {
            // EL SALTO: Enviamos el código a tu app de Android
            window.location.href = "com.tuapp.asistenteia://auth?code=" + code;
        } else if (error) {
            window.location.href = "com.tuapp.asistenteia://auth?error=" + error;
        }
    </script>
</body>
</html>
