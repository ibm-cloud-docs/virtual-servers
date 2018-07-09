---



copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# FAQs: servidores (geral)

## Qual é a diferença entre "Inicialização de imagem" e "Carregamento de imagem"?
Tanto a Inicialização de imagem quanto o Carregamento de imagem utilizam os modelos de imagem existentes, que são aplicados a um dispositivo para substituir o sistema operacional existente ou para complementar o sistema operacional em uma tentativa de solucionar um problema existente. A principal diferença entre o processo de Inicialização e Carregamento é o tipo de imagem que é usado. Ao executar o processo de Inicialização ou Carregamento de imagem, assegure-se de ter feito backup de todos os dados que você pode querer recuperar.

   * Inicialização de Imagem é uma maneira de inicializar um dispositivo usando um ISO fornecido pelo {{site.data.keyword.BluSoftlayer_full}} para recuperação do sistema ou um ISO que foi transferido por upload usando o recurso *Importar Imagem* no {{site.data.keyword.slportal_full}}. O ISO pode ser uma versão limpa do sistema operacional do dispositivo ou um disco de recuperação que pode ser usado em uma tentativa de solucionar um problema com o dispositivo.
   * Carregamento de Imagem é um método de Recarregamento de SO que utiliza um modelo de imagem que foi capturado de um dispositivo ou transferido por upload usando o recurso *Importação de Imagem* no {{site.data.keyword.slportal}}. A opção *Carregamento de imagem* executa o recarregamento usando um VHD, que limpa o dispositivo de todos os dados e substitui o sistema operacional e arquivos existente por uma versão "como nova" da imagem selecionada.

## Por que não posso me conectar ao console KVM?
Se não for possível se conectar ao console KVM, revise as dicas de resolução de problemas a seguir para ajudar na resolução do problema. Se ocorrerem problemas adicionais, entre em contato com o suporte. Para obter mais informações sobre como entrar em contato com o suporte, veja [Obtendo ajuda e suporte](../vsi/vsi_ts_index.html).

   * O console KVM é um applet Java. Antes de acessar o console, o Java deve ser instalado. Para obter mais informações sobre a instalação do Java, veja [Download de Java grátis ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.java.com/en/download/){: new_window}.  
   * Se o Java estiver instalado, assegure-se de que uma conexão tenha sido estabelecida usando VPN. Se uma conexão não estiver estabelecida, um aviso de que uma conexão VPN é necessária será exibido ao tentar conectar-se ao console KVM.
   * O console KVM pode gerar uma ou mais caixas pop-up durante o processo de conexão. Ative pop-ups do {{site.data.keyword.slportal}} para assegurar que uma conexão possa ser feita.
   * Você pode receber um erro "Os aplicativos Java foram bloqueados pelas configurações de segurança". Para dispositivos iKVM bare metal, deve-se incluir uma exceção para o Endereço IP do dispositivo IPMI. Para dispositivos VSI, certifique-se de permitir "https://control.softlayer.com" e o endereço IP do KVM. Para obter mais informações, veja [Por que os aplicativos Java são bloqueados pelas configurações de segurança com o Java mais recente? ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.java.com/en/download/help/java_blocked.xml){: new_window}.
   * Se as condições acima tiverem sido atendidas e você receber um erro que afirma: "Manifest de Permissões necessárias ausente em main.jar", os applets Java não foram ativados no Painel de Controle do Java. Essa configuração foi introduzida como uma precaução de segurança do Oracle no Java SE v7. Ative os applets no Painel de Controle para resolver esse problema.

     **Nota:** se usar o Mac OSX em conjunto com o Google Chrome, consulte Informações e requisitos do sistema para instalar e usar o Mac Java 7 no website do Java.

   * Se você estiver tentando se conectar a um VSI por meio do Java padrão e não estiver obtendo nada, exceto erros, também será possível tentar usar o VNC.

Se você tiver concluído todas as verificações acima e ainda assim não for possível se conectar ao console KVM, entre em contato com o Suporte para obter assistência adicional na resolução do problema. Se tiver sido feita uma conexão com o console, mas os problemas ocorrerem ao se conectar ao dispositivo, assegure-se de que as credenciais que estão sendo usadas para acessar o dispositivo sejam válidas. Entre em contato com o administrador de conta para verificar as credenciais, se necessário.

## Perdi minha senha para o meu servidor. Como posso recuperá-la?
Se a senha raiz ou do administrador para seu servidor repentinamente não estiver funcionando, será possível verificar algumas coisas antes de entrar em contato com o suporte.

   * Você está copiando e colando a senha? Se não, tente. Além disso, cole a senha em um bloco de notas para assegurar que nenhum espaço esteja sendo copiado acidentalmente com a senha.
   * Se o servidor contiver o cPanel, é possível que o cPHulk tenha bloqueado seu endereço IP devido a logins com falha? Se sim, será possível acessar o servidor usando o KVM ou IPMI e incluir na lista de desbloqueio seu endereço IP em cPHulk com "/scripts/cphulkdwhitelist" seguido por seu endereço IP.
   * Alguém tentou recentemente mudar a senha para o servidor modificando a senha no {{site.data.keyword.slportal}}? Mudar a senha no {{site.data.keyword.slportal}} muda apenas o que você vê como a senha. Isso não muda a senha que o servidor está usando. Se isso aconteceu, é possível entrar em contato com o Suporte e eles podem normalmente recuperar a senha de trabalho original.
   * Pode ser necessário inicializar no modo de resgate do seu sistema operacional para ser possível redefinir sua senha. Para obter mais informações, consulte [Ativando um kernel de resgate](/docs/vsi/vsi_launch_rescue.html).

Se tudo isso foi verificado e ainda assim você não conseguir se conectar ao servidor usando a senha, entre em contato com o suporte usando um chamado e solicite uma reconfiguração de senha. O Suporte precisará reinicializar o servidor para reconfigurar a senha, portanto assegure-se de que você esteja preparado para aprovar a reinicialização e/ou fornecer um prazo de manutenção em que gostaria que isso ficasse pronto. A maioria das reconfigurações de senha pode ser realizada em 15 minutos. No {{site.data.keyword.slportal}}, é possível criar um chamado acessando **Suporte > Incluir Chamado** e usar o assunto *"Reinicializações e Acesso ao Console"*.

## As partições LVM são suportadas como um sistema de arquivos válido?
O LVM (Logical Volume Management) fornece gerenciamento lógico de sistemas de arquivos no Linux. No ambiente do {{site.data.keyword.BluSoftlayer}}, o LVM não é suportado como um esquema de particionamento inicializável. As instâncias de servidor virtual não podem ser pedidas com o LVM e a importação de imagens que usam o LVM como uma partição de inicialização falha em provisionar isso. Caso o LVM seja requerido na partição de inicialização, a oferta bare metal poderá suportar o LVM na inicialização para determinados sistemas operacionais. Com o suporte e a configuração do OS adequados, os Discos VSI secundários podem ser usados para partições LVM; no entanto, é importante observar que o LVM não é um sistema de arquivos suportado para Flex Image ou Modelos de imagem. Se você tiver mais perguntas, abra um chamado com a equipe de suporte que pode ajudá-lo.

## Rotas 161.26.0.0/16 pré-configuradas em hosts de cliente
O {{site.data.keyword.BluSoftlayer}} está ativando uma nova rota em todos os servidores recentemente provisionados para suportar produtos futuros.
   * A rota aponta qualquer endereço no intervalo de 161.26.0.0/16 (161.26.0.0 255.255.0.0 | 161.26.0.0 -161.26.255.255) para a rede privada de backend.
   * Esse bloco de IPs é designado ao {{site.data.keyword.BluSoftlayer_notm}} pelo IANA e não será anunciado na Internet pública.
   * Apenas sistemas {{site.data.keyword.BluSoftlayer_notm}} serão tratados fora desse espaço.
   * As ACLs em servidores de cliente, servidores virtuais e gateways Vyatta precisarão ser atualizadas para permitir que os hosts do cliente usem os serviços de Infraestrutura configurados com endereços IP fora desse intervalo.

## Como incluir o novo roteamento para vários OSes

   <table>
   <CAPTION>Tabela 1. Incluindo uma rota por OS</CAPTION>
   <THEAD>
   <TR>
   <th>Sistema operacional</th>
   <th>Etapas</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Windows 2003 Standard e Enterprise</td>
   <td>
   Inclua a rota persistente por meio da linha de comandos, digitando:
   <blockquote>route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p</blockquote>
   <b>Nota:</b> substitua 10.0.0.1 por seu endereço IP de gateway privado.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Server Core
   </td>
   <td>
   Inclua a rota persistente por meio da linha de comandos, digitando:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Nota:</b> substitua 10.0.0.1 por seu endereço IP de gateway privado.
   </td>
   </tr>
   <tr>
   <td>Windows 2008 Web, Standard, Enterprise e Datacenter</td>
   <td>
   Inclua a rota persistente por meio da linha de comandos, digitando:
   <blockquote>
   route add 161.26.0.0 mask 255.255.0.0 10.0.0.1 -p
   </blockquote>
   <b>Nota:</b> substitua 10.0.0.1 por seu endereço IP de gateway privado.
   </td>
   </tr>
    <tr>
   <td>RedHat, Fedora e CentOS</td>
   <td>
   Crie uma nova rota editando/criando o arquivo a seguir: <i>/etc/sysconfig/network-scripts/route-eth0</i>
   <p>Depois de criar esse arquivo, deve-se incluir as informações a seguir nele: <i>161.26.0.0/16 via 10.0.0.1</i>
   </p>
   <b>Nota:</b> substitua 10.0.0.1 por seu endereço IP de gateway privado.
   </td>
   </tr>
   <tr>
   <td>Ubuntu e Debian</td>
   <td>
   Em seu arquivo <i>/etc/network/interfaces</i>, inclua a linha a seguir no final do arquivo:
   <blockquote>
   up route add -net 161.26.0.0/16 gw 10.0.0.1
   </blockquote>
   <b>Nota:</b> substitua 10.0.0.1 por seu endereço IP de gateway privado.
   </td>
   </tr>
   <tr>
   <td>Vyatta</td>
   <td><i>set protocols static route 161.26.0.0/16 next-hop 172.16.0.26</i>
   <p>
   <b>Nota:</b> substitua 172.16.0.26 pelo gateway da sub-rede em que a máquina está, que deve ser o mesmo que o gateway definido para a rota 10.0.0./8.</p>
   </td>
   </tr>
   <tr>
   <td>ESXi</td>
   <td>Use o comando a seguir para incluir a rota no host ESXi:
   <blockquote>
   esxcfg-route -a 161.26.0.0/16 10.0.0.1
   </blockquote>
   <b>Nota:</b> substitua 10.0.0.1 por seu endereço IP de gateway privado.</td>
   </tr>
   <tr>
   <td>CoreOS</td>
   <td>Crie um arquivo de rota estática em /etc/systemd/network denominado 10-static.network que se parece com este:
   <blockquote>
   [Route]
   Gateway=10.0.0.1
   Destination=161.26.0.0/16
   </blockquote>
   <b>Nota:</b> substitua 10.0.0.1 por seu endereço IP de gateway privado.</td>
   </tr>
   </TBODY>
   </table>
   
   <a name="top"></a>

## Posso permitir que o sistema de monitoramento emita uma reinicialização automática e alerte um técnico de suporte no caso de o servidor parar de responder?

Sim, com a ordem de nosso serviço **Reinicialização automatizada de falha de monitoramento**, é possível configurar o sistema de monitoramento para reinicializar automaticamente o servidor e emitir um chamado para um técnico de suporte se um alerta de monitoramento for emitido. Como um serviço adicional, fornecemos **Monitoramento NOC**, em que você receberá notificação pessoal no caso de um problema monitoramento ocorrer. Para saber mais sobre essas duas ofertas, consulte [Server Monitoring ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://www.softlayer.com/services/monitoring/){:new_window}.

## O que é um espelho cvsup?

É possível atualizar em um espelho cvsup local que foi executado para você. Assegure-se de que o supfile tenha a entrada a seguir:

```
*default host=cvsup.service.softlayer.com
```
{:pre }

Os distfiles também são espelhados e estão disponíveis em freebsd.org. É possível incluir a linha a seguir no arquivo */etc/make.conf* para tentar fazer download do repositório local primeiro:

```
MASTER_SITE_OVERRIDE?="http://mirrors.service.softlayer.com/freebsd/distfiles/${DIST_SUBDIR}/"
```
{:screen }

Se o arquivo não for localizado lá, ele seguirá o Makefile de porta individual e será movido para o próximo espelho.



