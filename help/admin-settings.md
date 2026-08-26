---
title: 관리자 설정
description: CRM 필드, 활동 동기화, 이메일 옵트아웃 및 기타 Sales Qualifier 관리 설정을 관리하는 방법을 알아봅니다.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/vbtO6I67ZEaZz3oio9InNErvq5D0wjbRxyDZpTq8Lzo'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
internal-label: Administration
source-git-commit: 8573d3891d5c8ec8a05637f160f120f933b0ec61
workflow-type: tm+mt
source-wordcount: 670
ht-degree: 0%

---


# 관리자 설정

**[!UICONTROL 관리 설정]**&#x200B;을 사용하여 CRM 통합을 구성하고, 지식 센터를 관리하고, 전자 메일 옵트아웃을 구성하십시오.

Sales Qualifier은 Salesforce 또는 Microsoft Dynamics 365에 연결합니다. 이 연결을 통해 Account Qualification Agent(AQA)에는 리드, 계정, 연락처, 활동 및 소유자에 대한 일관된 보기가 제공됩니다. Sales Qualifier은 또한 CRM에 전달 활동 및 옵트아웃 상태를 다시 쓰고 Marketo에 전달 활동을 동기화할 수 있습니다.

CRM 연결, 필드 매핑 및 활동 동기화를 구성하려면 **[!UICONTROL 관리]** > **[!UICONTROL 관리 설정]** > **[!UICONTROL CRM 연결]**&#x200B;로 이동합니다. 표준 사용자는 구성된 CRM 데이터 및 필터를 사용할 수 있지만 이러한 설정을 변경할 수는 없습니다. CRM을 처음 연결하려면 [시작](getting-started.md#connect-your-crm)을 참조하세요.

>[!IMPORTANT]
>
>**[!UICONTROL 관리자 설정]**&#x200B;에 액세스하려면 `Sales Qualifier` 및 `Sales Qualifier Admins` 사용자 그룹 모두의 구성원이 필요합니다. [사용자 역할 및 권한](user-roles-permissions.md)을 참조하세요.

## CRM MCP 및 포함된 플러그인

Sales Qualifier은 다음과 같은 방식으로 CRM과 작동합니다.

* **CRM MCP 쿼리** - Account Qualification Agent은 라이브 CRM 데이터를 쿼리하여 응답과 통찰력이 레코드의 현재 상태를 반영하도록 합니다.
* **포함된 플러그인**—CRM 플러그인은 CRM의 [!DNL Marketo Sales Insights]&#x200B;(MSI) 인사이트 및 에이전트 데이터를 표시합니다. 플러그인을 사용하여 Sales Qualifier에 잠재 고객을 추가합니다.
* **활동 동기화**—관리자가 **[!UICONTROL 활동 동기화]**&#x200B;를 켜면 봉사 활동이 CRM 및 Marketo에 동기화됩니다.

## CRM 액세스 범위

Sales Qualifier은 CRM에서 사용자, 연락처, 소유자 매핑, 리드, 계정, 기회 및 활동을 읽습니다. 기록된 전달 활동 및 옵트아웃 상태만 CRM에 쓰고, 전달 활동을 Marketo에 동기화합니다. CRM 관리자는 Salesforce 또는 Dynamics에서 API 액세스를 준비합니다. 그런 다음 Sales Qualifier 관리자가 CRM을 연결하고 인바운드 필드를 매핑한 다음 활동을 동기화할지 여부를 선택합니다.

>[!NOTE]
>
>[시작](getting-started.md#connect-your-crm)의 자격 증명 단계에서 CRM 개체에 대한 읽기 액세스를 설명합니다. 활동 동기화 또는 옵트아웃 다시 쓰기를 켜는 경우 CRM 관리자와 함께 CRM 구성에 필요한 해당 쓰기 액세스 권한을 부여합니다.

## CRM 필드 매핑(인바운드 매핑)

CRM이 연결된 후 연결을 위해 **[!UICONTROL 관리]**&#x200B;를 선택하고 **[!UICONTROL 인바운드 매핑]**&#x200B;을 엽니다. 인바운드 매핑은 Sales Qualifier이 애플리케이션으로 가져오는 CRM 필드를 제어합니다.

1. **[!UICONTROL 섹션 추가]**&#x200B;를 선택합니다.
1. 섹션 이름과 설명을 입력합니다.
1. 엔터티 유형을 선택합니다. 기본적으로 **[!UICONTROL 잠재 고객]**&#x200B;이 선택됩니다. **[!UICONTROL 연락처]**, **[!UICONTROL 계정]** 및 **[!UICONTROL 기회]**&#x200B;도 사용할 수 있습니다.
1. 가져올 CRM 필드를 선택하십시오.

   각 필드 행에는 **[!UICONTROL 표시 이름]**, **[!UICONTROL 필드 이름]** 및 **[!UICONTROL 데이터 형식]**&#x200B;이 표시됩니다.

1. **[!UICONTROL 잠재 고객]** 목록에서 필터로 사용할 수 있도록 하려는 각 잠재 고객, 연락처 또는 영업 기회 필드에 대해 **[!UICONTROL 필터링 가능]**&#x200B;을 설정합니다.
1. 섹션을 미리 보고 **[!UICONTROL 추가]**&#x200B;를 선택합니다.

매핑된 필드는 Sales Qualifier의 해당 영역에 표시됩니다.

* 잠재 고객 필드는 **[!UICONTROL 개인]** 탭에 나타납니다.
* 계정 필드는 **[!UICONTROL 계정]** 탭에 나타납니다.
* 영업 기회 필드는 **[!UICONTROL 계정 영업 기회]** 섹션에 표시됩니다. 필터링 가능한 영업 기회 필드는 **[!UICONTROL 내 영업 기회 연락처]**&#x200B;에도 고유한 열로 표시되며, 연락처 필드와 구분하기 위해 **[!UICONTROL 단계(영업 기회)]**&#x200B;와 같은 레이블이 있습니다.

## 활동 동기화 구성(아웃바운드 매핑)

1. **[!UICONTROL CRM 연결]**&#x200B;에서 연결된 CRM에 대해 **[!UICONTROL 관리]**&#x200B;를 선택합니다.
1. **[!UICONTROL 아웃바운드 매핑]**&#x200B;을 엽니다.
1. **[!UICONTROL 활동 동기화]**&#x200B;를 켜서 Sales Qualifier 지원 활동을 CRM 및 Marketo에 동기화합니다. 이메일 전송, 열기, 클릭 및 회신된 활동에는 아웃바운드 워크플로우 이름이 포함됩니다.

활동 동기화가 꺼져 있으면 Sales Qualifier에서 인바운드 CRM 데이터를 계속 사용하지만 아웃바운드 활동을 CRM 또는 Marketo에 동기화하지 않습니다.

## 글로벌 이메일 옵트아웃 구성

1. 왼쪽 탐색에서 **[!UICONTROL 관리]**&#x200B;를 확장하고 **[!UICONTROL 관리 설정]**&#x200B;을 선택합니다.
1. **[!UICONTROL 준수]**&#x200B;에서 **[!UICONTROL 전자 메일 설정]**&#x200B;을 선택하세요.
1. **[!UICONTROL 모든 전자 메일에 옵트아웃 링크 포함]**&#x200B;을 켜서 아웃바운드 전자 메일에 구독 취소 바닥글을 추가합니다.
1. **[!UICONTROL 옵트아웃 메시지 템플릿]**&#x200B;에 바닥글 텍스트를 입력하십시오. 구독 취소 링크가 표시되어야 하는 `{opt_out_link}` 토큰을 포함합니다.

설정이 자동으로 저장됩니다.

잠재 고객이 링크를 선택하면 Sales Qualifier은 해당 잠재 고객에게 이메일 전송을 중단하고 옵트아웃 상태를 연결된 CRM에 동기화합니다.

## 참조: 샘플 API 매개 변수

CRM 팀은 이러한 예를 사용하여 읽기 액세스가 예상 리드 필드를 반환하는지 확인할 수 있습니다.

### Dynamics OData 예

```text
$select=fullname,_ownerid_value,leadid,emailaddress1,jobtitle,statuscode,createdon,modifiedon,statecode
$filter=_ownerid_value eq '<crmUserId>' [AND additional filters]
$expand=Lead_ActivityPointers(...),parentaccountid(...)
$orderby=modifiedon desc
```

### Salesforce SOQL 예

```sql
SELECT Id, Salutation, FirstName, LastName, Name, Title, Company, Email,
  LeadSource, Status, OwnerId, LastModifiedDate, LastActivityDate, CreatedDate,
  (SELECT Id, Subject, ActivityDate, Status FROM Tasks ORDER BY ActivityDate DESC LIMIT 1),
  (SELECT Id, Subject, ActivityDateTime FROM Events ORDER BY ActivityDateTime DESC LIMIT 1)
FROM Lead
WHERE OwnerId = '<crmUserId>' AND IsDeleted = false
ORDER BY LastModifiedDate DESC
```

>[!MORELIKETHIS]
>
>* [시작](getting-started.md)
>* [사용자 역할 및 권한](user-roles-permissions.md)
>* [잠재 고객](prospects.md)
