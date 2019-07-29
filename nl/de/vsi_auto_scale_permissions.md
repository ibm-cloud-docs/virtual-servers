---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-14"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Benutzerberechtigungen für automatische Skalierung einrichten
{: #user-permissions-required-to-use-auto-scale}

Für den Zugriff auf die Optionen zur automatischen Skalierung sind spezielle Benutzerberechtigungen erforderlich, die über die Funktionalität zum Bestellen und Verwalten von {{site.data.keyword.virtualmachinesshort}} hinausgehen. Um auf die Features für die automatische Skalierung zuzugreifen, müssen Sie über die Berechtigung zum Verwalten aller virtuellen Server für das Konto sowie zum Verwalten aller in der Zukunft hinzugefügten virtuellen Einheiten verfügen.

Führen Sie die folgenden Schritte aus, wenn Sie der Kontoadministrator sind und Benutzern die Berechtigung zum Zugriff auf die Optionen für die automatische Skalierung erteilen möchten:

1. Melden Sie sich auf der Seite für [Access (IAM) ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/iam#/users){: new_window} in der {{site.data.keyword.cloud}}-Konsole an. 
2. Wählen Sie auf der Registerkarte **Benutzer** die Option **Anzeigen nach: Benutzer der klassischen Infrastruktur** aus.
3. Wählen Sie einen Benutzer aus und klicken Sie dann auf die Registerkarte **Klassische Infrastruktur**.
4. Erweitern Sie die Ansicht der Kategorie **Einheiten** auf der Registerkarte **Berechtigungen** und wählen Sie dann **Gruppen für automatische Skalierung verwalten** aus.
5. Klicken Sie auf **Anwenden**.

## Nächste Schritte

Nachdem Sie nun über die Berechtigung für den Zugriff und die Verwendung der Optionen für die automatische Skalierung verfügen, sind Sie bereit, diese Funktion zu verwenden. Lesen Sie zunächst die folgenden Informationen:

1. [Datenverkehrsspitzen mit der zeitplanbasierten automatischen Skalierung verwalten](/docs/vsi?topic=virtual-servers-managing-schedule-based-auto-scaling)
2. [Datenverkehrsspitzen mit der ressourcenbasierten automatischen Skalierung verwalten](/docs/vsi?topic=virtual-servers-managing-resourced-based-auto-scaling)
3. [Häufig gestellte Fragen: Automatische Skalierung](/docs/vsi?topic=virtual-servers-faqs-auto-scale)

