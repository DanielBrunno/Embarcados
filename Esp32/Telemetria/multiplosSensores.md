  Este estudo visa desenvolver um firmware em ESP32 com leitura de múltiplos sensores e envio de frames de telemetria ("mapa de registradores"), 
irei estruturá-la em linguagem C modular não-bloqueante (sem uso de delay() para não parar o funcionamento do hardware). Para ser embarcado na
minha placa ESP32 WROOM-32D como o módulo de telemetria, segurança e iluminação de um projeto de plataforma robótica.

1. Arquitetura modular e conexão com a plataforma robótica:

   Serão seis sub-sistemas e para que os subsistemas rodem simultaneamente sem travar a leitura dos ultrassônicos, nem o PWM do buzzer, o firmware será dividido em máquinas de estado assíncronas e um protocolo de registradores virtuais via UART (Serial).
   
