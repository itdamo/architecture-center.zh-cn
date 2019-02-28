---
title: CAF：云原生安全基线策略
titleSuffix: Microsoft Cloud Adoption Framework for Azure
ms.service: architecture-center
ms.subservice: enterprise-cloud-adoption
ms.custom: governance
ms.date: 02/11/2019
description: 云原生安全基线策略
author: BrianBlanchard
ms.openlocfilehash: fc161009f6ce7aa2b775fe6b3b53ff1e1d62a848
ms.sourcegitcommit: 273e690c0cfabbc3822089c7d8bc743ef41d2b6e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2019
ms.locfileid: "55900464"
---
# <a name="cloud-native-security-baseline-policy"></a>云原生安全基线策略

[安全基线](overview.md)是[云治理的五项规则](../governance-disciplines.md)之一。 该规则侧重于常规安全主题，包括网络保护、数字资产、数据等。如[策略评审指南](../policy-compliance/what-is-a-cloud-policy-review.md)中所述，CAF 包含三个级别的**示例策略**：云原生、企业和云设计原则都符合这五种规则。 本文讨论了安全基线策略的云原生示例策略。

> [!NOTE]
> Microsoft 无权决定企业或 IT 策略。 本文旨在帮助你为内部策略评审做好准备。 假定在尝试使用此示例策略之前，将根据你的公司策略对此示例策略进行扩展、验证和测试。 不鼓励使用此示例策略。

## <a name="policy-alignment"></a>策略对齐方式

此示例策略合成了云原生方案，这意味着 Azure 提供的工具和平台足以降低部署中的业务风险。 在此方案中，假定默认 Azure 服务的简单配置提供了足够的资产保护。

## <a name="cloud-security-and-compliance"></a>云安全性和符合性

安全性已集成到 Azure 的各个方面，提供了源自全球安全智能、面向客户的完善控制和安全强化基础结构的独特安全优势。 这一功能强大的组合可帮助保护应用程序和数据，为你遵从法规提供支持，并为所有规模的组织提供符合成本效益的安全性。 这种方法为任何安全策略创建了一个强大的起点，但还是有必要提供与所使用的安全服务相关的同样强大的安全做法。

### <a name="built-in-security-controls"></a>内置安全控件

如果安全控件不直观显示且需要单独进行配置，则很难维护强大的安全基础结构。 Azure 包含各种服务的内置安全控件，可帮助你快速保护数据和工作负载，并跨混合环境管理风险。 借助集成的合作伙伴解决方案，还可轻松将现有保护转移到云。

### <a name="cloud-native-identity-policies"></a>云原生标识策略

标识正在成为安全性的新边界控制平面，而在此之前，人们一直将网络视为边界层。 网络边界出现越来越多的漏洞，与在自带设备 (BYOD) 和云应用程序演变之前相比，边界防御不再那样有效。 Azure 标识管理和访问控制可实现对所有应用程序的无缝、安全访问。

用于跨云和本地目录标识的示例云原生策略可能包括以下要求：

* 通过基于角色的访问控制 (RBAC)、多重身份验证 (MFA) 和单一登录 (SSO) 授权访问资源
* 快速缓解被怀疑遭到泄露的用户标识
* 实时 (JIT)，在逐个任务的基础上授予足够的访问权限，以限制过度特权管理员凭据的泄露
* 通过 Azure Active Directory 扩展用户标识并跨多个环境访问策略

虽然在安全基线的上下文中理解[标识基线](../identity-baseline/overview.md)很重要，但[云治理的五个规则](../overview.md)将[标识基线](../identity-baseline/overview.md)称为独立于安全基线的自己的规则。

### <a name="network-access-policies"></a>网络访问策略

网络控制包括配置、管理和保护网络元素（例如虚拟网络、负载均衡、DNS 和网关）。 这种控制为服务提供了一种通信和互操作的方法。 Azure 包括可靠和安全的网络基础结构以支持应用程序和服务连接需求。 Azure 中的资源之间、本地资源与 Azure 托管的资源之间，以及 Internet 与 Azure 之间都可能存在网络连接。

用于网络控制的云原生策略可能包括以下要求：

* 可能不允许在云原生策略中与本地资源建立混合连接（虽然在 Azure 中技术上可行）。 如果证明混合连接是必要的，那么更强大的企业安全策略示例将是更具相关性的参考。
* 用户可以使用虚拟网络和网络安全组与 Azure 建立安全连接。
* 本机 Microsoft Azure 防火墙通过有限的端口访问保护主机免受恶意网络流量的攻击。 此策略的一个很好的示例是要求通过 RDP - TCP/UDP 端口 3389 阻止（或不启用）直接到 VM 的流量。
* Web 应用程序防火墙和 Azure DDoS 防护等服务可保护应用程序并确保 Azure 中运行的虚拟机的可用性。 不应禁用或滥用这些功能。

### <a name="data-protection"></a>数据保护

在云中保护数据的关键问题之一是考虑数据可能将发生的状态，以及适用于每种状态的控制类型。 根据 Azure 数据安全和加密最佳做法的目的，相关建议主要关注以下数据状态：

* 数据加密控制内置于从虚拟机到存储和 SQL 数据库的服务中。
* 当数据在云和客户之间移动时，可以使用行业标准加密协议对其进行保护。
* 使用 Azure Key Vault，用户能够保护并控制云应用程序和服务使用的加密密钥及其他机密。
* Azure 信息保护有助于对应用中的敏感数据进行分类、标记和保护。

虽然这些功能内置于 Azure 中，但上述每个功能都需要配置，并且可能会增加成本。 强烈建议将每个云原生功能与[数据分类策略](../policy-compliance/what-is-data-classification.md)对齐。

### <a name="security-monitoring"></a>安全监视

安全监视是对资源进行审核的前瞻性策略，可识别不符合组织标准或最佳做法的系统。 Azure 安全中心跨混合云工作负载提供统一的安全基线和高级威胁防护。 有了安全中心，即可对各种工作负载应用安全策略、减少受到的威胁，以及检测和响应攻击，包括：

* 使用 Azure 安全中心在所有本地和云工作负载上获得统一的安全视图
* 用于确保符合性并修复任何漏洞的持续监视和安全评估
* 用于简化调查的交互式工具和上下文威胁智能
* 广泛的日志记录和与现有安全信息的集成

### <a name="extending-cloud-native-policies"></a>扩展云原生策略

使用云可以减少一些安全负担。 Microsoft 为 Azure 数据中心提供物理安全性，并帮助保护云平台免受 DDoS 攻击等基础结构威胁。 鉴于 Microsoft 每天都有成千上万的网络安全专家致力于安全工作，减轻网络攻击的资源相当可观。 事实上，虽然组织曾经担心云是否安全，但现在大多数人都明白，考虑到 Microsoft 等供应商在人员和专业基础设施方面的投资水平，云实际上比大多数本地数据中心更安全。

即使对云原生安全基线进行了此项投资，也建议任何安全基线策略扩展默认的云原生策略。 以下是应考虑的扩展策略示例，即使在云原生环境中也是如此：

* **保护 VM**。 安全应该是每个组织的首要任务，有效地实现它需要几项操作。 必须评估安全状态，防范安全威胁，然后检测并快速响应发生的威胁。
* **保护 VM 内容**。 设置定期自动备份对于防止用户错误至关重要。 但这还不够；还必须确保备份不受网络攻击的影响，并在你需要时可用。
* **监视 VM 和应用程序**。 此模式包含多个任务，包括深入了解 VM 的运行状况，了解它们之间的交互，以及建立监视这些 VM 运行的应用程序的方法。 所有这些任务对于保持应用程序全天候运行都至关重要。

## <a name="next-steps"></a>后续步骤

现在你已经查看了云原生解决方案的示例安全基线策略，请返回[策略审核指南](../policy-compliance/what-is-a-cloud-policy-review.md)开始在此示例的基础上构建你自己的云采用策略。

> [!div class="nextstepaction"]
> [使用“策略评审指南”生成你自己的策略](../policy-compliance/what-is-a-cloud-policy-review.md)