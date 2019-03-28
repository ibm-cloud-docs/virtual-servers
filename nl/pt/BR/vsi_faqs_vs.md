---

copyright:
  years: 2017, 2018
lastupdated: "2018-10-30"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:faq: data-hd-content-type='faq'}


# FAQs: servidores virtuais  
{: #faqs-virtual-servers}

## Quais tipos de servidores virtuais estão disponíveis para uso?
{:faq}

O {{site.data.keyword.BluSoftlayer_full}} oferece alguns tipos de servidores virtuais. A oferta padrão é um servidor virtual baseado em público, que é um ambiente de diversos locatários, adequado para uma variedade de necessidades. Se você está procurando um ambiente de locatário único, considere a oferta de Virtual Server dedicado. A opção do servidor virtual dedicado é ideal para aplicativos com requisitos de recursos mais rigorosos. Para obter mais informações sobre as ofertas atuais de servidor virtual, veja [Introdução aos servidores virtuais](/docs/vsi?topic=virtual-servers-getting-started-tutorial).

## Onde posso localizar informações de precificação para tipos de instância pública?
{:faq}

Para informações de precificação, consulte [Construir seu servidor virtual ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers){: new_window}.

## Onde posso localizar as informações de precificação para as instâncias públicas virtuais?
{:faq}

Para obter as informações de precificação, consulte a
[Calculadora de fornecimento de
servidores virtuais](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator).

## Posso incluir armazenamento em disco para meu Virtual Server por hora ou mensal?
{:faq}

Você pode fazer upgrade ou downgrade do armazenamento em disco para qualquer servidor virtual atualizando suas opções de armazenamento nos campos *Primeiro disco* a *Quinto disco* na tela *Configuração* do dispositivo que deseja atualizar. Para obter mais informações, veja [Reconfigurando um servidor virtual existente](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers).

## Quantos Virtual Servers por hora posso inicializar?
{:faq}

Por padrão, uma conta tem um limite de 20 instâncias que podem ser executadas em servidores virtuais públicos, servidores virtuais dedicados e servidores bare metal a qualquer momento.  Se desejar aumentar esse limite, entre em contato com o suporte para nos contar um pouco mais sobre o que você está fazendo e de quantas instâncias simultâneas pode precisar.

## Como eu serei faturado pela largura da banda para meus Virtual Servers por hora?
{:faq}

O faturamento virtual por hora é dividido para o tráfego de entrada e de saída. Todo o tráfego de entrada para seu servidor virtual é livre de encargos. O tráfego de saída é medido e cobrado por GB, com totais avaliados no término de seu período de faturamento.

## Em quais casos meu servidor virtual é migrado para um host diferente?
{:faq}
Em casos limitados, um servidor virtual pode precisar ser migrado para um host diferente. Se uma migração é necessária, o servidor virtual é encerrado, migrado e, em seguida, reiniciado. Um servidor virtual pode ser migrado nos casos a seguir:

* Um hypervisor precisa ser atualizado, um host está sendo desatribuído ou um host não tem permissão para assumir novas instâncias. Se um host estiver marcado para qualquer uma dessas mudanças, quando um de seus servidores virtuais for reinicializado no {{site.data.keyword.slportal_full}}, a reinicialização acionará automaticamente o servidor virtual para ser migrado para um host diferente.
* Manutenção de infraestrutura. Você pode receber um e-mail indicando que é necessária a manutenção em um sistema que está hospedando seu servidor virtual. Seu servidor virtual pode precisar ser migrado como parte da manutenção da infraestrutura.
* Um upgrade para uma instância existente. Para desempenho consistente, se você fizer upgrade de uma instância, ele poderá ser migrado para um host diferente para assegurar que receba a CPU e a memória dedicadas apropriadas.

Durante uma janela de manutenção, você poderá ver uma opção **Migrar Host** exibida no menu **Ações** de seu dispositivo no {{site.data.keyword.slportal}}. **Migrar Host** permite migrar o servidor virtual para um novo host para sua conveniência durante um período de manutenção especificado. Se você não iniciar a migração durante o período de manutenção, o servidor virtual será migrado automaticamente para concluir a manutenção necessária. A opção **Migrar Host** não persiste e fica disponível apenas durante períodos de manutenção que são comunicados por meio de notificações de manutenção.

Você também poderá ver a opção **Migrar Host** se um de seus servidores virtuais precisar ter um determinado nível de hypervisor que não está disponível no host atual.

## O que acontece com os meus dados quando meu armazenamento portátil é excluído?
{:faq}

Quando o armazenamento é excluído, quaisquer ponteiros para os dados nesse volume são removidos, portanto, os dados se tornam completamente inacessíveis. Se o armazenamento físico for provisionado novamente para outra conta, um novo conjunto de ponteiros será designado. Não há como a nova conta acessar quaisquer dados que possam ter estado no armazenamento físico. O novo conjunto de ponteiros mostra todos 0s. Quando novos dados são gravados no volume/LUN, todos os dados inacessíveis que ainda existem são sobrescritos.

## Posso usar uma assinatura Red Hat Cloud Access para criar um servidor virtual?
{:faq}

Sim. Ao importar uma imagem, é possível especificar que você fornecerá a licença do sistema operacional. Para obter mais informações, consulte [Usar Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription). Então você pode solicitar um servidor virtual desse modelo de imagem e usar sua assinatura existente do [Red Hat Cloud Access ![Ícone de link externo](../icons/launch-glyph.svg "Ícon de link externo")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window}.

## Qual é a diferença entre um servidor virtual e um virtual private server (VPS)?
{:faq}
Um servidor virtual é semelhante às plataformas virtual private server (VPS) ou virtual dedicated server (VDS) com as quais você pode já estar familiarizado. Esses ambientes de "servidor virtual" permitem que ambientes distintos sejam provisionados de forma privada e segura em um único nó de hardware, mas o VDS e o VPS são mais limitados em suas capacidades. As opções VPS e VDS são geralmente limitadas a uma arquitetura de único servidor, portanto, os únicos recursos que podem ser incluídos ou divididos entre cada servidor virtual em um VDS ou VPS são os recursos fisicamente instalados nesse servidor único.

Os servidores virtuais são provisionados em uma arquitetura de nuvem multisservidor que agrupa todos os recursos de hardware disponíveis para as instâncias individuais usarem. Os servidores virtuais podem alavancar uma plataforma de armazenamento primário com base na SAN de alta capacidade compartilhada ou armazenamento em disco local de alto desempenho. Como cada instância faz parte do ambiente de nuvem maior, a comunicação entre todos os servidores virtuais é instantânea.

<!--## I'm unable to connect to the virtualization API. How can I fix this?-->

<!--This error generally occurs because a password is outdated. To fix this, update the root or Administrator password for the virtual server's operating system in the {{site.data.keyword.slportal_full}}.-->

## Por que eu recebo um erro de capacidade ao fornecer um servidor virtual?
{:faq}

Ao fornecer um servidor virtual, você pode receber uma mensagem de erro informando que não há capacidade suficiente para concluir a solicitação. Quando o fornecimento falha, todas as instâncias de servidor virtual dessa solicitação específica falham. Um erro de capacidade ocorre quando há recursos insuficientes disponíveis no roteador ou no data center para preencher a solicitação de serviço. Existem vários motivos pelos quais você pode receber esse erro. A disponibilidade de recurso muda frequentemente, portanto, você pode esperar e tentar novamente mais tarde. Para obter mais informações sobre as estratégias para evitar esse erro, consulte [Considerações de capacidade](/docs/vsi?topic=virtual-servers-capacity-considerations).
