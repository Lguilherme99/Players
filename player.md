# Player de Mídia Digital da SWIFT

O Player de mídia digital é um equipamento da SWIFT projetado para transmitir conteúdo para painéis de LED e TVs. Ele recebe informações da empresa VTT, responsável pela atualização do conteúdo, que inclui comerciais da SWIFT. O pessoal de marketing da SWIFT envia novos conteúdos para a VTT, que, por sua vez, os envia para os players.

### Foto do Player (caso perguntem sobre o Player explicar e mostrar a foto)
<img src="https://github.com/Lguilherme99/Players/blob/main/Player.PNG" alt="Player de Mídia Digital" width="300px">

## Infraestrutura Necessária

Cada loja da SWIFT possui um NICHO, que é um espaço com uma portinha, projetado para guardar equipamentos. Dentro desse nicho, há um ponto de rede conectado ao rack de TI da loja. Esse ponto deve estar ligado a um modem de banda larga ou a uma antena 4G. Algumas lojas usam banda larga da Claro ou VIVO Fibra, enquanto outras possuem antena 4G.

### Foto do Nicho (caso perguntem algo sobre o nicho explicar e mostrar a foto)
<img src="https://github.com/Lguilherme99/Players/blob/main/Nicho.jpg" alt="Nicho de Equipamentos" width="300x">

Para garantir o funcionamento do Player, verifique os seguintes pontos:

### Conexões
1. O Player deve estar conectado a um cabo de rede diretamente ao ponto de rede.
2. A fonte de alimentação deve estar conectada à tomada.
3. Se a loja possui uma TV, o cabo HDMI do Player deve estar conectado diretamente à TV.
   Foto da TV: (caso perguntem algo sobre a TV explicar e mostrar a foto)
   <img src="https://github.com/Lguilherme99/Players/blob/main/TV.jpg" alt="Conexão com TV" width="300px">

4. Se a loja possui um painel de LED, conecte o cabo HDMI do Player a um ponto no Player e ao equipamento SendBox. Para isso, um conversor de HDMI para DVI é necessário (o DVI é usado para converter o HDMI do Player para o SendBox).

   Foto Painel de LED (caso perguntem sobre o painel mostrar a foto)
   <img src="https://github.com/Lguilherme99/Players/blob/main/Painel%20de%20LED.jpg" alt="Conexão com Painel de LED" width="300px">

5. Um cabo de rede do SendBox deve estar conectado ao painel de LED.
6. Um cabo com ponta P2 e RCA deve ser conectado do Player a um amplificador, que é responsável pelo áudio das caixas de som da SWIFT.

## Possíveis Problemas e Soluções

### 1. Player Offline
Se o Player estiver offline, siga estas etapas:

- Verifique a Internet: Acesse o painel de lojas no Grafana através da URL: [Grafana SWIFT](http://grafana.swift.com.br/d/MqX7ba-Sz/lojas?orgId=3).

1. No dashboard, verifique a linha chamada CFTV; se estiver online, a internet da banda larga está funcionando. Para lojas com antena, entre em contato com a equipe de monitoria/conectividade para validação.

2. **Validação do Ponto de Rede**:
   - Verifique se o ponto de rede do Player está conectado ao modem de banda larga ou à antena.
   - Utilize um testador de cabos ou um notebook para validar a conexão. Conecte o cabo de rede ao notebook e verifique se há acesso à internet. 
   - Solicite um comando `IPCONFIG` para verificar se o IP está na faixa correta (ex: `172.16.0.1` ou `192.168.0.1`).
   Se o Player estiver offline, siga estas etapas:

Verifique a Internet: Acesse o painel de lojas no Grafana através da URL: http://grafana.swift.com.br/d/MqX7ba-Sz/lojas?orgId=3.

No dashboard, verifique a linha chamada CFTV; se estiver online, a internet da banda larga está funcionando. Para lojas com antena, entre em contato com a equipe de monitoria para validação.
Validação do Ponto de Rede:

Verifique se o ponto de rede do Player está conectado ao modem de banda larga ou à antena.
Utilize um testador de cabos ou um notebook para validar a conexão. Conecte o cabo de rede ao notebook e verifique se há acesso à internet. Se não houver ponto de rede, conecte o cabo diretamente no rack e teste a conexão.
Solicite um comando IPCONFIG para verificar se o IP está na faixa correta (ex: 172.16.0.1 ou 192.168.0.1).
Se necessário, utilize um testador de cabos para identificar onde o cabo está conectado no rack. Caso o ponto de rede não esteja conectado ao link de banda larga, conecte-o ao modem da Claro ou VIVO ou à antena.
Conectando o Player:

Após conectar o cabo de rede ao modem ou à antena, teste novamente a conexão no notebook. Se funcionar, reconecte ao Player e verifique se ele fica online através do painel da VTSIGN: https://painel.vtsign.com.br/Login.vtt.
Login:
Usuário: swift.ti
Senha: Mudar@2024
Verificando as Configurações de Rede:

Se o Player não ficar online, direcione o controle para o sensor do Player, clique na "casinha" e acesse as configurações de rede.
Verifique se o Player está obtendo um endereço IPV4 (ex: 192.168 ou 172.16). Se estiver recebendo IPV6 (com letras), isso significa que não funcionará.
Se estiver com IPV4, peça ao técnico que abra o TeamViewer QS para obter a ID. Essa ID deve ser compartilhada com a equipe da VTT no grupo "Swift suporte VTT" no WhatsApp. A equipe conectará e resolverá o problema.
Painel de LED:

Para painéis de LED, o técnico precisará de um cabo conversor de HDMI para VGA e de um monitor da loja (que possui apenas VGA). Conecte o conversor e o HDMI ao monitor para realizar os procedimentos necessários para validar o IP e abrir o TeamViewer QS.
Se o Player não obtiver IPV4, tente conectá-lo via Wi-Fi. O nome do Wi-Fi é SWIFT. Se não conectar, será necessário trocar o Player.

...

### 2. Troca do Player
Para solicitar um novo Player:

1. Abra um chamado no Automidia pelo link: [Servicedesk JBS](https://servicedesk.jbs.com.br/).

2. Na abertura do chamado, informe o número da loja e descreva a necessidade de um novo Player. Encaminhe o chamado para a equipe de Infraestrutura.
Após a validação do equipamento, desça para o TRP e pegue o novo Player.
Conecte o novo Player ao Wi-Fi do celular corporativo (lembre-se de conectar o HDMI para VGA no monitor para visualizar as configurações do Player).
Abra o TeamViewer QS, obtenha a ID e informe à equipe da VTT no grupo WhatsApp, fornecendo também o número e nome da loja.
Se a loja estiver a até 30 km de distância, solicite um motoboy com o seguinte modelo de mensagem:

Prezados, bom dia!
Tudo bem?

Por gentileza, solicito um frete para o seguinte endereço abaixo.

Frete 1º

L5121 - SWIFT VILA MASCOTE
Endereço: AV STA CATARINA, 806 - VILA MASCOTE, São Paulo - SP, 04378-000
C/C: 17256
Conteúdo: 1 kit player (Player android + fonte + controle)

Atenciosamente,
Envie para o e-mail: motoboy@swift.com.br, com cópia para sustentacao@swift.com.br.

Após a coleta, deixe o Player com a fonte e controle guardados, próximos à copa. O motoboy irá retirar e enviar para a loja. Ao chegar, solicite um Findup para a loja e acompanhe pelo celular corporativo da T.I.

Para lojas acima de 30 km, peça para o Egon solicitar o Lalamove ou, se for em outra cidade, peça para a distrital levar o novo Player.


### 3. Problemas com o Cabo de Rede
Se o cabo de rede ou ponto de rede não estiver funcionando no testador de cabos, solicite que o RJ45 e o Keystone sejam refeitos. Se isso não resolver, será necessário abrir um chamado para a equipe de monitoria, a fim de que o cabo ou ponto de rede sejam totalmente refeitos pela equipe de cabeamento estruturado.

...

### 4. Mensagem de Erro DUID no Painel de LED ou TV
4. Mensagem de Erro DUID no Painel de LED ou TV
Caso o painel de LED ou TV apresente a mensagem DUID (ID) e solicite digitar uma chave para validar:

Se não for uma TV, será necessário solicitar um Findup para que um técnico conecte o monitor com o conversor no Player e tente abrir o TeamViewer QS. A ID deve ser compartilhada com a VTT para que eles possam acessar e resolver o problema.
Se for uma TV, o procedimento pode ser realizado pela loja (o procedimento é pegar o controle apontar para o sensor do Player e clicar no botão da “casinha”, procurar pelo aplicativo Teamviewer QS e passar a ID para informamos ao suporte da VTT.

