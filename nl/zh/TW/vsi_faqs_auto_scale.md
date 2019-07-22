---

copyright:
  years: 2014, 2019
lastupdated: "2019-05-13"

keywords:

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 常見問題：自動調整
{: #faqs-auto-scale}

## 自動調整是否支援「裸機自動調整」實例？
{: faq}

目前，自動調整不支援「裸機自動調整」實例。

## 自動調整是否適用於負載平衡器？
{: faq}

是，自動調整目前可用於本端負載平衡器，並使用一部分的負載平衡器 API。如需相關資訊，請參閱[調整負載平衡器](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 有哪些不同的自動調整終止原則？
{: faq}

有三種自動調整終止原則：最新、最舊，以及最接近下次收費。這些說明當縮減時，群組如何選擇要刪掉的成員。如需相關資訊，請參閱[終止原則](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 何謂自動調整原則？
{: faq}

原則會保留一組動作及一組觸發程式。原則通常包含下列元素：名稱、緩和、動作及觸發程式。如需相關資訊，請參閱[原則](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 何謂自動調整觸發程式？
{: faq}

觸發程式是可以滿足的條件（僅當群組為作用中時）。觸發程式有三種類型：一次性、重複及資源用量。如需相關資訊，請參閱[觸發程式](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 何謂「VSI 成員計數上限」？
{: faq}

它是群組容許存在的最多成員。如需相關資訊，請參閱 [VSI 成員計數上限](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 何謂「VSI 成員計數下限」？
{: faq}

它是群組容許存在的最少成員。如需相關資訊，請參閱 [VSI 成員計數下限](/docs/vsi?topic=virtual-servers-auto-scale-terminology)。

## 何謂自動調整資產？
{: faq}

資產是群組中無助於成員計數且未以任何方式自動控制的固定成員。資產的存在旨在提供其他資訊給原則觸發程式。比方說，如果使用 CPU 百分比作為觸發程式，則資產有助於整個群組 CPU 百分比。目前，群組只能具有虛擬來賓資產，且其數量沒有限制。此外，不需要群組。

## 何謂自動調整群組？
{: faq}

群組（調整群組）是資產、成員、調整負載平衡器、VLAN 及原則的群組特定集合。群組具有所有調整參數，包括成員計數界限，以及已調整的虛擬伺服器實例成員範本。

## 何謂自動調整成員？
{: faq}

成員是群組中的調整單位。根據原則動作，將會自動佈建或收回成員。目前，所有成員都是虛擬伺服器實例。在作用中的群組上，成員數目絕不少於下限或超過上限。雖然原則的動作通常會新增成員，但是使用者也可以手動新增成員。
