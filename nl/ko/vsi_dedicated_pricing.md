---

copyright:
  years: 2017, 2019
lastupdated: "2019-05-22"

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 전용 호스트 가격
{: #dedicated-virtual-server-pricing}

전용 호스트에 대한 가격은 시간별 및 월별 모델로 제공됩니다.
{:shortdesc}

인스턴스가 전용 호스트에 프로비저닝되므로 전용 호스트 가격은 모든 vCPU, RAM, 로컬 스토리지 및 업링크 포트 속도 컴포넌트를 포함합니다. 가격에 대한 자세한 정보는 [가상 서버 프로비저닝 계산기 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/cloud-computing/bluemix/virtual-servers/calculator){: new_window}를 참조하십시오.

전용 호스트를 사용하는 경우에는 첫 번째, 두 번째, 세 번째, 네 번째 및 다섯 번째 디스크에서 추가 로컬 스토리지 디스크를 사용할 수 있습니다. 또한 각 보조 디스크에는 400GB의 추가 용량이 있습니다.

시간별 인스턴스는 시간별 및 월별 호스트에 프로비저닝될 수 있습니다. 월별 인스턴스는 월별 호스트에만 프로비저닝될 수 있습니다.

|호스트 구성 |vCPU	|RAM(GB) |로컬 스토리지(TB SSD) |
| ------------------ | ---- | -------- | ---------------------- |
| 56x242x1.2  	     |56 	|242    |        	1.2	          |
| 56x484x1.2         |56  |   484    |          1.2           |
{: caption="표 1. 전용 호스트 구성" caption-side="top"}

가격은 지역에 따라 다릅니다.
{:note}

SAN(네트워크 연결된), 프리미엄 OS 및 SW 추가 기능은 전용 호스트에 프로비저닝된 인스턴스에 따라 각 인스턴스마다 시간별 또는 월별로 비용이 청구됩니다. 각 컴포넌트에 대한 가격은 공용 인스턴스 및 전용 인스턴스에 대한 기존 오퍼링과 동일합니다. 

예를 들어, 다음 구성을 갖춘 전용 호스트에 프로비저닝된 전용 인스턴스는 인스턴스별로 비용 청구되지 않습니다. vCPU, RAM, 로컬 스토리지 및 업링크 포트 속도는 전용 호스트 비용에 포함되어 있습니다. 

* 8개 vCPU
* 16GB RAM
* 100GB 로컬 SSD(첫 번째 디스크)
* 400GB 로컬 SSD(두 번째 디스크)
* 400GB 로컬 SSD(세 번째 디스크)
* 1Gbps 공용 및 사설 네트워크 업링크(전용 호스트) 

