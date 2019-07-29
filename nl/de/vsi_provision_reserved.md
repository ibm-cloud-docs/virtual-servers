---

copyright:
  years: 2018
lastupdated: "2018-10-05"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Reservierte Kapazität und Instanzen bereitstellen
{: #provisioning-reserved-capacity-and-instances}

## Vorbereitungen

Reservierte Kapazität und Instanzen können Sie über den {{site.data.keyword.cloud}}-Katalog bereitstellen. Die von Ihnen reservierte Kapazität müssen Sie vor den virtuellen Serverinstanzen bereitstellen.

**Anmerkung**: Wenn Sie kein Kontoadministrator sind, muss Ihr Benutzerkonto über die Berechtigung zum Verwalten reservierter Kapazität verfügen****. Die Berechtigung eines Benutzers kann vom Kontoadministrator über die Registerkarte **Portalberechtigungen** in der Konsole festgelegt werden. Weitere Informationen zum Aktualisieren von Berechtigungen finden Sie in [Infrastrukturzugriff verwalten](/docs/iam?topic=iam-mngclassicinfra).

## Beim IBM Cloud-Katalog anmelden

Führen Sie die folgenden Schritte aus, um sich beim {{site.data.keyword.cloud_notm}}-Katalog anzumelden und mit dem Bereitstellen der von Ihnen reservierten Kapazität und Instanzen zu beginnen.

  1. Melden Sie sich beim [{{site.data.keyword.cloud_notm}}-Katalog ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/){: new_window} mit Ihren eindeutigen Berechtigungsnachweisen an.

## Reservierte Kapazität bereitstellen

Führen Sie im {{site.data.keyword.cloud_notm}}-Katalog die folgenden Schritte aus, um die von Ihnen reservierte Kapazität bereitzustellen.

  1. Klicken Sie im Bereich für die Datenverarbeitungsinfrastruktur**** auf die Kachel **Virtuelle Server**.
  2. Wählen Sie die Option **Reservierter virtueller Server** aus.
  3. Klicken Sie auf **Erstellen**.
  4. Erstellen Sie neue reservierte Kapazität, indem Sie **Zusätzliche neue Kapazität** auswählen. Geben Sie auf der Seite **Reservierte Kapazität** die folgenden Informationen ein bzw. wählen Sie die entsprechenden Optionen aus:

| Feld                   | Wert               |                                                                                                                                                                                                                                                                                                                                 
| ----------------------- | ------------------- |
| Name                    | Sie müssen einen Namen für die von Ihnen reservierte Kapazität eingeben. |                                                                                                                                                                                                                                                                                                       
| Virtuelle Serverkapazität | Wählen Sie die Anzahl der Instanzen aus, die der reservierten Kapazität zugeordnet werden sollen (max. 20 Instanzen) |                                                                                                                                                                                                                                                
| Standort                | Wählen Sie den Standort aus, der für Ihre Workloads erforderlich ist. Standorte umfassen Regionen. Jede Region stellt einen separaten geografischen Bereich dar. **Anmerkung:** Sie können nicht für jede einzelne virtuelle Serverinstanz, die Sie im Rahmen dieser reservierten Kapazität bereitstellen, einen anderen Standort auswählen. Mit Ihrer Auswahl legen Sie den Standort für alle virtuellen Serverinstanzen fest, die Sie im Rahmen dieser reservierten Kapazität bereitstellen. |
| POD                     | Wählen Sie den passenden POD zu Ihrem Standort aus. |
| Laufzeiten des Plans              | Entscheiden Sie sich für eine 1- oder 3-jährige Laufzeit. |                                                                                                                                                                                                                                                                                            
| Profil                 | Wählen Sie eines der gängigen Profile oder alle verfügbaren vCPU-RAM-Kombinationen von SAN-gestütztem Speicher aus ('Ausgewogen' (balanced), 'Hauptspeicher' (memory) oder 'Datenverarbeitung' (compute)). **Anmerkung:** Es ist weder eine Kombination von unterschiedlichen Profilgrößen innerhalb der zu dieser Kapazität zugeordneten Gruppe virtueller Serverinstanzen noch eine nachträgliche Änderung möglich. Die Gruppe der von Ihnen reservierten virtuellen Serverinstanzen muss dieselbe Größe aufweisen. |
{: caption="Tabelle 1. Optionen für die Bereitstellung reservierter Kapazität" caption-side="top"}


## Reservierte Instanzen bereitstellen

Nach dem Bereitstellen der reservierten Kapazität können Sie nun die reservierten virtuellen Serverinstanzen bereitstellen. Reservierte virtuelle Serverinstanzen können zu einem beliebigen Zeitpunkt während der Vertragslaufzeit bereitgestellt werden, da Ihnen die betreffende Kapazität garantiert wird. Führen Sie die folgenden Schritte aus, um Ihre reservierten Instanzen bereitzustellen:

1. Wählen Sie im {{site.data.keyword.cloud_notm}}-Katalog die Kachel **Virtuelle Server** im Bereich für die Datenverarbeitungsinfrastruktur**** aus.
2. Wählen Sie die Option **Reservierter virtueller Server** aus.
3. Klicken Sie auf **Erstellen**.
4. Geben Sie zum Bereitstellen einer reservierten virtuellen Serverinstanz die folgenden Informationen ein bzw. wählen Sie die entsprechenden Optionen aus:

| Feld                     | Wert               |                                                                                                                                                                                                                                                                                                                                 
| ------------------------- | ------------------- |
| Name                      | Sie müssen einen Namen für die von Ihnen reservierten virtuellen Serverinstanzen eingeben. |                                                                                                                                                                                                                                                                                                       
| Abrechnung                   | Wählen Sie eine Abrechnung auf Stunden- oder Monatsbasis aus. |                                                                                                                                                                                                                                                
| Reservierte Kapazität         | Wählen Sie die von Ihnen reservierte Kapazität oder - zum Bereitstellen zusätzlicher reservierter Kapazität - die Option **Zusätzliche neue Kapazität** aus. |                                                                                                                                                                                                     
| Add-ons                   | Wählen Sie bei Bedarf zusätzliche Speicher-, Netzwerk- oder Softwareoptionen aus. |                                                                                                                                                                                                                                                                                            
{: caption="Tabelle 1. Optionen für die Bereitstellung reservierter Kapazität" caption-side="top"}

## Nächste Schritte

Nachdem Ihr virtueller Server bereitgestellt wurde und einsatzbereit ist, können Sie Ihre virtuellen Server über die
{{site.data.keyword.cloud_notm}}-Konsole oder über die {{site.data.keyword.slapi_short}} konfigurieren. Weitere Informationen finden Sie unter [Virtuelle Server konfigurieren](/docs/vsi?topic=virtual-servers-configuring-virtual-servers#configuring-virtual-servers).

Bei Fragen zur reservierten Kapazität und zu reservierten Instanzen ziehen Sie den Abschnitt [Häufig gestellte Fragen (FAQs): Reservierte Kapazität und Instanzen](/docs/vsi?topic=virtual-servers-faqs-reserved-capacity-and-instances#faqs-reserved-capacity-and-instances) zurate. 
