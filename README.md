## Controle de LED com Python, Mediapipe & Arduino | OpenCV Python | Integração com Arduino

Este projeto foi desenvolvido durante o primeiro semestre na FATEC - Carapicuíba, como parte da disciplina de Laboratório de Hardware.

Neste projeto, adaptei um Arduino e alguns LEDs para controlar o acendimento de LEDs com base no número de dedos levantados, usando mediapipe para detectar os dedos e realizar cálculos para determinar a quantidade de dedos levantados.

### Tecnologias Utilizadas

#### Protótipação
- **Tinkercad**: Utilizado para a construção digital do hardware.

#### Backend
- **C++**: Para configuração da placa Arduino Uno.
- **Python**: Para o funcionamento geral do sistema.

### Vídeos de Referência

- [Vídeo base para o projeto](https://www.youtube.com/watch?v=hKbtfto9trw&t=11s)
- [Vídeo para entendimento do HandScanner](https://www.youtube.com/watch?v=RbqGPFrWZC8)

### Problema Resolvido

Durante o desenvolvimento, encontrei um problema relacionado ao uso do **pyfirmata**, que resultava no seguinte erro: `module 'inspect' has no attribute 'getargspec'`. Esse erro foi resolvido com a ajuda de uma solução encontrada no StackOverflow.

- [Resposta no StackOverflow](https://stackoverflow.com/questions/74585622/pyfirmata-gives-error-module-inspect-has-no-attribute-getargspec)

#### Correção Aplicada

A correção foi feita alterando a versão do Python e modificando o código no arquivo `pyfirmata.py`, substituindo a linha:

```python
len_args = len(inspect.getargspec(func)[0])

len_args = len(inspect.getfullargspec(func)[0])

```
### Demo https://i.imgur.com/nqTiED8.mp4

