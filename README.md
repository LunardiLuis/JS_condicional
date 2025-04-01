<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificação de idade</title>
    <link rel="stylesheet" href="./styles.css">
</head>
<body>
    <div class="Container">
        <h1>Verificador de Idade</h1>
        <input type="number" id="idadeInput">
        <button onclick="verificarIdade()">Verificar</button>
        <p id="resultado"></p>
    </div>
    <script>
        function verificarIdade(){
            const idade = parseInt(document.getElementById('idadeInput').value);
            let mensagem = "";
            if(isNaN(idade) || idade < 0){
            mensagem = "por favor, insira uma idade valida";
            }else if(idade < 18){
            mensagem = "você é menos de idade";
            }else if(idade < 60){
            mensagem = "você é um adulto";
            }else{
            mensagem = "você e idoso";
            }
            document.getElementById('resultado').innerText = mensagem;
        }
    </script>
</body>
</html>

body{
    font-family: Arial, Helvetica, sans-serif;
    text-align: center;
    margin: 50px;
}

.Container{
    max-width: 400px;
    margin: auto;
    padding: 20px;
    border: 2px solid #333;
    border-radius: 10px;
}

input, button{
    margin: 10px;
    padding: 10px;
    font-size: 16px;
}
