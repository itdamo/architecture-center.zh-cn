---
title: CAF：Azure 安全指南
titleSuffix: Microsoft Cloud Adoption Framework for Azure
ms.service: architecture-center
ms.subservice: enterprise-cloud-adoption
ms.custom: governance
ms.date: 02/11/2019
description: Microsoft 提供哪些安全指南？
author: BrianBlanchard
ms.openlocfilehash: 845b02422e2df63425e29acdfd9b43b744934c9f
ms.sourcegitcommit: 273e690c0cfabbc3822089c7d8bc743ef41d2b6e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2019
ms.locfileid: "55900467"
---
<!-- markdownlint-disable MD026 -->

# <a name="what-security-guidance-does-microsoft-provide"></a>Microsoft 提供哪些安全指南？

## <a name="security-guidance-and-tools"></a>安全指南和工具

Microsoft 引入了[服务信任平台](https://servicetrust.microsoft.com)和合规性管理器，可帮助解决以下问题：

- 应对合规性管理挑战
- 履行满足监管要求的责任
- 对企业云服务利用率执行自助审核和风险评估

这些工具旨在帮助组织在选择和使用 Microsoft 云服务时，履行复杂的合规性义务并改进数据保护功能。

服务信任平台 (STP) 提供了详尽的信息和工具，可帮助用户满足使用 Microsoft 云服务（包括 Azure、Office 365、Dynamics 365 和 Windows）的需求。 STP 是一站式服务，提供与 Microsoft 云相关的安全、监管、合规性和隐私信息。 我们在上面发布对云服务和工具执行自助风险评估所需的信息和资源。 创建 STP 是为了帮助跟踪 Azure 中的法规遵从性活动，其中包括：

- 合规性管理器：合规性管理器是 Microsoft 服务信任平台中一个基于工作流的风险评估工具，可用于跟踪、分配和验证组织与 Microsoft 云服务（例如 Office 365、Dynamics 365 和 Azure）相关的法规遵从性活动。 下一节将对其做详细介绍。
- 信任文档：目前有三类指南可提供丰富的资源来评估 Microsoft 云，了解 Microsoft 在安全性、合规性和隐私方面的举措；并帮助用户采取行动来改进数据保护功能。 其中包括：
- 审核报表：使用审核报表，可以随时了解 Microsoft 云服务的最新隐私、安全性和合规性相关信息。 这包括 ISO、SOC、FedRAMP 和其他审计报表、桥接信函以及与 Microsoft 云服务（如 Azure、Office 365、Dynamics 365 等）的独立第三方审核相关的材料。
- 数据保护指南：数据保护指南提供有关 Microsoft 云服务如何保护数据的信息，并介绍如何管理组织的云数据安全性和合规性。 其中包括深入研究的白皮书，详细介绍了 Microsoft 如何设计和运营云服务、常见问题解答，年终安全评估报表、渗透测试结果，以及帮助用户进行风险评估和改进数据保护功能的指南。
- Azure 安全性与合规性蓝图：蓝图提供的资源可帮助你生成和启动云支持的应用程序，进而遵守严格的法规和标准。 凭借比任何其他云提供商更多的认证，你可以放心地将关键工作负载部署到 Azure，其蓝图包括：

- 行业特定的概述和指导
- 客户责任矩阵
- 具有威胁模型的参考架构
- 控制实现矩阵
- 部署参考体系结构的自动化系统
- 隐私资源：提供数据保护影响评估、数据主体请求 (DSR) 和数据泄露通知的文档，用户可将其纳入自己的问责制计划，从而支持一般数据保护条例 (GDPR)。

- GDPR 入门：Microsoft 产品和服务可帮助组织在收集或处理个人数据时符合 GDPR 要求。 STP 旨在提供有关 Microsoft 服务中可用于满足 GDPR 特定要求的功能信息。 该文档可在 GDPR 问责制方面提供帮助，并且有助于理解技术和组织措施。 提供数据保护影响评估、数据主体请求 (DSR) 和数据泄露通知的文档，用户可将其纳入自己的问责制计划，从而支持 GDPR。
  - 数据主体请求：GDPR 授予个人（或数据主体）在其个人数据处理方面的某些权利。 其中包括纠正不准确数据，擦除数据或限制数据处理，以及接收数据和完成将数据传输到另一个控制方的请求的权利。
  - 数据安全漏洞：GDPR 强制执行在发生个人数据安全漏洞时向数据控制方和处理者发出通知的要求。 STP 提供以下信息：Microsoft 如何首先尝试阻止安全漏洞；Microsoft 如何检测到安全漏洞；Microsoft 如何在发生安全漏洞时做出响应并通知作为数据控制方的你。
  - 数据保护影响评估：Microsoft 将帮助控制方完成 GDPR 数据保护影响评估。 GDPR 提供必须执行 DPIA 时的详尽清单，例如，自动处理分析和类似活动；处理大量特殊类别的个人数据，以及对公共可访问区域进行大规模系统监测。
  - 其他资源：除了上述部分中讨论的工具指南外，STP 还提供了其他资源，包括区域合规性、安全与合规中心的其他资源，以及有关服务信任平台、合规性管理器和隐私/GDPR 的常见问题。
- 区域合规性：STP 为 Microsoft 在线服务提供了大量合规性文档和指南，用于满足包括捷克共和国、波兰和罗马尼亚在内的不同地区的合规性要求。

## <a name="unique-intelligent-insights"></a>独特的智能见解

随着安全性信号的数量和复杂性的增加，要确定这些信号是否是可信威胁，然后采取行动，这个过程需要花费太长时间。 Microsoft 提供了无与伦比的云安全智能，有助于快速检测和修正威胁。

## <a name="azure-threat-intelligence"></a>Azure 威胁智能

通过使用安全中心内提供的“威胁智能”选项，IT 管理员可根据环境识别安全威胁。 例如，可以识别某台特定的计算机是否是僵尸网络的一部分。 当攻击者非法安装秘密将此计算机连接到命令和控制的恶意软件时，该计算机就成为了僵尸网络的节点。 威胁智能还可以识别来自地下通信通道（例如暗网）的潜在威胁。

为了构建这种威胁智能系统，安全中心使用 Microsoft 中来自多个源的数据。 安全中心使用此数据根据环境识别潜在威胁。 “威胁智能”窗格包括三个主要选项：

- 检测到的威胁类型
- 威胁源
- 威胁智能地图

## <a name="machine-learning-in-azure-security-center"></a>Azure 安全中心中的机器学习

Azure 安全中心深入分析了来自各种 Microsoft 和合作伙伴解决方案的大量数据，可帮助用户实现更高的安全性。 为了利用这些数据，公司使用数据科学和机器学习来预防威胁、进行检测并执行最终调查。

从广义上讲，Azure 机器学习有助于实现两个目标：

## <a name="next-generation-detection"></a>下一代检测

攻击者愈发趋于自动化和复杂化。 他们也使用数据科学。 他们会反向工程保护并生成可支持行为突变的系统。 他们将自己的活动伪装成噪音，并从错误中快速学习。 机器学习可帮助我们应对这些演变趋势。

## <a name="simplified-security-baseline"></a>简化的安全基准

做出有效的安全决策并非易事。 它需要具备安全性方面的经验和专业知识。 一些大型组织拥有这样的专家，但许多公司却没有。 Azure 机器学习使客户在做出安全决策时，能够从其他组织的智慧中受益。

## <a name="behavioral-analytics"></a>行为分析

行为分析是一种技术，该技术会对数据进行分析并将数据与一系列已知模式对比。 不过，这些模式不是简单的特征， 需要对大型数据集运用复杂的机器学习算法来确定。 或者由分析专家通过仔细分析恶意行为来确定。 Azure 安全中心可以使用行为分析对虚拟机日志、虚拟网络设备日志、结构日志、故障转储和其他资源进行分析，确定受攻击的资源。