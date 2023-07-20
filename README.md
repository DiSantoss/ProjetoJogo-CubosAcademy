# Jogo Básico para Treinar a Lógica de Programação
Este é um joguinho básico desenvolvido em JavaScript utilizando a biblioteca p5.js. O objetivo do jogo é mover o personagem pela tela até alcançar o ponto final. Para executar o código, você pode seguir os passos abaixo:

## Passos para Executar o Código
1. Acesse o site p5js.org em seu navegador.

2. Caso queira executar o jogo no link fornecido pelo criador do jogo, utilize o seguinte link: Joguinho Básico. Isso permitirá que você jogue o jogo diretamente sem fazer alterações.

3. Caso prefira criar o seu próprio arquivo, siga os passos abaixo:

3.1 Clique em "Editor" no site do p5.js para abrir o editor de código.

3.2 Copie o código fornecido abaixo (lembre-se de copiar apenas o que está dentro das aspas, sem as aspas).
```
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
  if (andarX < 0) {
    andarX = 0;
  }
  if (andarY < 0) {
    andarY = 0;
  }
  if (andarX > tela - tamanho) {
    andarX = tela - tamanho;
  }
  if (andarY > tela - tamanho) {
    andarY = tela - tamanho;
  }

  background(220)

  for (let i = 0; i < tela / tamanho; i++) {
    for (let j = 0; j < tela / tamanho; j++) {
      image(grama, i * tamanho, j * tamanho, tamanho, tamanho)
    }
  }

  image(personagem, andarX, andarY, tamanho, tamanho)

  if (andarX === tela - tamanho && andarY === tela - tamanho) {

    rect(160, 160, 256, 256)
    textSize(35)
    text('GANHOU', 200, 300)

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

function keyPressed() {
  if (keyIsDown(DOWN_ARROW)) {
    andarY += velocidade
  }
  if (keyIsDown(UP_ARROW)) {
    andarY -= velocidade
  }
  if (keyIsDown(LEFT_ARROW)) {
    andarX -= velocidade
  }
  if (keyIsDown(RIGHT_ARROW)) {
    andarX += velocidade
  }
}
```
4. No editor p5.js, clique na seta ao lado esquerdo do nome "sketch.js" para executar o jogo.

5. Na seta ao lado direito de "Sketch Files," clique e selecione uma imagem de sua preferência para a grama e outra para o personagem. Certifique-se de adicionar as imagens no mesmo diretório (pasta) do arquivo index.html, style.css e sketch.js.

6. Nas variáveis personagem e grama do código, substitua os nomes das imagens pelo caminho da imagem que você escolheu. Exemplo:

```
personagem = loadImage('person.jpg')
grama = loadImage('grama.jpg')
```
7. Clique no botão de "Executar" para iniciar o jogo.

# Start
![image](https://github.com/DiSantoss/ProjetoJogo-CubosAcademy/assets/99044745/f8ba1f40-a443-43aa-a698-37f90b5ffb18)

# Movimentação
![image](https://github.com/DiSantoss/ProjetoJogo-CubosAcademy/assets/99044745/4f3957b0-c20a-4648-9f6f-4cc888301cf8)

# Fim
![image](https://github.com/DiSantoss/ProjetoJogo-CubosAcademy/assets/99044745/b4ddfa12-d755-4baa-8daf-438f022be49e)

# Restart
![image](https://github.com/DiSantoss/ProjetoJogo-CubosAcademy/assets/99044745/e8751421-9cb8-47a2-9ba8-01f060177b82)





# Agradecimentos
Gostaríamos de agradecer à Cubos Academy e ao nosso Mestre Guido por fornecerem esse ensinamento e oportunidade de aprendizado com este joguinho básico. Aproveite o jogo e divirta-se enquanto treina a sua lógica de programação!
