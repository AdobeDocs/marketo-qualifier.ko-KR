---
title: '[!DNL Adobe Marketo Qualifier] 릴리스 정보'
description: '[!DNL Adobe Marketo Qualifier]의 새로운 기능을 알아봅니다.'
feature: Agentic AI, Sales Insights, Account Journeys
role: User
source-git-commit: bf94a2d28913093923f446025405339e4e64919c
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 11%
---
# [!DNL Adobe Marketo Qualifier] 릴리스 정보

## 예정된 릴리스

* 스마트 대상(Beta)을 통해 올바른 계정과 잠재 고객을 찾아 우선 순위를 지정합니다. 원하는 계정을 일반 언어로 설명하고 CRM 데이터 및 성장 신호를 추가하고 채점된 잠재 고객을 검토한 다음 아웃바운드 워크플로우에 추가합니다. [자세히 알아보기](smart-audience.md)
* 연락처 및 영업 기회 필드와 함께 계정 필드별로 연락처를 필터링하여 올바른 연락처를 찾고 아웃바운드 워크플로우를 보다 정확하게 타깃팅합니다. [자세히 알아보기](prospects.md#filter-and-find-prospects)
* 연락처에는 관련 계정 및 소유자 이름이 표시되며, 이제 잠재 고객의 페이지에 30일에서 90일 동안의 마케팅 활동이 표시됩니다. [자세히 알아보기](prospects.md#review-prospect-details)

## 10-08-2026

이번 릴리스에는 다음이 포함됩니다.

* 아웃바운드 워크플로우를 재사용하거나 실행 중인 워크플로우의 터치포인트를 변경한 후 복제하고 사본을 편집합니다. 복사본은 잠재 고객이 없는 비공개 초안으로 시작하며 원래 워크플로우는 변경되지 않습니다. [자세히 알아보기](outbound-workflows.md#duplicate-an-outbound-workflow)
* 목표, 타기팅, 터치포인트 및 설정 간의 탐색을 통해 컴팩트한 레이아웃으로 아웃바운드 워크플로우를 구성합니다. [자세히 알아보기](outbound-workflows.md#create-an-outbound-workflow)
* 이메일 답글의 옵트아웃 요청 지우기는 자동으로 인식됩니다. 잠재 고객이 옵트아웃으로 표시되며 더 이상의 터치포인트는 전송되지 않습니다. [자세히 알아보기](outbound-workflows.md#opt-out-requests-in-replies)
* 웹 조사와 제품별 고객 사례 연구를 결합한 간단한 브리핑을 통해 관련성 및 식별된 소스별로 작성된 토론 요점을 준비합니다. [자세히 알아보기](prospects.md#generate-meeting-prep)
* 생성된 이메일은 품질 지침에 따라 검사되고 필요할 때 다시 작성한 후 검토합니다. 모든 이메일이 전송되기 전에 여전히 검토, 편집 및 승인합니다. [자세히 알아보기](outbound-workflows.md#review-and-refine-generated-emails)

## 09-22-2026

이번 릴리스에는 다음이 포함됩니다.

* 포함된 CRM 플러그 인에서 [!DNL Marketo Sales Insights] 및 agentic 데이터를 보고 [!DNL Marketo Qualifier]에 잠재 고객을 추가하십시오. [자세히 알아보기](admin-settings.md#crm-mcp-and-the-embedded-plugin)
* 최상의 선택, 내 시청 목록, 웹 활동, 이메일 참여 및 웨비나 활동으로 CRM 잠재 고객의 우선 순위를 지정합니다. [자세히 알아보기](admin-settings.md#prioritize-leads-in-the-crm-plugin)
* 실시간 [!DNL Marketo] 활동이 워크플로 기준과 일치하는 경우 아웃바운드 워크플로에 잠재 고객을 자동으로 등록합니다. [자세히 알아보기](home.md#automatically-enroll-prospects-from-marketing-highlights)
* 잠재 고객 컨텍스트를 검토하고 잠재 고객 목록을 내보내고 [!DNL Marketo Optimizer] Prime 및 Ultimate 인스턴스에서 AI 사용자 요약을 봅니다. [자세히 알아보기](prospects.md#review-prospect-context-and-export-the-list)
* 작업 대기열에서 생성된 잠재 고객 이메일을 검토 및 승인하고 아웃바운드 워크플로우 동안 에이전트 제안을 회신 [자세히 알아보기](tasks.md)

## 09-08-2026

이번 릴리스에는 다음이 포함됩니다.

* 프로필 설정에서 사용자 자신의 이메일 드래프팅 스타일을 한 번 설정하면 생성된 모든 이메일이 이를 따릅니다. [자세히 알아보기](profile-settings.md#email-drafting-context)
* 새 모임 리서치 탭에서 잠재 고객의 페이지에서 목표 기반 또는 사용자 지정 모임 준비를 생성합니다. [자세히 알아보기](prospects.md#generate-meeting-prep)
* 관리자는 팀원에게 아웃바운드 워크플로우를 할당하고 워크플로우 설정을 기본값으로 재설정할 수 있습니다. [자세히 알아보기](outbound-workflows.md#create-an-outbound-workflow)
* CSV에서 잠재 고객을 가져올 때 사용자 지정 필드를 매핑하고 생성된 이메일에서 해당 값을 사용합니다. [자세히 알아보기](prospects.md#build-your-prospect-list)
* 생성된 이메일은 사용자가 가져오는 모든 추가 잠재 고객 데이터를 사용하며 기본적으로 잠재 고객의 언어로 작성될 수 있습니다. [자세히 알아보기](outbound-workflows.md#step-5-add-prospects-and-start-email-generation)
* 아웃바운드 성과는 기본적으로 열람률과 클릭률을 보여주며 원시 카운트 및 조직 수준의 총 잠재 고객에 대한 토글이 표시됩니다. [자세히 알아보기](performance.md)
* CRM 동기화 규칙은 전망이 아웃바운드 워크플로우를 통해 이동할 때 CRM 상태를 자동으로 업데이트합니다. [자세히 알아보기](admin-settings.md#configure-crm-sync-rules)
* [!DNL Marketo Qualifier], CRM, [!DNL Marketo] 및 [!DNL Marketo Optimizer] 데이터에서 AI 채팅에 질문합니다. [자세히 알아보기](ai-assistant.md#ask-ai-chat-across-your-connected-data)

## 08-17-2026

[!DNL Marketo Qualifier]은(는) 이제 독립 실행형 앱으로 사용할 수 있습니다. [!DNL Marketo Engage] 및 [!DNL Marketo Optimizer]을(를) 지원합니다.

이번 릴리스에는 다음이 포함됩니다.

* AI가 생성한 활동 요약 및 신호 기반 점수를 통한 잠재 고객 및 계정 우선 순위 지정. 잠재 고객 또는 [계정](accounts.md#account-insights)에 대해 [자세히 알아보기](prospects.md#review-prospect-details).
* AI가 제안한 케이던스 및 초안 이메일이 포함된 목표 기반 아웃바운드 워크플로우입니다. [자세히 알아보기](outbound-workflows.md)
* 전화 통화, LinkedIn InMails 및 이메일 검토를 위한 통합 작업 대기열. [자세히 알아보기](tasks.md)
* 달력 통합을 통한 자동 모임 예약. [자세히 알아보기](outbound-workflows.md#meeting-booking)
* 자체 플레이북 자료에 AI 전달을 위한 지식 센터. [자세히 알아보기](admin-settings.md#knowledge-center)
* CRM, 참여 및 지식 센터 데이터를 기반으로 하는 자연어 질문에 대한 AI 채팅. [자세히 알아보기](ai-assistant.md)
* 이메일 및 모임 예약 성과 보고서. [자세히 알아보기](performance.md)
* CRM 또는 Outlook에서 액세스할 수 있는 브라우저 및 전자 메일 플러그인. [자세히 알아보기](admin-settings.md#crm-mcp-and-the-embedded-plugin)
* Salesforce 및 Microsoft Dynamics 365 통합 지원. [자세히 알아보기](integrations.md)
