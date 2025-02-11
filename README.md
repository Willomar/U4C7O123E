# 🎮 Controle de Servomotor com PWM e LED no Raspberry Pi Pico 🚀

Este projeto demonstra o controle de um servomotor e um LED utilizando PWM (Modulação por Largura de Pulso) no **Raspberry Pi Pico**. O servomotor é controlado para se mover suavemente entre 0° e 180°, enquanto o brilho do LED é ajustado proporcionalmente à posição do servomotor. 💡

---

## 🛠️ Componentes Utilizados

- **Raspberry Pi Pico**: Microcontrolador utilizado para gerar os sinais PWM. 🖥️
- **Servomotor**: Motor micro servo padrão, controlado pelo GPIO 22. 🎯
- **LED**: LED simples conectado ao GPIO 12, com brilho controlado por PWM. 💡
- **Simulador Wokwi**: Ambiente de simulação utilizado para testar o projeto. 🎮

---

## 🔌 Diagrama de Conexões

O projeto foi simulado no Wokwi com o seguinte diagrama de conexões:

```json
{
  "version": 1,
  "author": "Willomar Sares dos Santos",
  "editor": "wokwi",
  "parts": [
    { "type": "wokwi-pi-pico", "id": "pico", "top": -3.15, "left": -6, "attrs": {} },
    { "type": "wokwi-servo", "id": "servo1", "top": 17.2, "left": 115.2, "attrs": {} },
    {
      "type": "wokwi-led",
      "id": "led2",
      "top": 111.6,
      "left": -159.4,
      "attrs": { "color": "red" }
    }
  ],
  "connections": [
    [ "servo1:GND", "pico:GND.8", "black", [ "h-9.6", "v-38.4", "h-39.6" ] ],
    [ "servo1:V+", "pico:3V3", "red", [ "h-28.8", "v-28.7", "h-20.4" ] ],
    [ "servo1:PWM", "pico:GP22", "blue", [ "h-9.6", "v29", "h-20.4" ] ],
    [ "pico:GP12", "led2:A", "green", [ "h0" ] ],
    [ "led2:C", "pico:GND.1", "black", [ "v0", "h-18.8", "v0", "h0", "v0", "h0", "v0" ] ]
  ],
  "dependencies": {}
}
🎥 Vídeo Explicativo
Confira o vídeo explicativo do projeto:
[Vídeo Explicativo
](https://youtu.be/aj70q1q8hks
)
🚀 Funcionamento do Projeto
O projeto realiza as seguintes operações:

Posicionamento do Servomotor:

O servomotor é posicionado em 0°, 90° e 180°, com pausas de 5 segundos em cada posição. ⏱️

O LED é desligado em 0°, com brilho médio em 90° e brilho máximo em 180°. 💡

Movimentação Suave:

Após posicionar o servomotor nas três posições, o código entra em um loop onde o servomotor se move suavemente entre 0° e 180°. 🔄

O brilho do LED é ajustado proporcionalmente à posição do servomotor. 🌈

Controle de Brilho do LED:

O brilho do LED é controlado por PWM, variando de 0% (desligado) a 100% (brilho máximo) conforme a posição do servomotor. 💡
