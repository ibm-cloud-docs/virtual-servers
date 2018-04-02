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


# Einheitenzugriff verwalten
{: #managing-device-access}

Für den Zugriff und die Verwaltung der Details für eine bestimmte Einheit benötigt Ihr Benutzerkonto die entsprechenden Berechtigungen.  Nachdem der Kontoadministrator Ihr Benutzerkonto für den Zugriff auf eine Einheit berechtigt hat, können Sie die Einheitendetails im {{site.data.keyword.slportal_full}} oder in der API anzeigen.  Welche Informationen oder Aktionen für Sie angezeigt werden, hängt vom Einheitentyp und von den Berechtigungen Ihres Benutzerkontos ab.
{:shortdesc}

**Hinweis:** Wenn Ihr Konto Einheiten enthält, für die Sie keine Zugriffsrechte besitzen, wird eine Nachricht "nicht gefunden" angezeigt, wenn Sie versuchen, auf die betreffenden Einheiten zuzugreifen.

Sie können in Ihrem Konto allen Benutzern außer Ihnen selbst Einheitenzugriff erteilen. Nur ein Kontoadministrator kann auf alle Einheiten in seinem Kundenkonto zugreifen und den Zugriff für alle anderen Benutzer in seinem Konto festlegen. 

Sie benötigen die folgenden Berechtigungen, um auf die Einheitendetails für öffentliche virtuelle Server oder dedizierte virtuelle Server zuzugreifen.

**Details für virtuelle Server anzeigen**

Ermöglicht das Anzeigen von IP-Adressen, Betriebssystemtyp, Kennwörtern und weiteren Details für einen angegebenen virtuellen Server.  Diese Berechtigung ermöglicht außerdem das Ändern von Kennwörtern für virtuelle Server im Portal. Ein Benutzer muss über dieses Zugriffsrecht verfügen, um öffentliche Instanzen, dedizierte Instanzen und dedizierte Hostinstanzen anzuzeigen.

**Details für virtuelle dedizierte Hosts anzeigen**

Ermöglicht das Anzeigen von IP-Adressen, Betriebssystemtyp, Kennwörtern und weiteren Details für einen angegebenen dedizierten Host.  Diese Berechtigung ermöglicht außerdem das Migrieren dedizierter Instanzen auf einen anderen dedizierten Host. Ein Benutzer muss über dieses Zugriffsrecht verfügen, um dedizierte Hosts anzuzeigen.

## Berechtigungen zum Anzeigen virtueller Serverinstanzen hinzufügen
Führen Sie die folgenden Schritte aus, um die Berechtigung *Details für virtuelle Server anzeigen* für beliebige der Ihnen untergeordneten Benutzer hinzuzufügen. Nur ein Kontoadministrator kann Berechtigungen für andere Benutzer in seinem Konto erteilen.  

1. Öffnen Sie das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window}, indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Wählen Sie in der Navigationsleiste **Konto > Benutzer** aus, um die Anzeige 'Benutzer' aufzurufen.
3. Klicken Sie auf den gewünschten Benutzernamen, um das Benutzerprofil aufzurufen.
4. Klicken Sie auf das Symbol **Portalberechtigungen**, um die Anzeige für Portalberechtigungen aufzurufen.
5. Wählen Sie auf der Registerkarte *Einheit* die Óption **Details für virtuelle Server anzeigen** aus, um diese Berechtigung zum Profil des Benutzers hinzuzufügen.

Führen Sie als nächstes die folgenden Schritte aus, um Zugriff auf einer bestimmten Einheitenebene bereitzustellen.

1. Klicken Sie auf das Symbol **Einheitenzugriff**, um die Anzeige 'Einheitenzugriff' aufzurufen.
2. Klicken Sie auf die Registerkarte **Schnellzugriff**. 
   Hinweis: Eine andere Option ist das Auswählen einer einzelnen Einheit.
3. Wählen Sie in der Dropdown-Liste *Einheitentyp* den Eintrag **Alle virtuellen Server** aus.
4. Wählen Sie das Kontrollkästchen **Zugriff automatisch erteilen, wenn neue Einheiten hinzugefügt werden** aus, wenn der zugeordnete Benutzer immer Zugriff auf diesen Einheitentyp erhalten soll.
5. Überprüfen Sie, dass die richtigen Einheiten ausgewählt sind.
6. Klicken Sie auf **Einheitenzugriff aktualisieren**.

## Berechtigungen zum Anzeigen dedizierter Hosts hinzufügen
Führen Sie die folgenden Schritte aus, um die Berechtigung *Details für virtuelle dedizierte Hosts anzeigen* für beliebige der Ihnen untergeordneten Benutzer hinzuzufügen. Nur ein Kontoadministrator kann Berechtigungen für andere Benutzer in seinem Konto erteilen.

1. Öffnen Sie das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window}, indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Wählen Sie in der Navigationsleiste **Konto > Benutzer** aus, um die Anzeige 'Benutzer' aufzurufen.
3. Klicken Sie auf den gewünschten Benutzernamen, um das Benutzerprofil aufzurufen.
4. Klicken Sie auf das Symbol **Portalberechtigungen**, um die Anzeige für Portalberechtigungen aufzurufen.
5. Wählen Sie auf der Registerkarte *Einheit* die Option **Details für virtuelle dedizierte Hosts anzeigen** aus, um diese Berechtigung zum Profil des Benutzers hinzuzufügen.

Führen Sie als nächstes die folgenden Schritte aus, um Zugriff auf einer bestimmten Einheitenebene bereitzustellen.

1. Klicken Sie auf das Symbol **Einheitenzugriff**, um die Anzeige 'Einheitenzugriff' aufzurufen.
2. Klicken Sie auf die Registerkarte **Schnellzugriff**. 
   Hinweis: Eine andere Option ist das Auswählen einzelner Einheiten.
3. Wählen Sie in der Dropdown-Liste *Einheitentyp* den Eintrag **Alle dedizierten Hosts** aus.
4. Wählen Sie das Kontrollkästchen **Zugriff automatisch erteilen, wenn neue Einheiten hinzugefügt werden** aus, wenn der zugeordnete Benutzer immer Zugriff auf diesen Einheitentyp erhalten soll.
5. Überprüfen Sie, dass die richtigen Einheiten ausgewählt sind.
6. Klicken Sie auf **Einheitenzugriff aktualisieren**.

**Hinweis:** Sie können auch den API-Service SoftLayer_User_Customer::addBulkDedicatedHostAccess verwenden, um einem Benutzer Zugriff auf einen oder mehrere dedizierte Hosts zu erteilen. Weitere Informationen finden Sie unter [Mehrfachen dedizierten Hostzugriff hinzufügen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://sldn.softlayer.com/reference/services/softlayer_user_customer/addbulkdedicatedhostaccess){: new_window}.  

## Nächste Schritte
Die Benutzerberechtigungen werden nach dem Absenden der Änderungen sofort aktualisiert. Wenn Berechtigungen erteilt wurden, kann der Benutzer die ausgewählten Funktionen anzeigen und aufrufen. Wenn Berechtigungen widerrufen wurden, kann der betreffende Benutzer die Funkionen nicht mehr anzeigen oder aufrufen. Berechtigungen können jederzeit erneut aktualisiert werden.
