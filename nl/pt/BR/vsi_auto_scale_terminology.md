---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Terminologia de escala automática
{: #auto-scale-terminology}

Use os termos a seguir para aumentar sua compreensão do recurso de escala automática.

* **Grupo do Auto Scale:** um grupo de escala automática é um conjunto de servidores idênticos e, opcionalmente, um balanceador de carga, definido pela configuração de ativação que você configurou. O grupo pode aumentar e reduzir a escala em resposta à carga, conforme definido pela política de ajuste de escala que você configura e ligado à sua configuração de grupo de ajuste de escala.
* **<a name="group_name"></a>Nome do grupo:** um nome do grupo deve ser exclusivo na conta e é necessário antes de um grupo de ajuste de escala poder ser definido. O nome do grupo pode ser editado a qualquer momento.
* **<a name="cooldown"></a>Grupo de resfriamento do grupo:** o período após qualquer mudança de status no grupo de escala automática antes de uma política poder ser considerada "ativa" e iniciar novamente. Uma espera é necessária; ela pode ser configurada como 0, que é efetivamente desligada. Um resfriamento não pode ser configurado por mais de 10 dias. O tempo de espera fornece ao grupo de escala automática o tempo para recalibrar e as médias de métricas para refletir as mudanças.
  * **Grupo de escala automática de resfriamento:** a quantia de tempo que deve passar depois que um grupo se tornar ativo antes de qualquer ação de política ser executada.
  * **Espera de política:** igual à espera do grupo, exceto que substitui a configuração apenas para essa política. Se não fornecido, o valor de espera do grupo é utilizado.
* **<a name="member"></a>Membro:** um grupo contém membros, que são servidores virtuais automaticamente escalados pelo grupo.
* **<a name="min_virtual_member"></a>Contagem mínima de membros:** o menor número de membros permitidos em um grupo de escala automática. Os usuários podem garantir que um grupo de escala automática com um status ativo nunca terá menos membros do que o número configurado. Se o número real de membros for menor que a contagem de membro atual, membros serão criados automaticamente para atingir o mínimo. Se as VLANs estiverem presentes no grupo de escala automática e não estiverem associadas a um item de faturamento, o valor deverá pelo menos ser 1.
* **<a name="max_virtual_member"></a>Contagem máxima de membros:** o maior número de membros permitidos em uma escala automática. Os usuários podem garantir que um grupo de escala automática com um status ativo nunca terá mais membros do que o número configurado. Se, durante a criação ou edição, o número real de membros for maior do que a contagem de membro atual, membros serão removidos automaticamente para atingir o máximo.
* **Ativos:** um servidor existente na conta que nunca é escalado com o grupo, mas pode participar de números de coleta de métrica. Atualmente, apenas ativos de servidor virtual são suportados. Não é necessário que um grupo de escala automática tenha nenhum ativo.
* **<a name="status"></a>Status:** o status do grupo de escala automática é um valor derivado com base no que seus membros estão fazendo e se o grupo foi suspenso. Os status para um grupo de escala automática incluem:
  * **Ajuste de escala:** usado quando nenhum membro foi provisionado ainda ou tem uma transação de fornecimento ativa em execução. No status de ajuste de escala, um grupo de escala automática não pode ser acionado para escalar e somente propriedades não acionáveis podem ser editadas.
  * **Ocupado:** usado quando qualquer membro tem uma transação ativa, mas a transação não é uma transação de fornecimento ou de recuperação. No status ocupado, um grupo de escala automática não pode ser acionado para ajuste de escala e somente propriedades não acionáveis podem ser editadas.
  * **Suspenso:** usado quando um membro não está escalonando ou ocupado, mas foi configurado como Suspenso. No status Suspenso, um grupo de escala automática não pode ser acionado para ajuste de escala; no entanto, qualquer propriedade pode ser editada. Quaisquer ações que ocorreriam como resultado de uma criação ou edição de grupo não ocorrem até que o usuário retome o grupo de escala automática. Um grupo de escala automática pode ser suspenso manualmente pelo usuário ou automaticamente se houver um erro ao escalar o grupo automático por qualquer motivo. Um grupo de escala automática só pode ser retomado por um usuário.
  * **Ativo:** um grupo de escala automática estará ativo se ele não estiver escalando, ocupado ou suspenso. Quando ativo, um valor de grupo de escala automática pode ser editado e todos os acionadores podem ser iniciados.
* **<a name="termination"></a>Política de finalização:** a política de finalização é como o grupo de escala automática escolhe qual membro remover ao reduzir a escala. Há três políticas para escolher:
  * **Mais recente:** o membro que é provisionado mais recentemente será removido.
  * **Mais antigo:** o membro cuja data de provisão for a mais antiga será removido.
  * **Mais perto da próxima carga:** o membro que está chegando mais perto da próxima carga será removido. Atualmente, como os membros são faturados por hora, o mais perto da próxima carga será o membro que tenha usado a maioria dos minutos da hora atual.
* **<a name="multi-vlan"></a>Grupo de escala de múltiplas VLANs:** um grupo que tem servidores que são provisionados para múltiplas VLANs. Além das regras existentes do grupo de escala, há regras que controlam especificamente o grupo de escala de múltiplas VLANs:
  * Todas as VLANs devem ser compradas para um grupo de escala de múltiplas VLANs.
  * Mais de uma VLAN pública ou privada não é permitida em um único roteador.
  * A VLAN com o menor número de membros é selecionada ao realizar o ajuste de escala, fornecendo seu par público e privado, se fornecido.
  * A VLAN com o menor número de membros é selecionada ao realizar o ajuste de escala, fornecendo seu par público e privado, se fornecido.
* **<a name="balanced term"></a>Configuração de finalização balanceada:** se o sinalizador de sinalização balanceada for configurado, o grupo de escala diminuirá a escala dos membros de maneira a preservar o balanceamento entre os pares de VLAN configurados. A política de finalização será usada se houver incerteza sobre qual membro usar para manter o equilíbrio (por exemplo, há o mesmo número de membros em dois ou mais pares de VLAN). Se a sinalização não estiver configurada, a política de finalização será usada independentemente de quantos membros estiverem em cada VLAN.
* **Modelo de membro:** um modelo de membro está no grupo de escala automática e “informa” ao grupo a ordem dos servidores virtuais dentro do grupo. Coisas para manter em mente ao usar um modelo de membro:
  * O ID da conta deve ser fornecido e deve ser o mesmo que o grupo do Auto Scale.
  * Se especificado, o faturamento deve ser configurado por hora.
  * Se o data center for fornecido, ele deverá estar na mesma recuperação e conter as VLANs no grupo.
  * As VLANs não podem ser fornecidas para o modelo. Se o usuário precisar especificar VLANs para membros, ele deverá usar as VLANs do grupo de Escala automática.
  * Se algum balanceador de carga estiver configurado no grupo Escala automática, o modelo não poderá ser apenas rede privada.
* **<a name="vlan"></a>VLANs:** opcionalmente, o usuário pode fornecer uma coleção de VLANs para o fornecimento de servidores membros. Somente um par de VLANs pode ser fornecido por roteador. Se múltiplos pares de VLAN forem fornecidos para múltiplos roteadores, o sistema de ajuste de escala garantirá que os membros sejam incluídos uniformemente entre os roteadores. Consulte “configuração de finalização balanceada“ para saber mais sobre a remoção uniforme de membros em vários pares de VLANs.
  * A escala automática tenta reutilizar uma VLAN pública que você tem atrás do roteador. Uma nova VLAN pública será criada no mesmo roteador se uma VLAN pública não for selecionada, e não se indica uma apenas privada.
  * A Escala automática não permitirá que um grupo seja criado sem uma VLAN Privada selecionada quando uma Pública for. Será possível ver o erro "Modelo guest inválido, erro: somente a VLAN de front-end foi especificada. Especifique a VLAN de back-end também. Todas as VLANs públicas devem ter um par de VLAN privada. A finalização balanceada poderá ser ativada apenas em grupos de escala com múltiplas VLANs balanceadas". Isso não se aplica a grupos de Rede privada somente.
* **<a name="scalelb"></a>Balanceadores de carga de escala:** um grupo pode conter configurações de balanceador de carga a serem aplicadas a membros quando o fornecimento é concluído. A opção para escalar os balanceadores de carga atualmente funciona apenas com os balanceadores de carga locais e usa algumas das APIs de balanceador de carga. O endereço IP virtual do balanceador de carga deve estar na mesma conta que o grupo de escala automática. O balanceador de carga também deve estar em um local válido de acordo com a VLAN, o data center do servidor virtual e a região. Atualmente, se quaisquer balanceadores de carga forem fornecidos, o servidor virtual deverá ter o data center fornecido. O servidor virtual é automaticamente posicionado atrás do balanceador de carga durante o fornecimento. Os itens que compõem um balanceador de carga de escala incluem:
  * **ID do endereço IP virtual:** o ID do balanceador de carga a ser usado.
  * **Porta de serviço:** a porta de entrada. Um registro de grupo de serviços existente é usado, se presente para essa porta. Caso contrário, ele será criado com algumas das informações a seguir.
  * **Percentual de alocação:** a porcentagem de conexões por segundo que o servidor virtual é alocado no conjunto total de conexões por segundo do IP virtual. Por exemplo, se o IP virtual tiver 250 conexões por segundo e o valor for 25 por cento, outros servidores virtuais nesse IP virtual poderão ser alocados somente até 75 por cento das outras conexões por segundo. Esse não é um máximo que pode ser distribuído, mas uma alocação pura do conjunto no qual as conexões são usadas ou não. Se o servidor virtual existir para a porta específica, o número deverá corresponder ao percentual de alocação existente.
  * **Método de roteamento:** como o tráfego é roteado entre os servidores. Se o servidor virtual existir para a porta específica, o número deverá corresponder ao método de roteamento existente.
  * **Tipo de roteamento:** o tipo de roteamento a ser executado entre os servidores. Se o servidor virtual existir para a porta específica, o número deverá corresponder ao tipo de roteamento existente.
  * **<a name="health_check"></a>Verificação de funcionamento:** o tipo de verificação a ser executada nos servidores. Se HTTP_CUSTOM for verificado, os atributos poderão ser fornecidos para o método de HTTP, a URL e a resposta esperada.
  * **Porta:** a porta a ser usada durante as verificações de funcionamento e quando o tráfego é enviado por meio do balanceador de carga.
* **<a name="policies"></a>Políticas:** um grupo de escala automática pode ter qualquer número de políticas. Uma política contém um conjunto de ações e um conjunto de acionadores. Os acionadores são opcionais e podem não ser fornecidos caso o usuário prefira iniciar as ações da política manualmente. Somente um acionador deve ser satisfeito para a ação a ser iniciada. Uma política consiste em:
  * **Nome:** uma política deve ter um nome e o nome deve ser exclusivo no grupo do Auto Scale.
  * **Espera de política:** configurar uma espera de política é opcional, no entanto, se fornecida, ela substitui a espera de grupo para quando uma política pode começar a ser acionada após uma mudança de status do grupo. Isso não tem relação com a origem da mudança de status do grupo e pode ser considerado ativo após um grupo se tornar ativo.
  * **<a name="actions"></a>Ações:** atualmente, o único tipo de ação é uma ação de escala. As ações podem ser iniciadas somente em grupos ativos. As ações de escala incluem o seguinte:
    * **Quantidade:** o número de membros a serem escalados. O número pode ser positivo ou negativo e o valor é dependente do tipo de escala.
    * **Tipo de escala:** há três tipos de escala – absoluto, relativo e percentual:
      * **Absoluto ("Exato" na GUI):** absoluto força o grupo de escala automática a um número configurado de membros, independentemente da contagem de membros atual. O ajuste de escala absoluto pode incluir aumento de escala, redução de escala ou nenhum deles. O número deve estar dentro do intervalo mínimo e máximo do grupo.
      * **<a name="relative"></a>Relativo:** a escala relativa resulta no grupo de escala automática aumentando ou diminuindo a escala pela quantia específica. Independentemente da quantia, o sistema certifica-se de que o grupo de escala automática não tenha a escala reduzida abaixo de seu mínimo ou acima de seu máximo. Por exemplo, o mínimo de um grupo é 5, sua contagem atual é 7 e a quantidade de escala relativa é -4. A contagem é tratada como se fosse apenas -2 no momento da chamada, uma vez que não é possível escalar para abaixo de 5.
      * **Percentual:** a escala percentual resulta no aumento ou na redução da escala do grupo de escala automática com base em uma porcentagem positiva ou negativa. O número é um percentual da contagem atual de membros do grupo de escala automática. Qualquer percentual extra após o ponto decimal é sempre ignorado. Se a quantia de porcentagem da escala for zero, ela será tratada automaticamente como -1 ou 1, dependendo se o valor da porcentagem original era positivo ou negativo. Por exemplo, se um grupo tiver 27 membros e a quantia for 12 (para 12 por cento), isso significaria 3,24 membros, que se arredonda para 3. Mas se o grupo tivesse apenas 2 membros, significaria 0,24 membros, o que geralmente seria arredondado para 0, mas é arredondado automaticamente para pelo menos 1.
  * **<a name="triggers"></a>Acionadores:** os acionadores são condicionantes que podem ser satisfeitos. Há três tipos de acionadores – único, de repetição ou uso de recurso:
    * **Uma vez:** o acionador único leva uma única data e será iniciado se o grupo de escala automática estiver ativo. Todos os horários estão no formato UTC.
    * **<a name="triggers_repeat"></a>De repetição:** o acionador de repetição dura um planejamento formatado em cron e é acionado com base nesse planejamento se o grupo está ativo.
    * **Uso de recurso:** o acionador de uso de recurso tem uma coleção de observações de recursos. Quando todas as observações de recursos são atendidas, o acionador é considerado satisfeito.
      * **Observações:** uma observação de recurso é um conjunto único de parâmetros para observar um determinado valor da métrica em todos os membros e ativos do grupo de escala automática. Os parâmetros são:
        * **Algoritmo:** esse é o algoritmo para combinar valores de métrica. O único algoritmo que é suportado é a média móvel exponencialmente ponderada (EWMA).
        * **Métrica:** as métricas são baseadas nos valores a seguir:
          * **Percentual de CPU:** uma porcentagem de CPU.
          * **Entrada de rede na rede privada:** os bytes recebidos por segundo na interface virtual privada.
          * **Saída de rede na rede privada:** os bytes de saída por segundo na interface virtual privada.
          * **Entrada de rede na rede pública:** os bytes recebidos por segundo na interface virtual pública.
          * **Saída de rede na rede privada:** Os bytes de saída por segundo na interface virtual pública.
        * **Operador:** o valor usado ao verificar se uma métrica está abaixo ou acima de um determinado valor. O único valor aceito é o caractere literal maior que (>) ou menor que (<).
        * **Período:** o número de segundos em que a métrica é agregada ao compará-la com o valor específico. Quando a agregação da métrica começa, ela não é considerada válida até que tenha coletado pelo menos para o período. Por exemplo, se um grupo tiver um resfriamento de 300 segundos e um relógio de recurso que agregar uma métrica acima de 500 segundos, o relógio não poderá ser satisfeito até que 800 segundos sejam passados. As métricas serão consideradas inválidas até que a espera tenha passado. O valor agregado também será considerado inválido até que tenha decorrido, pelo menos, o número de segundos no período de agregação. Um período não pode ter menos de dois minutos ou mais de dois dias.
        * **Valor:** o valor com o qual comparar. Para a métrica de porcentagem de CPU, deve ser entre 5 e 100. Para as métricas de rede, ele deve ser no mínimo 0.
