---



copyright:
  years: 2018
lastupdated: "2018-10-05"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Fornecendo a capacidade e as instâncias reservadas

## Antes de iniciar 

É possível fornecer a capacidade e as instâncias reservadas por meio do catálogo do {{site.data.keyword.cloud}}. Deve-se fornecer a capacidade reservada antes das instâncias de servidor virtual.

**Nota**: se você não for o administrador da conta, a conta do usuário deverá incluir a permissão **Gerenciar capacidades reservadas**. O administrador da conta pode conceder a permissão do usuário na guia **Permissões do portal** no console. Para obter mais informações sobre como atualizar as permissões, consulte [Gerenciando o acesso à infraestrutura](/docs/iam/mnginfra.html).

## Efetuando login no catálogo do IBM Cloud

Use as etapas a seguir para efetuar login no catálogo do {{site.data.keyword.cloud_notm}} para começar a fornecer a capacidade e as instâncias reservadas.

  1. Efetue login no catálogo do [{{site.data.keyword.cloud_notm}}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/){: new_window} usando as credenciais exclusivas. 

## Fornecendo a capacidade reservada 

No catálogo do {{site.data.keyword.cloud_notm}}, conclua as etapas a seguir para fornecer a capacidade reservada.

  1. Na seção **Infraestrutura de cálculo**, clique no bloco **Virtual Servers**.
  2. Selecione a opção **Virtual Server reservado**.
  3. Clique em **Criar**.
  4. Para criar a nova capacidade reservada, selecione **Nova capacidade +**. Na página
**Capacidade reservada**, insira ou selecione as informações a seguir: 

| Campo                   | Valor               |                                                                                                                                                                                                                                                                                                                                 
| ----------------------- | ------------------- |
| Nome                    |Um nome é necessário para a capacidade reservada.|                                                                                                                                                                                                                                                                                                       
| Capacidade do servidor virtual |Selecione o número de instâncias que você deseja designar a essa capacidade reservada (limite de 20 instâncias).|                                                                                                                                                                                                                                                
| Local                |Selecione o local específico que é necessário para as cargas de trabalho. Os locais são
compostos de regiões; cada região é uma área geográfica separada. **Nota:** não é possível selecionar locais individuais para cada instância de servidor virtual que você fornece dentro dessa capacidade reservada. A sua seleção é o local para todas as instâncias de servidor virtual que você fornece dentro dessa capacidade reservada.|
| POD                     |Selecione o POD específico para a sua localização.|
| Termos do Plano              |Escolha entre um prazo de contrato de um ou três anos.|                                                                                                                                                                                                                                                                                            
| Perfil                 |Selecione entre perfis populares ou todas as combinações disponíveis de vCPU e RAM de armazenamento suportado pela SAN (balanceado, memória ou cálculo). **Nota:** não é possível combinar diferentes tamanhos de perfil dentro do conjunto de instâncias de servidor virtual designado para essa capacidade ou mudá-los posteriormente. O conjunto de instâncias de servidor virtual que você reserva deve ter o mesmo tamanho.| 
{: caption="Tabela 1. Seleções de fornecimento de capacidade reservada" caption-side="top"}


## Fornecendo as instâncias reservadas

Depois de ter fornecido a capacidade reservada, é hora de fornecer as instâncias de servidor virtual reservadas. As instâncias de servidor virtual reservadas podem ser fornecidas a qualquer momento durante o prazo do contrato porque a capacidade é garantida. Conclua as etapas a seguir para fornecer as instâncias reservadas:

1. No catálogo do {{site.data.keyword.cloud_notm}}, selecione o bloco **Virtual Servers** na seção **Infraestrutura de cálculo**.
2. Selecione a opção **Virtual Server reservado**. 
3. Clique em **Criar**. 
4. Para fornecer uma instância de servidor virtual reservada, insira ou selecione as informações a seguir:

| Campo                     | Valor               |                                                                                                                                                                                                                                                                                                                                 
| ------------------------- | ------------------- |
| Nome                      |Um nome é necessário para a instância de servidor virtual reservada.|                                                                                                                                                                                                                                                                                                       
| Faturamento                   |Selecione um faturamento mensal ou por hora.|                                                                                                                                                                                                                                                
| Capacidade Reservada         |Selecione a capacidade reservada ou selecione **Nova capacidade +** para fornecer a capacidade reservada adicional.|                                                                                                                                                                                                     
| Complementos                   |Escolha qualquer armazenamento, rede ou software adicional.|                                                                                                                                                                                                                                                                                            
{: caption="Tabela 1. Seleções de fornecimento de capacidade reservada" caption-side="top"}

## Próximas Etapas

Depois de ter fornecido a capacidade e as instâncias reservadas do servidor virtual, é possível começar a gerenciá-las. Para obter mais informações, veja [Gerenciando servidores virtuais](vsi_managing.html). Se você tiver dúvidas sobre a capacidade e as instâncias reservadas, consulte [Perguntas frequentes: capacidade e instâncias reservadas](vsi_faqs_reserved.html). 
