---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-09"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}

# FAQs: servidores virtuais  
{: #faqs-virtual-servers}

## Quais tipos de servidores virtuais estão disponíveis para uso?
{: faq}
O {{site.data.keyword.BluSoftlayer_full}} oferece alguns tipos de servidores virtuais dentro de sua infraestrutura clássica. A oferta padrão é um servidor virtual baseado em público, que é um ambiente de diversos locatários, adequado para uma variedade de necessidades. Se você está procurando um ambiente de locatário único, considere a oferta de Virtual Server dedicado. A opção do servidor virtual dedicado é ideal para aplicativos com requisitos de recursos mais rigorosos. Para obter mais informações sobre as ofertas atuais de servidor virtual, veja [Introdução aos servidores virtuais](/docs/vsi?topic=virtual-servers-getting-started-with-virtual-servers#getting-started-with-virtual-servers).

O IBM Cloud oferece a infraestrutura da nuvem particular virtual (VPC), que é a plataforma de nuvem de próxima geração. Você cria seu próprio espaço no {{site.data.keyword.cloud_notm}} para executar um ambiente isolado dentro da nuvem pública usando o VPC. O VPC fornece a segurança de uma nuvem particular com a agilidade e a facilidade de uma nuvem pública. Para obter mais informações, consulte [Sobre a nuvem particular virtual](https://cloud.ibm.com/docs/vpc-on-classic?topic=vpc-on-classic-about).

## Onde posso localizar informações de precificação para tipos de instância pública?
{: faq}

Para informações de precificação, consulte [Construir seu servidor virtual ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud/virtual-servers){: new_window}.

## Onde posso localizar as informações de precificação para as instâncias públicas virtuais?
{: faq}

A estimativa de seu custo para um servidor {{site.data.keyword.cloud_notm}} para suportar sua carga de trabalho inicia no [catálogo do {{site.data.keyword.cloud_notm}}](https://cloud.ibm.com/catalog). No catálogo, selecione **Cálculo** e escolha o tipo de servidor - Bare Metal Server, Virtual Server ou Virtual Server for VPC (Virtual Private Cloud). Para obter informações de precificação, consulte a [Calculadora de provisionamento de servidores virtuais ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}.

## Posso incluir armazenamento em disco para meu servidor virtual por hora ou mensal?
{: faq}

É possível fazer upgrade ou fazer downgrade do armazenamento em disco para qualquer servidor virtual atualizando suas opções de armazenamento nos campos *Primeiro disco* até *Quinto disco* na tela *Configuração* do dispositivo que você deseja atualizar. Para obter mais informações, veja [Reconfigurando um servidor virtual existente](/docs/vsi?topic=virtual-servers-reconfiguring-virtual-servers#reconfiguring-virtual-servers).

## Quantos servidores virtuais por hora posso iniciar?
{: #concurrent}
{: faq}

O número de instâncias que podem ser executadas depende do nível de maturidade da sua conta. Por padrão, uma conta com mais de 45 dias tem um limite de 20 instâncias que podem ser executadas em servidores virtuais públicos, servidores virtuais dedicados e servidores bare metal, a qualquer momento. Uma conta mais recente tem um limite menor. Se desejar aumentar seu limite, entre em contato com o suporte para informar-nos mais sobre o que está fazendo e quantas instâncias simultâneas você pode precisar.

## Como serei faturado pela largura da banda para os meus servidores virtuais por hora?
{: faq}

O faturamento virtual por hora é dividido para o tráfego de entrada e de saída. Todo o tráfego de entrada para seu servidor virtual é livre de encargos. O tráfego de saída é medido e cobrado por GB, com totais avaliados no término de seu período de faturamento.

## Em quais casos meu servidor virtual é migrado para um host diferente?
{: faq}

Em casos limitados, um servidor virtual pode precisar ser migrado para um host diferente. Se uma migração é necessária, o servidor virtual é encerrado, migrado e, em seguida, reiniciado. Um servidor virtual pode ser migrado nos casos a seguir:

* Um hypervisor precisa ser atualizado, um host está sendo desatribuído ou um host não tem permissão para assumir novas instâncias. Se um host estiver marcado para qualquer uma dessas mudanças, quando um de seus servidores virtuais for reinicializado por meio do console do {{site.data.keyword.cloud_notm}}, a reinicialização acionará automaticamente o servidor virtual a ser migrado para um host diferente.
* Manutenção de infraestrutura. Você pode receber um e-mail indicando que é necessária a manutenção em um sistema que está hospedando seu servidor virtual. Seu servidor virtual pode precisar ser migrado como parte da manutenção da infraestrutura.
* Um upgrade para uma instância existente. Para desempenho consistente, se você fizer upgrade de uma instância, ele poderá ser migrado para um host diferente para assegurar que receba a CPU e a memória dedicadas apropriadas.
* Um host dedicado falha. Instâncias dedicadas são migradas para outro host vazio sem usar qualquer capacidade existente que você possa ter.

Durante uma janela de manutenção, é possível ver uma opção **Migrar host** ser exibida no menu **Ações** de seu dispositivo no console do {{site.data.keyword.cloud_notm}}. **Migrar Host** permite migrar o servidor virtual para um novo host para sua conveniência durante um período de manutenção especificado. Se você não iniciar a migração durante o período de manutenção, o servidor virtual será migrado automaticamente para concluir a manutenção necessária. A opção **Migrar Host** não persiste e fica disponível apenas durante períodos de manutenção que são comunicados por meio de notificações de manutenção.

Você também poderá ver a opção **Migrar Host** se um de seus servidores virtuais precisar ter um determinado nível de hypervisor que não está disponível no host atual.

## O que acontece com os meus dados quando meu armazenamento portátil é excluído?
{: faq}

Quando o armazenamento é excluído, quaisquer ponteiros para os dados nesse volume são removidos, portanto, os dados se tornam inacessíveis. Se o armazenamento físico for reprovisionado para outra conta, um novo conjunto de ponteiros será designado. Não há como a nova conta acessar quaisquer dados que possam ter estado no armazenamento físico. O novo conjunto de ponteiros mostra todos 0s. Quando novos dados são gravados no volume/LUN, todos os dados inacessíveis que ainda existem são sobrescritos.

## Posso usar uma assinatura Red Hat Cloud Access para criar um servidor virtual?
{: faq}

Sim. Ao importar uma imagem, é possível especificar que você fornecerá a licença do sistema operacional. Para obter mais informações, consulte [Usar Red Hat Cloud Access](/docs/infrastructure/image-templates?topic=image-templates-using-your-own-os-license-or-subscription#using-your-own-os-license-or-subscription). Então você pode solicitar um servidor virtual desse modelo de imagem e usar sua assinatura existente do [Red Hat Cloud Access ![Ícone de link externo](../icons/launch-glyph.svg "Ícon de link externo")](https://www.redhat.com/en/technologies/cloud-computing/cloud-access){: new_window}.

## Qual é a diferença entre um servidor virtual e um virtual private server (VPS)?
{: faq}

Um servidor virtual é semelhante às plataformas virtual private server (VPS) ou virtual dedicated server (VDS) com as quais você pode já estar familiarizado. Esses ambientes de "servidor virtual" permitem que ambientes distintos sejam provisionados de forma privada e segura em um único nó de hardware, mas o VDS e o VPS são mais limitados em suas capacidades. As opções VPS e VDS são geralmente confinadas a uma arquitetura de servidor único. Os únicos recursos que podem ser incluídos ou divididos entre cada servidor virtual em um VDS ou VPS são os recursos que são instalados fisicamente nesse servidor único.

Os servidores virtuais são provisionados em uma arquitetura de nuvem multisservidor que agrupa todos os recursos de hardware disponíveis para as instâncias individuais usarem. Os servidores virtuais podem usar uma plataforma de armazenamento primária baseada em SAN de alta capacidade compartilhada ou armazenamento em disco local de alto desempenho. Como cada instância faz parte do ambiente de nuvem maior, a comunicação entre todos os servidores virtuais é instantânea.

## Por que eu recebo um erro de capacidade ao fornecer um servidor virtual?
{: faq}

Ao fornecer um servidor virtual, você pode receber uma mensagem de erro informando que não há capacidade suficiente para concluir a solicitação. Quando o fornecimento falha, todas as instâncias de servidor virtual dessa solicitação específica falham. Um erro de capacidade ocorre quando há recursos insuficientes disponíveis no roteador ou no data center para preencher a solicitação de serviço. Há uma série de razões pelas quais você pode receber esse erro. A disponibilidade de recurso muda frequentemente, portanto, você pode esperar e tentar novamente mais tarde. Para obter mais informações sobre as estratégias para evitar esse erro, consulte [Considerações de recurso para instâncias de servidor virtual](/docs/vsi?topic=virtual-servers-capacity-considerations#capacity-considerations).

## Como efetuar login no meu servidor?
{: faq}

Efetue login em seu console e navegue para o menu **Dispositivos**. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices). Na **Lista de dispositivos**, selecione a sua instância. É possível visualizar e gerenciar os nomes de usuário e senhas do dispositivo a serem usados para efetuar login. Para obter mais informações, consulte [Visualizando e gerenciando nomes de usuário e senhas do dispositivo](https://test.cloud.ibm.com/docs/vsi?topic=virtual-servers-view-update-user-name-password-for-device). 

## Como usar a VPN para acessar a rede privada do IBM Cloud?
{: faq}

É possível efetuar login na VPN por meio da [interface da web](https://www.softlayer.com/VPN-Access){: external} ou usar um [cliente VPN independente](/docs/infrastructure/iaas-vpn?topic=VPN-standalone-vpn-clients) para Linux, macOS ou Windows. Para obter mais informações sobre o que fazer quando você estiver conectado à VPN, consulte [Usar VPN SSL](/docs/infrastructure/iaas-vpn?topic=VPN-use-ssl-vpn).

## Como reinicializar meu servidor virtual?
{: faq}

A reinicialização do dispositivo pode ocorrer por meio da **Lista de dispositivos** ou da visualização de captura instantânea de uma instância individual. Navegue para a instância de servidor virtual na **Lista de dispositivos** em seu console. Para obter mais informações, consulte [Navegando para dispositivos](/docs/vsi?topic=virtual-servers-navigating-devices). Selecione **Ações** para o dispositivo que você deseja gerenciar e selecione **Reinicializar**.

## Como usar o kernel de resgate?
{: faq}

Inicializar em um kernel de resgate será útil se você estiver tendo um problema com o servidor. Para ativar o kernel de resgate, selecione o nome do dispositivo na **Lista de dispositivos** em seu console. No menu **Ações**, selecione **Modo de resgate** ou selecione **Inicializar por meio da imagem** para uma instância do Windows. Para obter mais informações, consulte [Ativando o kernel de resgate](/docs/vsi?topic=virtual-servers-launching-rescue).

## Onde localizo o status de rede?
{: faq}

É possível acessar a página **Status** diretamente em [{{site.data.keyword.cloud_notm}} - Status](https://cloud.ibm.com/status){: external} para visualizar o status atual de recursos em todas as localizações do {{site.data.keyword.cloud_notm}}. É possível filtrar a lista selecionando componentes e locais específicos (por exemplo, é possível selecionar servidores virtuais e visualizar a conectividade de rede).

## Como solicitar um relatório de conformidade?
{: faq}

Para obter informações sobre como visualizar ou solicitar informações de conformidade, incluindo relatórios SOC, consulte [Como saber se meus dados estão seguros?](/docs/overview?topic=overview-security)

