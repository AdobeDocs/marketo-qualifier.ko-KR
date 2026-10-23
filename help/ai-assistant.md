---
title: AI 채팅 사용
description: '[!DNL Adobe Marketo Qualifier]에서 AI Chat을 사용하여 계정을 조사하고, 봉사 활동 초안을 작성하고, CRM, 참여 및 지식 센터 데이터를 기반으로 답변을 얻는 방법에 대해 알아봅니다.'
feature: Agentic AI, Sales Insights, Account Journeys
role: User
TQID: 'https://experienceleague.adobe.com/LHCHAk0rsNwLsKFhKMlHaLL7xkkCEAKFNDMEonb2TdQ'
product_v2:
  - id: d98caee2-fd67-486e-9513-36435358ebff
    internal-label: Adobe Marketo Qualifier
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
    internal-label: Artificial intelligence
source-git-commit: bf94a2d28913093923f446025405339e4e64919c
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 1%
---

# AI 채팅

AI Chat은 판매 컨텍스트를 기반으로 자연어 질문에 답변합니다. [!DNL Adobe Marketo Qualifier]을(를) 종료하지 않고 계정을 조사하고, 통화를 준비하고, 봉사 활동 초안을 작성하고, 작업의 우선 순위를 매기는 데 사용합니다.

![AI 채팅 단추](assets/ai-chat.png){width="800" zoomable="yes"}

## AI 채팅 열기

채팅 패널을 열려면 부동 **[!UICONTROL AI 채팅]** 버튼을 선택합니다. 잠재 고객, 계정 또는 아웃바운드 워크플로우를 볼 수 있도록 현재 페이지 옆에 패널이 열립니다. 패널의 크기를 조정하려면 가장자리를 드래그합니다. 패널을 닫으려면 **[!UICONTROL AI 채팅]**&#x200B;을 다시 선택하세요.

>[!NOTE]
>
>AI Chat 사용 가능 여부는 조직의 구성 및 권한에 따라 다릅니다. **[!UICONTROL AI 채팅]** 단추가 나타나지 않으면 계정에 대해 기능이 활성화되지 않습니다.

## 데이터 소스

AI Chat은 다음 소스를 사용할 수 있습니다.

* [지식 센터](admin-settings.md#knowledge-center)에 있는 조직의 플레이북입니다.
* 잠재 고객, 연락처, 계정, 기회 및 활동을 포함한 연결된 CRM입니다.
* [!DNL Marketo] 활동 및 참여 데이터.
* Account Qualification Agent이 수집한 계정 연구 및 최근 뉴스입니다.
* 공개 웹 조사.

## AI 채팅 사용

다음 유형의 작업에 AI 채팅 사용:

* **조사 및 요약**: 거래처, 구매 그룹 또는 잠재 고객의 최근 참여에 대한 요약을 요청하세요.
* **빌드 위치 지정**: 회의 전에 도우미에게 특정 계정에 대한 솔루션을 배치하도록 요청하십시오.
* **초안 작성 및 세분화**: 전자 메일을 작성하거나 다시 작성하도록 요청하세요. 색조, 길이, 언어 및 이모지를 포함할지 여부를 지정합니다.
* **권장 사항 가져오기**: 우선 순위를 지정할 잠재 고객 또는 계정을 요청하거나 새 아웃바운드 워크플로우에 대한 목표 또는 케이던스를 요청합니다.
* **연락처 세부 정보 찾기**: 도우미에게 연락처와 배경 정보를 추가하여 잠재 고객을 보강하도록 요청하십시오.

## 연결된 데이터 전체에 걸쳐 AI 채팅에 묻기

AI Chat은 [!DNL Marketo Qualifier], CRM, [!DNL Marketo], [!DNL Marketo Optimizer] 및 회사 인텔리전스 데이터에서 질문에 답변할 수 있습니다. 정보를 조회하거나 컨텍스트를 검색하려면 일반 언어로 질문하십시오. 이러한 연결된 데이터 조회는 데이터를 읽고 보고합니다. 프로그램이나 캠페인을 만들거나 편집하거나 시작하지는 않습니다.

다음은 몇 가지 샘플 프롬프트입니다. 프롬프트에서 더 구체적일수록 결과는 더 집중됩니다.

잠재 고객 및 계정:

* &quot;참여 상태가 새로운 잠재 고객을 찾습니다.&quot;
* &quot;Adobe 회사를 조사하라.&quot;
* &quot;잠재 고객에 대한 전체 프로필을 나에게 주세요.&quot;
* &quot;지난 30일 동안의 아웃바운드 성능을 표시합니다.&quot;
* 지난 30일 동안의 예약된 회의를 나열합니다.

기술 자료 센터:

* &quot;가격 이의를 처리할 때 이용할 수 있는 담보는 무엇입니까?&quot;
* &quot;경쟁사와 차별화되는 주요 차별화 요소는 무엇입니까?&quot;
* &quot;지식 센터에 문서를 나열합니다.&quot;
* &quot;문서 요약&quot;

CRM:

* &quot;열린 기회를 나열합니다.&quot;
* &quot;이름과 이메일로 처음 5개의 잠재 고객을 나열합니다.&quot;
* &quot;잠재 고객 또는 거래처에 대한 영업 활동 표시&quot;

[!DNL Marketo]:

* &quot;내 스마트 캠페인 찾아보기&quot;
* &quot;이름이 &#39;획득됨&#39;인 스마트 목록을 가져옵니다.&quot;
* &quot;내 프로그램을 찾아보거나 이름으로 프로그램을 가져옵니다.&quot;
* &quot;[!DNL Marketo] 활동 유형을 나열합니다.&quot;

[!DNL Adobe Journey Optimizer B2B Edition]:

* &quot;여정이 몇 개나 있습니까?&quot;
* &quot;성향은 내 대상자를 어떻게 분할합니까?&quot;
* &quot;내 계정에는 어떤 랜딩 페이지가 있습니까?&quot;
* &quot;어떤 리드 필드가 채점으로 연결됩니까?&quot;

회사 정보:

* &quot;기업이 사용하는 기술은 무엇입니까?&quot;
* &quot;회사에 대한 최근 뉴스를 표시합니다.&quot;
* &quot;지정된 회사와 유사한 회사를 찾습니다.&quot;
* &quot;회사에 대한 빈 일자리 목록을 작성하라.&quot;

### 현재 범위 및 제한

* 연결된 데이터 조회를 읽고 데이터에 대해 보고합니다. 프로그램을 만들거나, 캠페인을 시작하거나, CRM 레코드를 편집하지 않습니다.
* [스마트 대상(Beta)](smart-audience.md)에서 채팅은 목록 저장, 정보 열 추가, 계정 및 잠재 고객 필터링 및 우선 순위 지정, 기존 아웃바운드 워크플로우에 선택한 잠재 고객 추가 등 대상 목록에 대한 작업을 지원합니다. CRM에 기록되지 않거나 이메일 검토 및 승인을 대체하지 않습니다.
* AI 채팅은 정보를 조회합니다. 보고 도구가 아닙니다. 해당 분기의 이메일 상태 또는 지난 10일 동안 만든 잠재 고객 목록과 같은 [!DNL Marketo] 스타일의 분석 또는 시간 경과에 따른 트렌드를 빌드하지 않습니다. 이 작업에 기본 [!DNL Marketo] 보고를 사용합니다.

## 플레이북의 기본 답변

[기술 자료 센터](admin-settings.md#knowledge-center) 플레이북을 사용하려면 질문에 있는 기술 자료 센터를 참조하세요. 예:

`From the Knowledge Center, help me position our security solution for ABC Corp ahead of tomorrow's call.`

응답은 플레이북의 메시지를 반영합니다.

## 응답에 대한 피드백 제공

엄지손가락 위로 또는 엄지손가락 아래로 컨트롤을 사용하여 생성된 콘텐츠를 평가합니다. 귀하의 피드백은 향후 응답을 개선하는 데 도움이 됩니다.

## AI 응답 검토

AI가 생성한 응답은 정확하지 않을 수 있습니다. 사용하기 전에 모든 콘텐츠를 검토하십시오.

* 사실, 이름, 숫자를 신뢰하기 전에 확인하세요.
* 초안 이메일을 주의 깊게 읽고 보내기 전에 개인화합니다.
* 완성된 결과물이 아닌 어시스턴트의 출력을 시작점으로 사용합니다.

Adobe Generative AI 용어는 조직의 AI 채팅 사용을 제어합니다.

>[!MORELIKETHIS]
>
>* [기술 자료 센터](admin-settings.md#knowledge-center)
>* [계정](accounts.md)
>* [아웃바운드 워크플로](outbound-workflows.md)
