# Diagramas

Para melhor compreensão do projeto foram desenvolvidos diagramas que explicam o funcionamento da arquitetura do programa. Sendo assim, foram desenvolvidos dois diagramas descrevendo a comunicação CANopen e um diagrama de classes da biblioteca local ManoplaLelyBBB (versão no padrão UML e versão mais detalhada dos métodos e atributos).

## Diagrama da Comunicação CANopen
Para descrever a comunicação CANopen foram desenvolvidos, dois diagramas: o primeiro descreve (CANopen Node) apresenta a estrutura e operação geral do protocolo; já o segundo (Master/Slave) apresenta a comunicação das estruturas Master e Slave presentes na CANopen.

O CANopen é um protocolo baseado no barramento CAN, usado em redes industriais para comunicação eficiente e em tempo real entre dispositivos. Ele organiza os dados em um Dicionário de Objetos, suporta configuração de rede, monitoramento de erros e sincronização, sendo ideal para automação e controle distribuído.

## Diagrama de Classes Manopla
O diagrama de classes é um tipo de modelagem de sistemas utilizado em programas orientados a objetos, em que demonstra-se a estrutura das classes do sistema (atributos e métodos) e como elas se relacionam (relações de herança, agregação, composição etc.).

A Manopla é um sistema de controle baseado no protocolo CANopen, projetado para operar motores em aplicações industriais ou robóticas. Ela integra hardware e software para gerenciar a comunicação com dispositivos CAN, configurando parâmetros como modos de movimento, velocidade e posição. Utilizando a biblioteca Lely, a Manopla orquestra eventos assíncronos, realiza callbacks para sincronização e monitora estados dos motores em tempo real, oferecendo um controle preciso e configurável.