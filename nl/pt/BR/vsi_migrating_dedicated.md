---



copyright:
  years: 2017
lastupdated: "2017-10-24"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Migrando uma instância de host dedicado para outro host
{: #migrating-dedicated-host}

É possível migrar suas instâncias de host dedicado de um host para outro dentro do mesmo POD. Selecione a instância a ser migrada na página Detalhes do dispositivo do host ou na página Detalhes do dispositivo da instância. Observe que somente duas instâncias podem ser migradas por vez e o tempo necessário para migrar depende do disco. Os discos SAN são migrados mais rápido porque os discos locais requerem copiar o disco. As instâncias em migração ficam off-line enquanto estão sendo migradas; o host permanece ativo para quaisquer de suas outras instâncias de host dedicado.
{:shortdesc}

Use as etapas a seguir para migrar as instâncias de host dedicado para outro host dedicado dentro do mesmo POD na página Detalhes do dispositivo do *host dedicado original*. 

1. Acesse o [{{site.data.keyword.slportal_full}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) usando suas credenciais exclusivas. 
2. Clique em **Dispositivo > Lista de dispositivos** e selecione o host ou a instância hospedada na lista.
3. Clique na lista suspensa **Ações** ao lado da instância dedicada a ser migrada.
4. Selecione **Migrar** e insira o host para o qual a instância está sendo migrada; lembre-se, o host de destino deve estar dentro do mesmo POD que o host original.
5. Clique no botão **Migrar**. 

A migração será iniciada imediatamente. Durante a migração, a instância dedicada fica off-line até que seja ligada em seu novo host. É possível visualizar a página Detalhes do dispositivo do host de destino para assegurar que a instância tenha sido migrada corretamente.

Use as etapas a seguir para migrar as instâncias de host dedicado para outro host dedicado dentro do mesmo POD na página Detalhes da *instância de host dedicado*.

1. Acesse o [{{site.data.keyword.slportal}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/) usando suas credenciais exclusivas.
2. Clique em **Dispositivo > Lista de dispositivos** e selecione a instância hospedada a ser migrada na lista.
3. Clique no link **Migrar** no lado direito da página.
4. Selecione o host de destino para o qual migrar a instância; lembre-se, o host de destino deve estar dentro do mesmo POD que o host original.
5. Clique no botão **Migrar**.

A migração será iniciada imediatamente. Durante a migração, a instância dedicada fica off-line até que seja ligada em seu novo host. É possível visualizar a página Detalhes do dispositivo do host de destino para assegurar que a instância tenha sido migrada corretamente.

## Próximas Etapas
Depois de migrar uma instância de host dedicado, confirme se a migração funcionou verificando se o seu Status está verde na página Detalhes do dispositivo do novo host dedicado.
