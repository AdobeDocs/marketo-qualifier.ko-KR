---
title: 사용자 역할 및 권한
description: Sales Qualifier 사용자 그룹이 애플리케이션 및 관리 액세스를 제어하는 방법에 대해 알아봅니다.
feature: Agentic AI, Sales Insights, Account Journeys
role: Admin
TQID: 'https://experienceleague.adobe.com/9X9DYGMvLGcPG--G6rHcDEk91hdT9-XYc9wbiL2Qoww'
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4bid: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: e1e0219c-f879-479f-8427-888ed2a6e9c2id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: d6a8091bd893ea80a26edfc1526646aec037223f
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 4%

---


# 사용자 역할 및 권한

Sales Qualifier은 두 개의 필수 사용자 그룹을 사용하여 판매 태스크를 조직 전체 구성과 구분합니다.

## 필수 사용자 그룹

| 그룹 | 누구 | 부여 내용 |
| --- | --- | --- |
| `Sales Qualifier` | 관리자를 포함한 모든 사용자 | 잠재 고객, 계정, 참여 계획, 작업, 성능 및 프로필 설정과 같은 애플리케이션에 대한 액세스 권한. |
| `Sales Qualifier Admins` | `Sales Qualifier` 그룹 외에 관리자만 | 조직 전체의 CRM 연결, 기술 자료 센터 및 규정 준수 설정을 제어하는 **[!UICONTROL 관리 설정]**&#x200B;에 대한 액세스 권한. |

표준 사용자에게는 `Sales Qualifier` 그룹만 필요합니다. 관리자는 두 그룹 모두에서 멤버십이 필요합니다. 이 그룹을 만들려면 [시작하기](getting-started.md)를 참조하세요.

조직에서는 선택적 `Sales Qualifier BDR managers` 그룹도 만들 수 있습니다. 구성원은 전자 메일 성능 보고서에 액세스할 수 있습니다.

## 관리자 액세스

**[!UICONTROL 관리 설정]**&#x200B;은(는) 두 필수 그룹에 속하는 사용자에 대해서만 **[!UICONTROL 관리]**&#x200B;에 표시됩니다. 이러한 설정에 대한 변경 사항은 전체 조직에 적용됩니다.

## 관리자가 제어하는 항목

| 설정 | 구성 위치 | 효과 |
| --- | --- | --- |
| CRM 연결 및 필드 매핑 | [통합](integrations.md#map-crm-fields-inbound-mapping) | 잠재 고객 또는 계정에 대해 표시되는 CRM 필드와 필터로 사용할 수 있는 필드를 결정합니다. |
| 글로벌 이메일 옵트아웃 | [통합](integrations.md#configure-global-email-opt-out) | 모든 아웃바운드 이메일에 구독 취소 바닥글을 추가합니다. |
| 지식 센터 및 플레이북 | [기술 자료 센터](knowledge-center.md) | 회사 플레이북을 아웃바운드 프롬프트 및 [AI 채팅](ai-assistant.md)에서 사용할 수 있도록 합니다. |
| 활동 동기화 | [통합](integrations.md#configure-activity-sync-outbound-mapping) | Sales Qualifier 도달 활동이 CRM에 표시되는지 여부를 결정합니다. |

표준 사용자는 이러한 설정을 사용할 수 있지만 변경할 수는 없습니다. 예상 필터, 플레이북 참조 또는 CRM 필드가 누락된 경우 관리자에게 문의하십시오.

>[!MORELIKETHIS]
>
>* [시작](getting-started.md)
>* [통합](integrations.md)
>* [기술 자료 센터](knowledge-center.md)
