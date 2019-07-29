---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-07"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:note: .note}
{:table: .aria-labeledby="caption"}


# Einheitenzugriff verwalten
{: #managing-device-access}

Für den Zugriff auf die und die Verwaltung der Details für eine bestimmte Einheit benötigt Ihr Benutzerkonto die korrekten Berechtigungen. Nachdem der Kontoadministrator Ihr Benutzerkonto für den Zugriff auf eine Einheit berechtigt hat, können Sie die Einheitendetails in der {{site.data.keyword.cloud}}-Konsole oder in der {{site.data.keyword.slapi_short}} anzeigen. Welche Informationen oder Aktionen für Sie angezeigt werden, hängt vom Einheitentyp und von den Berechtigungen Ihres Benutzerkontos ab.
{:shortdesc}

Wenn Ihr Konto Einheiten enthält, für die Sie keine Zugriffsrechte besitzen, wird eine Nachricht "nicht gefunden" angezeigt, wenn Sie versuchen, auf die betreffenden Einheiten zuzugreifen.
{:note}

Sie können in Ihrem Konto allen Benutzern außer Ihnen selbst Einheitenzugriff erteilen. Nur ein Kontoadministrator kann auf alle Einheiten in seinem Kundenkonto zugreifen und den Zugriff für alle anderen Benutzer in seinem Konto festlegen. 

Sie benötigen die folgenden Berechtigungen, um auf die Einheitendetails für öffentliche virtuelle Server oder dedizierte virtuelle Server zuzugreifen.

* **Details des virtuellen Servers anzeigen** - Ermöglicht das Anzeigen von IP-Adressen, des Betriebssystemtyps, von Kennwörtern und weiteren Details für einen angegebenen virtuellen Server. Diese Berechtigung ermöglicht außerdem das Ändern von Kennwörtern für virtuelle Server im Portal. Sie müssen über dieses Zugriffsrecht verfügen, um öffentliche Instanzen, dedizierte Instanzen und dedizierte Hostinstanzen anzuzeigen.

* **Details des dedizierten virtuellen Hosts anzeigen** - Ermöglicht das Anzeigen von IP-Adressen, des Betriebssystemtyps, von Kennwörtern und weiteren Details für einen angegebenen dedizierten Host. Diese Berechtigung ermöglicht außerdem das Migrieren dedizierter Instanzen auf einen anderen dedizierten Host. Sie müssen über dieses Zugriffsrecht verfügen, um dedizierte Hosts anzuzeigen.


## Berechtigungen für Ihre Benutzer hinzufügen
Führen Sie die folgenden Schritte aus, wenn Sie der Kontoadministrator sind und Benutzern die Berechtigung zum Anzeigen der Details für virtuelle Server und der Details für dedizierte Hosts erteilen möchten.

1. Melden Sie sich auf der Seite für [Access (IAM) ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/iam#/users){: new_window} in der {{site.data.keyword.cloud}}-Konsole an. 
2. Wählen Sie auf der Registerkarte **Benutzer** die Option **Anzeigen nach: Benutzer der klassischen Infrastruktur** aus.
3. Wählen Sie einen Benutzer aus und klicken Sie dann auf die Registerkarte **Klassische Infrastruktur**.
4. Erweitern Sie die Ansicht der Kategorie **Einheiten** auf der Registerkarte **Berechtigungen** und wählen Sie dann **Details zu virtuellen Servern anzeigen** und **Details zu virtuellen dedizierten Hosts anzeigen** aus.
5. Klicken Sie auf **Anwenden**.

### Spezielle Berechtigungen auf Einheitenebene hinzufügen
Führen Sie die folgenden Schritte aus, um Benutzern Zugriff auf einer bestimmten Einheitenebene bereitzustellen.

1. Wählen Sie auf der Registerkarte **Benutzer** die Option **Anzeigen nach: Benutzer der klassischen Infrastruktur** aus. 
2. Wählen Sie einen Benutzer aus und klicken Sie dann auf die Registerkarte **Klassische Infrastruktur**.
3. Wählen Sie im Abschnitt **Typ auswählen** auf der Registerkarte **Einheiten** die entsprechende Berechtigung aus: **Alle Bare Metal Server**, **Alle dedizierten Hosts** oder **Alle virtuellen Server**. 
4. Wählen Sie im Abschnitt **Späteren Zugriff aktivieren** auf der Registerkarte **Einheiten** die entsprechende Berechtigung aus: **Automatischer Bare Metal Server-Zugriff**, **Automatischer Zugriff auf dedizierte Hosts** oder **Automatischer Zugriff auf virtuelle Server**. Diese Berechtigung ermöglicht Ihren Benutzern den ständigen Zugriff auf den Einheitentyp, wenn neue Einheiten hinzugefügt werden.
5. Klicken Sie auf **Festlegen**, um die neuen Berechtigungen anzuwenden.

## Berechtigungen für Ihre Benutzer im Kundenportal hinzufügen
Führen Sie die folgenden Schritte aus, wenn Sie der Kontoadministrator sind und Benutzern die Berechtigung zum Anzeigen der Details für virtuelle Server und der Details für dedizierte Hosts erteilen möchten.

1. Öffnen Sie das [{{site.data.keyword.slportal}} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://control.softlayer.com/){: new_window}, indem Sie Ihre eindeutigen Berechtigungsnachweise eingeben.
2. Wählen Sie in der Navigationsleiste **Konto > Benutzer** aus, um die Anzeige 'Benutzer' aufzurufen.
3. Klicken Sie auf den gewünschten Benutzernamen, um das Benutzerprofil aufzurufen.
4. Klicken Sie auf das Symbol **Portalberechtigungen**, um die Anzeige für Portalberechtigungen aufzurufen.
5. Wählen Sie auf der Registerkarte **Einheit** die Optionen **Details zu virtuellen Servern anzeigen** und **Details zu virtuellen dedizierten Hosts anzeigen** aus, um diese Berechtigungen zum Profil Ihres Benutzers hinzuzufügen.

### Spezielle Berechtigungen auf Einheitenebene im Kundenportal hinzufügen
Führen Sie als nächstes die folgenden Schritte aus, um Zugriff auf einer bestimmten Einheitenebene bereitzustellen.

1. Klicken Sie auf das Symbol **Einheitenzugriff**, um die Anzeige 'Einheitenzugriff' aufzurufen.
2. Klicken Sie auf die Registerkarte **Schnellzugriff**. 
3. Wählen Sie in der Dropdown-Liste **Einheitentyp** die Optionen **Alle virtuellen Server** und **Alle dedizierten Hosts** aus.
4. Wählen Sie das Kontrollkästchen **Zugriff automatisch erteilen, wenn neue Einheiten hinzugefügt werden** aus, wenn der zugeordnete Benutzer immer Zugriff auf diesen Einheitentyp erhalten soll.
5. Überprüfen Sie, dass die richtigen Einheiten ausgewählt sind.
6. Klicken Sie auf **Einheitenzugriff aktualisieren**.

Sie können auch den API-Service SoftLayer_User_Customer::addBulkDedicatedHostAccess verwenden, um einem Benutzer Zugriff auf einzelne oder mehrere dedizierte Hosts zu erteilen. Weitere Informationen finden Sie unter [Mehrfachen dedizierten Hostzugriff hinzufügen ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://softlayer.github.io/reference/services/SoftLayer_User_Customer/addBulkDedicatedHostAccess/){: new_window}.  
{:note}

## Nächste Schritte
Die Benutzerberechtigungen werden nach dem Absenden der Änderungen sofort aktualisiert. Wenn Berechtigungen erteilt wurden, kann der Benutzer die ausgewählten Funktionen anzeigen und aufrufen. Wenn Berechtigungen widerrufen wurden, kann der betreffende Benutzer die Funkionen nicht mehr anzeigen oder aufrufen. Berechtigungen können jederzeit erneut aktualisiert werden.

