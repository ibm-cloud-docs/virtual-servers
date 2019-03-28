---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-14"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Modelos de imagem
{: #image-templates}

Com modelos de imagem de {{site.data.keyword.BluVirtServers}}, é possível capturar a imagem de um dispositivo para replicar rapidamente sua configuração com mudanças mínimas no processo de pedido.
{:shortdesc}

Os modelos de imagem fornecem uma opção de imagem para todos os {{site.data.keyword.BluVirtServers_short}}, independentemente do sistema operacional. Os modelos de imagem permitem capturar uma imagem de um servidor virtual existente e criar um novo baseado na imagem capturada. Os modelos de imagem não são compatíveis com os servidores bare metal.

## Como funcionam os modelos de imagem
As duas ações principais para qualquer modelo de imagem são criar e implementar. Quando você solicita a criação de uma imagem, o sistema automatizado do {{site.data.keyword.BluSoftlayer_full}} coloca seu servidor off-line. Enquanto o servidor está off-line, um backup compactado de seus dados é criado, as informações de configuração são registradas e o modelo de imagem é armazenado na SAN do {{site.data.keyword.BluSoftlayer_notm}}. Durante o estágio de implementação do modelo de imagem, o sistema automatizado constrói um novo servidor que é baseado nos dados que são reunidos da imagem selecionada. O processo de implementação faz ajustes para o volume, restaura os dados copiados e, em seguida, faz mudanças de configuração final (por exemplo, configurações de rede) para o novo host.

Para obter mais informações sobre modelos de imagem, veja [Introdução aos modelos de imagem](/docs/infrastructure/image-templates?topic=image-templates-getting-started-with-image-templates).
