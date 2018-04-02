---



copyright:
  years: 1994, 2017
lastupdated: "2017-12-12"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Fazendo upgrade de velocidade da porta no Windows

A velocidade de porta padrão para servidores clientes (para as redes públicas e privadas) é 10 Mbps. Se você quiser fazer upgrade de uma das velocidades de porta para 100 Mbps ou 1000 Mbps, abra um chamado com a solicitação. As vendas solicitam a aprovação do encargo mínimo e um técnico muda as velocidades de porta em sua rede.

Depois que o upgrade é concluído no lado da rede, codifique permanentemente as interfaces de rede apropriadas no servidor.

Siga estas etapas para forçar a velocidade da porta em um servidor Windows. **Nota:** sempre se conecte ao servidor na rede em que você NÃO estiver trabalhando para evitar que seja bloqueado no servidor.

1. Selecione **Iniciar > Selecionar painel de controle > Selecionar conexões de rede**.
2. Clique na conexão de rede na qual você está tentando fazer upgrade/downgrade.
  * Para upgrades da Porta pública, selecione **Conexão da área local 2** OU **Front-end**.
  * Para upgrades da Porta privada, selecione **Conexão da área local** OU **Backend**.
3. Na janela Status da conexão, verifique se a placa de rede selecionada é a porta da qual você deseja fazer upgrade.
4. Selecione a guia de suporte (observe o Endereço IP):
  * Para um upgrade da Porta pública, o IP deve ser um endereço IP público.
  * Para um upgrade da Porta privada, o IP deve ser um endereço 10.x.x.x.
5. Se os endereços IP não corresponderem, repita as etapas 1 a 3 para a outra Conexão de rede.

## Status de LAN

Selecione a **Guia Geral** novamente e, em seguida, selecione **Propriedades.** Uma nova janela aparece.

Na guia **Geral** da janela **Propriedades da conexão**, selecione **Configurar**. A janela de propriedades do driver aparece.

1. Selecione a guia **Avançado**.
2. Selecione **Velocidade do Link e Duplex** na lista de propriedades.
3. Selecione a guia **Valor** à direita e configure a velocidade da porta para a qual você está fazendo upgrade com full duplex:
  1. Para 10 MBS, selecione: 10 Mbps/Integral
  2. Para 100 MBS, selecione: 100 Mbps/Integral
  3. Para 1000 MBS, selecione: automático
4. Clique em OK.  

Isso faz com que o servidor comece a usar a nova velocidade imediatamente, portanto, você pode ser brevemente desconectado enquanto o link renegocia.
