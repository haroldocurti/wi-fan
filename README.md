# wi-fan
Dar capacidades de comunicação e controle wi-fi a um ventilador Mondial, integrando-o através do ESPHOME ao Homeassistant.

## Introdução
O projeto nasceu da necessidade de operar os ventiladores da casa pelo sistema de automação Home Assistant. Com isto, será possível ligar e desligar e incluir em automações os aparelhos que não tinham esta capacidade.

## Hardware

### O Ventilador
<img src="https://user-images.githubusercontent.com/83146137/192291599-20a5dae7-fb0e-43e2-b2c0-98bdd5edf9bc.png" width="100" height="100">

Usei em meu projeto um ventilador Mondial Turbo Force 8, que dispõe de três velocidades e também um sistema de repelente. O sistema de repelente não será utilizado e será inutilizado para dar espaço ao microcontrolador que comandará o aparelho.
Não é necessário executar nenhuma modificação na parte elétrica do motor, apenas no encoder.

### Módulo relé de 4 canais.
<img src="https://user-images.githubusercontent.com/83146137/192291049-3f74a98f-0710-49bf-82d1-384580286a7d.png" width="100" height="100">
Usado para substituir fisicamente o encoder original do ventilador.

### Encoder Rotacional KY-040
<img src="https://user-images.githubusercontent.com/83146137/192290706-da0ba3c4-fa64-4dae-8186-1db56c847a6f.png" width="100" height="100">

É um encoder rotatório comumente usado para medir movimento rotacional de um eixo, pois converte movimentos rotativos em impulsos elétricos. Ele foi usado para servir de interface de operação manual do ventilador.

### Microcontrolador Esp8266 NodeMCU
<img src="https://user-images.githubusercontent.com/83146137/192289854-d0066552-fa72-4392-9d72-a62aa2305a0e.png" width="100" height="100">

É o cérebro do sistema. Foi escolhido por ter Wi-fi, numero de pinos e tamanho adequado.
Descrição do Microcontrolador (por FILIPEFLOP):
O módulo Wifi ESP8266 NodeMCU é uma placa de desenvolvimento que combina o chip ESP8266, uma interface usb-serial e um regulador de tensão 3.3V.

## Software

Incluirei aqui apenas o que foi usado em mais alto nível, excluindo coisas como, por exemplo, sistema operacional, como fazer flash do arquivo para o MCU, etc...

### ESPHOME
