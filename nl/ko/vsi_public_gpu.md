---



copyright:
  years: 2017, 2018
lastupdated: "2018-6-18"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU 특성(flavor)은 리소스 관리 및 비용 절감을 위해 더 많은 컴퓨팅 밀도가 필요한 고성능 워크로드에 가장 적합합니다. GPU 특성은 그래픽 및 데이터가 많은 애플리케이션이나 빠른 속도를 필요로 하는 새 애플리케이션 개발에 적합합니다. 

NVDIA Tesla P100 GPU를 기반으로 하는 {{site.data.keyword.cloud_notm}} Accelerated Compute "ac1" 특성은 블록 및 로컬 SSD 스토리지를 모두 제공합니다. 다음 GPU 특성은 다음에서 선택할 수 있습니다.  

  <table>
<CAPTION>표 1. GPU 특성</CAPTION>
<THEAD>
<TR>
<th>특성</th>
<th>GPU</th>
<th>GPU RAM(GB)</th>
<th>vCPU</th>
<th>vCPU RAM(GB)</th>
<th>스토리지 유형</th>
<th>부트 디스크(GB)</th>
<th>보조 디스크(GB)</th>
</TR>
</THEAD>
<TBODY>
<tr>
<td>ac1.8x60</td>
<td>P100 1개</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>블록(SAN)</td>
<td>25 및 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.8x60</td>
<td>P100 1개</td>
<td>16</td>
<td>8</td>
<td>60</td>
<td>로컬 SSD</td>
<td>100</td>
<td>2 x 300</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>P100 2개</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>블록(SAN)</td>
<td>25 및 100</td>
<td>4 x 2000</td>
</tr>
<tr>
<td>ac1.16x120</td>
<td>P100 2개</td>
<td>32</td>
<td>16</td>
<td>120</td>
<td>로컬 SSD</td>
<td>100</td>
<td>2 x 600</td></tr>

</TBODY>
</table>

**참고:** GPU 특성은 _DAL13_, _LON06_ 및 _WDC07_ 데이터 센터에서 사용 가능합니다. 

## 시작하기 전에
다음의 GPU 전제조건을 검토하십시오.

1. GPU 특성의 가상 서버는 HVM(Hardware Virtual Machine) 부트 모드를 지원하는 운영 체제에서만 사용할 수 있습니다. HVM 부트 모드를 지원하는 다음의 운영 체제 목록을 참조하십시오.  
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Ubuntu 16
  - Windows 2012 R2
  - Windows 2016

2. 적절한 NVIDIA 드라이버 및 소프트웨어가 설치되어 있어야 합니다. 소프트웨어 및 NVIDIA 드라이버에 대한 자세한 정보는 [GPU 드라이버 및 소프트웨어 패키지 설치](../vsi/vsi_gpu_nvidia_drivers.html)를 참조하십시오.  
**참고:** 설치하는 소프트웨어는 필수 소프트웨어 및 운영 체제별 고유한 구성을 포함해야 합니다.

# GPU 추가 또는 제거
초기 주문 후 가상 서버의 GPU 수를 변경할 수 있습니다. 그러나 이는 프로비저닝한 GPU 수에 따라 다릅니다. 사용자에게는 다음 옵션 중 하나가 있습니다. 프로비저닝 주문 화면에서는 다음 옵션 중 하나가 있습니다. 
- 하나의 GPU가 프로비저닝된 경우에는 다른 GPU를 추가할 수 있습니다. 
- 두 개의 GPU가 프로비저닝된 경우에는 하나의 GPU로 되돌릴 수 있습니다. 
