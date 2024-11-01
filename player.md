# Player de Mídia Digital da SWIFT

O Player de mídia digital é um equipamento da SWIFT projetado para transmitir conteúdo para painéis de LED e TVs. Ele recebe informações da empresa VTT, responsável pela atualização do conteúdo, que inclui comerciais da SWIFT. O pessoal de marketing da SWIFT envia novos conteúdos para a VTT, que, por sua vez, os envia para os players.

### Foto do Player (caso perguntem sobre o Player explicar e mostrar a foto)
<img src="https://github.com/Lguilherme99/Players/blob/main/Player.PNG" alt="Player de Mídia Digital" width="400px">

## Infraestrutura Necessária

Cada loja da SWIFT possui um NICHO, que é um espaço com uma portinha, projetado para guardar equipamentos. Dentro desse nicho, há um ponto de rede conectado ao rack de TI da loja. Esse ponto deve estar ligado a um modem de banda larga ou a uma antena 4G. Algumas lojas usam banda larga da Claro ou VIVO Fibra, enquanto outras possuem antena 4G.

### Foto do Nicho (caso perguntem algo sobre o nicho explicar e mostrar a foto)
<img src="https://github.com/Lguilherme99/Players/blob/main/Nicho.jpg" alt="Nicho de Equipamentos" width="400px">

Para garantir o funcionamento do Player, verifique os seguintes pontos:

### Conexões
1. O Player deve estar conectado a um cabo de rede diretamente ao ponto de rede.
2. A fonte de alimentação deve estar conectada à tomada.
3. Se a loja possui uma TV, o cabo HDMI do Player deve estar conectado diretamente à TV.
   Foto da TV: (caso perguntem algo sobre a TV explicar e mostrar a foto)
   <img src="https://github.com/Lguilherme99/Players/blob/main/TV.jpg" alt="Conexão com TV" width="400px">

4. Se a loja possui um painel de LED, conecte o cabo HDMI do Player a um ponto no Player e ao equipamento SendBox. Para isso, um conversor de HDMI para DVI é necessário (o DVI é usado para converter o HDMI do Player para o SendBox).

   Foto Painel de LED (caso perguntem sobre o painel mostrar a foto)
   <img src="https://github.com/Lguilherme99/Players/blob/main/Painel%20de%20LED.jpg" alt="Conexão com Painel de LED" width="400px">

5. Um cabo de rede do SendBox deve estar conectado ao painel de LED.
6. Um cabo com ponta P2 e RCA deve ser conectado do Player a um amplificador, que é responsável pelo áudio das caixas de som da SWIFT.

## Possíveis Problemas e Soluções

### 1. Player Offline
Se o Player estiver offline, siga estas etapas:

- Verifique a Internet: Acesse o painel de lojas no Grafana através da URL: [Grafana SWIFT](http://grafana.swift.com.br/d/MqX7ba-Sz/lojas?orgId=3).

1. No dashboard, verifique a linha chamada CFTV; se estiver online, a internet da banda larga está funcionando. Para lojas com antena, entre em contato com a equipe de monitoria para validação.

2. **Validação do Ponto de Rede**:
   - Verifique se o ponto de rede do Player está conectado ao modem de banda larga ou à antena.
   - Utilize um testador de cabos ou um notebook para validar a conexão. Conecte o cabo de rede ao notebook e verifique se há acesso à internet. 
   - Solicite um comando `IPCONFIG` para verificar se o IP está na faixa correta (ex: `172.16.0.1` ou `192.168.0.1`).

...

### 2. Troca do Player
Para solicitar um novo Player:

1. Abra um chamado no Automidia pelo link: [Servicedesk JBS](https://servicedesk.jbs.com.br/).
2. Na abertura do chamado, informe o número da loja e descreva a necessidade de um novo Player.

...

### 3. Problemas com o Cabo de Rede
Se o cabo de rede ou ponto de rede não estiver funcionando no testador de cabos, solicite que o RJ45 e o Keystone sejam refeitos.

...

### 4. Mensagem de Erro DUID no Painel de LED ou TV
Caso o painel de LED ou TV apresente a mensagem DUID (ID) e solicite digitar uma chave para validar:

- Se não for uma TV, será necessário solicitar um Findup para que um técnico conecte o monitor com o conversor no Player e tente abrir o TeamViewer QS.
