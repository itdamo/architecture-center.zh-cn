---
title: CAF：什么是云策略评审？
description: 什么是云策略评审？
author: BrianBlanchard
ms.date: 2/8/2019
ms.openlocfilehash: b879f261e16ffc72180417e2e0f533e2eaa435ba
ms.sourcegitcommit: 273e690c0cfabbc3822089c7d8bc743ef41d2b6e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2019
ms.locfileid: "55900580"
---
<!-- markdownlint-disable MD026 -->

# <a name="what-is-a-cloud-policy-review"></a>什么是云策略评审？

云策略审核是云中[治理成熟度](../overview.md)迈出的第一步。 此过程的目标是使现有的企业 IT 策略现代化。 完成后，更新的策略可为基于云的资源提供同等级别的风险缓解。 本文介绍了云策略评审流程及其重要性。

## <a name="why-perform-a-cloud-policy-review"></a>为什么要执行云策略评审？

大多数企业通过执行与管理策略一致的流程来管理 IT。 在小型企业中，这些策略可能是轶事式的，流程可能定义不严格。 随着企业发展成为大型企业，往往会更清晰地记录策略和流程并始终如一地执行。

随着公司企业 IT 策略的成熟，对过去技术策略的依赖倾向于渗透到管理策略中。 例如，常见的灾难恢复过程包括强制进行异地磁带备份的策略。 此包含假定依赖于一种类型的技术（磁带备份），该技术可能不再是最相关的解决方案。

云转换创造了一个自然的拐点，重新考虑过去的遗留策略决策。 云中的技术功能和默认流程发生了很大变化，继承风险也是如此。 利用前面的示例，磁带备份策略源于单点故障的风险，即将数据保存在一个位置，业务需要通过降低此风险来最小化风险。 在云部署中，有几个选项可以提供相同的风险缓解，并且恢复时间目标 (RTO) 要低得多。 例如：

- 云原生解决方案可以实现 SQL Azure 数据库的异地复制
- 混合解决方案可以利用 Azure Site Recovery (ASR) 将 IaaS 工作负载复制到多个数据中心

在执行云转换时，策略通常会管理对云采用团队可用的许多工具、服务和流程。 如果这些策略基于传统技术，则可能会阻碍团队推动更改的工作。 在最糟糕的情况下，迁移团队会完全忽略重要的策略来启用变通方案。 两者都不是可接受的结果。

## <a name="the-cloud-policy-review-process"></a>云策略评审流程

云策略评审将现有 IT 治理和 IT 安全策略与[云治理的五个规则](../overview.md)对齐：[成本管理](../cost-management/overview.md)、[安全基线](../security-baseline/overview.md)、[标识基线](../identity-baseline/overview.md)、[资源一致性](../resource-consistency/overview.md)和[部署加速](../deployment-acceleration/overview.md)。

对于这些规则中的每一个，评审流程都遵循以下步骤：

1. 查看与特定规则相关的现有本地策略，查找两个关键数据点：遗留依赖项和已识别的业务风险。
2. 通过提出一个简单的问题来评估每个业务风险：“云模型中是否仍然存在业务风险？”
3. 如果风险仍然存在，请通过记录必要的缓解措施（而不是技术解决方案）重新编写策略。
4. 与云采用团队一起查看更新的策略，以了解所需缓解的潜在解决方案。

## <a name="example-of-a-policy-review-for-a-legacy-policy"></a>遗留策略的策略评审示例

要提供该过程的示例，让我们再次使用前一节中的磁带备份策略：

- 公司策略要求对所有生产系统强制进行异地磁带备份。 在此策略中，可以看到两个感兴趣的数据点：
  - 对磁带备份解决方案的遗留依赖
  - 与在生产设备相同的物理位置存储备份相关的假定业务风险。
- 风险是否仍然存在？ 是的。 即使在云中，依赖单一设施确实会产生一些风险。 此风险影响业务的可能性低于本地解决方案中存在的可能性，但风险仍然存在。
- 重写策略。 对于数据中心范围内的灾难，必须存在一种在停机 24 小时内在不同的数据中心和不同的地理位置恢复生产系统的方法。
- 与云采用团队一起评审。 根据所实施的解决方案，有多种方法可以遵守此资源一致性策略。

## <a name="tools-to-help-create-modern-policies"></a>帮助制定现代策略的工具

为了帮助加速制定现代策略，云治理的五个规则中的每一个都提供了一系列示例策略。 这些示例策略将从三个设计假设之一开始：

- **云原生**：部署的解决方案是云原生的，可以利用 Azure 中的默认解决方案，只需最少的配置。
- **企业版**：部署的解决方案很复杂，需要混合云部署模型。 这需要对某些治理规则进行更复杂的实施。
- **符合云设计原则 (CDP)**：部署的解决方案必须遵循 CDP 中定义的体系结构轴，这需要更高级别的治理。  

对于每个规则，需要在每个级别创建示例策略。 每个示例都旨在触发企业环境中的想法和对话。 请注意，这些示例不能用作正确构建的公司 IT 策略的替代方案。