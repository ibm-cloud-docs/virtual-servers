---

copyright:
  years: 2018, 2019
lastupdated: "2019-05-31"

keywords: apps, deploy, virtual server, App Service, vsi, virtual machine, delivery pipeline, virtual deployment

subcollection: virtual-servers

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:table: .aria-labeledby="caption"}

# Bereitstellung auf virtuellem Server durchführen
{: #deploying-to-a-virtual-server}

Wenn Sie über ein nutzungsabhängiges Konto (Pay-As-You-Go Account) verfügen, dann können Sie den [App-Service](https://{DomainName}/developer/appservice/starter-kits){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") von {{site.data.keyword.cloud}} verwenden, um Ihre Apps in verschiedenen Umgebungstypen einschließlich virtuellen Serverinstanzen bereitzustellen. Eine virtuelle Serverinstanz emuliert eine Bare-Metal-Maschine und stellt eine häufig verwendete Bereitstellungsoption dar, wenn lokale Workloads in die Cloud verschoben werden.
{: shortdesc}

Eine virtuelle Serverinstanz bietet im Vergleich zu anderen Konfigurationen eine verbesserte Transparenz, Voraussagbarkeit und Automatisierung für alle Workloadtypen. Kombinieren Sie sie mit einem Bare Metal Server-System, um eindeutige Workloadkombinationen zu erstellen. Sie können beispielsweise eine leistungsfähige Datenbanklogik oder Systeme für maschinelles Lernen mit Bare-Metal- und GPU-Konfigurationen erstellen, die unter einem Debian Linux-basierten Betriebssystem ausgeführt werden. 

Die Bereitstellung einer virtuellen Serverinstanz kann ein komplexer und zeitaufwendiger Prozess sein, den Sie jedoch mithilfe des {{site.data.keyword.cloud_notm}} App Service schnell und einfach ausführen können.

Services werden nicht an die virtuelle Serverinstanz gebunden. Sie können keine Services zu einer Anwendung in einem virtuellen Server hinzufügen. Allerdings ist es weiterhin möglich, einen {{site.data.keyword.cloud_notm}}-Service in einer Anwendung zu nutzen, die in einem virtuellen Server ausgeführt wird, wenn Sie die Berechtigungsnachweise für die App verfügbar machen, die in der virtuellen Serverinstanz ausgeführt wird.
{: important}

## Apps bereitstellen
{: #create-deploy-vsi}

Der App-Service stellt eine virtuelle Serverinstanz für Sie bereit, lädt ein Image, das Ihre App umfasst, erstellt eine Devops-Toolchain und leitet den ersten Bereitstellungszyklus für Sie ein.

1. [Erstellen Sie eine App](/docs/apps?topic=creating-apps-tutorial-scratch#tutorial-scratch). 
2. Klicken Sie auf der Seite mit den Appdetails auf **Continuous Delivery konfigurieren**.
3. Wählen Sie **Virtuellen Server bereitstellen** und außerdem die Region aus, in der Ihr Server ausgeführt werden soll.

## Funktionsweise des Bereitstellungsprozesses

Der Prozess zur Bereitstellung eines virtuellen Servers basiert auf verschiedenen Schlüsseltechnologien, zu denen Terraform, die Pipelineaktivierung, das API-Schlüsselmanagement (Git-Operationen) sowie Kenntnisse des Toolchain-Prozesses gehören. 

### Über Terraform bereitstellen

In einer dynamisch erstellten virtuellen Instanz können alle App-Service-Starter-Kits über [Terraform](https://ibm-cloud.github.io/tf-ibm-docs/v0.10.0/){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") bereitgestellt werden. Hierbei handelt es sich um eine Open-Source-Infrastruktur, die als Code-Framework genutzt wird. 

### Pipelinebereitstellung aktivieren

Wenn Sie ein Starter-Kit erstellen, das mit dem {{site.data.keyword.cloud_notm}} [App-Service](https://{DomainName}/developer/appservice/starter-kits){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") arbeitet, dann wird die virtuelle Serverinstanz aktiviert. Nach Erstellung der App können Sie auswählen, wo die App bereitgestellt werden soll. Die Starter-Kits werden aktiviert, um die Bereitstellung mithilfe einer Continuous-Delivery-Toolchain zu unterstützen. Starter-Kits können als Ziel Kubernetes, Cloud Foundry und Virtual Server-Instanzen verwenden. Die Toolchain umfasst ein Quellcode-Repository und eine Bereitstellungspipeline.

Die Option für virtuelle Server verfügt über mehrere Phasen. Zuerst wird der App-Code vorbereitet und in einem GitLab-Git-Repository gespeichert und der Quellcode wird zur Erstellung einer Toolchain mit einer Pipeline benutzt. Die Pipeline wird definiert, um den Code zu erstellen und ihn in einem Debian-Paketmanagerformat zu packen. Anschließend stellt Terraform eine virtuelle Instanz bereit. Abschließend wird die App bereitgestellt, installiert und in dem aktiven virtuellen Image gestartet. Ihr Zustand wird anschließend geprüft.

Die Pipeline verwendet eine Gruppe von Benutzerkonteneigenschaften und ein neues SSH-Schlüsselpaar, um die Bereitstellung in der Infrastruktur durchzuführen. Diese Eigenschaften werden automatisch an die Toolchain übergeben, jedoch aus Sicherheitsgründen nicht im Git-Quellcode gespeichert.

Führen Sie die folgenden Schritte aus, um diese Umgebungseigenschaften anzuzeigen. 

1. Klicken Sie auf der Detailseite der App auf **Toolchain anzeigen**.
2. Klicken Sie auf die Kachel **Bereitstellungspipeline**.
3. Klicken Sie auf das Symbol zum **Konfigurieren der Stage** und dann für die Build-Stage auf **Stage konfigurieren**.
4. Klicken Sie auf die Registerkarte **Umgebungseigenschaften**, um die Eigenschaften anzuzeigen. In der folgende Tabelle finden Sie Informationen zu den verfügbaren Eigenschaften.

| Eigenschaft  | Beschreibung  |
|-----------|--------------|
| `TF_VAR_ibm_sl_api_key` | Der [API-Schlüssel der Infrastruktur](/docs/apps?topic=creating-apps-vsi-deploy#iaas-key) stammt aus der Konsole für die klassische Infrastruktur. |
| `TF_VAR_ibm_sl_username` | Der [Benutzername der Infrastruktur](/docs/apps?topic=creating-apps-vsi-deploy#user-key), mit dem das Konto für die klassische Infrastruktur angegeben wird |
| `TF_VAR_ibm_cloud_api_key` | Der {{site.data.keyword.cloud_notm}} [API-Schlüssel](/docs/apps?topic=creating-apps-vsi-deploy#platform-key) wird zur Aktivierung der Serviceerstellung verwendet. |
| `PUBLIC_KEY` | Der [öffentliche Schlüssel](/docs/apps?topic=creating-apps-vsi-deploy#public-key), der zum Aktivieren des Zugriffs auf die virtuelle Serverinstanz definiert wird. |
| `PRIVATE_KEY` | Der [private Schlüssel](/docs/apps?topic=creating-apps-vsi-deploy#public-key), der zum Aktivieren des Zugriffs auf die virtuelle Serverinstanz definiert wird. Sie müssen die Formatierung mit dem Zeilenvorschubzeichen `\n` verwenden. |
| `VI_INSTANCE_NAME` | Der automatisch generierte Name für die virtuelle Serverinstanz. |
| `GIT_USER` | Wenn Sie den [Terraform-Status](/docs/apps?topic=creating-apps-vsi-deploy#tform-state) zum Speichern des Status des Befehls 'apply' festlegen, dann wird der GitLab-Benutzername benötigt. |
| `GIT_PASSWORD` | Wenn Sie den [Terraform-Status](/docs/apps?topic=creating-apps-vsi-deploy#tform-state) zum Speichern des Status des Befehls 'apply' festlegen, dann wird das GitLab-Kennwort benötigt. |
{: caption="Tabelle 1. Zur Aktivierung zu ändernde Umgebungsvariablen" caption-side="top"}


#### API-Schlüssel für klassische Infrastruktur
{: #iaas-key}

Für Terraform ist ein API-Schlüssel für die klassische Infrastruktur erforderlich, um Infrastrukturressourcen erstellen zu können. Der API-Schlüssel wird während der Bereitstellung automatisch abgerufen. Führen Sie die folgenden Schritte aus, um einen Schlüssel manuell abzurufen.

1. Rufen Sie die [Benutzerliste](https://{DomainName}/iam#/users){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") auf. Sie können auch auf **Verwalten** > **Zugriff (IAM)** klicken und dann **Benutzer** auswählen.
2. Klicken Sie auf einen Benutzernamen und dann auf **Benutzerdetails**.
3. Klicken Sie im Abschnitt für die API-Schlüssel auf **Schlüssel für klassische Infrastruktur hinzufügen**.
4. Kopieren Sie den API-Schlüssel `TF_VAR_ibm_sl_api_key` oder laden Sie ihn herunter und speichern Sie ihn an einem sicheren Ort. Sie können die Details des API-Schlüssels später mithilfe der Option **Details anzeigen** im Menü **Aktionen** ![Symbol für Aktionsliste](../icons/action-menu-icon.svg) abrufen.
5. Fügen Sie den kopierten Wert für den API-Schlüssel in die Toolchain-Konfiguration ein, um `TF_VAR_ibm_sl_api_key` zu ersetzen.

Weitere Informationen hierzu finden Sie in den Abschnitten zum [Verwalten von API-Schlüsseln für die klassische Infrastruktur](/docs/iam?topic=iam-classic_keys#classic_keys) und zu den [Berechtigungen für die klassische Infrastruktur](/docs/iam?topic=iam-infrapermission#infrapermission).

#### Benutzername für klassische Infrastruktur
{: #user-key}

Der Benutzername für die klassische Infrastruktur wird ebenfalls automatisch abgerufen und während der Bereitstellung verwendet. Führen Sie die folgenden Schritte aus, um den Benutzernamen manuell abzurufen.

1. Rufen Sie [Benutzerliste](https://{DomainName}/iam#/users){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") auf. Sie können auch auf **Verwalten** > **Zugriff (IAM)** klicken und dann **Benutzer** auswählen.
2. Klicken Sie auf einen Benutzernamen und dann auf **Benutzerdetails**.
3. Suchen Sie die Eigenschaft **VPN-Benutzername**.
4. Schneiden Sie diesen Wert aus und fügen Sie ihn ein, um die Toolchain-Konfiguration `TF_VAR_ibm_sl_username` zu ersetzen.

#### {{site.data.keyword.cloud_notm}}-API-Schlüssel
{: #platform-key}

Um in Terraform Services auf Plattformebene (z. B. Datenbanken und Compose-Services) zu erstellen, wird der {{site.data.keyword.cloud_notm}}-API-Schlüssel automatisch abgerufen und als Umgebungsvariable in Ihrer Pipeline gespeichert. Führen Sie die folgenden Schritte aus, um einen {{site.data.keyword.cloud_notm}}-API-Schlüssel manuell abzurufen.

1. Rufen Sie [Benutzerliste](https://{DomainName}/iam#/users){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") auf. Sie können auch auf **Verwalten** > **Zugriff (IAM)** klicken und dann **Benutzer** auswählen.
2. Klicken Sie auf einen Benutzernamen und dann auf **Benutzerdetails**.
3. Suchen Sie den Abschnitt für die API-Schlüssel und klicken Sie dann auf **IBM Cloud-API-Schlüssel erstellen**.
4. Geben Sie einen Namen und eine Beschreibung ein und klicken Sie dann auf **Erstellen**.
5. Wenn das Fenster geöffnet wird, klicken Sie auf **Anzeigen**, um den Schlüssel zu überprüfen.
6. Kopieren Sie den Schlüssel und fügen Sie ihn in die Zwischenablage ein oder laden Sie den Schlüssel herunter.
7. Ersetzen Sie den Wert in der Toolchain-Konfiguration `TF_VAR_ibm_cloud_api_key` durch den Wert, der generiert wurde.

#### Öffentliche und private Schlüssel
{: #public-key}

Damit die Toolchain die Debian-Paketierung in der virtuellen Serverinstanz installieren kann, generiert die Bereitstellungsinfrastruktur automatisch ein Paar aus einem privaten und einem öffentlichen SSH-Schlüssel, um die Git-Inhalte an die Instanz zu übertragen.

Gehen Sie wie folgt vor, um diesen Schritt manuell auszuführen:
1. Verwenden Sie in Ihrem Client die folgenden Anweisungen, um ein [Paar aus einem öffentlichen und einem privaten Schlüssel](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") zu erstellen.
2. Rufen Sie die [Ansicht für die SSH-Schlüssel der Infrastruktur](https://{DomainName}/iam/#/users){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") auf. Sie können auch auf **Menü** > **Klassische Infrastruktur** > **Einheiten** > **Verwalten** > **SSH-Schlüssel** klicken.
3. Klicken Sie auf **Hinzufügen**.
4. Kopieren Sie die Inhalte des öffentlichen Schlüssels, den Sie zuvor erstellt haben, und fügen Sie sie in die Schlüsselinhalte ein.
5. Ordnen Sie dem Schlüssel einen Namen zu und klicken Sie dann auf **Hinzufügen**.

Der private Schlüssel muss in einer einzigen Zeile angegeben werden. Ersetzen Sie die Angaben für neue Zeilen durch `\n`. Beispiel:
{: tip}

```
---------BEGIN RSA KEY----------\nasdfasdfeqwtqf13rf1eqwfwe\netq3efaewf23fa23f23f\n.....\n----------END RSA KEY-------------
```
{: screen}

#### Terraform-Status aktivieren
{: #tform-state}

Terraform unterstützt die Speicherung des Status für den Terraform-Befehl `apply`. Diese Statusdatei führt den Befehl `apply` ein zweites Mal aus, um festzustellen, ob eine der Terraform-Konfigurationsdateien geändert wurde. Der Status wird im Git-Repository gespeichert, in dem die App und die Konfiguration automatisch eingerichtet werden.

Um den Statusspeicher zu aktivieren, werden `GIT_USER` und `GIT_PASSWORD` automatisch als Eigenschaften in den Toolchain-Umgebungsvariablen konfiguriert. Führen Sie die folgenden Schritte aus, um auf diese Werte zuzugreifen:

1. Greifen Sie in der Toolchains-Ansicht auf das Git-Repository des Code-Tools zu.
2. Klicken Sie in GIT Lab auf das **Profilsymbol** und dann auf **Einstellungen**.
3. Klicken Sie auf **Konto** und kopieren Sie den Benutzernamen und ersetzen Sie den Wert für `GIT_USER`.
4. Klicken Sie auf **Zugriffstokens**.
5. Definieren Sie einen Namen für Ihr Token, wählen Sie einen Bereich aus und klicken Sie dann auf **Persönliches Zugriffstoken erstellen**.
6. Klicken Sie im Feld `Neues persönliches Zugriffstoken` auf **Kopieren** und ersetzen Sie den Wert von `GIT_PASSWORD` in den Toolchain-Eigenschaften.

Der Terraform-Status wird in einem Zweig namens `terraform` gespeichert und löst die Pipeline-Ausführung nicht aus, wenn eine Änderung durchgeführt wurde.

### Git-Operationen aktivieren
{: #git-repo-vsi}

Wenn die App in {{site.data.keyword.cloud_notm}} bereitgestellt wird, wird ein GitLab-Repository erstellt, um den Code für die Quellcodeverwaltung zu hosten. Mithilfe von Git-Operationen können Sie es Teams ermöglichen, mit Ihrer App zu arbeiten und Änderungen an Ihre App zu übergeben. Im Folgenden finden Sie die Ordner in diesem Repository und eine Beschreibung zu deren Inhalt.

#### Ordner 'debian'
{: #debian-folder}

Im Ordner `debian` wird die Konfiguration gespeichert, die zum Aktivieren der Paketierung der App in einem [Debian-Paket](https://www.debian.org/doc/manuals/debian-faq/ch-pkgtools.en.html){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") erforderlich ist.

#### Ordner 'terraform'
{: #terraform-folder}

Im Ordner `terraform` wird die Konfiguration für die Infrastruktur als Code gespeichert, der zur Bereitstellung von Infrastrukturressourcen verwendet werden kann. Die Datei `main.tf` ist die Hauptquelle für die Änderung der Optionen für Ihre Terraform-Konfiguration.

```json
resource "ibm_compute_vm_instance" "vm1" {
    hostname = "${var.vi_instance_name}"
    domain = "example.com"
    os_reference_code = "DEBIAN_8_64"
    datacenter = "${var.datacenter}"
    network_speed = 100
    hourly_billing = true
    private_network_only = false
    cores = 1
    memory = 1024
    disks = [25]
    local_disk = false
    ssh_key_ids = [
        "${ibm_compute_ssh_key.ssh_key_gip.id}"
    ]
}
```

Mit Terraform können Sie auch Bare Metal Server-Systeme bereitstellen. Weitere Informationen hierzu finden Sie in der [Providerdokumentation zu IBM Terraform](https://ibm-cloud.github.io/tf-ibm-docs/v0.10.0/){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") und im [Git-Repository für IBM Terraform-Provider](https://github.com/IBM-Cloud/terraform-provider-ibm){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link").

Die Datei `variables.tf` kann zum Ändern des Rechenzentrums benutzt werden, das als Ziel für die Erstellung der virtuellen Instanz verwendet werden soll. Informationen zum Anzeigen der Liste der definierten Rechenzentren auf der Plattform finden Sie unter [Rechenzentren](https://www.ibm.com/cloud/data-centers/){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link").

Standardmäßig ist die Terraform-Datei für Washington und `wdc04` konfiguriert.
```json
variable "datacenter" {
  description = "Washington"
  default = "wdc04"
}
```

### Informationen zu Toolchain-Stages
{: #toolchain-stages-vsi}

Die Toolchain zeigt die Infrastruktur und die Appbereitstellung in einer einfachen Pipeline an. Unterteilen Sie die Infrastruktur in eine Pipeline für die Codekomponente und eine Pipeline für die Appbereitstellung.

Der Toolchain-Prozess verfügt über fünf Stages.

1. In der Build-Stage wird das Git-Repository geklont und der Code wird in einem Debian-Paket paketiert.
2. In der Terraform-Planungsstage wird ein Terraform-Plan vorbereitet.
  ```console
  terraform init -input=false
  terraform validate
  terraform plan -var "ssh_public_key=$PUBLIC_KEY" -input=false -out tfplan
  ```

3. In der Terraform-Anwendungsstage wird die Terraform-Konfiguration angewendet und es wird gewartet, bis die IP-Adresse des virtuellen Servers verfügbar ist.

  ```console
  terraform apply -auto-approve -input=false tfplan
  terraform output "host ip" > hostip.txt
  ```

4. In der Stage für Bereitstellen, Installieren und Starten wird das in der ersten Stage erstellte Debian-Paket in den aktiven virtuellen Server verschoben und dort installiert und anschließend gestartet.
5. In der Stage für die Statusprüfung (Health Check) wird überprüft, ob der Statusendpunkt in der App zur Verfügung steht. Anschließend wird die Pipeline ausgeführt.

In den Protokollen der Stage für die Statusprüfung finden Sie Informationen dazu, wie auf die App nach ihrem Start zugegriffen werden kann. Klicken Sie auf die in den Protokollen aufgeführten URL-Links mit der IP-Adresse und dem Port der App.
