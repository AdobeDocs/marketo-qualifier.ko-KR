---
title: CRM 연결
description: Salesforce 또는 Microsoft Dynamics 365에 Marketo Qualifier을 설치하고 아웃바운드 워크플로우 및 Marketo 캠페인에 대한 Salesforce 작업을 구성하는 방법에 대해 알아봅니다.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
  - id: f8f8b877-7295-5853-989f-e21f73bc94c4
    internal-label: Administration
subfeature_v2:
  - id: d2fe5f36-5653-5902-937c-9d3026104284
    internal-label: CRM integrations
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: 633ca975d4fe58bdcc84caf633049ae1190b0f56
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%
---

# CRM 연결

담당자가 Salesforce 또는 Microsoft Dynamics 365를 종료하지 않고 리드, 연락처 및 계정 기록 페이지에서 [!DNL Marketo Sales Insights] 및 AI가 생성한 인사이트를 사용할 수 있도록 [!DNL Adobe Marketo Qualifier] CRM 플러그인을 설치하십시오. 또한 이 플러그인은 [CRM에서 잠재 고객의 우선 순위 지정](admin-settings.md#prioritize-leads-in-the-crm-plugin)을 위한 홈 보기를 제공합니다.

Salesforce에서 담당자는 리드 및 연락처 목록 보기 및 개별 레코드 페이지에서 아웃바운드 워크플로우 또는 Marketo 캠페인에 잠재 고객을 추가할 수도 있습니다.

## 시작하기에 앞서

플러그인을 설치하고 사용하는 사람들이 필요한 액세스 권한을 보유하고 있는지 확인하십시오.

* **Salesforce 관리자**: 패키지를 설치하고 페이지 레이아웃을 편집할 수 있는 권한입니다.
* **Microsoft Dynamics 365 관리자**: Power Apps의 대상 환경으로 솔루션을 가져올 수 있는 권한.
* **담당자**: Marketo Qualifier 및 관련 CRM 레코드에 대한 액세스

플러그 인을 설치하는 것은 [CRM을 Marketo Qualifier에 연결](getting-started.md#connect-your-crm)하는 것과 별개입니다.

## Salesforce에 설치

패키지를 설치한 다음 해당 구성 요소를 담당자가 사용하는 레코드 페이지에 추가합니다.

1. [Salesforce 설치 페이지](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=salesforce)를 열고 관리자로 Salesforce에 로그인합니다.
1. 패키지 설치 페이지에서 **[!UICONTROL 모든 사용자에 대해 설치]**&#x200B;를 선택한 다음 **[!UICONTROL 설치]**&#x200B;를 선택합니다.

   Salesforce 권한을 통해 개별 사용자의 액세스를 제어할 수 있습니다.

1. 서드파티 액세스를 승인하라는 메시지가 표시되면 승인 확인란을 선택하고 **[!UICONTROL 계속]**&#x200B;을 선택합니다.
1. 설치가 완료되면 **[!UICONTROL 완료]**&#x200B;를 선택하십시오.

   설치하는 데 몇 분 정도 소요됩니다. 패키지가 **[!UICONTROL 설치된 패키지]** 페이지에 표시되는지 확인하십시오.

1. Lightning App Builder에서 리드, 연락처 및 계정 기록 페이지를 편집하고 Marketo Qualifier 구성 요소를 추가합니다.

### 목록 보기에 작업 추가

잠재 고객 및 연락처 목록 보기를 위해 **[!UICONTROL 아웃바운드 워크플로에 추가]** 및 **[!UICONTROL Marketo 캠페인에 추가]**&#x200B;를 별도로 구성합니다. 패키지에 포함된 버튼을 사용하여 중복을 방지하십시오.

1. **[!UICONTROL 설정]** > **[!UICONTROL 개체 관리자]**(으)로 이동하여 **[!UICONTROL 리드]** 또는 **[!UICONTROL 연락처]**&#x200B;를 선택합니다.
1. **[!UICONTROL 단추, 링크 및 작업]**&#x200B;을 열고 목록 단추 **[!UICONTROL 아웃바운드 워크플로우에 AMQ 추가]** 및 **[!UICONTROL Marketo 캠페인에 AMQ 추가]**&#x200B;를 찾습니다.
1. 개체의 **[!UICONTROL 목록 보기 단추 레이아웃]**&#x200B;을 열고 **[!UICONTROL 편집]**&#x200B;을 선택합니다.

   Salesforce 설정에 따라 목록 보기 레이아웃이 **[!UICONTROL 검색 레이아웃]** > **[!UICONTROL 목록 보기]** 아래에 있을 수 있습니다.

1. 두 목록 단추를 **[!UICONTROL 선택한 단추]**(으)로 이동하고 저장합니다.
1. 다른 객체에 대해 이 작업을 반복합니다.

담당자는 목록 보기에서 하나 이상의 레코드를 선택한 다음 작업을 선택합니다.

### 기록 페이지에 작업 추가

레코드 페이지 작업은 목록 보기 단추와 별도로 구성해야 합니다. 사용 중인 각 리드 및 연락처 페이지 레이아웃에 두 작업을 모두 추가합니다.

1. **[!UICONTROL 설정]** > **[!UICONTROL 개체 관리자]**(으)로 이동하여 **[!UICONTROL 리드]** 또는 **[!UICONTROL 연락처]**&#x200B;를 선택합니다.
1. **[!UICONTROL 단추, 링크 및 작업]**&#x200B;을 열고 세부 정보 단추 **[!UICONTROL 아웃바운드 워크플로우에 AMQ 추가]** 및 **[!UICONTROL Marketo 캠페인에 AMQ 추가]**&#x200B;를 찾습니다.
1. **[!UICONTROL 페이지 레이아웃]**&#x200B;을 열고 담당자에게 할당된 레이아웃을 편집하세요.
1. **[!UICONTROL Salesforce Mobile 및 Lightning Experience 작업]**&#x200B;에 두 세부 단추를 모두 추가하고 저장합니다.
1. 적용 가능한 각 레이아웃에 대해 를 반복하고 다른 오브젝트에 대해 를 반복합니다.

작업은 레코드의 작업 모음 또는 메뉴에 나타나고 보고 있는 레코드에 적용됩니다.

>[!NOTE]
>
>이러한 작업은 Salesforce 모바일 앱이 아닌 데스크탑 Salesforce Lightning Experience에서 작동합니다. **[!UICONTROL Salesforce Mobile 및 Lightning Experience Actions]**&#x200B;이라는 레이아웃 섹션도 데스크톱 작업에 사용됩니다.

### 누락된 단추 바꾸기

패키지된 단추가 없으면 개체의 **[!UICONTROL 단추, 링크 및 작업]**&#x200B;에 대체 단추를 만드십시오.

1. **[!UICONTROL 새 단추 또는 링크]**&#x200B;를 선택하십시오.
1. `Add to Outbound Workflow` 또는 `Add to Marketo Campaign`과(와) 같은 작업 레이블을 입력하십시오.
1. 목록 보기의 경우 **[!UICONTROL 목록 단추]**&#x200B;를 선택하고 레코드 페이지의 경우 **[!UICONTROL 세부 정보 페이지 단추]**&#x200B;를 선택합니다.
1. **[!UICONTROL 컨텐츠 Source]**&#x200B;을(를) **[!UICONTROL Visualforce 페이지]**(으)로 설정하고 작업, 개체 및 배치와 일치하는 패키지의 작업 페이지를 선택하십시오.

   리드 목록, 리드 세부 정보, 연락처 목록 및 연락처 세부 정보 배치는 서로 다른 페이지를 사용합니다. 선택한 페이지가 구성 중인 배치와 일치하는지 확인합니다.

1. 목록 단추의 경우 **[!UICONTROL 행 선택 필요]**&#x200B;를 선택합니다.
1. 위에서 설명한 대로 단추를 저장하고 적절한 목록 보기 단추 레이아웃 또는 레코드 페이지 작업에 추가합니다.

### Salesforce 작업 확인

레이아웃을 저장한 후 리드 및 연락처 목록 보기와 레코드 페이지에 두 작업이 모두 표시되는지 확인합니다. 선택한 레코드로 각 목록 작업을 테스트하고 개별 레코드에서 각 레코드 페이지 작업을 테스트합니다.

작업을 사용할 수 없거나 작업이 열리지 않으면 다음 검사를 사용합니다.

| 문제 | 확인할 사항 |
| --- | --- |
| 목록 보기에서 단추 누락 | 목록 단추가 올바른 개체의 **[!UICONTROL 목록 보기 단추 레이아웃]**&#x200B;에서 **[!UICONTROL 선택한 단추]**&#x200B;에 있는지 확인하고 레이아웃을 저장합니다. |
| 기록 페이지에서 단추 누락 | 세부 정보 단추가 사용자에게 할당된 레이아웃의 **[!UICONTROL Salesforce Mobile 및 Lightning Experience 작업]**&#x200B;에 있는지 확인하십시오. 조직에서 동적 작업을 사용하는 경우 레코드 페이지의 작업 가시성도 확인하십시오. |
| 단추를 만들 때 필요한 페이지 옵션을 사용할 수 없음 | 표시 유형이 목록 보기의 경우 **[!UICONTROL 목록 단추]**, 레코드 페이지의 경우 **[!UICONTROL 세부 정보 페이지 단추]**&#x200B;인지 확인하십시오. |
| 작업이 열리지 않거나 액세스 오류를 표시합니다. | 사용자가 Marketo Qualifier 및 선택한 레코드에 액세스할 수 있는지 확인합니다. |

## Microsoft Dynamics 365에 설치

플러그 인 패키지를 담당자가 근무하는 환경으로 가져옵니다.

1. [Microsoft Dynamics 365 설치 페이지](https://experience.adobe.com/solutions/OneAdobe-sales-workflow-optimizer-sales-insight-ui/install/sales-insight?crm=dynamics)를 열고 패키지 ZIP 파일을 다운로드합니다.
1. 관리자로 [Power Apps](https://make.powerapps.com/)에 로그인하고 대상 환경을 선택하십시오.
1. **[!UICONTROL 솔루션]**&#x200B;을 열고 **[!UICONTROL 솔루션 가져오기]**&#x200B;를 선택합니다.
1. **[!UICONTROL 찾아보기]**&#x200B;를 선택하고 다운로드한 ZIP 파일을 선택한 다음 **[!UICONTROL 다음]**&#x200B;을 선택합니다.
1. 패키지 세부 정보를 검토하고 **[!UICONTROL 다음]**&#x200B;을(를) 선택하십시오.
1. 미리 채워진 환경 변수 값을 유지하고 **[!UICONTROL 가져오기]**&#x200B;를 선택합니다.
1. 솔루션을 성공적으로 가져왔음을 알리는 확인 메시지가 페이지 맨 위에 표시될 때까지 기다립니다.

가져오기는 몇 분 정도 소요됩니다.

>[!MORELIKETHIS]
>
>* [CRM 플러그 인에서 잠재 고객 우선 순위 지정](admin-settings.md#prioritize-leads-in-the-crm-plugin)
>* [통합](integrations.md)
>* [시작](getting-started.md)
