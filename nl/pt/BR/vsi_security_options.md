---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-04"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Firewalls
{: #virtual-server-security-options}

Com {{site.data.keyword.BluVirtServers}}, você tem várias opções de firewall que fornecem uma camada de segurança essencial.  As opções de firewall são provisionadas sob demanda, sem interrupções de serviço. Os serviços de firewall evitam que tráfego indesejado ocorra em seus servidores, reduzindo a probabilidade de um ataque e permitindo que seus recursos do servidor sejam dedicados para o seu uso desejado.
{:shortdesc}

Os firewalls estão disponíveis como um recurso complementar para todos os servidores na rede pública de Infraestrutura.

Como parte do processo de pedido, é possível selecionar um hardware específico do dispositivo ou um firewall de software para fornecer proteção. Como alternativa, é possível implementar dispositivos de firewall dedicados no ambiente e implementar o servidor virtual em uma VLAN protegida.  

Um servidor virtual não pode ser protegido por dois dispositivos de firewall na mesma interface.
{:note}

Para obter mais informações, veja as coleções de tópicos de segurança a seguir.

* [Hardware Firewalls (Shared)](/docs/infrastructure/hardware-firewall-shared?topic=hardware-firewall-shared-about-hardware-firewall-shared-)
* [Hardware Firewalls (Dedicated)](/docs/infrastructure/hardware-firewall-dedicated?topic=hardware-firewall-dedicated-about-the-hardware-firewall-dedicated-)
