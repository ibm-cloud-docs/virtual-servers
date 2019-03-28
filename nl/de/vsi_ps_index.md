---

copyright:
  years: 2014, 2018
lastupdated: "2018-10-18"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:new_window: target="_blank"}

# Bereitstellungsscripts
{: #provisioning-scripts}

Ein Bereitstellungsscript ist ein Script, das während des Bereitstellungsprozesses in eine Einheit heruntergeladen werden oder in die Einheit heruntergeladen und in ihr ausgeführt werden kann. Bereitstellungsscripts für vorhandene Konten werden im {{site.data.keyword.slportal_full}} verwaltet. Während des Bestellprozesses können Sie Scripts für neue Konten oder Scripts, die noch nicht erfasst wurden, manuell eingeben.

Alternativ dazu können Sie auch ein für die Cloud-Initialisierung aktiviertes Image verwenden und Benutzerdaten angeben, um Konfigurationstasks oder Scripts automatisch auszuführen. Weitere Informationen finden Sie in [Bereitstellung mit einem für die Cloud-Initialisierung aktiverten Image](/docs/infrastructure/image-templates?topic=image-templates-provisioning-with-a-cloud-init-enabled-image#provisioning-with-a-cloud-init-enabled-image).
{: tip}

Während des Bereitstellungsprozesses werden Bereitstellungsscripts, denen eine HTTP-URL zugeordnet ist, in die Einheit heruntergeladen. Nach der Bereitstellung muss ein Administrator das Script manuell in der Einheit ausführen. Scripts, denen eine HTTPS-URL zugeordnet ist, werden heruntergeladen und automatisch ausgeführt. Bereitstellungsscripts stehen aktuell für standardmäßige Linux-Betriebssysteme (Cent, RHEL, Fedora, Debian oder Ubuntu) und für Windows und FreeBSD zur Verfügung. Andere Systeme, wie beispielsweise Vyatta, Netscaler, XenServer oder VMware werden nicht unterstützt. Das Bereitstellungsscript kann eine beliebige Datei sein, die vom Betriebssystem ausgeführt wird; hierzu gehören auch binäre Dateien oder Dateien in einer beliebigen vom Betriebssystem unterstützten Sprache.

Weitere Informationen finden Sie in [Bereitstellungsscript verwalten](/docs/vsi?topic=virtual-servers-managing-a-provisioning-script).
