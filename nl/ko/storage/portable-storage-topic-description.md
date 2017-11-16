---
copyright:
  years: 1994, 2017
lastupdated: "2017-09-13"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# 휴대용 스토리지 볼륨 정보

휴대용 스토리지 볼륨은 {{site.data.keyword.BluVirtServers_short}}에서 독점적으로 사용 가능한 보조 스토리지 솔루션입니다. 한 번에 하나의 가상 서버에 연결될 수 있습니다. 또한 {{site.data.keyword.cloud}} 네트워크의 임의의 데이터 센터에 존재하는 가상 서버 간에 데이터를 전송하고자 하는 경우에 이상적인 솔루션입니다. 휴대용 스토리지 볼륨은 원시의 형식화되지 않은 블록 레벨의 스토리지에 대한 액세스가 필요한 데이터베이스 애플리케이션 및 {{site.data.keyword.BluVirtServers_short}} 간에 대형 데이터 세트를 이동하는 데 유용합니다.

휴대용 스토리지 볼륨이 원래 가상 서버가 아닌 다른 데이터 센터 내의 가상 서버에 연결되는 경우, {{site.data.keyword.cloud}}의 내부 시스템이 볼륨을 새 데이터 센터 내의 SAN으로 복사합니다. 그런 다음 시스템이 복사된 볼륨의 무결성을 확인하고 원래 데이터 센터 SAN에서 원래 휴대용 볼륨을 제거합니다.

## 다음 단계
휴대용 스토리지 볼륨 사용에 대한 자세한 정보는 다음 태스크를 참조하십시오.
* [휴대용 스토리지 액세스](../storage/access-portable-storage-screen.html)
* [휴대용 스토리지 설명 편집](../storage/edit-description-portable-storage-volume-psv.html)
