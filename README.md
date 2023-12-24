# CRIANDO PROJETO PORTIFOLIO GIT/GITHUB

|**_Instalação GIT_**|

|**_Instalação GITHUB_**|

|**_Criação Portifolio_**|

|**_Salvando dados Portifolio_**|

|**_Clonando dados do Portifolio_**|


|**_Jogo de 🏓 

!DOCTYPE html>
<html>
<head>
<title>Primeiro Jogo</title>
<style>

*{
	overflow: hidden;
    margin: 0;
    padding: 0;
}

</style>
</head>

<body>

<h1><center>Jogo de Ping-Pong</center></h1>

<canvas></canvas>
<script>

//Formato do canvas para imagens do jogo
const canvasEl = document.querySelector("canvas"),
canvasCtx = canvasEl.getContext("2d")

const lineWidth = 15

		function setup(){
		//Tamanho da tela do jogo
		canvasEl.width = canvasCtx.width = window.innerWidth
    	canvasEl.height = canvasCtx.height = window.innerHeight
		
}

		function draw(){
		//Stilo e tamanho preenchimento do campo
		canvasCtx.fillStyle = "#000000"
        canvasCtx.fillRect(0, 0, window.innerWidth, window.innerHeight)
        
        
        //Desenhando a linha de marcação central do campo
        canvasCtx.fillStyle = "#ffffff"
        const x = window.innerWidth / 2 - lineWidth / 2
        const y = 0
        const w = lineWidth
        const h = window.innerHeight
        canvasCtx.fillRect(x, y, w, h)
        
        
        //Desenhando a raquete esquerda
        canvasCtx.fillRect(10, 100, lineWidth , 200)
        
         //Desenhando a raquete direita
        canvasCtx.fillRect(window.innerWidth - lineWidth - 10, 200, lineWidth, 200)
        
        //Desenhando a bola do jogo
        
        canvasCtx.beginPath()
		canvasCtx.arc(200, 100, 10, 0, 2 * Math.PI, false);
        canvasCtx.fill()
		     
}

setup()
draw()

		</script>
	</body>
</html>


