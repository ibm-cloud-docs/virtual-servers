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

#  Recarregando o OS
É possível recarregar o sistema operacional (OS) em um dispositivo a qualquer momento para restaurar um dispositivo para sua ordem de trabalho original ou para reconfigurar um dispositivo com software diferente. Um recarregamento de OS remove todos os dados do dispositivo e aplica uma configuração "como nova", conforme especificado durante o processo de configuração da configuração de Recarregamento de OS. Como os recarregamentos de OS limpam todos os dados do dispositivo, se os dados não foram submetidos a backup antes do recarregamento, eles serão excluídos permanentemente e não poderão ser recuperados.
{:shortdesc}

**Importante:** se você deseja reter seus dados, faça backup de todos os dados antes de executar um recarregamento.

## Executando o recarregamento
1. Na **Lista de dispositivos**, clique no servidor que precisa de um Recarregamento de OS.
2. No menu **Ações** na parte superior esquerda da página, selecione **Recarregamento de OS**.
3. Determine se você deseja recarregar a configuração existente ou recarregar o dispositivo com uma nova configuração.

   <table>
   <CAPTION>Tabela 1. Opções de recarregamento de OS</CAPTION>
   <THEAD>
   <TR>
   <th>Tipo de recarregamento</th>
   <th>Etapas</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Se você deseja recarregar usando uma nova configuração...</td>
   <td>
   <ol>
   <li>Clique em <b>Editar</b> para a Categoria que requer uma atualização.</li>
   <li>Selecione o novo software para aplicar ao dispositivo na lista <i>Selecionar software</i>.</li>
   </ol>
   </td>
   </tr>
   <tr>
   <td>Se desejar recarregar usando a configuração existente...</td>
   <td>Continue com a próxima etapa.</td>
   </tr>
   </TBODY>
   </table>

4. Determine se um script de Pós-instalação deve ser aplicado após o dispositivo ser provisionado.

   Se você deseja aplicar um script de pós-instalação, selecione o script na lista suspensa Script existente ou insira a URL qualificada para o novo script.  Caso contrário, continue com a próxima etapa.

5. Para dispositivos físicos, determine se as partições instaladas devem ser incluídas, removidas ou permanecer inalteradas.
   
   <table>
   <CAPTION>Tabela 2. Opções de ação de partição</CAPTION>
   <THEAD>
   <TR>
   <th>Ação de partição</th>
   <th>Etapas</th>
   </TR>
   </THEAD>
   <TBODY>
   <tr>
   <td>Para incluir partições instaladas...</td>
   <td>
   <ul>
   <li>Clique no link <b>Incluir outra partição</b>.</li>
   <li>Insira o nome exato da partição.</li>
   <li>Insira o tamanho da partição (em GBs). Se desejar, será possível selecionar Crescer para crescer a partição para preencher o espaço em disco restante.
   <p><b>Nota:</b> somente uma partição pode ser selecionada para crescer em qualquer momento. Essa partição é maior do que o tamanho especificado e preenche toda a capacidade disponível. A capacidade da partição de Crescimento é calculada subtraindo o tamanho combinado de todas as outras partições do número de Capacidade total que é fornecido na seção Partições instaladas.</p>
   </li>
   </ul>
   </td>
   </tr>
   <tr>
   <td>Para excluir partições instaladas...</td>
   <td>Clique no ícone <b>Excluir</b> para excluir a partição.</td>
   </tr>
   <tr>
   <td>Para permanecer inalterado...</td>
   <td>Continue com a próxima etapa.</td>
   </tr>
   </TBODY>
   </table>
    
6. Determine se deseja aplicar um ou mais chaves SSH ao dispositivo.

7. Marque as caixas de seleção aplicáveis para as opções desejadas a serem aplicadas ao dispositivo durante ou após o Recarregamento de OS.

   **Nota:** as opções variam com base no dispositivo. Nem todas as opções estão disponíveis para todo dispositivo.

8. Clique no botão **Recarregar acima da configuração** para continuar com o pop-up de Revisão. Clique no botão **Cancelar** para cancelar as mudanças para o dispositivo e sair da tela.

9. Verifique se todos os detalhes na seção Nova configuração estão corretos.  

10. Clique no botão **Confirmar recarregamento de OS** para confirmar e iniciar o Recarregamento de OS. Clique no botão **Cancelar** para cancelar a ação.

## O que vem a seguir?
Depois de iniciar o processo de Recarregamento de S.O., o dispositivo é colocado off-line e o processo de Recarregamento de S.O. é iniciado.
O período no qual um recarregamento de S.O. ocorre varia com base na configuração atual e nova do dispositivo.
Durante o processo de configuração, o tempo mínimo para o Recarregamento de OS é exibido em cada tela.
O intervalo de tempo exibido é uma estimativa feita pelo sistema e é fornecido como uma cortesia. Se o recarregamento levar mais de 24 horas, entre em contato com nossa equipe de Suporte. Quando o dispositivo retorna on-line, ele funciona conforme especificado na Nova configuração para o Recarregamento de S.O. Todos os dados salvos anteriormente no dispositivo são perdidos, mas poderão ser restaurados se um backup do dispositivo tiver sido feito antes de seu recarregamento.
Caso não tenha sido feito backup dos dados, eles não poderão ser recuperados.
 
Para registrar novamente seu dispositivo com o eVault, veja [Registrando novamente seu dispositivo com o eVault ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://knowledgelayer.softlayer.com/procedure/how-do-i-re-register-evault){: new_window}.
