# JavaScript - Proz
Exercícios realizados durante a disciplina 'Linguagem de Programação', ministrada no curso de _Desenvolvimento de Sistemas_ da Escola Proz

<hr>

### **Variáveis, Operadores Aritméticos, Concatenação, Relacionais e Lógicos - parte 1**

**Q1.** Crie um programa cujo objetivo é inserir seus dados pessoais (nome, idade, gênero e cidade) e armazenar em cada variável determinada e depois exibidos na tela.
```
var nome = prompt("Digite seu nome: ")

var idade = prompt("Agora, informe sua idade:")

var genero = prompt("Informe o gênero: ") 

var cidade = prompt("Informe onde você mora:")

document.write("Olá, " + nome + ", vc tem " + idade + " anos de idade.Seu gênero é " + genero + " e vc mora em " + cidade + ".")
```
**Q2.** Dado o cálculo 12 x 3 + 4 - 8 / 2 % 3, qual o resultado segundo a precedência de operadores?
```
//Adicionar parênteses só para confirmar 
var calculo =  (12 * 3) + 4 - (8 / 2) % 3

document.write(" O resultado da expressão 12 * 3 + 4 - 8 / 2 % 3 é: " + calculo)
```
**Q3.** Crie um programa que utilize os métodos de Strings, onde o usuário envia uma frase e o programa exibe as informações dessa frase (tamanho, letra maiúscula, letra minúscula, substring e index).
```
var filme ="Vingadores - Guerra Infinita"

//tamanho - quantidade de caracteres
document.write("<br>A quantidade de caracteres é : " + filme.length)

//letra minúscula
document.write("<br>Texto em letras maiúsculas: " + filme.toLowerCase())

//letra maiúscula
document.write("<br>Texto em letras minúscúsculas: " + filme.toUpperCase())

//substring
document.write("<br>Texto cortado: " + filme.substring(12, 20))

//index da letra G
document.write("<br>index da letra G: " + filme.indexOf("G"))

```
### **Variáveis, Operadores Aritméticos, Concatenação, Relacionais e Lógicos - parte 2**

**Q1.** Crie um programa que peça ao usuário para inserir dois números. Verifique se eles são iguais e exiba uma mensagem indicando o resultado.
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comparador de Números</title>
</head>
<body>
    <h1>Comparador de Números</h1>
    <button onclick="compararNumeros()">Verificar Números</button>
    <p id="resultado"></p>

    <script>
        function compararNumeros() {
            const num1 = parseFloat(prompt("Digite o primeiro número:"));
            const num2 = parseFloat(prompt("Digite o segundo número:"));
            const resultado = document.getElementById('resultado');

            if (isNaN(num1) || isNaN(num2)) {
                resultado.textContent = "Por favor, insira números válidos.";
                resultado.style.color = "orange";
                return;
            }

            if (num1 === num2) {
                resultado.textContent = `Você digitou ${num1} e ${num2}. Os números são iguais.`;
                resultado.style.color = "green";
            } else {
                resultado.textContent = `Você digitou ${num1} e ${num2}. Os números são diferentes.`;
                resultado.style.color = "red";
            }
        }
    </script>
</body>
</html>

exercío1.html
Displaying exercío1.html.
Temas 03 e 04: Operadores (Relacionais e Lógicos) e Estruturas Condicionais
Thamyres Andrade Soares
•
Nov 21 (Edited Nov 24)
50
/100
50 points out of possible 100
1-Crie um programa que peça ao usuário para inserir dois números. Verifique se eles são iguais e exiba uma mensagem indicando o resultado.

2-Crie um programa que peça ao usuário para inserir dois números. Verifique se eles são pares e exiba uma mensagem indicando o resultado.

3-Crie um programa que peça ao usuário para inserir dois números. Verifique se eles são ímpares e exiba uma mensagem indicando o resultado.

4-Crie um aplicativo que calcule o Índice de Massa Corporal (IMC) de uma pessoa. Peça o peso e a altura, e calcule o IMC usando a fórmula: IMC = peso / (altura * altura). E por fim, indique, de acordo com o resultado, se a pessoa está: 
Abaixo do normal
Normal
Sobrepeso
Obesidade grau I
Obesidade grau II
```
**Q2.** Crie um programa que peça ao usuário para inserir dois números. Verifique se eles são pares e exiba uma mensagem indicando o resultado.
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificador de Números Pares</title>
</head>
<body>
    <h1>Verificador de Números Pares</h1>
    <button onclick="verificarPares()">Verificar Números</button>
    <p id="resultado"></p>

    <script>
        function verificarPares() {
            const num1 = parseFloat(prompt("Digite o primeiro número:"));
            const num2 = parseFloat(prompt("Digite o segundo número:"));
            const resultado = document.getElementById('resultado');

            if (isNaN(num1) || isNaN(num2)) {
                resultado.textContent = "Por favor, insira números válidos.";
                resultado.style.color = "orange";
                return;
            }

            const par1 = num1 % 2 === 0;
            const par2 = num2 % 2 === 0;

            if (par1 && par2) {
                resultado.textContent = `Você digitou ${num1} e ${num2}. Ambos são pares.`;
                resultado.style.color = "green";
            } else if (!par1 && !par2) {
                resultado.textContent = `Você digitou ${num1} e ${num2}. Ambos são ímpares.`;
                resultado.style.color = "red";
            } else {
                const par = par1 ? num1 : num2;
                const impar = par1 ? num2 : num1;
                resultado.textContent = `Você digitou ${num1} e ${num2}. ${par} é par e ${impar} é ímpar.`;
                resultado.style.color = "blue";
            }
        }
    </script>
</body>
</html>
```
**Q3.** Crie um programa que peça ao usuário para inserir dois números. Verifique se eles são ímpares e exiba uma mensagem indicando o resultado.
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Verificador de Números Ímpares</title>
</head>
<body>
    <h1>Verificador de Números Ímpares</h1>
    <button onclick="verificarImpares()">Verificar Números</button>
    <p id="resultado"></p>

    <script>
        function verificarImpares() {
            const num1 = parseFloat(prompt("Digite o primeiro número:"));
            const num2 = parseFloat(prompt("Digite o segundo número:"));
            const resultado = document.getElementById('resultado');

            if (isNaN(num1) || isNaN(num2)) {
                resultado.textContent = "Por favor, insira números válidos.";
                resultado.style.color = "orange";
                return;
            }

            const impar1 = num1 % 2 !== 0;
            const impar2 = num2 % 2 !== 0;

            if (impar1 && impar2) {
                resultado.textContent = `Você digitou ${num1} e ${num2}. Ambos são ímpares.`;
                resultado.style.color = "green";
            } else if (!impar1 && !impar2) {
                resultado.textContent = `Você digitou ${num1} e ${num2}. Nenhum dos dois é ímpar.`;
                resultado.style.color = "red";
            } else {
                const impar = impar1 ? num1 : num2;
                const par = impar1 ? num2 : num1;
                resultado.textContent = `Você digitou ${num1} e ${num2}. ${impar} é ímpar e ${par} é par.`;
                resultado.style.color = "blue";
            }
        }
    </script>
</body>
</html>
```
**Q4.** Crie um aplicativo que calcule o Índice de Massa Corporal (IMC) de uma pessoa. Peça o peso e a altura, e calcule o IMC usando a fórmula: IMC = peso / (altura * altura). E por fim, indique, de acordo com o resultado, se a pessoa está: 
* Abaixo do normal
* Normal
* Sobrepeso
* Obesidade grau I
* Obesidade grau II
* Obesidade grau III
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de IMC</title>
</head>
<body>
    <h1>Calculadora de IMC</h1>
    <button onclick="calcularIMC()">Calcular IMC</button>
    <p id="resultado"></p>

    <script>
        function calcularIMC() {
            const peso = parseFloat(prompt("Digite seu peso (em kg):"));
            const altura = parseFloat(prompt("Digite sua altura (em metros): (ex: 1.75)"));
            const resultado = document.getElementById('resultado');

            if (isNaN(peso) || isNaN(altura) || peso <= 0 || altura <= 0) {
                resultado.textContent = "Por favor, insira valores válidos para peso e altura.";
                resultado.style.color = "orange";
                return;
            }

            const imc = peso / (altura * altura);
            let classificacao = "";

            if (imc < 18.5) {
                classificacao = "Abaixo do normal";
                resultado.style.color = "blue";
            } else if (imc >= 18.5 && imc < 25) {
                classificacao = "Normal";
                resultado.style.color = "green";
            } else if (imc >= 25 && imc < 30) {
                classificacao = "Sobrepeso";
                resultado.style.color = "yellow";
            } else if (imc >= 30 && imc < 35) {
                classificacao = "Obesidade grau I";
                resultado.style.color = "orange";
            } else if (imc >= 35 && imc < 40) {
                classificacao = "Obesidade grau II";
                resultado.style.color = "red";
            } else {
                classificacao = "Obesidade grau III";
                resultado.style.color = "darkred";
            }

            resultado.textContent = `Seu IMC é ${imc.toFixed(2)}. Classificação: ${classificacao}.`;
        }
    </script>
</body>
</html>


```
**Q5.** Desenvolva um jogo interativo de pedra, papel e tesoura onde o usuário pode competir contra o computador. Dica: utilize o método de Matemática random para criar um número aleatório.
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo: Pedra, Papel e Tesoura</title>
</head>
<body>
    <h1>Pedra, Papel e Tesoura</h1>
    <button onclick="jogar()">Jogar</button>
    <p id="resultado"></p>

    <script>
        function jogar() {
            const escolhas = ["Pedra", "Papel", "Tesoura"];
            const escolhaUsuario = prompt("Escolha: Pedra, Papel ou Tesoura?").trim().toLowerCase();
            const escolhaComputador = escolhas[Math.floor(Math.random() * 3)].toLowerCase();

            const resultado = document.getElementById('resultado');

            if (!["pedra", "papel", "tesoura"].includes(escolhaUsuario)) {
                resultado.textContent = "Escolha inválida! Por favor, escolha Pedra, Papel ou Tesoura.";
                resultado.style.color = "orange";
                return;
            }

            resultado.style.color = "black";
            if (escolhaUsuario === escolhaComputador) {
                resultado.textContent = `Empate! Você escolheu ${escolhaUsuario} e o computador também escolheu ${escolhaComputador}.`;
            } else if (
                (escolhaUsuario === "pedra" && escolhaComputador === "tesoura") ||
                (escolhaUsuario === "papel" && escolhaComputador === "pedra") ||
                (escolhaUsuario === "tesoura" && escolhaComputador === "papel")
            ) {
                resultado.textContent = `Você venceu! Você escolheu ${escolhaUsuario} e o computador escolheu ${escolhaComputador}.`;
                resultado.style.color = "green";
            } else {
                resultado.textContent = `Você perdeu! Você escolheu ${escolhaUsuario} e o computador escolheu ${escolhaComputador}.`;
                resultado.style.color = "red";
            }
        }
    </script>
</body>
</html>
```
### **Funções**

**Q1.** Para um site de e-commerce, desenvolva um programa com uma função que calcula o preço total com base na quantidade de produtos inserida pelo usuário. A entrada é recebida como uma string e precisa ser convertida em um número inteiro antes de ser multiplicada pelo preço unitário.
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Preço</title>
</head>
<body>
    <h1>Calculadora de Preço de Produtos</h1>
    <label for="precoUnitario">Preço Unitário (R$):</label>
    <input type="number" id="precoUnitario" placeholder="Digite o preço unitário" required>
    <br><br>
    <label for="quantidade">Quantidade:</label>
    <input type="text" id="quantidade" placeholder="Digite a quantidade" required>
    <br><br>
    <button onclick="calcularPrecoTotal()">Calcular</button>
    <h2 id="resultado"></h2>

    <script>
        function calcularPrecoTotal() {
            // Pegando os valores dos campos
            var precoUnitario = document.getElementById('precoUnitario').value;
            var quantidade = document.getElementById('quantidade').value;

            // Verificando se a entrada é válida
            if (isNaN(precoUnitario) || isNaN(quantidade)) {
                document.getElementById('resultado').innerText = 'Erro: Por favor, insira valores numéricos válidos.';
                return;
            }

            // Convertendo os valores para números
            precoUnitario = parseFloat(precoUnitario);
            quantidade = parseInt(quantidade);

            // Calculando o preço total
            var precoTotal = precoUnitario * quantidade;

            // Exibindo o resultado
            document.getElementById('resultado').innerText = 'O preço total da compra é: R$ ' + precoTotal.toFixed(2);
        }
    </script>
</body>
</html>
```
**Q2.** Desenvolva um programa para aplicar descontos aplicativo que ajuda os usuários a rastrear seus gastos. Como parte deste aplicativo, os usuários podem inserir o preço de um produto, o valor do desconto e o aplicativo calcula o valor total após aplicar um desconto.
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Desconto</title>
</head>
<body>
    <h1>Calculadora de Desconto</h1>
    <label for="precoOriginal">Preço Original (R$):</label>
    <input type="number" id="precoOriginal" placeholder="Digite o preço original" required>
    <br><br>
    <label for="desconto">Valor do Desconto (%):</label>
    <input type="number" id="desconto" placeholder="Digite o desconto em %" required>
    <br><br>
    <button onclick="calcularPrecoComDesconto()">Calcular Preço com Desconto</button>
    <h2 id="resultado"></h2>

    <script>
        function calcularPrecoComDesconto() {
            // Pegando os valores dos campos
            var precoOriginal = document.getElementById('precoOriginal').value;
            var desconto = document.getElementById('desconto').value;

            // Verificando se a entrada é válida
            if (isNaN(precoOriginal) || isNaN(desconto)) {
                document.getElementById('resultado').innerText = 'Erro: Por favor, insira valores numéricos válidos.';
                return;
            }

            // Convertendo os valores para números
            precoOriginal = parseFloat(precoOriginal);
            desconto = parseFloat(desconto);

            // Calculando o preço com desconto
            var precoComDesconto = precoOriginal - (precoOriginal * (desconto / 100));

            // Exibindo o resultado
            document.getElementById('resultado').innerText = 'O preço total após o desconto é: R$ ' + precoComDesconto.toFixed(2);
        }
    </script>
</body>
</html>
```
**Q3.** Desenvolva uma calculadora.
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Simples</title>
</head>
<body>
    <h1>Calculadora Simples</h1>
    <label for="numero1">Número 1:</label>
    <input type="number" id="numero1" placeholder="Digite o primeiro número" required>
    <br><br>
    <label for="numero2">Número 2:</label>
    <input type="number" id="numero2" placeholder="Digite o segundo número" required>
    <br><br>
    <label for="operacao">Operação:</label>
    <select id="operacao">
        <option value="soma">Soma</option>
        <option value="subtracao">Subtração</option>
        <option value="multiplicacao">Multiplicação</option>
        <option value="divisao">Divisão</option>
    </select>
    <br><br>
    <button onclick="calcular()">Calcular</button>
    <h2 id="resultado"></h2>

    <script>
        function calcular() {
            // Pegando os valores dos campos
            var numero1 = document.getElementById('numero1').value;
            var numero2 = document.getElementById('numero2').value;
            var operacao = document.getElementById('operacao').value;

            // Convertendo os valores para números
            numero1 = parseFloat(numero1);
            numero2 = parseFloat(numero2);

            // Verificando se as entradas são válidas
            if (isNaN(numero1) || isNaN(numero2)) {
                document.getElementById('resultado').innerText = 'Erro: Por favor, insira números válidos.';
                return;
            }

            // Calculando o resultado de acordo com a operação selecionada
            var resultado;
            switch (operacao) {
                case 'soma':
                    resultado = numero1 + numero2;
                    break;
                case 'subtracao':
                    resultado = numero1 - numero2;
                    break;
                case 'multiplicacao':
                    resultado = numero1 * numero2;
                    break;
                case 'divisao':
                    if (numero2 === 0) {
                        document.getElementById('resultado').innerText = 'Erro: Divisão por zero não é permitida.';
                        return;
                    }
                    resultado = numero1 / numero2;
                    break;
                default:
                    document.getElementById('resultado').innerText = 'Erro: Operação inválida.';
                    return;
            }

            // Exibindo o resultado
            document.getElementById('resultado').innerText = 'Resultado: ' + resultado.toFixed(2);
        }
    </script>
</body>
</html>
```
### Laços de Repetição + Datas + POO - Programação Orientada a Objetos

**Q1.** Desenvolva um programa que informa a tabuada de um número inserido pelo usuário.
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Tabuada inserida pelo usuário</title>
</head>
<body>
    <h1>Tabuada</h1>
    <script>
        
        var num  = prompt ("Digite um número de 0 a 10");
        document.write("<br o número escolhido foi " + num);
        
        //transformaão em número:
        //prompt = numero: 

        num = parseInt(num);

        while(num > 10){
        var num  = prompt ("Digite um número de 0 a 10");
       
        }
        
    for (var contador = 0; contador<= 10; contador++) {
            document.write("<br>O número é: " + num * contador);
        }

        

    </script>
</body>
</html>
```
**Q2.** Conforme com o que você aprendeu sobre manipulação de datas, faça as contas: quantos dias se passaram da data do seu nascimento até o dia de hoje?
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    
    <title>Document</title>
</head>
<body>
    <script>
        var dataAtual = new Date(); //Objeto Data
        //O mês começa com zero em Janeiro 0 a 11
        document.write(dataAtual.getDate() + "/" + (dataAtual.getMonth() + 1) + "/" + dataAtual.getFullYear());

        var meudia = new Date (2007, 9, 5);

        var totalDias = (dataAtual.getTime() - meudia.getTime()); //em seg
        document.write("<br> total de dias: " + totalDias);

/*
        1min = 60s
        1h = 3600s
        1d = 86400s 86.400.000 milessegundos

*/
         var int = 542192652354
         var int2 = 86400000

         document.write("<br> O número de dias que você viveu é " + Math.ceil(totalDias)/int2)

    </script>
</body>
</html>
```
**Q3.** Utilizando a programação Orientada a Objetos, monte um modelo de construção de um sistema de uma das empresas abaixo: 
* Netflix
* Ifood
* Airbnb
* Uber/99
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Airbnb DS - Proz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
            background-color: #f9f9f9;
        }
        h1, h2 {
            color: #333;
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        input, button {
            padding: 10px;
            font-size: 14px;
            margin-top: 5px;
            width: 100%;
            max-width: 300px;
            box-sizing: border-box;
        }
        button {
            background-color: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #0056b3;
        }
        .accommodation-item {
            padding: 10px;
            margin: 10px 0;
            background: white;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
        .accommodation-item button {
            background-color: red;
            margin-top: 5px;
        }
        .empty-message {
            color: #888;
            font-style: italic;
        }
    </style>
</head>
<body>
    <h1>Airbnb Curso de DS</h1>

    <h2>Adicionar Acomodação</h2>
    <form id="accommodationForm">
        <label for="title">Título:</label>
        <input type="text" id="title" placeholder="Ex: Casa na praia" required>

        <label for="location">Localização:</label>
        <input type="text" id="location" placeholder="Ex: Rio de Janeiro" required>

        <label for="price">Preço (R$):</label>
        <input type="number" id="price" placeholder="Ex: 200" required>

        <button type="submit">Adicionar</button>
    </form>

    <h2>Acomodações</h2>
    <div id="accommodationList">
        <p class="empty-message">Nenhuma acomodação cadastrada ainda.</p>
    </div>

    <script>
        const accommodations = [];
        const accommodationForm = document.getElementById('accommodationForm');
        const accommodationList = document.getElementById('accommodationList');

        // Renderizar lista de acomodações
        function renderAccommodations() {
            accommodationList.innerHTML = accommodations.length === 0
                ? '<p class="empty-message">Nenhuma acomodação cadastrada ainda.</p>'
                : '';

            accommodations.forEach((acc, index) => {
                const item = document.createElement('div');
                item.className = 'accommodation-item';
                item.innerHTML = `
                    <p><strong>${acc.title}</strong></p>
                    <p>Localização: ${acc.location}</p>
                    <p>Preço: R$ ${acc.price}</p>
                    <button onclick="removeAccommodation(${index})">Remover</button>
                `;
                accommodationList.appendChild(item);
            });
        }

        // Adicionar acomodação
        accommodationForm.onsubmit = function (event) {
            event.preventDefault();

            const title = document.getElementById('title').value;
            const location = document.getElementById('location').value;
            const price = document.getElementById('price').value;

            accommodations.push({ title, location, price });

            renderAccommodations();
            accommodationForm.reset();
        };

        // Remover acomodação
        function removeAccommodation(index) {
            accommodations.splice(index, 1);
            renderAccommodations();
        }
    </script>
</body>
</html>
```
