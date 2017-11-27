---



copyright:
  years: 2017
lastupdated: "2017-05-17"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Recarregando o OS usando um modelo de imagem
Semelhante ao Recarregamento de OS padrão, o recarregamento de um dispositivo de um Modelo de imagem permite aos usuários restaurar ou reconfigurar um dispositivo com base em um modelo de imagem preexistente que está associado à conta do Portal do Cliente em uso. Durante o processo de Recarregamento de OS padrão, as opções de configuração para o dispositivo podem ser selecionadas individualmente, enquanto o recurso Carregamento de imagem carrega a configuração exatamente como ela aparece no modelo de imagem. Ainda é possível incluir recursos opcionais antes de executar o recarregamento.
Use as etapas a seguir para executar um recarregamento de OS de um modelo de imagem usando o recurso Carregamento de imagem no Portal do Cliente.
{:shortdesc}

## Executando o recarregamento usando um modelo de imagem
1. Faça backup de todos os dados no dispositivo.
  
   **Nota:** os Recarregamentos de OS resultam em todos os dados sendo limpos do disco rígido. Se os dados não forem submetidos a backup antes da iniciação do Recarregamento de OS, eles não poderão ser recuperados. O Bluemix (Softlayer) não faz backup de quaisquer dados armazenados em dispositivos do cliente e não é responsável por qualquer perda de dados associados ao processo de Recarregamento de OS.
  
2. Na página Lista de dispositivos, selecione **Carregamento de imagem** no menu **Ações** para o dispositivo desejado.

3. Marque a caixa de seleção do modelo de imagem desejado para selecionar o modelo de imagem que será carregado no dispositivo.

   **Nota:** antes de concluir o recarregamento, o modelo de imagem será copiado para o data center que contém o dispositivo, se ele ainda não estiver localizado no mesmo data center. Se o modelo de imagem deverá ser copiado para o data center apropriado, uma taxa adicional poderá ser cobrada se o modelo não for excluído do local depois que o Recarregamento de OS ocorrer.
  
4. Determine se você deseja incluir quaisquer recursos opcionais. Quaisquer recursos opcionais selecionados são incluídos no dispositivo como parte do processo de recarregamento.
   
   <table>
   <CAPTION>Tabela 1. Recursos opcionais</CAPTION>
   <THEAD>
   <TR>
   <th>Recursos opcionais</th>
   <th>Etapas</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   </tr>
   <tr>
   <td>Sim, eu desejo incluir recursos opcionais.</td>
   <td>
   <ol>
   <li>Clique em <b>Carregar imagem selecionada</b>.</li>
   <li>Revise a configuração de imagem e continue ou cancele.</li>
   <li>Clique em <b>Confirmar recarregamento de OS</b> para confirmar a ação e iniciar o processo de recarregamento de OS.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Não, eu não desejo incluir recursos opcionais.</td>
   <td>Clique em <b>Visualizar recursos opcionais</b>.</td>
   </tr>
   </TBODY>
   </table>

5. Configure opções adicionais, conforme relevante. Consulte as informações a seguir para obter mais detalhes.
   
   <dl>
   <dt>Script de pós-instalação</dt>
   <dd>Inclui um script de pós-instalação novo ou existente.</dd>
   <dt>Chave SSH</dt>
   <dd>Inclui uma chave SSH no dispositivo após a ação de recarregamento. </dd>
   <dt>Reconfigurar senha do IPMI</dt>
   <dd> Essa opção está disponível somente para dispositivos físicos. </dd>
   <dt>Aplicar upgrades de BIOS da placa-mãe</dt>
   <dd>Essa opção está disponível somente para dispositivos físicos. </dd>
   <dt>Aplicar atualizações de firmware para todos os discos rígidos</dt>
   <dd>Essa opção está disponível somente para dispositivos físicos.</dd>
   <dt>Incluir no conjunto sobressalente após Recarregamento de OS</dt>
   <dd>Essa opção está disponível somente em dispositivos físicos e requer aprovação interna antes de ficar disponível em uma conta.</dd>
   <dt>Apagar todos os discos rígidos</dt>
   <dd> Essa opção está disponível somente em dispositivos físicos e requer permissões de usuário especiais configuradas pelo administrador da Conta.</dd>
   <dt>Recarregamento de OS com preservação de disco</dt>
   <dd>Retém todos os dados no disco primário atual durante o processo de Recarregamento de OS. A preservação de disco resulta na unidade primária sendo convertida em um dispositivo de Armazenamento móvel. Essa opção está disponível somente em dispositivos virtuais e incorre em encargos adicionais com base nos padrões de faturamento (por hora ou mensal) do dispositivo. É possível cancelar os encargos cancelando o dispositivo de Armazenamento móvel a qualquer momento após ele ter sido criado.</dd>
   </dl>

6. Clique em **Carregar imagem selecionada**.

7. Revise a configuração da imagem e clique em **Avançar** para continuar na próxima tela ou **Cancelar** para cancelar a ação.

   **Nota:** depois de clicar em **Avançar**, todas as portas de rede para o dispositivo são sistematicamente encerradas e o dispositivo fica indisponível por até 15 minutos. Durante esse tempo, a ação pode ser cancelada a qualquer momento clicando em **Cancelar**. A próxima etapa deverá ser concluída dentro de 15 minutos após clicar em **Avançar** ou as etapas anteriores deverão ser concluídas novamente. Esse processo está em vigor como uma proteção para assegurar que nenhum dado adicional seja incluído em um dispositivo entre a confirmação da configuração e a iniciação do Recarregamento de OS.

8. Clique em **Confirmar recarregamento de OS** para confirmar a ação e iniciar o processo de recarregamento OS. Clique em **Cancelar** para cancelar a ação.

## O que vem a seguir?
Depois de iniciar o processo de Recarregamento de S.O., o dispositivo é colocado off-line e o processo de Recarregamento de S.O. é iniciado.
O período no qual um recarregamento de S.O. ocorre varia com base na configuração atual e nova do dispositivo.
Se o recarregamento levar mais de 24 horas, entre em contato com nossa equipe de Suporte. Quando o dispositivo retorna on-line, ele funciona conforme especificado na Nova configuração para o Recarregamento de S.O. Todos os dados salvos anteriormente no dispositivo são perdidos, mas poderão ser restaurados se um backup do dispositivo tiver sido feito antes de seu recarregamento. Caso não tenha sido feito backup dos dados, eles não poderão ser recuperados.

 Para registrar novamente seu dispositivo com eValut, veja [Registrando novamente seu dispositivo com o eVault ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
