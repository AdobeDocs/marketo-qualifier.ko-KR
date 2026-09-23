---
title: 마케팅 하이라이트 설정
description: Marketo을 Adobe Marketo Qualifier에 연결하여 담당자가 마케팅 하이라이트에서 라이브 Marketo 활동으로 잠재 고객을 보고 필터링할 수 있는 방법에 대해 알아봅니다.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
    internal-label: Integrations
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 042ebc0019d33019940ff8ad98c0635cb97235f0
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 1%
---

# 마케팅 하이라이트 설정

마케팅 하이라이트는 이메일 열기 및 클릭 수, 웹 방문 횟수 및 양식 채우기와 같은 각 잠재 고객의 라이브 [!DNL Marketo] 활동을 보여줍니다. 이 문서에서는 활동이 유입될 수 있도록 [!DNL Marketo] 인스턴스를 연결하는 방법에 대해 설명합니다.

>[!IMPORTANT]
>
>이 설정을 완료하려면 Adobe Developer Console 및 [!DNL Marketo]의 **[!UICONTROL 관리자]**&#x200B;에 액세스해야 합니다. Adobe 연락처 및 [!DNL Marketo] 관리자와 함께 아래 네 가지 부분을 완료하십시오.

설치 프로그램에는 네 가지 부품이 있습니다.

* A부: Adobe Developer Console에서 API 자격 증명 만들기
* 파트 B: Adobe Marketo 한정자 엔드포인트 및 식별자를 수집합니다.
* 파트 C: [!DNL Marketo Engage]에서 웹후크를 구성합니다.
* D부: Smart Campaign 트리거에 웹후크를 추가합니다.

설정이 완료되면 사용자는 **[!UICONTROL 잠재 고객]** > **[!UICONTROL 마케팅 하이라이트]**&#x200B;에서 이 활동을 보고 필터링합니다.

## A부: API 자격 증명 만들기 {#part-a-create-api-credentials}

이 자격 증명을 사용하면 [!DNL Marketo]에서 Marketo 한정자를 안전하게 인증할 수 있습니다.

인증서를 생성하려면 다음을 수행합니다.

1. [Adobe Developer Console](https://developer.adobe.com/console/)&#x200B;(으)로 이동하여 Adobe ID으로 로그인합니다.
1. **[!UICONTROL 새 프로젝트 만들기]**&#x200B;를 선택하거나 기존 프로젝트를 여십시오.
1. 프로젝트의 이름을 변경하려면 **[!UICONTROL 프로젝트 편집]**&#x200B;을 선택하고 `Marketo Qualifier Marketing Highlights`과(와) 같은 식별 가능한 이름을 입력한 다음 **[!UICONTROL 저장]**&#x200B;을 선택하십시오.
1. **[!UICONTROL API 추가]**&#x200B;를 선택하고 **[!UICONTROL Experience Platform API]**&#x200B;를 선택한 후 **[!UICONTROL 다음]**&#x200B;을 선택합니다.
1. 인증 유형으로 **[!UICONTROL OAuth 서버 간]**&#x200B;을(를) 선택한 후 **[!UICONTROL 다음]**&#x200B;을(를) 선택하십시오.

   **[!UICONTROL OAuth Server-to-Server]**&#x200B;을(를) 사용하면 [!DNL Marketo]에서 사용자가 로그인할 필요 없이 해당 서버에서 직접 Marketo 한정자 API를 호출할 수 있습니다.

1. 45자 이하의 자격 증명 이름을 입력하십시오(예: `Marketo Qualifier Marketing Highlights Creds`).
1. 제품 프로필을 연결하려면 선택한 다음 **[!UICONTROL 구성된 API 저장]**&#x200B;을 선택하십시오.
1. **[!UICONTROL 연결된 자격 증명]**&#x200B;에서 **[!UICONTROL OAuth 서버 간]** 자격 증명을 엽니다. **[!UICONTROL 클라이언트 암호 검색]**&#x200B;을 선택한 다음 **[!UICONTROL 클라이언트 ID]** 및 **[!UICONTROL 클라이언트 암호]**&#x200B;를 복사합니다. [파트 C](#part-c-configure-the-marketo-webhook)에서 이 값을 사용합니다.

>[!WARNING]
>
>클라이언트 암호를 비공개로 유지합니다. 암호처럼 취급하고 이메일로 보내지 마십시오. 조직의 승인된 보안 채널을 사용하여 웹후크를 구성하는 사람과 공유합니다.

## 파트 B: 엔드포인트 및 식별자 수집 {#part-b-gather-your-endpoint-and-identifiers}

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

## C부: Marketo 웹후크 구성 {#part-c-configure-the-marketo-webhook}

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

## D부: Smart Campaign 트리거에 웹후크 추가 {#part-d-add-the-webhook-to-a-trigger-smart-campaign}

기존 Smart Campaign 또는 새 Smart Campaign 트리거에 **[!UICONTROL Call Webhook]** 흐름 단계를 추가합니다. 해당 캠페인의 스마트 목록 트리거는 Marketo Qualifier로 전송되는 활동을 결정합니다.

Webhook를 추가하려면:

1. 기존 트리거 스마트 캠페인을 열거나 새 트리거를 만듭니다(**[!UICONTROL 마케팅 활동]** > **[!UICONTROL 새로 만들기]** > **[!UICONTROL 스마트 캠페인]**).
1. **[!UICONTROL 스마트 목록]** 탭에서 전송할 활동에 대한 트리거 또는 트리거를 추가합니다(예: **[!UICONTROL 전자 메일에서 링크 클릭]**, **[!UICONTROL 양식 작성]** 또는 **[!UICONTROL 웹 페이지 방문]**).
1. **[!UICONTROL 흐름]** 탭에서 **[!UICONTROL 웹후크 호출]** 단계를 추가하고 [파트 C](#part-c-configure-the-marketo-webhook)에서 만든 웹후크를 선택합니다.
1. 스마트 캠페인을 활성화합니다.

해당 Smart Campaign의 활동이 이제 Marketo 한정자로 전송됩니다. 담당자는 **[!UICONTROL 잠재 고객]** > **[!UICONTROL 마케팅 하이라이트]**&#x200B;에서 이 활동을 보고 필터링합니다.

>[!MORELIKETHIS]
>
>* [통합 관리](integrations.md)
>* [잠재 고객](prospects.md)
>* [시작](getting-started.md)
