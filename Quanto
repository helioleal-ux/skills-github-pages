<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Timer para 17:00:00</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #timer {
            font-size: 48px;
            color: #333;
        }
    </style>
</head>
<body>
    <h1>Tempo restante até as 17:00:00</h1>
    <div id="timer">Carregando...</div>

    <script>
        function updateTimer() {
            const now = new Date();
            const targetTime = new Date();
            targetTime.setHours(17, 0, 0, 0); // Define o horário alvo como 17:00:00

            // Calcula a diferença em milissegundos
            let diff = targetTime - now;

            // Se o horário já passou, ajusta para o próximo dia
            if (diff < 0) {
                targetTime.setDate(targetTime.getDate() + 1);
                diff = targetTime - now;
            }

            // Converte a diferença para horas, minutos e segundos
            const hours = Math.floor(diff / (1000 * 60 * 60));
            const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const seconds = Math.floor((diff % (1000 * 60)) / 1000);

            // Exibe o timer
            document.getElementById('timer').textContent = 
                `${String(hours).padStart(2, '0')}:${String(minutes).padStart(2, '0')}:${String(seconds).padStart(2, '0')}`;
        }

        // Atualiza o timer a cada segundo
        setInterval(updateTimer, 1000);
        updateTimer(); // Chama a função imediatamente para evitar o carregamento
    </script>
</body>
</html>
