---



copyright:
  years: 2017
lastupdated: "2017-11-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# 균형 로컬 스토리지 특색
균형 로컬 스토리지 특성(flavor)은 주로 높거나 낮은 대기 시간 I/O 성능을 필요로 하는 대형 데이터베이스 클러스터를 위한 특성입니다. 이 오퍼링은 리소스가 초과 구독되지 않으므로 고성능을 발휘합니다. 네트워크 성능의 범위는 표준에서 프리미엄입니다.

오퍼링은 다음과 같은 로컬 스토리지 옵션과 함께 다양한 특성 및 데이터 센터에서 사용 가능합니다.

* [로컬 HDD](vsi_public_balanced_local.html#HDD)
* [로컬 SSD](vsi_public_balanced_local.html#SSD)

## 로컬 HDD {: #HDD}
 
<table>
<CAPTION>표 1. 로컬 HDD를 사용하는 균형 로컬 스토리지 특성</CAPTION>
<THEAD>
<TR>
<th>특성</th>
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

**스토리지 참고:**
* <sup>(*)</sup>균형 로컬 특성에는 100GB 로컬 스토리지 부트 디스크가 자동으로 제공됩니다. 그런 다음 사용자가 두 번째 디스크를 선택할 수 있습니다(위 테이블에 표시된 옵션). 모든 추가 로컬 디스크는 선택사항입니다. 500GB 이상을 필요로 하는 경우에는 두 개의 추가 디스크가 필요합니다(예: 2 x 250GB의 로컬 스토리지를 필요로 하는 8개 코어).
*	최대 로컬 스토리지는 코어 수에 따라 제한됩니다. 
*	균형 로컬 스토리지는 글로벌 형식으로 사용 가능합니다. 그러나, 스토리지의 유형(로컬 SSD 또는 로컬 HDD)은 데이터 센터 위치에 따라 다릅니다. 
*	기본 또는 보조 디스크는 분리할 수 없습니다.

다음 데이터 센터는 로컬 HDD가 있는 균형 로컬 스토리지 가상 서버를 지원합니다.

|데이터 센터(로컬 HDD) |        |
|------------ |------  |  
|AMS01        |SEA01   |
|DAL01        |SJC01   | 
|DAL05        |SNG01   |
|DAL06        |WDC01   |
|HKG02        |        |        
|HOU02        |        |  
{: caption="표 1. 지원되는 데이터 센터(로컬 HDD)" caption-side="top"}

모든 지원 운영 체제(RHEL, CentOS, Windows, Ubuntu 및 기타), 지원 데이터베이스 및 소프트웨어 추가 기능 또한 이 오퍼링과 함께 사용할 수 있습니다.  

## 로컬 SSD {: #SSD}
<table>
<CAPTION>표 1. 로컬 SSD를 사용하는 균형 로컬 스토리지 특성</CAPTION>
<THEAD>
<TR>
<th>특성</th>
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

**스토리지 참고:**
* <sup>(*)</sup>균형 로컬 특성에는 100GB 로컬 스토리지 부트 디스크가 자동으로 제공됩니다. 그런 다음 사용자가 두 번째 디스크를 선택할 수 있습니다(위 테이블에 표시된 옵션). 모든 추가 로컬 디스크는 선택사항입니다. 500GB 이상을 필요로 하는 경우에는 두 개의 추가 디스크가 필요합니다(예: 2 x 250GB의 로컬 스토리지를 필요로 하는 8개 코어).
*	최대 로컬 스토리지는 코어 수에 따라 제한됩니다. 
*	균형 로컬 스토리지는 글로벌 형식으로 사용 가능합니다. 그러나, 스토리지의 유형(로컬 SSD 또는 로컬 HDD)은 데이터 센터 위치에 따라 다릅니다. 
*	기본 또는 보조 디스크는 분리할 수 없습니다.

다음 데이터 센터는 로컬 SSD가 있는 균형 로컬 스토리지 가상 서버를 지원합니다.

|데이터 센터(로컬 SSD) |        |         |
|------- |------  |------ | 
|AMS03   |LON06   |SJC03  |
|CHE01   |MEL01   |SJC04  | 
|DAL09   |MEX01   |SYD01  |
|DAL10   |MIL01   |SYD04  |
|DAL12   |MON01   |TOK02  |       
|DAL13   |OSL01   |TOR01  |
|FRA02   |PAR01   |WDC04  |
|LON02   |SAO01   |WDC06  |
|LON04   |SEO01   |WDC07 | 
{: caption="표 2. 지원되는 데이터 센터(로컬 SSD)" caption-side="top"}

모든 지원 운영 체제(RHEL, CentOS, Windows, Ubuntu 및 기타), 지원 데이터베이스 및 소프트웨어 추가 기능 또한 이 오퍼링과 함께 사용할 수 있습니다.  
