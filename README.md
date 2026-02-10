# XSS-reflected-portswigger
passo a passo da resoluçao do primeiro lab de XSS do portswigger

esse lab pode ser encontrado em:
https://portswigger.net/web-security/cross-site-scripting/reflected/lab-html-context-nothing-encoded
a descrição do lab:
This lab contains a simple reflected cross-site scripting vulnerability in the search functionality.
To solve the lab, perform a cross-site scripting attack that calls the alert function.

Este laboratório contém uma vulnerabilidade simples de cross-site scripting refletido na funcionalidade de busca. Para resolver o laboratório, execute um ataque de cross-site scripting que invoque a função de alerta.
De acordo com a descrição do lab precisamos executar um ataque que chame a função alert.
como o lab se trata de um simples XSS refletido, podemos trabalhar com um payload mais simples como o:

<script>alert()</script>

O próprio portswigger tem uma página com diversos tipos de payloads, para as mais variadas situações.
https://portswigger.net/web-security/cross-site-scripting/cheat-sheet

para atacar uma vulnerabilidade XSS refletida, precisamos procurar um campo onde possamos passar o nosso payload. um campo de pesquisa por exemplo.
ao acessarmos a área do laboratório, logo na pagina inicial nos deparamos com o capo de pesquisa.

Image1


Tudo o que precisamos fazer agora é digitar o nosso payload nesse campo e clicar em search, para que o alerta seja emitido na tela.

Image2

O alerta foi gerado. 
Após clicar em ok e fechar o alerta, voltamos a pagina do laboratório onde aparece a mensagem de lab solved.

Image3


