---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Häufig gestellte Fragen: Automatische Skalierung
{: #faqs-auto-scale}

## Unterstützt die automatische Skalierung Bare-Metal-Instanzen mit automatischer Skalierung?
{: faq}

Momentan werden Bare-Metal-Instanzen mit automatischer Skalierung von dem Feature für die automatische Skalierung nicht unterstützt.

## Kann das Feature für die automatische Skalierung zusammen mit Lastausgleichsfunktionen eingesetzt werden?
{: faq}

Ja, das Feature für die automatische Skalierung kann zusammen mit lokalen Lastausgleichsfunktionen eingesetzt werden und verwendet einen Teil der APIs für Lastausgleichsfunktionen. Weitere Informationen hierzu finden Sie im Abschnitt zur [Skalierung von Lastausgleichsfunktionen](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Welche Beendigungsrichtlinien für das Feature für die automatische Skalierung stehen zur Verfügung?
{: faq}

Es gibt drei Beendigungsrichtlinien für das Feature für die automatische Skalierung: 'Neuestes Datum', 'Ältestes Datum' und 'Nächste Belastung'. Diese Richtlinien beschreiben, wie in der Gruppe ausgewählt wird, welches Mitglied bei einem Scale-down entfernt werden soll. Weitere Informationen hierzu finden Sie im Abschnitt zur [Beendigungsrichtlinie](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Was sind Richtlinien für die automatische Skalierung?
{: faq}

Eine Richtlinie enthält eine Reihe von Aktionen und eine Gruppe von Auslösern. Richtlinien setzen sich in der Regel aus diesen Elementen zusammen: Name, Übergangszeitraum, Aktion und Auslöser. Weitere Informationen finden Sie im Abschnitt zu den [Richtlinien](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Was sind Auslöser für die automatische Skalierung?
{: faq}

Auslöser sind Bedingungen, die erfüllt werden können (nur bei aktiven Gruppen). Die folgenden drei Auslösertypen stehen zur Verfügung: 'Einmalig', 'Wiederholt' und 'Ressourcenverwendung'. Weitere Informationen finden Sie im Abschnitt zu den [Auslösern](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Was ist die maximale Anzahl der VSI-Mitglieder?
{: faq}

Dieser Wert gibt an, wie viele Mitglieder eine Gruppe maximal enthalten darf. Weitere Informationen hierzu finden Sie im Abschnitt zur [maximalen Anzahl der VSI-Mitglieder](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Was ist die Mindestanzahl der VSI-Mitglieder?
{: faq}

Dieser Wert gibt an, wie viele Mitglieder eine Gruppe mindestens enthalten muss. Weitere Informationen hierzu finden Sie im Abschnitt zur [Mindestanzahl der VSI-Mitglieder](/docs/vsi?topic=virtual-servers-auto-scale-terminology).

## Was ist ein Asset für die automatische Skalierung?
{: faq}

Bei einem Asset handelt es sich um ein festes Mitglied einer Gruppe, das bei der Anzahl der Mitglieder nicht berücksichtigt wird und nicht automatisch kontrolliert wird. Das Asset ist vorhanden, um zusätzliche Informationen für die Richtlinienauslöser bereitzustellen. Ein Asset kann beispielsweise in den CPU-Prozentsatz der gesamten Gruppe einfließen, wenn der CPU-Prozentsatz als Auslöser verwendet wird. Derzeit kann eine Gruppe nur über virtuelle Gastassets verfügen, deren Anzahl nicht begrenzt ist. Darüber hinaus ist keine Gruppe erforderlich.

## Was ist eine Gruppe für die automatische Skalierung?
{: faq}

Eine Gruppe (Skalierungsgruppe) ist eine gruppenspezifische Zusammenstellung von Assets, Mitgliedern, Lastausgleichsfunktionen für die Skalierung, VLANs und Richtlinien. Eine Gruppe umfasst alle Parameter für die Skalierung einschließlich der Grenzwerte für die Mitgliederanzahl sowie die Mitgliedervorlagen für die skalierten virtuellen Serverinstanzen.

## Was ist ein Mitglied für die automatische Skalierung?
{: faq}

Ein Mitglied ist eine skalierte Einheit in einer Gruppe. Mitglieder werden auf Basis von Richtlinienaktionen automatisch bereitgestellt oder freigegeben. Momentan handelt es sich bei allen Mitgliedern um virtuelle Serverinstanzen. In einer aktiven Gruppe ist niemals eine Anzahl von Mitgliedern enthalten, die den Mindestwert unterschreitet bzw. den Maximalwert übersteigt. Obwohl Mitglieder normalerweise mithilfe der Aktionen einer Richtlinie hinzugefügt werden, können sie auch manuell von einem Benutzer hinzugefügt werden.
