LAB10 - Projeto Final
Controle de LED Using Python,Mediapipe & Arduino | OpenCV Python l Python e integração com Arduino

Primeiro a prototipação do hardware no Arduino no Tinkercad, um website para a prototipação do sistema do hardware com uma fácil aplicação, montagem e entendimento. Com esse software primeiro ajustei todos os Jumpers, Leds e portas digitais do arduíno. 
 
Com protótipo feito e com a biblioteca StandardFirmata já instalada na placa, fizemos os testes de integração. Então com tudo certo passei para a montagem física.
 
Hardware físico já montado. Então partimos para a programação em python para fazer o hand scanner para acender os Leds conforme a quantidade de dedos contados levantados contados pelo scanner do sistema. 


Primeiro fizemos a lógica da leitura das mãos utilizando Mediapipi e OpenCV. Então vamos para o código para realizar tanto a abertura da câmera e leitura das mãos e também realizar a contagem dos dedos levantavam com uma matemática de pontos de coordenadas.  
 
Aqui já realizamos o entendimento da biblioteca e como se faz o hand scann, também como fazer a logica matemática para saber quais dedos estão levantados ou não. Agora partimos para a aplicação desses inputs dos dedos levantados para os inputs para ascender os leds do hardware previamente montado.
 
Aqui temos os dois códigos para o perfeito funcionamento da nossa aplicação. No código da direita temos a importação das bibliotecas, após temos a abertura do vídeo e atribuindo ele a um laço infinito, e também atribuindo um quantidade de dedos detectados e dedos levantados, após fazemos a logica matemática para contar os dedos levantados utilizando as coordenadas dos pontos da mão que são os pontinhos vermelhos em cada extremidade da mão, quando o numero da ponta tem um valor inferior de coordenada de um ponto 2 números abaixo na matriz dos pontos significa que o dedo esta abaixado, logo se a coordenada do dedo é superior a do seu relativo em 1 ponto abaixo na matriz ele está levantado. 
E no código da esquerda vemos essa lógica sendo aplicada para que esses inputs ascendam os leds. 
 
 



# Vídeo base para o projeto.
https://www.youtube.com/watch?v=hKbtfto9trw&t=11s

# Vídeo para o entendimento do handscaner.
https://www.youtube.com/watch?v=RbqGPFrWZC8

#As resposta sobre a questão do pyfirmata no StackOverflow .https://stackoverflow.com/questions/74585622/pyfirmata-gives-error-module-inspect-has-no-attribute-getargspec

# Correção de alguns erros pelo StackOverflow corrigindo a versão do python e trocando a linha de código no arquivo pyfirmata de: 
len_args = len(inspect.getargspec(func)[0]) para 
len_args = len(inspect.getfullargspec(func)[0]) 

