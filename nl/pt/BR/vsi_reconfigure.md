---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Reconfigurando um servidor virtual existente
{: #reconfiguring-virtual-servers}

Após um servidor virtual ser provisionado, é possível fazer upgrade ou downgrade de sua configuração a qualquer momento.  

**Nota importante:** há vários servidores virtuais públicos disponíveis em perfis pré-configurados. Por um tempo limitado, é possível modificar qualquer servidor virtual que estava disponível antes dos perfis pré-configurados. Em seguida, será necessário migrar ou cancelar as instâncias existentes e reordenar.

Não é possível modificar o núcleo, a RAM ou o tamanho do disco individuais de um servidor virtual que usa perfis. Deve-se escolher um perfil diferente que tenha os núcleos, a RAM e o tamanho do disco pré-configurados de que você precisa. O perfil do servidor virtual que você seleciona determina os núcleos, a RAM e os tamanhos de disco válidos.  

Os servidores virtuais dedicados são mais customizáveis; portanto, é possível modificar os núcleos, RAM e tamanhos de disco individuais.

Use as etapas a seguir para reconfigurar um servidor virtual existente.
{:shortdesc}

## Modificando um servidor virtual existente (que usa perfis pré-configurados)
1. Acesse o [console](https://cloud.ibm.com/classic?){: new_window}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo") com as credenciais que você recebeu em um e-mail quando sua conta foi criada inicialmente. Como alternativa, é possível efetuar login no [{{site.data.keyword.slportal}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){:new_window}. 
2. Na Lista de dispositivos, clique no nome do servidor virtual que você deseja reconfigurar.
3. Na guia **Configuração**, é possível clicar em **Modificar** ou **Modificar a configuração do dispositivo** para atualizar os itens a seguir.
  <dl>
  <dt>Tamanho</dt>
  <dd>Selecione um novo tamanho.</dd>
  <p><note>Nota: ao modificar um perfil que usa armazenamento local, não é possível alternar para um perfil que usa armazenamento não local. Da mesma forma, quando você modifica um perfil que usa armazenamento não local, não é possível alternar para um perfil que usa armazenamento local.
  </note></p>
  </dl>
4. Depois de especificar as mudanças para o servidor virtual, conclua a atualização de configuração.
  <dl>

  <dt>Data do upgrade</dt>
  <dd>É possível clicar na caixa de seleção Imediatamente para uma atualização imediata ou planejar um horário para que a atualização se torne ativa.</dd>

  <dt>Horário do upgrade</dt>
  <dd>Insira a data (AAAA-MM-DD) para que a atualização se torne ativa.</dd>

  <dt>Notas</dt>
  <dd>Insira quaisquer notas aplicáveis para seu dispositivo. </dd>
  </dl>

5. Clique em **Continuar**.
6. Revise sua confirmação de ordem quanto à precisão.  Clique em **Editar** para editar seu upgrade.
7. Clique em **Confirmar** para confirmar sua ordem e aplicar as mudanças a seu dispositivo.

## Modificando um servidor virtual existente (anterior aos perfis pré-configurados) ou um servidor virtual dedicado
1. Na Lista de dispositivos, clique no nome do servidor virtual que você deseja reconfigurar.
2. Na guia **Configuração**, é possível clicar no link **Upgrade de Núcleo ou RAM** para atualizar os itens a seguir.

|   Opções de Upgrade       |  Descrição                                                                                                |
| ----------------------- | ----------------------------------------------------------------------------------------------------------- |
| Data do Upgrade            | Insira a data (AAAA-MM-DD) para que a atualização se torne ativa.                                                |
| Horário do Upgrade            | Selecione o horário nas caixas suspensas para a hora do dia para que a atualização se torne ativa ou clique na caixa de seleção **Imediato** para uma atualização imediata.                                                                                        |
| Núcleos                   | Selecione o número de núcleos para a atualização, se aplicável. |
| RAM                     | Selecione a quantia de RAM a ser aplicada ao seu dispositivo para a atualização, se aplicável.   |
| Velocidades da Porta de Uplink      | Selecione as novas velocidades da porta de uplink para seu dispositivo, se aplicável. |
| Largura da Banda Pública        | Selecione a quantia (em GB) de largura da banda pública para seu dispositivo, se aplicável.   |
| Primeiro Disco – Quinto Disco | Selecione a opção de espaço/armazenamento de disco para seu primeiro disco, se aplicável. Consulte **Notas sobre Disco** abaixo para obter informações adicionais.                                                                                                                               |
| Notas                   | Insira quaisquer notas aplicáveis para seu dispositivo.                                                                 |
{: caption="Tabela 1. Opções de implementação" caption-side="top"}   

  **Notas sobre Disco:**
  * O armazenamento Local e de SAN está disponível.  Verifique novamente sua seleção para assegurar que sua opção de armazenamento esteja correta.
  * Para servidores virtuais públicos, se você estiver fazendo upgrade do armazenamento local e precisar de mais núcleo ou RAM, poderá perder seu disco secundário. Ao modificar um perfil de servidor virtual que usa armazenamento local, o perfil é pré-configurado para você e os perfis que não são comparáveis não podem ser selecionados.
3. Clique em **Continuar**.
4. Revise sua confirmação de ordem quanto à precisão.  Clique em **Editar** para editar seu upgrade.
5. Clique em **Confirmar** para confirmar sua ordem e aplicar as mudanças a seu dispositivo.
