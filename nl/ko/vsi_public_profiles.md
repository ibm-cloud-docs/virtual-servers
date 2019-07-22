---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-14"

keywords: public virtual servers, network traffic, virtual server deployment, profile

subcollection: virtual-servers

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tips: .tips}
{:note: .note}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 프로파일
{: #about-virtual-server-profiles}

{{site.data.keyword.cloud}} 가상 서버 인스턴스를 프로비저닝하는 경우 지원되는 프로파일 제품군에서 선택할 수 있습니다. 프로파일은 가상 서버 인스턴스를 시작하도록 빠르게 인스턴스화될 수 있는 vCPU과 RAM을 결합하여 구성됩니다. {{site.data.keyword.cloud_notm}} 콘솔의 인기 있는 프로파일 구성에서 선택하거나 사용자 요구사항에 가장 적합한 프로파일 목록에서 선택할 수 있습니다.
{:shortdesc}

다음 가상 서버 인스턴스 제품군이 사용 가능합니다.

인스턴스 유형에 따라 일부 제품군이 사용 불가능할 수 있습니다.
{:note}

| 제품군 |설명                                                                                              |
| ----------------------- | -------------------------------------------------------------------------------------------------------- | 
|[밸런스됨](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced) |성능과 확장성 사이에 균형이 잡혀야 하는 일반 클라우드 워크로드에 가장 적합합니다. NAS(Network-Attached Storage)를 사용합니다. |
|[밸런스된 로컬 스토리지](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#balanced-local-storage) | 대기 시간은 매우 짧으며 높은 I/O 성능을 필요로 하는 대형 데이터베이스 워크로드에 적합합니다. |
|[컴퓨팅](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#compute) |중간에서 높은 수준의 웹 트래픽 워크로드에 가장 적합합니다. |
|[메모리](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#memory)  |메모리 캐싱 및 실시간 분석 워크로드에 가장 적합합니다. |
|[GPU](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#gpu)  |고성능 워크로드에 가장 적합합니다. |
{: caption="표 1. 공용 가상 서버 제품군 선택사항" caption-side="top"}

이러한 제품군 중 일부는 IBM Cloud Virtual Servers for VPC에도 사용할 수 있습니다. 자세한 정보는 [IBM Cloud Virtual Servers for Virtual Private Cloud](/docs/vsi-is?topic=virtual-servers-is-gettingstartedvsigen#gettingstartedvsigen)를 참조하십시오.
{:tip}

## 밸런스됨
{: #balanced}

밸런스된 프로파일(NAS(Network-Attached Storage)에 적용)은 성능과 스케일의 밸런스가 필요한 일반 클라우드에 적합합니다. 네트워크 성능의 범위는 표준에서 프리미엄입니다.

이 오퍼링은 다음 프로파일에서 사용 가능합니다.

| 프로파일   | vCPU    |RAM     |스토리지 유형 |
| --------- | ------- | ------- | ------------ |
|B1.1x2    |1       |2GB    |SAN          |
|B1.1x4    |1       |4GB    |SAN          |
|B1.2x4    |2       |4GB    |SAN          |
|B1.2x8    |2       |8GB    |SAN          |
|B1.4x8    |4       |8GB    |SAN          |
|B1.4x16   |4       |16GB   |SAN          |
|B1.8x16   |8       |16GB   |SAN          |
|B1.8x32   |8       |32GB   |SAN          |
|B1.16x32  |16      |32GB   |SAN          |
|B1.16x64  |16      |64GB   |SAN          |
|B1.32x64  |32      |64GB   |SAN          |
|B1.32x128 |32      |128GB  |SAN          |
|B1.48x192 |48      |192GB  |SAN          |
{: caption="표 2. NAS(Network-Attached Storage)의 밸런스됨 프로파일" caption-side="top"}

### 스토리지 참고사항

* 최대 2TB의 추가 디스크가 사용 가능(총 4개 디스크가 허용됨)한 SAN 기본 부트 디스크(25GB 또는 100GB)입니다.
* SAN 스토리지를 사용하는 공용 가상 서버에 대한 가격은 가상 CPU, 메모리 및 최소 기본 부트 디스크를 포함합니다. 추가 디스크 가격은 선택하는 디스크 크기 및 수량에 따라 달라집니다.  

밸런스됨 프로파일(NAS(Network-Attached Storage)에 적용)은 모든 데이터 센터에서 사용 가능합니다.

모든 지원 운영 체제(RHEL, CentOS, Windows, Ubuntu 및 기타), 지원 데이터베이스 및 소프트웨어 추가 기능 또한 이 오퍼링과 함께 사용할 수 있습니다. 

## 밸런스된 로컬 스토리지
{: #balanced-local-storage}

벨런스된 로컬 스토리지 프로파일은 주로 대기 시간은 매우 짧으며 높은 I/O 성능을 필요로 하는 대형 데이터베이스 워크로드에 적합합니다. 네트워크 성능의 범위는 표준에서 프리미엄입니다.

오퍼링은 다음과 같은 로컬 스토리지 옵션과 함께 다양한 프로파일 및 데이터 센터에서 사용 가능합니다.

* [로컬 HDD ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#HDD)
* [로컬 SSD ](/docs/vsi?topic=virtual-servers-about-virtual-server-profiles#SSD)

### 로컬 HDD
{: #HDD}
 
<table>
<CAPTION>표 3. 로컬 HDD를 사용하는 밸런스된 로컬 스토리지 프로파일</CAPTION>
<THEAD>
<TR>
<th>프로파일</th>
<th>vCPU</th>
<th>RAM</th>
<th>2차 디스크<sup>(*)</sup></th>
<th>스토리지 유형</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL1.1x2</td>
<td>1</td>
<td>2GB</td>
<td>25, 100GB</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.1x4</td>
<td>1</td>
<td>4GB</td>
<td>25, 100GB</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.2x4</td>
<td>2</td>
<td>4GB</td>
<td>100, 200GB</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.2x8</td>
<td>2</td>
<td>8GB</td>
<td>100, 200GB</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.4x8</td>
<td>4</td>
<td>8GB</td>
<td>150, 300GB</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.4x16</td>
<td>4</td>
<td>16GB</td>
<td>150, 300GB</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.8x16</td>
<td>8</td>
<td>16GB</td>
<td>250GB, (2 x 250GB)</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.8x32</td>
<td>8</td>
<td>32GB</td>
<td>250GB, (2 x 250GB)</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.16x32</td>
<td>16</td>
<td>32GB</td>
<td>300GB, (2 x 300GB)</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.16x64</td>
<td>16</td>
<td>64GB</td>
<td>300GB, (2 x 300GB)</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.32x64</td>
<td>32</td>
<td>64GB</td>
<td>400GB, (2 x 400GB)</td>
<td>로컬 HDD</td>
</tr>
<tr>
<td>BL1.32x128</td>
<td>32</td>
<td>128GB</td>
<td>400GB, (2 x 400GB)</td>
<td>로컬 HDD</td>
</tr>
</TBODY>
</table>

#### 스토리지 참고사항
* <sup>(*)</sup>밸런스된 로컬 스토리지 프로파일에는 100GB 로컬 스토리지 부트 디스크가 자동으로 제공됩니다. 그런 다음 사용자가 두 번째 디스크를 선택할 수 있습니다(표 3에 표시된 옵션). 모든 추가 로컬 디스크는 선택사항입니다. 500GB 이상을 필요로 하는 경우에는 두 개의 추가 디스크가 필요합니다(예: 2 x 250GB의 로컬 스토리지를 필요로 하는 8개 코어).
*	최대 로컬 스토리지는 코어 수에 따라 제한됩니다. 
*	밸런스된 로컬 스토리지는 글로벌 형식으로 사용 가능합니다. 그러나, 스토리지의 유형(로컬 SSD 또는 로컬 HDD)은 데이터 센터 위치에 따라 다릅니다. 
*	기본 또는 보조 디스크는 분리할 수 없습니다.

다음 데이터 센터는 로컬 HDD가 있는 밸런스된 로컬 스토리지 가상 서버를 지원합니다.

| 사용 가능한 데이터 센터 - 로컬 HDD |       |
| ---------------------- | ----- |
| 댈러스(DAL01)          | 댈러스(DAL05)    |
| 댈러스(DAL06)          | 휴스턴(HOU02)    |
| 시애틀(SEA01)          | 산호세(SJC01)    |
| 워싱턴, DC(WDC01)      |                  |
{: class="simple-tab-table"}
{: caption="표 4. 사용 가능한 데이터 센터(로컬 HDD) - 아메리카" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd1}
{: tab-title="Americas"}

| 사용 가능한 데이터 센터 - 로컬 HDD |
| ---------------------- |
| 암스테르담(AMS01)      |
{: class="simple-tab-table"}
{: caption="표 5. 사용 가능한 데이터 센터(로컬 HDD) - 유럽" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd2}
{: tab-title="Europe"}

| 사용 가능한 데이터 센터 - 로컬 HDD |
| ---------------------- |
| 홍콩(HKG02)      | 
| 싱가포르(SNG01)      |
{: class="simple-tab-table"}
{: caption="표 6. 사용 가능한 데이터 센터(로컬 HDD) - 아시아 태평양" caption-side="top"}
{: tab-group="Local-HDD"}
{: #local-hdd3}
{: tab-title="Asia-Pacific"}

모든 지원 운영 체제(RHEL, CentOS, Windows, Ubuntu 및 기타), 지원 데이터베이스 및 소프트웨어 추가 기능 또한 이 오퍼링과 함께 사용할 수 있습니다.  

### 로컬 SSD 
{: #SSD}

<table>
<CAPTION>표 7. 로컬 SSD를 사용하는 밸런스된 로컬 스토리지 프로파일</CAPTION>
<THEAD>
<TR>
<th>프로파일</th>
<th>vCPU</th>
<th>RAM</th>
<th>2차 디스크<sup>(*)</sup></th>
<th>스토리지 유형</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>BL2.1x2</td>
<td>1</td>
<td>2GB</td>
<td>25, 100GB</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.1x4</td>
<td>1</td>
<td>4GB</td>
<td>25, 100GB</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.2x4</td>
<td>2</td>
<td>4GB</td>
<td>100, 200GB</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.2x8</td>
<td>2</td>
<td>8GB</td>
<td>100, 200GB</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.4x8</td>
<td>4</td>
<td>8GB</td>
<td>150, 300GB</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.4x16</td>
<td>4</td>
<td>16GB</td>
<td>150, 300GB</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.8x16</td>
<td>8</td>
<td>16GB</td>
<td>250GB, (2 x 250GB)</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.8x32</td>
<td>8</td>
<td>32GB</td>
<td>250GB, (2 x 250GB)</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.16x32</td>
<td>16</td>
<td>32GB</td>
<td>300GB, (2 x 300GB)</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.16x64</td>
<td>16</td>
<td>64GB</td>
<td>300GB, (2 x 300GB)</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.32x64</td>
<td>32</td>
<td>64GB</td>
<td>400GB, (2 x 400GB)</td>
<td>로컬 SSD</td>
</tr>
<tr>
<td>BL2.32x128</td>
<td>32</td>
<td>128GB</td>
<td>400GB, (2 x 400GB)</td>
<td>로컬 SSD</td>
</tr>
</TBODY>
</table>

#### 스토리지 참고사항
* <sup>(*)</sup>밸런스된 로컬 스토리지 프로파일에는 100GB 로컬 스토리지 부트 디스크가 자동으로 제공됩니다. 그런 다음 사용자가 두 번째 디스크를 선택할 수 있습니다(위 테이블에 표시된 옵션). 모든 추가 로컬 디스크는 선택사항입니다. 500GB 이상을 필요로 하는 경우에는 두 개의 추가 디스크가 필요합니다(예: 2 x 250GB의 로컬 스토리지를 필요로 하는 8개 코어).
*	최대 로컬 스토리지는 코어 수에 따라 제한됩니다. 
*	밸런스된 로컬 스토리지는 글로벌 형식으로 사용 가능합니다. 그러나, 스토리지의 유형(로컬 SSD 또는 로컬 HDD)은 데이터 센터 위치에 따라 다릅니다. 
*	기본 또는 보조 디스크는 분리할 수 없습니다.

다음 데이터 센터는 로컬 SSD가 있는 밸런스된 로컬 스토리지 가상 서버를 지원합니다.

| 사용 가능한 데이터 센터 - 로컬 SDD |        |
| ---------------------------------- | ------ |
| 댈러스(DAL09)                      | 댈러스(DAL10)          |
| 댈러스(DAL12)                      | 댈러스(DAL13)          |
| 케레타로(MEX01)                    | 몬트리올(MON01)        |
| 상파울루(SAO01)                    | 산호세(SJC03)          |
| 산호세(SJC04)                      | 토론토(TOR01)          |
| 워싱턴, DC(WDC04)                  | 워싱턴, DC(WDC06)      |
| 워싱턴, DC(WDC07)                  |                        |
{: class="simple-tab-table"}
{: caption="표 8. 사용 가능한 데이터 센터(로컬 SDD) - 아메리카" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd1}
{: tab-title="Americas"}

| 사용 가능한 데이터 센터 - 로컬 SDD |       |
| ---------------------------------- | ----- |
| 암스테르담(AMS03)                  | 프랑크푸르트(FRA02) |
| 런던(LON02)                        | 런던(LON04)       |
| 런던(LON06)                        | 밀라노(MIL01)     |
| 오슬로(OSL01)                      | 파리(PAR01)       |
{: class="simple-tab-table"}
{: caption="표 9. 사용 가능한 데이터 센터(로컬 SDD) - 유럽" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd2}
{: tab-title="Europe"}

| 사용 가능한 데이터 센터 - 로컬 SDD |       |
| ---------------------------------- | ----- |
| 첸나이(CHE01)                      | 멜버른(MEL01)     |
| 서울(SEO01)                        | 시드니(SYD01)     |
| 시드니(SYD04)                      | 도쿄(TOK02)       |
{: class="simple-tab-table"}
{: caption="표 10. 사용 가능한 데이터 센터(로컬 SDD) - 아시아 태평양" caption-side="top"}
{: tab-group="Local-SDD"}
{: #local-sdd3}
{: tab-title="Asia-Pacific"}

모든 지원 운영 체제(RHEL, CentOS, Windows, Ubuntu 및 기타), 지원 데이터베이스 및 소프트웨어 추가 기능 또한 이 오퍼링과 함께 사용할 수 있습니다.

## 컴퓨팅
{: #compute}

컴퓨팅 프로파일은 웹 트래픽이 많은 워크로드, 프로덕션 일괄처리, 프론트 엔드 웹 서버와 같이 CPU 수요가 매우 높은 워크로드에 가장 적합합니다.

이 오퍼링은 다음 프로파일에서 사용 가능합니다.

| 프로파일      | vCPU     |RAM       |스토리지 유형 |
| ------------ | -------- | --------- | ------------ |
|C1.1x1       |1        |1GB      |SAN          |
|C1.2x2       |2        |2GB      |SAN          |
|C1.4x4       |4        |4GB      |SAN          |
|C1.8x8       |8        |8GB      |SAN          |
|C1.16x16     |16       |16GB     |SAN          |
|C1.32x32     |32       |32GB     |SAN          |
{: caption="표 11. 컴퓨팅 프로파일" caption-side="top"}

### 스토리지 참고사항
* 최대 2TB의 추가 디스크가 사용 가능(총 4개 디스크가 허용됨)한 SAN 기본 부트 디스크(25GB 또는 100GB)입니다.
* SAN 스토리지를 사용하는 공용 가상 서버에 대한 가격은 가상 CPU, 메모리 및 최소 기본 부트 디스크를 포함합니다. 추가 디스크 가격은 선택하는 디스크 크기 및 수량에 따라 달라집니다.  

컴퓨팅 프로파일은 모든 데이터 센터에서 사용 가능합니다.

모든 지원 운영 체제(RHEL, CentOS, Windows, Ubuntu 및 기타), 지원 데이터베이스 및 소프트웨어 추가 기능 또한 이 오퍼링과 함께 사용할 수 있습니다.

## 메모리
{: #memory}

메모리 프로파일은 대량의 캐싱 워크로드, 데이터베이스 사용량이 많은 애플리케이션, 인메모리 분석 워크로드와 같은 메모리 사용량이 많은 워크로드에 가장 적합합니다.

이 오퍼링은 다음 프로파일에서 사용 가능합니다.

| 프로파일      | vCPU     |RAM       |스토리지 유형 |
| ------------ | -------- | --------- | ------------ |
|M1.1x8       |1        |8GB      |SAN          |
|M1.2x16      |2        |16GB     |SAN          |
|M1.4x32      |4        |32GB     |SAN          |
|M1.8x64      |8        |64GB     |SAN          |
|M1.16x128    |16       |128GB    |SAN          |
|M1.30x240    |30       |240GB    |SAN          |
|M1.48x384    |48       |384GB    |SAN          |
|M1.56x448    |56       |448GB    |SAN          |
|M1.64x512    |64       |512GB    |SAN          |
{: caption="표 12. 메모리 프로파일" caption-side="top"}

### 스토리지 참고사항
* 최대 2TB의 추가 디스크가 사용 가능(총 5개 디스크가 허용됨)한 SAN 기본 부트 디스크(25GB 또는 100GB)입니다.
* SAN 스토리지를 사용하는 공용 가상 서버에 대한 가격은 가상 CPU, 메모리 및 최소 기본 부트 디스크를 포함합니다. 추가 디스크 가격은 선택하는 디스크 크기 및 수량에 따라 달라집니다.  

메모리 프로파일은 모든 데이터 센터에서 사용 가능합니다.

모든 지원 운영 체제(RHEL, CentOS, Windows, Ubuntu 및 기타), 지원 데이터베이스 및 소프트웨어 추가 기능 또한 이 오퍼링과 함께 사용할 수 있습니다.

## GPU
{: #gpu}

GPU 프로파일은 리소스 관리 및 비용 절감을 위해 추가 컴퓨팅 밀도가 필요한 고성능 워크로드에 가장 적합합니다. GPU 프로파일은 AI 프로세스, 그래픽 및 데이터가 많은 애플리케이션 또는 빠른 속도를 필요로 하는 새 애플리케이션 개발에 적합합니다.

NVDIA Tesla GPU를 기반으로 하는 {{site.data.keyword.cloud_notm}} Accelerated Compute “ac1” and "ac2" 프로파일은 모두 블록 및 로컬 SSD 스토리지를 제공합니다. 다음 GPU 프로파일은 다음에서 선택할 수 있습니다.  

<table>
<CAPTION>표 13. P100 GPU 프로파일</CAPTION>
<THEAD>
<TR>
<th>프로파일</th>
<th>GPU</th>
<th>GPU RAM(GB)</th>
<th>vCPU</th>
<th>vCPU RAM(GB)</th>
<th>스토리지 유형</th>
<th>부트 디스크(GB)</th>
<th>보조 디스크(2 및 3)(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60x25</td>
<td>P100 1개</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>블록(SAN)</td>
<td>25</td>
<td>없음</td>
</tr>
<tr>
<td>ac1.8x60x100</td>
<td>P100 1개</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>로컬 SSD 또는 SAN</td>
<td>100</td>
<td>없음(SAN)<br>300(로컬)</td>
</tr>
<tr>
<td>ac1.16x120x25</td>
<td>P100 2개</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>블록(SAN)</td>
<td>25</td>
<td>없음</td>
</tr>
<tr>
<td>ac1.16x120x100</td>
<td>P100 2개</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>로컬 SSD 또는 SAN</td>
<td>100</td>
<td>없음(SAN)<br>600(로컬)</td></tr>

</TBODY>
</table>

P100 GPU 프로파일은 _DAL13_, _LON06_ 및 _WDC07_ 데이터 센터에서 사용 가능합니다.
{: note}

<table>
<CAPTION>표 14. V100 GPU 프로파일</CAPTION>
<THEAD>
<TR>
<th>프로파일</th>
<th>GPU</th>
<th>GPU RAM(GB)</th>
<th>vCPU</th>
<th>vCPU RAM(GB)</th>
<th>스토리지 유형</th>
<th>부트 디스크(GB)</th>
<th>보조 디스크(2 및 3)(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac2.8x60x25</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>블록(SAN)</td>
<td>25</td>
<td>없음</td>
</tr>
<tr>
<td>ac2.8x60x100</td>
<td>1 V100</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>로컬 SSD 또는 SAN</td>
<td>100</td>
<td>없음(SAN)<br>300(로컬)</td>
</tr>
<tr>
<td>ac2.16x120x25</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>블록(SAN)</td>
<td>25</td>
<td>없음</td>
</tr>
<tr>
<td>ac2.16x120x100</td>
<td>2 V100</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>로컬 SSD 또는 SAN</td>
<td>100</td>
<td>없음(SAN)<br>600(로컬)</td></tr>

</TBODY>
</table>

V100 GPU 프로파일은 _DAL10_, _DAL12_, _LON04_ 및 _WDC07_ 데이터 센터에서 사용 가능합니다.
{: note}

### GPU 전제조건
다음의 GPU 전제조건을 검토하십시오.

1. GPU 프로파일의 가상 서버는 HVM(Hardware Virtual Machine) 부트 모드를 지원하는 운영 체제에서만 사용할 수 있습니다. HVM 부트 모드를 지원하는 다음 운영 체제 목록을 참조하십시오.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 적절한 NVIDIA 드라이버 및 소프트웨어가 설치되어 있어야 합니다. 소프트웨어 및 NVIDIA 드라이버에 대한 자세한 정보는 [GPU 드라이버 및 소프트웨어 패키지 설치](/docs/vsi?topic=virtual-servers-installing-gpu-drivers-and-software-packages#installing-gpu-drivers-and-software-packages)를 참조하십시오.  

설치하는 소프트웨어는 필수 소프트웨어 및 운영 체제별 고유한 구성을 포함해야 합니다.
{: note}

### GPU 추가 또는 제거 
초기 주문 후 가상 서버의 GPU 수를 변경할 수 있습니다. 그러나 이는 프로비저닝한 GPU 수에 따라 다릅니다. 사용자에게는 다음 옵션 중 하나가 있습니다.

- 하나의 GPU가 프로비저닝된 경우에는 다른 GPU를 추가할 수 있습니다.
- 두 개의 GPU가 프로비저닝된 경우에는 하나의 GPU로 되돌릴 수 있습니다.

