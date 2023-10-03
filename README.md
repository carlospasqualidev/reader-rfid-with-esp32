# Leitor RFID ESP32 com Comunicação Web

Este é um exemplo de código para um dispositivo baseado em ESP32 que usa um leitor RFID MFRC522 para ler informações de cartões RFID e enviá-las para um servidor web local. Este README fornece uma visão geral do projeto, instruções de configuração e uso.

## Visão Geral

Este projeto implementa um sistema que utiliza um módulo RFID MFRC522 e um ESP32 para ler informações de cartões RFID e enviar essas informações para um servidor web. Aqui estão os principais componentes e funcionalidades do projeto:

1. **Configuração Wi-Fi**: O ESP32 se conecta a uma rede Wi-Fi específica usando as credenciais fornecidas no código.

2. **Leitura de Cartão RFID**: O módulo RFID MFRC522 é usado para detectar a presença de cartões RFID e ler seus números de identificação únicos (NUID).

3. **Comunicação Web**: Quando um cartão RFID é lido com sucesso, o ESP32 cria uma conexão com um servidor web local (com base no endereço IP) e envia os dados do cartão em formato JSON para esse servidor.

4. **Página Web Simples**: O servidor web local fornece uma página HTML simples que exibe os dados do cartão RFID lido.

5. **Protocolo HTTP**: O dispositivo ESP32 utiliza o protocolo HTTP para enviar os dados do cartão RFID como uma solicitação POST para o servidor web.

6. **Manuseio de Timeout**: O código inclui uma lógica de timeout para garantir que a conexão com o servidor web seja encerrada após um período especificado de inatividade.

## Uso

Para utilizar este projeto, siga estas etapas:

1. **Configuração do Hardware**: Conecte o módulo RFID MFRC522 ao ESP32 conforme as instruções do fabricante.

2. **Configuração do Software**: Abra o código-fonte fornecido neste repositório e atualize as credenciais de rede Wi-Fi e as configurações do servidor web conforme necessário.

3. **Carregue o Código**: Carregue o código-fonte no ESP32 usando a IDE do Arduino ou outra ferramenta de programação.

4. **Teste o Projeto**: Coloque um cartão RFID próximo ao leitor MFRC522 para testar a funcionalidade. Os dados do cartão devem ser enviados para o servidor web local.

5. **Personalização**: Personalize o projeto de acordo com suas necessidades, como integrando-o a um sistema de controle de acesso ou rastreamento de presença.

## Requisitos de Hardware

- ESP32
- Módulo RFID MFRC522
- Rede Wi-Fi disponível
- Servidor web local (pode ser executado em um computador ou dispositivo Raspberry Pi)
