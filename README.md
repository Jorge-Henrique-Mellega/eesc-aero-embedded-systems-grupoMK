# Grupo SAA0356 - Sistemas Embarcados para Veículos Aéreos

Docente: Glauco Augusto de Paula Caurin
<br>
Integrantes do Grupo:<br>
                      Alice Czyz Froes Fontes - 11802478 <br>
                      Jorge Henrique Mellega - 11802610 <br>
                      Rhayna Christiani Vasconcelos Marques Casado - 13676429 <br>
                      Jackson Wagner Silva - 12696211 <br>
                      Vitor Marques Delmondes - 10820949 <br>

# Introdução
Este projeto do github é uma fork do projeto original desenvolvido por Henrique Garcia (@griloHBG), disponível em https://github.com/griloHBG/eesc-aero-embedded-systems. Portanto, o objetivo é realizar alterações de forma a corrigir bugs, tornar o software mais fácil de utilizar e expandir suas funcionalidades. Tais objetivos foram propostos pelo docente supracitado, cujo intuito é estimular o desenvolvimento dos alunos envolvidos na área de sistemas embarcados.

Este projeto visa a implementação de um sistema de controle de motores para sistemas embarcados utilizando diversas estratégias de controle, como PID e dLQR. 

Um controle PID (Proporcional, Integral, Derivativo) é uma técnica amplamente utilizada em sistemas de controle automático para ajustar a saída de um processo de modo a alcançar um valor desejado (setpoint). Esse tipo de controle combina três ações básicas: a componente proporcional (P), que responde ao erro instantâneo; a componente integral (I), que acumula o erro ao longo do tempo para corrigir desvios persistentes que o componente proporcional não consegue resolver; e a componente derivativa (D), que reage à taxa de variação do erro, ajudando a antecipar mudanças e reduzir excessos de resposta, embora seja sensível a ruídos e requeira ajustes cuidadosos.

Já o controle LQR é uma técnica de controle ótimo aplicada a sistemas dinâmicos lineares com realimentação de estados. Ele é usado para projetar um controlador que minimiza um funcional de custo quadrático, buscando um equilíbrio entre o desempenho do sistema e o esforço de controle.

# Quickstart

## Requisitos
Para utilizar o software, espera-se que o usuário tenha instalado em sua máquina as ferramentas git e docker. Para mais informações, consulte as documentações oficiais.

## Compilação para ARM
Primeiramente, realize o clone deste repositório git, navegue para a pasta do software e execute os comandos:

```bash
sudo docker build -f dockerfile/Dockerfile -t myimage .
sudo docker run -it -v .:/project --rm myimage bash
```

Note que "myimage" pode ser alterado para qualquer nome de sua preferência.

Uma vez dentro do container, execute:

```bash 
cd /project
mkdir build_arm
cd build_arm
cmake .. -DARM_TARGET=1
pkg-config --cflags liblely-coapp
pkg-config --libs liblely-coapp
make
```
Seu arquivo executável para ARM estará disponível na pasta build_arm com o nome "eesc-aero-embedded-systems-grupoMK".




