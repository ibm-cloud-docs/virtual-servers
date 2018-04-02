---



copyright:
  years: 2017, 2018
lastupdated: "2018-2-27"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# GPU
GPU 특성은 리소스 관리 및 비용 절감을 위해 더 많은 컴퓨팅 밀도가 필요한 고성능 워크로드에 가장 적합합니다. GPU는 그래픽 및 데이터가 많은 애플리케이션이나 고성능이 필요한 새로운 애플리케이션 개발에 적합합니다. 

NVDIA Tesla P100 GPU를 기반으로 {{site.data.keyword.cloud_notm}} Accelerated Compute "ac1" 제품군은 블록(ac1) 및 로컬 SSD 스토리지(acl1)를 제공합니다. 다음 GPU 특성은 다음에서 선택할 수 있습니다.   

<table>

<caption>표 1. GPU 특성</caption>

  
<thead>
<td rowspan="4"></td>
  <th colspan="4">GPU 특성</th>
<tr>
  <th>ac1.8x60</th>
  <th>acl1.8x60</th>
  <th>ac1.16x120</th>
  <th>acl1.16x120</th>
</tr>
</thead>
<TBODY>
<tr>
  <th><b>GPU</b></th>
  <td>1 x P100</td>
  <td>1 x P100</td>
  <td>2 x P100</td>
  <td>2 x P100</td>
</tr>
<tr>
  <th><b>GPU RAM(GB)</b></th>
  <td>16</td>
  <td>16</td>
  <td>32</td>
  <td>32</td>
</tr>

<tr>
  <th><b>vCPU</b></th>
  <td>8</td>
  <td>8</td>
  <td>16</td>
  <td>16</td>
</tr>

<tr>
  <th><b>vCPU RAM(GB)</b></th>
  <td>60</td>
  <td>60</td>
  <td>120</td>
  <td>120</td>
</tr>

<tr>
  <th><b>스토리지 유형</b></th>
  <td>블록(SAN)</td>
  <td>로컬 SSD</td>
  <td>블록(SAN)</td>
  <td>로컬 SSD</td>
</tr>

<tr>
  <th><b>부트 디스크(GB)</b></th>
  <td>25 및 100</td>
  <td>100</td>
  <td>25 및 100</td>
  <td>100</td>
</tr>

<tr>
  <th><b>보조 디스크(GB)</b></th>
  <td>4 x 2000</td>
  <td>2 x 300</td>
  <td>4 x 2000</td>
  <td>2 x 300</td>
</tr>

</TBODY>
</table>


**참고:** GPU 특성은 _DAL13_ 데이터 센터에서 사용 가능합니다. 

## 시작하기 전에
다음의 GPU 전제조건을 검토하십시오. 

1. GPU 제품군 가상 서버는 HVM(Hardware Virtual Machine) 부트 모드를 지원하는 운영 체제에서만 사용할 수 있습니다. HVM 부트 모드를 지원하는 다음의 운영 체제 목록을 참조하십시오.   
  - CentOS 7
  - Debian 8
  - RHEL 7
  - Windows 2012 R2
  - Windows 2016

2. 적절한 NVIDIA 드라이버 및 소프트웨어가 설치되어 있어야 합니다. 소프트웨어 및 NVIDIA 드라이버에 대한 자세한 정보는 [GPU 드라이버 및 소프트웨어 패키지 설치](../vsi/vsi_gpu_nvidia_drivers.html)를 참조하십시오. 

**참고:** 설치하는 소프트웨어는 필수 소프트웨어 및 운영 체제별 고유한 구성을 포함해야 합니다. 


