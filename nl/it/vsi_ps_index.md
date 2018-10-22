---
copyright:
  years: 2014, 2018
lastupdated: "2018-02-20"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Script di provisioning

Uno script di provisioning è uno script che può essere scaricato o scaricato ed eseguito, su un dispositivo durante il processo di provisioning. Per gli account esistenti, gli script di provisioning sono gestiti in {{site.data.keyword.slportal_full}}. Durante il processo di ordine, puoi immettere manualmente gli script per i nuovi account o quelli che ancora non sono stati tracciati.

Durante il processo di provisioning, gli script associati a un URL HTTP vengono scaricati nel dispositivo. Dopo il provisioning, un amministratore deve eseguire lo script manualmente sul dispositivo. Gli script associati a un URL HTTPS vengono scaricati ed eseguiti automaticamente. Gli script di provisioning sono al momento disponibili su sistemi operativi Linux standard (Cent, RHEL, Fedora, Debian o Ubuntu) e Windows e FreeBSD. Altri sistemi come Vyatta, Netscaler, XenServer, VMware non sono supportati. Lo script di provisioning può essere qualsiasi tipo di file eseguito dal sistema operativo, inclusi i file binari combinati o qualsiasi linguaggio supportato dal SO.

Per ulteriori informazioni, consulta [Gestione di uno script di provisioning](add-provisioning-script.html).
