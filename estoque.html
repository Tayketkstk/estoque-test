<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Controle de Estoque - Teste</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; }
        .input-group { display: flex; gap: 10px; margin-bottom: 10px; }
        input { padding: 10px; flex: 1; }
        button { padding: 10px 20px; background-color: #007bff; color: white; border: none; cursor: pointer; }
        .feedback { margin-top: 10px; }
        .success { color: green; }
        .error { color: red; }
    </style>
</head>
<body>
    <h1>Teste de Cadastro</h1>
    <div class="input-group">
        <input type="text" id="barcodeInput" placeholder="Código de Barras">
        <input type="text" id="routeInput" placeholder="Rota do Produto">
        <input type="text" id="descriptionInput" placeholder="Descrição do Produto">
    </div>
    <button onclick="registerProduct()">Cadastrar</button>
    <div id="registerFeedback" class="feedback"></div>

    <script>
        const SCRIPT_URL = "https://script.google.com/macros/s/AKfycbzLB8STbA71vrDFURcd5VDeMn7WeS7B0vv2GikQhR1xJGR9LFXWiz1nrx-4uDufDl8_/exec";

        async function registerProduct() {
            const barcode = document.getElementById('barcodeInput').value;
            const route = document.getElementById('routeInput').value;
            const description = document.getElementById('descriptionInput').value;
            const feedback = document.getElementById('registerFeedback');

            if (!barcode || !route || !description) {
                feedback.innerHTML = '<span class="error">Preencha todos os campos!</span>';
                return;
            }

            const data = { action: 'register', barcode, route, description, timestamp: new Date().toISOString() };

            try {
                console.log('Enviando requisição para:', SCRIPT_URL);
                const response = await fetch(SCRIPT_URL, {
                    method: 'POST',
                    body: JSON.stringify(data),
                    headers: { 'Content-Type': 'application/json' },
                    mode: 'cors'
                });
                console.log('Resposta recebida:', response);
                if (!response.ok) throw new Error(`HTTP error! Status: ${response.status}`);
                const result = await response.text();
                console.log('Resultado:', result);
                if (result === 'DUPLICATE') {
                    feedback.innerHTML = '<span class="error">Código já cadastrado!</span>';
                } else {
                    feedback.innerHTML = '<span class="success">Produto cadastrado!</span>';
                    clearInputs(['barcodeInput', 'routeInput', 'descriptionInput']);
                    setTimeout(() => feedback.innerHTML = '', 2000);
                }
            } catch (error) {
                feedback.innerHTML = '<span class="error">Erro: ' + error.message + '</span>';
                console.error('Erro detalhado:', error);
            }
        }

        function clearInputs(inputIds) {
            inputIds.forEach(id => document.getElementById(id).value = '');
        }

        async function testConnection() {
            try {
                const response = await fetch(SCRIPT_URL + '?action=report');
                console.log('Teste de conexão:', await response.text());
            } catch (error) {
                console.error('Erro no teste de conexão:', error);
            }
        }
        testConnection();
    </script>
</body>
</html>
