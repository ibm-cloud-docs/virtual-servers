---



copyright: years: 2015, 2017 lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Modelos de imagem
Com modelos de imagem de {{site.data.keyword.BluVirtServers}}, é possível capturar a imagem de um dispositivo para replicar rapidamente sua configuração com mudanças mínimas no processo de pedido. 
{:shortdesc}

Modelos de imagem padrão fornecem uma opção de criação de imagens para todos os {{site.data.keyword.BluVirtServers_short}}, independentemente do sistema operacional. Os Modelos de imagem padrão permitem capturar uma imagem de um servidor virtual existente e criar uma nova baseada na imagem capturada. Modelos de imagem padrão não são compatíveis com servidores bare metal.

## Como funcionam os modelos de imagem
As duas ações principais para qualquer modelo de imagem são criar e implementar. Quando você solicita a criação de uma imagem, o sistema automatizado do {{site.data.keyword.BluSoftlayer_full}} coloca seu servidor off-line. Enquanto o servidor está off-line, um backup compactado de seus dados é criado, as informações de configuração são registradas e o modelo de imagem é armazenado na SAN do {{site.data.keyword.BluSoftlayer_notm}}. Durante o estágio de implementação do modelo de imagem, o sistema automatizado constrói um novo servidor que é baseado nos dados que são reunidos da imagem selecionada. O processo de implementação faz ajustes para o volume, restaura os dados copiados e, em seguida, faz mudanças de configuração final (por exemplo, configurações de rede) para o novo host.

## Imagens Privadas

Imagens privadas são imagens que são criadas por um usuário na conta ou imagens que são criadas em outra conta e compartilhadas. Por padrão, todas as imagens que são criadas são privadas. 

## Imagens Públicas

Imagens públicas são máquinas pré-configuradas que são postadas pelo {{site.data.keyword.BluSoftlayer_notm}} ou divulgadas por clientes e estão disponíveis para uso por todos os clientes do {{site.data.keyword.BluSoftlayer_notm}}. Os servidores virtuais que são fornecidos por meio de Modelos de Imagem Pública geralmente são configurados para um desempenho otimizado, com combinações específicas de uma variedade de especificações de configuração.

Para obter mais informações sobre modelos de imagem, veja [Introdução aos modelos de imagem](/docs/infrastructure/image-templates/image_index.html).
