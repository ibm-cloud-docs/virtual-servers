---
copyright:
  years: 2014, 2018
lastupdated: "2018-10-18"
---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# Script di provisioning

Uno script di provisioning è uno script che può essere scaricato o scaricato ed eseguito, su un dispositivo durante il processo di provisioning. Per gli account esistenti, gli script di provisioning sono gestiti nel {{site.data.keyword.slportal_full}}. Durante il processo di ordine, puoi immettere manualmente gli script per i nuovi account o quelli che ancora non sono stati tracciati.

In alternativa, puoi utilizzare un'immagine abilitata a cloud-init e fornire i dati utente per eseguire automaticamente le attività di configurazione oppure eseguire gli script. Per ulteriori informazioni, vedi il documento relativo al [provisioning con un'immagine abilitata a cloud-init](/docs/infrastructure/image-templates/image_cloud-init.html#provisioning-with-a-cloud-init-enabled-image).
{: tip}

Durante il processo di provisioning, gli script di provisioning associati a un URL HTTP vengono scaricati nel dispositivo. Dopo il provisioning, un amministratore deve eseguire lo script manualmente sul dispositivo. Gli script associati a un URL HTTPS vengono scaricati ed eseguiti automaticamente. Gli script di provisioning sono al momento disponibili su sistemi operativi Linux standard (Cent, RHEL, Fedora, Debian o Ubuntu) e Windows e FreeBSD. Altri sistemi come Vyatta, Netscaler, XenServer, VMware non sono supportati. Lo script di provisioning può essere qualsiasi tipo di file eseguito dal sistema operativo, inclusi i file binari combinati o qualsiasi linguaggio supportato dal SO.

Per ulteriori informazioni, consulta [Gestione di uno script di provisioning](add-provisioning-script.html).
