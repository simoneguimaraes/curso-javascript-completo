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
	
	
  
## Aula 8 – Operadores (parte 2)

	

  
  
# Módulo 3 – Entendendo o DOM

  
  
  
