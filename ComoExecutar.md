Para executar esse código voce deve ir ao site p5js.org
Acessar na sua conta ou se nao quiser acessar, pode, mas não salvará nada e tambem pode executar o joguinho usando o meu link, caso nao queira fazer na sua propria conta, o meu link é : https://editor.p5js.org/d.2120leandro/sketches/fiFDQ-7ll

Para fazer o seu proprio arquivo faça os seguintes passos :

1° Clique em Editor
2° Copie esse código e cole na caixa de edição, (somente oque está dentro do aspas, nao cole com aspas):
"

let personagem
let grama

const tamanho = 64
const tela = 576
const velocidade = 64

let andarX = 0;
let andarY = 0;



function setup() {
  createCanvas(tela, tela)
  
  personagem = loadImage('person.jpg')
  grama = loadImage('grama.jpg')
  
  
}



function draw() {
  if(andarX < 0) {
 andarX = 0;}
  if(andarY < 0) {
andarY = 0
}
  if(andarX > tela - tamanho) {
 andarX = tela - tamanho}
  
  if(andarY > tela - tamanho) {
 andarY = tela - tamanho}
  
  
  background(220)
  
  
  for(let i = 0; i < tela/tamanho;i++ ) {
 for(let j = 0; j < tela/tamanho;j++ ) {
    image(grama,i*tamanho,j*tamanho,tamanho,tamanho)
  }
  }
   
  image(personagem,andarX,andarY,tamanho,tamanho)
  
  if(andarX === tela - tamanho && andarY === tela - tamanho) {
  
  rect(160,160,256,256)
  textSize(35)
  text('GANHOU',200,300)
    
    
    restart = createButton('Reiniciar')
    restart.mousePressed(reset)
    
    
    noLoop()
  }
  
  
}

function reset() {
  andarX = 0;
  andarY = 0;
  restart.remove()
  loop()
}


function keyPressed(){

  
  if(keyIsDown(DOWN_ARROW)) {
    andarY += velocidade
  }
  if(keyIsDown(UP_ARROW)) {
    andarY -= velocidade
  }
  if(keyIsDown(LEFT_ARROW)) {
    andarX -= velocidade
  }
  if(keyIsDown(RIGHT_ARROW)) {
    andarX += velocidade
  }
}

"

3° clique na seta ao lado esquerdo do nome "sketch.js".

4° na seta ao lado direito de "Sketch Files" 
clique e selecione uma imagem do seu gosto para a grama e uma imagem para o personagem, assim adicionando as imagens para o diretorio
obs: as imagens devem ficar listadas no mesmo diretorio (pasta) do arquivo index.html , style.css e sketch.js     

5° na variavel personagem e grama la no codigo, voce deve colocar o caminho da imagem dentro de loadImage colocando o nome do arquivo e a extensão que neste caso é jpg. Exemplo :
 personagem = loadImage('person.jpg')

 Pronto, pode apertar no botão de executar e ver o joguinho Funcionando


 Gostaria de agradecer a Cubos Academy e ao nosso Mestre Guido por esse ensinamento!

