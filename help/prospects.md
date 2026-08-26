---
title: Sales Qualifier의 잠재 고객
description: Sales Qualifier에서 잠재 고객 목록을 빌드하고, 필터링하고, 검토하여 지원 우선 순위를 결정하는 방법을 알아봅니다.
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/zf2H5rq1JlIT26LqLPMrm2Mq3tSIrLOiTEw6BXb1w2U'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 550
ht-degree: 2%

---


# 잠재 고객

액세스할 수 있는 잠재 고객 및 연락처를 보려면 왼쪽 탐색에서 **[!UICONTROL 잠재 고객]**&#x200B;을 선택하십시오. 각 잠재 고객의 상태와 최신 활동을 검토하려면 목록을 사용하십시오.

![잠재 고객 관리에 대한 잠재 고객 상태 및 마지막 활동을 표시하는 잠재 고객 표](./assets/prospects.png){width="800" zoomable="yes"}

* **[!UICONTROL 잠재 고객]** - 연결된 CRM에서 사용자에게 할당된 잠재 고객.
* **[!UICONTROL 연락처]**—연결된 CRM에서 사용자에게 할당된 연락처.
* **[!UICONTROL 마케팅 하이라이트]** - 이메일 열기 또는 클릭과 같은 라이브 Marketo 활동이 있는 잠재 고객.
* **[!UICONTROL 사용자 목록]**—수동으로 가져오거나 추가하는 잠재 고객.

## 잠재 고객 목록 작성

잠재 고객 목록은 두 개 이상의 소스에서 가져온 사람을 결합합니다.

* **CRM 잠재 고객** - Sales Qualifier에서 연결된 사용자에게 할당된 잠재 고객 및 연락처를 자동으로 가져옵니다. [통합](integrations.md)을 참조하세요.
* **가져온 잠재 고객** - CSV 파일에서 가져온 잠재 고객입니다.
* **수동으로 추가된 잠재 고객**—Sales Qualifier에 개별 잠재 고객이 추가되었습니다.

CRM에서 제공되지 않는 잠재 고객을 추가하려면:

1. **[!UICONTROL 잠재 고객]** 페이지에서 **[!UICONTROL 인물 목록]**&#x200B;을 선택하세요.

   ![사람 목록](assets/prospects-people-list.png){width="800" zoomable="yes"}

1. **[!UICONTROL + 직원 추가]**&#x200B;를 선택한 다음 **[!UICONTROL CSV 가져오기]** 또는 **[!UICONTROL 직원 추가]**&#x200B;를 선택합니다.

   * CSV 가져오기의 경우 CSV를 `firstname,email` 형식으로 업로드하십시오.
     이름과 이메일은 필수 항목입니다. 성은 선택 사항입니다. CSV 템플릿에는 CRM 리드 ID 열이 포함되어 있지 않지만 가져오기 전에 열과 해당 값을 파일에 추가할 수 있습니다. 가져오기에 실패한 경우 수정할 필드 또는 값에 대한 오류 메시지를 검토한 다음 파일을 다시 업로드하십시오.
   * 개인을 수동으로 추가하려면 양식에 해당 상세내역을 입력합니다.

1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

## 잠재 고객 필터링 및 찾기

목록의 범위를 좁히려면 **[!UICONTROL 필터]**&#x200B;을(를) 선택하십시오. 다음을 기준으로 필터링할 수 있습니다.

* 아웃바운드 워크플로 상태
* 제작자
* 직위
* 계정
* 소스
* 마지막 업데이트

관리자는 매핑된 CRM 필드를 필터로 사용할 수도 있습니다. **[!UICONTROL 관리자 설정]**&#x200B;에서 담당자가 잠재 고객을 찾는 데 사용하는 각 필드에 대해 **[!UICONTROL 필터링 가능]**&#x200B;을 켜십시오. [CRM 필드 매핑](integrations.md#map-crm-fields-inbound-mapping)을 참조하세요.

**[!UICONTROL 내 영업 기회 연락처]**&#x200B;에서 단계, 유형, 종료 날짜 등 연결된 영업 기회의 필드를 기준으로 연락처를 필터링할 수도 있습니다. 영업 기회 필드에는 연락처 필드와 구별되는 **[!UICONTROL 단계(영업 기회)]**&#x200B;와 같은 레이블이 있습니다. 관리자는 필터로 사용할 수 있는 영업 기회 필드를 제어합니다.

### Marketo 참여로 필터링

이메일 열기 및 클릭 수, 웹 방문, 양식 채우기, 즐거운 순간 등 실시간 [!DNL Marketo] 참여로 잠재 고객을 찾고 우선 순위를 지정합니다. 참여는 실시간에 가깝게 나타납니다.

Marketo 참여로 잠재 고객을 필터링하려면 다음을 수행하십시오.

1. **[!UICONTROL 필터]**&#x200B;를 선택하십시오.
1. [!DNL Marketo] 참여 필터를 추가하고 활동 유형, 캠페인 또는 기타 특성을 설정하여 중요한 참여에 집중하십시오.

각 잠재 고객은 최근 기록과 함께 최신 [!DNL Marketo] 활동을 보여줍니다.

Marketo 참여 필터링은 모든 프로덕션 영역에서 사용할 수 있습니다. 관리자가 조직과 샌드박스에 대해 이 설정을 켜고 마케터가 [!DNL Marketo]에서 1회 설정을 완료합니다. [Marketo 참여 필터링 사용](integrations.md#turn-on-marketo-engagement-filtering)을 참조하세요.

## 잠재 고객 세부 정보 검토

잠재 고객을 선택하여 프로필을 엽니다. 연락하기 전에 중요한 신호를 검토하십시오.

* **AI 사용자 요약** - 잠재 고객 또는 연락처 및 최근 참여에 대한 AI 작성 스냅숏입니다. 개별 활동을 검토하기 전에 요약을 사용하여 해당 사용자를 한 눈에 이해할 수 있습니다. AI 사용자 요약은 Adobe Journey Optimizer B2B edition Prime 또는 Ultimate을 실행하는 인스턴스에서 사용할 수 있습니다.
* **활동 목록** - 활동 및 최근 동작의 시간 순서대로 목록입니다.
* **타임라인 보기** - 채널 간 참여의 시각적 타임라인입니다.
* **본 콘텐츠**—잠재 고객이 본 웹 페이지 및 에셋입니다. 항목을 선택하여 엽니다.

>[!MORELIKETHIS]
>
>* [계정](accounts.md)
>* [아웃바운드 워크플로](outbound-workflows.md)
>* [AI 채팅](ai-assistant.md)
