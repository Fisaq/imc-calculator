# imc-calculator
<h1>Projeto de uma calculadora de IMC utilizando Javascript.</h1>

<div>
  <p> Este é um projeto que eu elaborei como parte da disciplina de Construcão de Software para Web, 
    neste eu desenvolvi uma calculadora de IMC utilizando JavaScript.</p>
<div/>
 
<div>
  <p> Para desenvolver o código eu criei uma funcão que ficaria responsável por aplicar a fórmula do IMC(massa/altura²). 
    Então eu criei 3 variáveis que receberiam valores antes estabelecidos no código em HTML, como mostrado à baixo:
    
    ```javascript
    const calcular = document.getElementById("calcular");

    function imc(){
      const nome = document.getElementById("nome").value;
      const altura = document.getElementById("altura").value;
      const peso = document.getElementById("peso").value;
      const resultado = document.getElementById("resultado");
    }
    ```
<div/>
