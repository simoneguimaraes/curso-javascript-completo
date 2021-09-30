# Módulo 2 – Comandos Básicos do Javascript

## Aula 5 – Variáveis e Tipos Primitivos

### Como criar comentários?
```
//  → uma única linha de código
```

```
/*    

*/    → mais de uma linha de código
```

### O que são variáveis?

A memória do computador tem espaços delimitados para receber valores (assim como vagas no estacionamento).

### Como declarar variáveis no Javascript?

```
A vaga a1 = carro1
(leia: a vaga a1 recebe o carro1)
a1 = carro2
(o carro1 saiu e entrou o carro2)
a1 = null
(a vaga está nula)

var n1 = 5      → int: número inteiro
var n2 = 8.5    → float: número real
var n3 = 15     → int: número inteiro

var s1 = “São Paulo”
var s2 = ‘Lumpa’
var s3 = `Janeiro`
```

### Regras para nomear as variáveis
- Podem começar com letra, $ ou _
- Não podem começar com números
- É possível usar letras ou números
- É possível usar acentos e símbolos
- Não podem conter espaços
- Não podem ser palavras reservadas

### Para entrar no Node, você vai precisar entrar no VS Code e digitar “crtl + shift + `” 
- digitar: node
- para limpar tela: ctrl + l
- para sair: .exit

### Quais são os tipos primitivos do Javascript?

#### Os tipos primordiais:
- Number:   5     18    -12    3.14
- String: “Google”    ‘Javascript’    `Maria`    ‘12553-120’
- Boolean: true     false
  
#### Outros tipos:
- Tipos internos de Number
      <ul> 
        <li>Infinity</li>
        <li>NaN (not a number)</li>
      </ul>
- Null
- Undefined
- Tipo interno de Object
      <ul> 
        <li>Array</li>
      </ul>
- Function
 
### Como conferir qual o tipo da variável que foi declarada?

typeof  → saber qual é o tipo da variavel
```
Colocar no terminal (Node): 
var num = 200
typeof num
```

### Consegue entender o que significa colocar um valor null dentro de uma variável em Javascript?
Null é representa um valor nulo ou vazio, e aponta para um objeto inexistente.

## Aula 6 – Tratamento de dados

### Como guardar o resultado de um prompt dentro de uma variável?
var nome = prompt(‘Qual é o seu nome’)

### Concatenação: para juntar a string com a variável
alert(‘É um prazer te conhecer, ‘ + nome)  

### Como somar variáveis?
```
var num1 = prompt(‘Digite um número: ‘)
var num2 = prompt(‘Digite outro número: ‘)
var sum = num1 + num2

alert(‘A soma dos valores é “ + sum)
```

### Como manipular dados e fazer a conversão?
O sinal de + serve tanto para somar quanto para concatenar:
- soma: number + number
- concatenar: string + string

O prompt retorna, por padrão, uma string. Então é preciso converter as variáveis num1 e num2 para number.

### Como converter String para Número em JavaScript?

Para converter string → número:
- Number.parseInt(n): converte para número inteiro
- Number.parseFloat(n): converte para número real

Na versão atualizada do Javascript, ele faz a conversão de forma automática: Number(n)

### Como converter Número para String em JavaScript?

Para converter número → string:
- String(n)
- n.toString()

var s = ‘JavaScript’
- ‘Eu estou aprendendo s’              // não faz interpolação
- ‘Eu estou aprendendo ‘ + s           // usa concatenação
- `Eu estou aprendendo ${s}`           // usa template string

### Interpolação (Template string)
- Nova forma de criar strings e tornar o seu código um pouco mais legível
- `O aluno ${nome} com ${idade} tirou a nota ${nota}.` 

### Formatando strings:

var s = ‘Javascript’
- s.lenght              → quantos caracteres a string tem
- s.toUpperCase()       → tudo para maiúsculas
- s.toLowerCase()       → tudo para minúsculas

### Consegue formatar um número para que ele se pareça com um valor monetário?

Exemplo:
```
<body>
  <script>
	var nome = prompt("Qual é o seu nome?")

//o prompt recebe o valor em string, entao voce precisa converter a string para numero real (float)
	
	var saldo = Number.parseFloat(prompt("Quanto quer depositar?"))
  		document.write(`Olá, ${nome}! <br> Seu nome tem ${nome.length} letras.<br>`)
  		document.write(`Seu nome em maiúsculas é ${nome.toUpperCase()}.<br>`)
  
  //transformar para Reais
	
	saldoFixado = saldo.toLocaleString("pt-BR", {style: "currency", currency: "BRL"})

  	
	document.write(`Depósito realizado. <br> Agora seu saldo é de ${saldoFixado}.`)
  
//coloca duas casas decimais e troca o ponto pela vírgula para ficar em reais
//saldoFixado = saldo.toFixed(2).replace(".", ",")

  </script>
</body>
```

## Aula 7 – Operadores (parte 1)
	
Quais são os operadores do Javascript?

### Aritméticos
```
3 + 2 → 5
3 - 2→ 5
3 * 2→ 6
3 / 2→ 1.5
3 % 2→ 1
3 ** 2→ 9
```
### Atribuição
```
var a = 5 + 3    →8
var b = a % 5  → 3 
var c = 5 * c ** 2 → 45
var d = 10 – a / 2  → 6
var e = 6 * 2 / d → 2
var f = b % e + 4 / e → 3
```
#### Auto-atribuições
```
var n = 3 → n = 3

n = n + 3 → n = 7
n = n – 5 → n = 2
```
#### Simplificando as operações
```
n = n + 3 → n+= 3
n = n – 5 → n -= 5 
```
### Qual a ordem de precedência dos operadores em JavaScript?
```
Parêntesis, potência, multiplicação, divisão, resto, adição, subtração.
```
```
5 + 3 / 2 → 5 + (3 / 2) → 6.5
```

### Como usar os operadores de incremento (pré-incremento e pós-incremento) no JavaScript?

#### Pré-incremento
```
var x = 5
x = x + 1 → x++ → 6
x = x – 1 →  x--  → 5
```
#### Pós-incremento
```
var x = 4
x = x + 1 → ++x → 5
x = x – 1 →  --x  → 4
```
## Aula 8 – Operadores (parte 2)
	
### Relacionais
```
>   → maior
<    → menor
>=  → maior ou igual
<=  → menor ou igual
==  → igual
!=   → diferente
```

#### Exemplos:
```
preço >= 200.50
idade < 18
curso == ‘Javascript’
n1 != n2
```

#### Identidade:
```
5 == 5    → true
5 == ‘5’  → true (é igual? O valor é igual.)
5 === ‘5’  → falso (é idêntico? O valor e tipo não são iguais.)
5 === ‘5’  → true (é idêntico? O valor e tipo são iguais.)
```
### Lógicos

#### !  → negação
```
! true →false
! false → true
```
#### &&  → conjunção (E)
```
true && true → true
true && false → false
false && true → false
false && false → false

A condição só me satisfaz se as duas forem verdadeiras.
```
#### ||  → disjunção (OU)
```
true && true → true
true && false → true
false && true → true
false && false → false

A condição me satisfaz se pelo menos um for verdadeiro.
```
##### Exemplo 1:
```
var a = 5
var b = 8

a > b && b % 2 == 0 
false  &&  true → false

a < b || b / 2 == 2 
true  ||  false → true
```
#### Exemplo 2:
```
idade >= 15 && idade <= 17
estado == ‘RJ’ || estado == ‘SP’
salario > 2500 && sexo != ‘masculino’
```
### Ordem de precedência das operações
```
Primeiro ele faz os operadores aritméticos, depois relacionais e depois lógicos.
Primeiro ele faz o NÃO, depois o E, depois o OU. 
```
```
Aritméticos > Relacionais > Lógicos (Não > E > OU)
```
### Ternário
```
?
:
```
```
teste ? true : false
media >= 7 ? ‘Aprovado’ : ‘Reprovado’
```
#### Exemplo 1:
```
var media = 9

media >= 7 ? ‘Aprovado’ : ‘Reprovado’      
→ ‘Aprovado’

media -= 3     
media >= 7 ? ‘Aprovado’ : ‘Reprovado’      
→ ‘Reprovado’
```
#### Exemplo 2:
```
var x = 8

var res = x % 2 == 0 ? 5 : 9

como (x % 2 == 0) é true 
→ 5
```
#### Exemplo 3:
```
var idade = 19
var entradaBar = idade >= 18 ? ‘Pode entrar.’ : ‘Não pode entrar.’
entradaBar
→ ‘Pode entrar.’

idade -= 5
var entradaBar = idade >= 18 ? ‘Pode entrar.’ : ‘Não pode entrar.’
entradaBar
→ ‘Não pode entrar.’
```
# Módulo 3 – Entendendo o DOM

## Aula 9 – Introdução ao DOM
	
### O que significa a sigla DOM? 
Document Object Model

### Para que serve o Document Object Model?
- Modelo de objetos para documentos. 
- Conjunto de objetos dentro do navegador que vai dar acesso aos componentes internos do website.
- Não funciona no Node.js, está presente no Javascript dentro do navegador.

### Como criar uma árvore DOM para o seu site?
A raiz dentro do navegador se chama window.
```
Alguns objetos do window:
- locations → qual é a localizacao do site (ex: url, pagina anterior, pagina atual)
- document → documento atual
	        ◦ HTML (é parent de head e body)
            ▪ head (é child do HTML)
                • meta
                • title
            ▪ body (é child do HTML)
            ▪ h1
            ▪ p
            ▪ p
                • strong
            ▪ div
- history → guarda de onde você veio e pra onde você vai, facilitando a navegação no site
```
### Como usar o Javascript para manipular o DOM?
```
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
	<style>
	body {
	background: rgb(40, 17, 75);
	color: white;
	font: normal 18pt Arial;
	}
	</style>
</head>
<body>
	<h1>Estudos DOM</h1>
	<p>Aqui vai o resultado</p>
	<p>Aprendendo a usar o <strong>DOM</strong> em Javascript.</p>
	<div>Clique em mim</div>
	<script>
	window.document.write(‘Olá mundo’)
	</script>
</body>
```

### Para quem servem os elementos Parent e Child em um DOM?

Elemento é todo item que aparece na árvore DOM.
<br>HTML é parent de Body e é child de Document.

### Como usar métodos de acesso ao DOM no Javascript?

Você pode selecionar os elementos para navegar dentro da árvore DOM.

Alguns métodos de acesso ao DOM são por:
```
1. Marca (TagName)
getElementByTagName()
var p1 = window.document.getElementsByTagName(“p”)[0] → para selecionar o primeiro parágrafo
document.write(“Está escrito nesse parágrafo: ” + p1.innerHTML)

var p2 = window.document.getElementByTagName(‘p’)[1] → para selecionar o segundo parágrafo
document.write(“Está escrito nesse parágrafo: ” + p1.innerText) 
→ innerText não leva a formatação. O innerHTML leva a formatação.

// para editar os elementos no javascript
p1.style.color = ‘blue’

var corpo = window.document.body
corpo.style.background = ‘black’
```
```
2. ID
getElementById()

<div id=’msg’>Clique em mim</div>

var d = window.document.getElementById(‘msg’)
d.style.background = ‘green’
d.innerText = ‘Estou aguardando...’
```
```
3. Nome
getElementByName()

<div name=’msg’>Clique em mim</div>

var c = window.document.getElementsByName(‘msg’)[0]
c.innerText = ‘Prazo confirmado.’
```
```
4. Classe
getElementByClassName()

<div class=’msg’>Clique em mim</div>
```
```
5. Seletor
querySelector

<div id=’msg’>Clique em mim</div>

var d = window.document.querySelector(‘div#msg’)
d.style.background = ‘blue’

<strong>id → representada por #</strong>
<strong>class → representada por .</strong>

<div class=’msg’>Clique em mim</div>

var d = window.document.querySelector(‘div.msg’)
d.style.background = ‘blue’
```
## Aula 10 – Eventos DOM

### Como funciona o DOM com Javascript?

Evento é tudo o que possa acontecer com o elemento. Por exemplo, uma <div>.

#### Exemplo 1: 
```
<head>
  <style>
        div#area {
            font: normal 20pt Arial;
            background: rgb(93, 136, 37);
            color: white;
            width: 200px;
            height: 200px;
            line-height: 200px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div id='area'>
        Interaja...
    </div>
</body>
```
	
#### Eventos de mouse
- mouseenter: dispara quando o mouse chegar dentro da <div>;
- mousemove: dispara enquanto o mouse estiver movendo dentro da <div>;
- mousedown: dispara quando clicou e segurou o mouse;
- mouseup: dispara no momento em que soltar o mouse;
- click: dispara no momento do click inteiro;
- mouseout: dispara enquanto o mouse estiver fora da <div>;
Para conhecer mais tipos de eventos: https://developer.mozilla.org/pt-BR/docs/Web/Events

### Como criar funções em Javascript?

Função: conjunto de códigos que vai ser executado quando o evento ocorrer.
```
function ação(parâmetro){
bloco
}
```
	
### Como ligar uma função a um evento em um formulário HTML5 usando JavaScript?

Exemplo:
```
<body>
    <div id='area' onclick='clicar()' onmouseenter='entrar()' onmouseout='saiu()'>
        Interaja...
    </div>
    <script>
        var area = window.document.getElementById('area')

        function clicar(){
            area.innerText = 'Clicou'
            area.style.background = 'red'
        }
        function entrar(){
            area.innerText = 'Entrou'
        }
        function saiu(){
            area.innerText = 'Saiu'
            area.style.background = 'green'
        }
    </script>
</body>
```
ou também pode ser feito assim:
```
<script>
        var area = window.document.getElementById('area')

        area.addEventListener('click', clicar)
        area.addEventListener('mouseenter', entrar)
        area.addEventListener('mouseout', sair)

        function clicar(){
            area.innerText = 'Clicou'
            area.style.background = 'red'
        }
        function entrar(){
            area.innerText = 'Entrou'
            area.style.background = 'yellow'
        }
        function sair(){
            area.innerText = 'Saiu'
            area.style.background = 'green'
        }
    </script>
```
### Como descobrir erros no Javascript?

Clicar com o botão direito, ir em ‘Inspect’, entrar no Console e ver o que está escrito.
```
Exemplo: ‘Uncaught TypeError? Cannot read property ‘getElementById’ of undefined at exemplo6.html:26’
```
Isso que dizer que ele não conseguiu ler o elemento ‘getElementById’ na linha 26 (ou para cima).

### Como pegar valores dentro de caixas de texto e fazer cálculos com eles?

#### Exemplo:
```
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Eventos</title>
    <style>
        body {
            font: normal 18pt Arial;
        }
        input {
            font: normal 18pt Arial;
            width: 100px;
        }
        div#res {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Somando Valores</h1>
    <input type="number" name="txtn1" id="txtn1"> +
    <input type="number" name="txtn2" id="txtn2">
    <input type="button" value="somar" onclick="somar()">
    <div id='res'>Resultado</div>
    <script>
        function somar() {
            var tn1 = window.document.getElementById('txtn1')
            var tn2 = window.document.querySelector('input#txtn2')
            var res = window.document.getElementById('res')
            var n1 = Number(tn1.value)
            var n2 = Number(tn2.value)
            var s = n1 + n2
            res.innerHTML = `A soma entre ${n1} e ${n2} é: <strong>${s}</strong>`
        }
    </script>
</body>
```
	
# Módulo 4 – 
  
