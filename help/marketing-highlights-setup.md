---
title: 마케팅 하이라이트 설정
description: 스마트 캠페인 플로우 단계를 통해 Marketo Engage에서 Marketo Qualifier으로 리드를 보내고, 검토할 마케팅 하이라이트 권장 사항을 얻는 방법에 대해 알아봅니다.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Marketo Qualifier
feature_v2:
  - id: da701e37-3227-4187-b68a-914277252a79
    internal-label: Integrations
subfeature_v2:
  - id: 7b0925d9-0dc0-5c75-a54d-2bcc31c6ebe4
    internal-label: Marketing highlights
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
source-git-commit: adcfe279f38ca319589612820351c48af750bad9
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 1%
---

# 마케팅 하이라이트 설정

Smart Campaign에 **[!UICONTROL Marketo Qualifier으로 보내기]** 흐름 단계를 추가하여 [!DNL Adobe Marketo Engage]에서 [!DNL Adobe Marketo Qualifier]&#x200B;(으)로 리드를 보냅니다. 담당자는 **[!UICONTROL 잠재 고객]** > **[!UICONTROL 마케팅 하이라이트]**&#x200B;에서 잠재 고객 및 해당 잠재 고객을 보낸 활동을 봅니다.

흐름 단계는 두 가지 유형의 스마트 캠페인에서 모두 작동합니다.

* **캠페인 트리거** 이메일 열기 및 클릭 수, 링크 클릭 수, 양식 채우기 및 웹 페이지 방문 수와 같은 작업을 수행할 때 참여를 보냅니다.
* **캠페인 일괄 처리** 캠페인이 실행될 때마다 적격 리드를 보냅니다.

잠재 고객이 아웃바운드 워크플로우의 타깃팅 기준과 일치하는 경우 Marketo Qualifier에서는 연결된 CRM에서 잠재 고객을 해당 소유자에게 전달하는 것을 권장합니다. 소유자는 등록 및 지원 전에 리드를 검토하고 승인합니다. 가망 고객은 자동으로 등록되지 않습니다.

마케팅 하이라이트는 북미, EMEA 및 오스트레일리아의 모든 프로덕션 지역에서 사용할 수 있습니다.

## 시작하기에 앞서 {#before-you-begin}

흐름 단계를 추가하기 전에 다음 전제 조건을 확인하십시오.

* Marketo 관리자가 **[!UICONTROL 관리자]**&#x200B;에서 Marketo Engage 인스턴스에 대해 **[!UICONTROL Marketo Qualifier으로 보내기]**&#x200B;를 설정했습니다.
* Marketo Qualifier이 [Salesforce 또는 Microsoft Dynamics 365](getting-started.md#connect-your-crm)에 연결되어 있으므로 각 리드는 해당 CRM 소유자와 일치할 수 있습니다.

>[!IMPORTANT]
>
>**[!UICONTROL Marketo Qualifier으로 보내기]** 흐름 단계에는 웹후크, 끝점 URL 또는 API 자격 증명이 필요하지 않습니다. 사용하기 위해 Adobe Developer Console에 액세스할 필요가 없습니다. 흐름 단계를 사용할 수 없는 경우 Marketo 관리자에게 문의하십시오.

## Smart Campaign으로 리드 보내기 {#send-leads-with-a-smart-campaign}

기존 Smart Campaign을 사용하거나 전송할 가망 고객 및 활동에 대해 하나를 만듭니다.

1. Marketo Engage에서 스마트 캠페인을 열거나 **[!UICONTROL 마케팅 활동]** > **[!UICONTROL 새로 만들기]** > **[!UICONTROL 스마트 캠페인]**&#x200B;을 선택하여 만드십시오.
1. **[!UICONTROL 스마트 목록]** 탭에서 적합한 잠재 고객을 정의합니다.

   * 트리거 캠페인의 경우 전송할 활동에 대한 트리거를 추가합니다(예: **[!UICONTROL 웹 페이지 방문]**, **[!UICONTROL 웹 페이지에서 링크 클릭]** 또는 **[!UICONTROL 전자 메일의 링크 클릭]**).
   * 배치 캠페인의 경우, 보낼 가망 고객에 대한 필터를 추가합니다.

1. **[!UICONTROL 흐름]** 탭에서 **[!UICONTROL Marketo Qualifier으로 보내기]** 흐름 단계를 추가합니다.
1. 트리거 캠페인을 활성화하거나 배치 캠페인을 실행 또는 예약합니다.
1. Marketo Qualifier에서 **[!UICONTROL 잠재 고객]** > **[!UICONTROL 마케팅 하이라이트]**&#x200B;를 열어 잠재 고객 및 해당 활동을 검토하십시오.

   활동은 잠재 고객이 도착한 방식을 보여 줍니다(예: **[!UICONTROL 일괄 캠페인에서 추가됨]**).

아웃바운드 워크플로우의 타깃팅 기준과 일치하는 리드는 해당 CRM 소유자에게만 권장됩니다. 권장 사항을 검토하려면 **[!UICONTROL 작업]** > **[!UICONTROL 에이전트 제안]**&#x200B;을 여십시오. [마케팅 추천 항목에서 추천 항목 받기](outbound-workflows.md#automatically-enroll-prospects-from-marketing-highlights) 및 [에이전트 제안](tasks.md#agent-suggestions)을 참조하세요.

## 기존 웹후크 설정 {#existing-webhook-setups}

다음 지침은 이전 Webhook 설정에 대해 설명합니다. **[!UICONTROL Marketo Qualifier으로 보내기]** 흐름 단계에는 필요하지 않습니다. 조직에서 이미 웹후크를 사용하고 있는 경우 해당 설정을 변경하기 전에 Marketo 관리자 및 Adobe 담당자와 협력하십시오.

+++Webhook 설정 지침

이 지침을 사용하려면 Adobe Developer Console 및 Marketo Engage의 **[!UICONTROL 관리자]**&#x200B;에 액세스해야 합니다.

### A부: API 자격 증명 만들기 {#part-a-create-api-credentials}

이 자격 증명을 사용하면 [!DNL Marketo]에서 Marketo Qualifier에 안전하게 인증할 수 있습니다.

인증서를 생성하려면 다음을 수행합니다.

1. [Adobe Developer Console](https://developer.adobe.com/console/)&#x200B;(으)로 이동하여 Adobe ID으로 로그인합니다.
1. **[!UICONTROL 새 프로젝트 만들기]**&#x200B;를 선택하거나 기존 프로젝트를 여십시오.
1. 프로젝트의 이름을 변경하려면 **[!UICONTROL 프로젝트 편집]**&#x200B;을 선택하고 `Marketo Qualifier Marketing Highlights`과(와) 같은 식별 가능한 이름을 입력한 다음 **[!UICONTROL 저장]**&#x200B;을 선택하십시오.
1. **[!UICONTROL API 추가]**&#x200B;를 선택하고 **[!UICONTROL Experience Platform API]**&#x200B;를 선택한 후 **[!UICONTROL 다음]**&#x200B;을 선택합니다.
1. 인증 유형으로 **[!UICONTROL OAuth 서버 간]**&#x200B;을(를) 선택한 후 **[!UICONTROL 다음]**&#x200B;을(를) 선택하십시오.

   **[!UICONTROL OAuth Server-to-Server]**&#x200B;을(를) 사용하면 [!DNL Marketo]에서 사용자가 로그인할 필요 없이 서버에서 직접 Marketo Qualifier API를 호출할 수 있습니다.

1. 45자 이하의 자격 증명 이름을 입력하십시오(예: `Marketo Qualifier Marketing Highlights Creds`).
1. 제품 프로필을 연결하려면 선택한 다음 **[!UICONTROL 구성된 API 저장]**&#x200B;을 선택하십시오.
1. **[!UICONTROL 연결된 자격 증명]**&#x200B;에서 **[!UICONTROL OAuth 서버 간]** 자격 증명을 엽니다. **[!UICONTROL 클라이언트 암호 검색]**&#x200B;을 선택한 다음 **[!UICONTROL 클라이언트 ID]** 및 **[!UICONTROL 클라이언트 암호]**&#x200B;를 복사합니다. [파트 C](#part-c-configure-the-marketo-webhook)에서 이 값을 사용합니다.

>[!WARNING]
>
>클라이언트 암호를 비공개로 유지합니다. 암호처럼 취급하고 이메일로 보내지 마십시오. 조직의 승인된 보안 채널을 사용하여 웹후크를 구성하는 사람과 공유합니다.

### 파트 B: 엔드포인트 및 식별자 수집 {#part-b-gather-your-endpoint-and-identifiers}

[파트 C](#part-c-configure-the-marketo-webhook)에 세 개의 값이 필요합니다.

* **끝점 URL**—해당 지역의 Marketo Qualifier 웹후크 주소입니다.
* **imsOrg ID**—Adobe IMS(Identity Management System)의 조직 식별자(양식: `{ORG_ID}@AdobeOrg`).
* **샌드박스 이름** - UI에 표시되는 표시 이름이 아닌 AEP URL(`sname` 값)에 표시되는 것과 동일한 Marketo Qualifier 샌드박스 이름입니다. 소문자 URL 값(예: `Prod`이 아닌 `prod`)을 사용하십시오.

| 지역 | Webhook 끝점 URL |
| --- | --- |
| 북미 | `https://5r6xakp9k3.execute-api.us-east-1.amazonaws.com/prod/external/marketo/signals` |
| EMEA | `https://pc72i8q1k3.execute-api.eu-west-1.amazonaws.com/prod/external/marketo/signals` |
| APAC / 오스트레일리아 | `https://5cxxxyqlai.execute-api.ap-southeast-2.amazonaws.com/prod/external/marketo/signals` |

{style="table-layout:auto"}

지역, imsOrg ID 또는 샌드박스 이름을 잘 모르는 경우 Adobe 담당자가 확인할 수 있습니다.

### C부: Marketo 웹후크 구성 {#part-c-configure-the-marketo-webhook}

Webhook을 생성하려면 다음을 수행합니다.

1. [!DNL Marketo]에서 **[!UICONTROL 관리자]** > **[!UICONTROL 웹후크]**&#x200B;를 선택합니다.
1. **[!UICONTROL 새 웹후크]**&#x200B;를 선택하십시오.
1. **[!UICONTROL URL]**&#x200B;을(를) [파트 B](#part-b-gather-your-endpoint-and-identifiers)의 지역에 대한 끝점 URL로 설정합니다.
1. **[!UICONTROL 요청 유형]**&#x200B;을(를) `POST`(으)로 설정합니다.
1. **[!UICONTROL 요청 토큰 인코딩]**&#x200B;을 `JSON`(으)로 설정합니다. 이 설정은 필수입니다.
1. 아래의 페이로드 템플릿을 **[!UICONTROL 템플릿]**&#x200B;에 붙여 넣으십시오. [!DNL Marketo]의 **[!UICONTROL 토큰 삽입]**&#x200B;을(를) 사용하여 인스턴스의 필드 이름과 일치시킵니다.

   >[!NOTE]
   >
   >JSON 인코딩을 사용하는 경우 문자열 토큰을 따옴표로 묶지 마십시오. [!DNL Marketo]이(가) 자동으로 추가합니다.

   ```json
   {
     "leadId": {{lead.Id:default=0}},
     "email": {{lead.Email Address:default=}},
     "fullName": {{lead.Full Name:default=}},
     "company": {{company.Company Name:default=}},
     "title": {{lead.Job Title:default=}},
     "department": {{lead.Department:default=}},
     "country": {{lead.Country:default=}},
     "score": {{lead.Lead Score:default=0}},
     "rating": {{lead.Lead Rating:default=}},
     "leadStatus": {{lead.Lead Status:default=}},
     "leadSource": {{lead.Lead Source:default=}},
     "isCustomer": {{lead.Is Customer:default=false}},
     "industry": {{company.Industry:default=}},
     "annualRevenue": {{company.Annual Revenue:default=0}},
     "numEmployees": {{company.Num Employees:default=0}},
     "campaignId": {{campaign.id:default=0}},
     "campaignName": {{campaign.name:default=}},
     "programName": {{program.name:default=}},
     "occurredAt": {{system.dateTime:default=}},
     "munchkinId": {{system.munchkinId:default=}},
     "triggerName": {{trigger.Trigger Name:default=}},
     "crmId": {{lead.SFDC ID:default=}},
     "crmType": {{lead.SFDC Type:default=}},
     "crmOwnerEmail": {{lead.Lead Owner Email Address:default=}},
     "crmOwnerFirstName": {{lead.Lead Owner First Name:default=}},
     "crmOwnerLastName": {{lead.Lead Owner Last Name:default=}},
     "attributes": {
       "asset": {{trigger.Name:default=}},
       "link": {{trigger.Link:default=}},
       "subject": {{trigger.Subject:default=}},
       "webPage": {{trigger.Web Page:default=}},
       "category": {{trigger.Category:default=}},
       "details": {{trigger.Details:default=}},
       "sentBy": {{trigger.Sent By:default=}},
       "receivedBy": {{trigger.Received By:default=}},
       "referrer": {{trigger.Referrer:default=}},
       "searchEngine": {{trigger.Search Engine:default=}},
       "searchQuery": {{trigger.Search Query:default=}},
       "imDescription": {{lead.Last Interesting Moment Desc:default=}},
       "imType": {{lead.Last Interesting Moment Type:default=}},
       "imDate": {{lead.Last Interesting Moment Date:default=}},
       "imSource": {{lead.Last Interesting Moment Source:default=}},
       "chatAgentName": {{trigger.Agent Name:default=}},
       "chatAgentEmail": {{trigger.Agent Email:default=}},
       "chatConversationStatus": {{trigger.Conversation Status:default=}},
       "chatConversationSummary": {{trigger.Conversation Summary:default=}},
       "chatGoalName": {{trigger.Goal name:default=}},
       "chatMeetingStatus": {{trigger.meeting status:default=}},
       "chatScheduledFor": {{trigger.Scheduled For:default=}},
       "chatDocumentName": {{trigger.Document Name:default=}},
       "chatDocumentUrl": {{trigger.Document URL:default=}},
       "chatPageUrl": {{trigger.Page URL:default=}}
     }
   }
   ```

1. **[!UICONTROL Webhook 작업]** > **[!UICONTROL 사용자 지정 헤더 설정]**&#x200B;을 선택한 다음 [파트 A](#part-a-create-api-credentials) 및 [파트 B](#part-b-gather-your-endpoint-and-identifiers)의 값을 사용하여 다음 헤더를 추가합니다.

   | Header | 값 |
   | --- | --- |
   | `Content-Type` | `application/json` |
   | `x-client-id` | 클라이언트 ID |
   | `x-client-secret` | 클라이언트 암호 |
   | `x-gw-ims-org-id` | imsOrg ID |
   | `x-sandbox-name` | 샌드박스 이름 |

   {style="table-layout:auto"}

1. **[!UICONTROL 저장]**&#x200B;을 선택합니다.

### D부: Smart Campaign 트리거에 웹후크 추가 {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

기존 Smart Campaign 또는 새 Smart Campaign 트리거에 **[!UICONTROL Call Webhook]** 흐름 단계를 추가합니다. 해당 캠페인의 스마트 목록 트리거는 Marketo Qualifier에 전송되는 활동을 결정합니다.

Webhook를 추가하려면:

1. 기존 트리거 스마트 캠페인을 열거나 새 트리거를 만듭니다(**[!UICONTROL 마케팅 활동]** > **[!UICONTROL 새로 만들기]** > **[!UICONTROL 스마트 캠페인]**).
1. **[!UICONTROL 스마트 목록]** 탭에서 전송할 활동에 대한 트리거 또는 트리거를 추가합니다(예: **[!UICONTROL 전자 메일에서 링크 클릭]**, **[!UICONTROL 양식 작성]** 또는 **[!UICONTROL 웹 페이지 방문]**).
1. **[!UICONTROL 흐름]** 탭에서 **[!UICONTROL 웹후크 호출]** 단계를 추가하고 [파트 C](#part-c-configure-the-marketo-webhook)에서 만든 웹후크를 선택합니다.
1. 스마트 캠페인을 활성화합니다.

이제 해당 Smart Campaign의 활동이 Marketo Qualifier으로 전송됩니다. 담당자는 **[!UICONTROL 잠재 고객]** > **[!UICONTROL 마케팅 하이라이트]**&#x200B;에서 이 활동을 보고 필터링합니다.

+++

>[!MORELIKETHIS]
>
>* [통합 관리](integrations.md)
>* [잠재 고객](prospects.md)
>* [시작](getting-started.md)
