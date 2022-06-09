# imc-calculator
<h1>Projeto de uma calculadora de IMC utilizando Javascript.</h1>

<div>
  <p> Este é um projeto que eu elaborei como parte da disciplina de Contrução de Software para Web, 
    neste eu desenvolvi uma calculadora de IMC utilizando JavaScript.</p>
<div/>
 
<div>
  <p> Para desenvolver o código eu criei uma função que ficaria responsável por aplicar a fórmula do IMC (massa/altura²). 
    Então eu criei três variáveis que receberiam valores antes estabelecidos no código em HTML, como mostrado à baixo:
    
~~~javascript
    const calcular = document.getElementById("calcular");
    
      function imc(){
         const nome = document.getElementById("nome").value;
         const altura = document.getElementById("altura").value;
         const peso = document.getElementById("peso").value;
         const resultado = document.getElementById("resultado");
    }
~~~
  </p>
<div/>
  
<div>
  <p> Após isso eu criei uma condição em que caso todos os campos da calculadora fossem preenchidos o cáculo do IMC seria realizado 
    e uma mensagem armazenada numa variável de nome "clasificacao" do tipo let, seria exibida na tela. 
    
~~~javascript
    
        if(nome !== "" && altura !== "" && peso !== ""){

        const valorIMC = (peso/(altura*altura)).toFixed(2);     
        let classificacao = "";

        if(valorIMC < 18.5)
            classificacao = "abaixo do peso!";

        else if(valorIMC < 25)
            classificacao = "com peso normal.";

        else if(valorIMC < 30)
            classificacao = "com sobrepeso!";

        else if(valorIMC < 35)
            classificacao = "com obesidade grau I.";

        else if(valorIMC < 40)
            classificacao = "com obesidade grau II.";

        else if(valorIMC > 40){
            classificacao = " com obesidade grau III."; 
        }
        
        resultado.textContent = `${nome} seu IMC é ${valorIMC} e você está ${classificacao}`;
        
    }
    
~~~
  </p>
<div/>
 
<div>
  <p> Caso algum campo não estivesse preenchido, uma mensagem seria exibida pedindo para que o usuário preencha todos os campos.
    
~~~javascript
    else
        resultado.textContent = "Preencha todos os campos!"
~~~
  </p>
<div/>
  
<div>
  <p> Por fim eu fiz com que a função fosse chamada quando o usuário clicasse no botão "calcular".
    
 ~~~javascript
    calcular.addEventListener("click", imc);
 ~~~
  </p>
<div/>
