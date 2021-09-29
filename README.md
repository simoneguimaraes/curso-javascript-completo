# Módulo 1 – Conhecendo o Javascript

## Aula 1 – O que o Javascript é capaz de fazer?

### O que é a linguagem Javascript/ECMAScript?
### O que é um cliente e um servidor?
### Para que servem as tecnologias HTML5, CSS3 e Javascript?
### Cite 4 sites que utilizam a linguagem JavaScript nos seus códigos.


## Aula 2 – Como chegamos até aqui?

### Qual empresa criou o Javascript?
### Qual a diferença entre as linguagens Java e Javascript?
### Qual é a relação que existe entre as linguagens Javascript e ECMAScript?
### O programa usado para acessar o WhatsApp no computador é feito em JavaScript.


## Aula 3 – Dando os primeiros passos

### Quais são os melhores livros de Javascript em português?
### Onde ter acesso à documentação oficial do Javascript em português e inglês?
### Quais são os requisitos de software para aprender a programar em Javascript?
### Qual é o melhor editor para códigos Javascript?
### Como instalar e configurar o Node.js?
### Para aprender Javascript, é realmente necessário saber muito inglês?
### Você está precisando de dicas para estudar e aprender de verdade?


## Aula 4 – Criando o seu primeiro script

### Você já sabe diferenciar dentro do seu codigo os trechos em HTML5, CSS3 e Javascript?
### Sabe organizar as pastas do seu projeto dentro do Visual Studio Code?
### Sabe como testar se o Node.js está devidamente instalado?

### Já sabe utilizar os comandos alert, confirm e prompt do Javascript?

alert(‘Seja bem-vindo/a)
<br>confirm(‘Você já é nosso aluno?’)
<br>prompt(‘Digite o seu nome’)
<br>
<br>O HTML é dividido entre as tagas <head> e <body>
<br>O CSS pode ser inserido no HTML com a tag <style>
<br>O JavaScript pode ser inserido no HTML com a tag <script>

# Módulo 2 – Comandos Básicos do Javascript

## Aula 5 – Variáveis e Tipos Primitivos

### Como criar comentários?

//            → uma única linha de código
<br>/*    
<br>*/    → mais de uma linha de código

### O que são variáveis?

A memória do computador tem espaços delimitados para receber valores (assim como vagas no estacionamento).

### Como declarar variáveis no Javascript?

A vaga a1 = carro1
<br>(leia: a vaga a1 recebe o carro1)
<br>a1 = carro2
<br>(o carro1 saiu e entrou o carro2)
<br>a1 = null
<br>(a vaga está nula)
<br>
<br>var n1 = 5      → int: número inteiro
<br>var n2 = 8.5    → float: número real
<br>var n3 = 15     → int: número inteiro
<br>
<br>var s1 = “São Paulo”
<br>var s2 = ‘Lumpa’
<br>var s3 = `Janeiro`

### Regras para nomear as variáveis

<ul>
  <li>Podem começar com letra, $ ou _</li>
  <li>Não podem começar com números</li>
  <li>É possível usar letras ou números</li>
  <li>É possível usar acentos e símbolos</li>
  <li>Não podem conter espaços</li>
  <li>Não podem ser palavras reservadas</li>
</ul>

### Para entrar no Node, você vai precisar entrar no VS Code e digitar “crtl + shift + `” 

<ul>
  <li>digitar: node</li>
  <li>para limpar tela: ctrl + l</li>
  <li>para sair: .exit</li>
</ul>

### Quais são os tipos primitivos do Javascript?

#### Os tipos primordiais:

<ul>
  <li>Number:   5     18    -12    3.14</li>
  <li>String: “Google”    ‘Javascript’    `Maria`    ‘12553-120’</li>
  <li>Boolean: true     false</li>
</ul>
  
#### Outros tipos:

<ul> 
  <li>Tipos internos de Number:</li>
      <ul> 
        <li>Infinity</li>
        <li>NaN (not a number)</li>
      </ul>
  <li>Null</li>
  <li>Undefined</li>
  <li>Tipo interno de Object</li>
      <ul> 
        <li>Array</li>
      </ul>
  <li>Function</li>
</ul>
 
### Como conferir qual o tipo da variável que foi declarada?

typeof  → saber qual é o tipo da variavel
<br>Colocar no terminal (Node): 
<br>var num = 200
<br>typeof num

### Consegue entender o que significa colocar um valor null dentro de uma variável em Javascript?

Null é representa um valor nulo ou vazio, e aponta para um objeto inexistente.

  
## Aula 6 – Tratamento de dados

### Como guardar o resultado de um prompt dentro de uma variável?

var nome = prompt(‘Qual é o seu nome’)

### Concatenação: para juntar a string com a variável
alert(‘É um prazer te conhecer, ‘ + nome)  

### Como somar variáveis?
var num1 = prompt(‘Digite um número: ‘)
<br>var num2 = prompt(‘Digite outro número: ‘)
<br>var sum = num1 + num2
<br>alert(‘A soma dos valores é “ + sum)

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
- `O aluno ${nome} com ${idade} tirou a nota ${nota} ` 

### Formatando strings:

var s = ‘Javascript’
- s.lenght              → quantos caracteres a string tem
- s.toUpperCase()       → tudo para maiúsculas
- s.toLowerCase()       → tudo para minúsculas

### Consegue formatar um número para que ele se pareça com um valor monetário?

Exemplo:
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

## Aula 7 – Operadores (parte 1)
	
Quais são os operadores do Javascript?

### Aritméticos
3 + 2 → 5
<br>3 - 2→ 5
<br>3 * 2→ 6
<br>3 / 2→ 1.5
<br>3 % 2→ 1
<br>3 ** 2→ 9

### Atribuição
var a = 5 + 3    →8
<br>var b = a % 5  → 3 
<br>var c = 5 * c ** 2 → 45
<br>var d = 10 – a / 2  → 6
<br>var e = 6 * 2 / d → 2
<br>var f = b % e + 4 / e → 3

#### Auto-atribuições

var n = 3 → n = 3

<br>n = n + 3 → n = 7
<br>n = n – 5 → n = 2

#### Simplificando as operações

n = n + 3 → n+= 3
<br>n = n – 5 → n -= 5 

### Qual a ordem de precedência dos operadores em JavaScript?

Parêntesis, potência, multiplicação, divisão, resto, adição, subtração.
<br>5 + 3 / 2 → 5 + (3 / 2) → 6.5

### Como usar os operadores de incremento (pré-incremento e pós-incremento) no JavaScript?

#### Pré-incremento
var x = 5
<br>x = x + 1 → x++ → 6
<br>x = x – 1 →  x--  → 5

#### Pós-incremento
var x = 4
<br>x = x + 1 → ++x → 5
<br>x = x – 1 →  --x  → 4

## Aula 8 – Operadores (parte 2)
	
### Relacionais
>   → maior
<br><    → menor
<br>>=  → maior ou igual
<br><=  → menor ou igual
<br>==  → igual
<br>!=   → diferente

#### Exemplos:
preço >= 200.50
<br>idade < 18
<br>curso == ‘Javascript’
<br>n1 != n2

#### Identidade:
5 == 5    → true
<br>5 == ‘5’  → true (é igual? O valor é igual.)
<br>5 === ‘5’  → falso (é idêntico? O valor e tipo não são iguais.)
<br>5 === ‘5’  → true (é idêntico? O valor e tipo são iguais.)

### Lógicos

#### !  → negação

! true →false
<br>! false → true

#### &&  → conjunção (E)

true && true → true
<br>true && false → false
<br>false && true → false
<br>false && false → false
<br>
<br>A condição só me satisfaz se as duas forem verdadeiras.

#### ||  → disjunção (OU)

true && true → true
<br>true && false → true
<br>false && true → true
<br>false && false → false
<br>
<br>A condição me satisfaz se pelo menos um for verdadeiro.

##### Exemplo 1:
var a = 5
<br>var b = 8
<br>
<br>a > b && b % 2 == 0 
<br>false  &&  true → false
<br>
<br>a < b || b / 2 == 2 
<br>true  ||  false → true

#### Exemplo 2:
idade >= 15 && idade <= 17
<br>estado == ‘RJ’ || estado == ‘SP’
<br>salario > 2500 && sexo != ‘masculino’

### Ordem de precedência das operações
Primeiro ele faz os operadores aritméticos, depois relacionais e depois lógicos.
<br>Primeiro ele faz o NÃO, depois o E, depois o OU. 
<br>
<br>Aritméticos > Relacionais > Lógicos (Não > E > OU)

### Ternário
?
<br>:
<br>
<br>teste ? true : false
<br>media >= 7 ? ‘Aprovado’ : ‘Reprovado’

#### Exemplo 1:
var media = 9
<br>
<br>media >= 7 ? ‘Aprovado’ : ‘Reprovado’      
<br>→ ‘Aprovado’
<br>
<br>media -= 3     
<br>media >= 7 ? ‘Aprovado’ : ‘Reprovado’      
<br>→ ‘Reprovado’

#### Exemplo 2:

var x = 8
<br>
<br>var res = x % 2 == 0 ? 5 : 9
<br>
<br>como (x % 2 == 0) é true 
<br>→ 5

#### Exemplo 3:

var idade = 19
<br>var entradaBar = idade >= 18 ? ‘Pode entrar.’ : ‘Não pode entrar.’
<br>entradaBar
<br>→ ‘Pode entrar.’
<br>
<br>idade -= 5
<br>var entradaBar = idade >= 18 ? ‘Pode entrar.’ : ‘Não pode entrar.’
<br>entradaBar
<br>→ ‘Não pode entrar.’
  
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
<br>
<br>Alguns objetos do window:
- locations → qual é a localizacao do site (ex: url, pagina anterior, pagina atual)
- document → documento atual
	<ul>
        <li>HTML (é parent de head e body)</li>
		<ul>
            <li>head (é child do HTML)</li>
			<ul>
                <li>meta</li>
                <li>title</li>
			</ul>
            <li>body (é child do HTML)</li>
            <li>h1</li>
            <li>p</li>
            <li>p</li>
			<ul>
                <li>strong</li>
			</ul>
            <li>div</li>
		</ul>
	</ul>
- history → guarda de onde você veio e pra onde você vai, facilitando a navegação no site

### Como usar o Javascript para manipular o DOM?

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

### Para quem servem os elementos Parent e Child em um DOM?

Elemento é todo item que aparece na árvore DOM.
<br>HTML é parent de Body e é child de Document.

### Como usar métodos de acesso ao DOM no Javascript?

Você pode selecionar os elementos para navegar dentro da árvore DOM.
<br>
<br>Alguns métodos de acesso ao DOM são por:

#### 1. Marca (TagName)
getElementByTagName()
<br>var p1 = window.document.getElementsByTagName(“p”)[0] → para selecionar o primeiro parágrafo
<br>document.write(“Está escrito nesse parágrafo: ” + p1.innerHTML)
<br>
<br>var p2 = window.document.getElementByTagName(‘p’)[1] → para selecionar o segundo parágrafo
<br>document.write(“Está escrito nesse parágrafo: ” + p1.innerText) → innerText não leva a formatação. O innerHTML leva a formatação.
<br>
<br>// para editar os elementos no javascript
<br>p1.style.color = ‘blue’
<br>
<br>var corpo = window.document.body
<br>corpo.style.background = ‘black’

#### 2. ID
getElementById()
<br>
<br><div id=’msg’>Clique em mim</div>
<br>
<br>var d = window.document.getElementById(‘msg’)
<br>d.style.background = ‘green’
<br>d.innerText = ‘Estou aguardando...’

#### 3. Nome
getElementByName()
<br>
<br><div name=’msg’>Clique em mim</div>
<br>
<br>var c = window.document.getElementsByName(‘msg’)[0]
<br>c.innerText = ‘Prazo confirmado.’

#### 4. Classe
<br>getElementByClassName()
<br>
<br><div class=’msg’>Clique em mim</div>

#### 5. Seletor
<br>querySelector
<br>
<br><div id=’msg’>Clique em mim</div>
<br>
<br>var d = window.document.querySelector(‘div#msg’)
<br>d.style.background = ‘blue’
<br>
<br><strong>id → representada por #</strong>
<br><strong>class → representada por .</strong>
<br>
<br><div class=’msg’>Clique em mim</div>
<br>
<br>var d = window.document.querySelector(‘div.msg’)
<br>d.style.background = ‘blue’
	
## Aula 10 – Eventos DOM
  

	
# Módulo 4 – 
  
