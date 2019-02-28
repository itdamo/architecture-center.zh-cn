---
title: CAF：大型企业 – 大型企业的多层治理
titleSuffix: Microsoft Cloud Adoption Framework for Azure
ms.service: architecture-center
ms.subservice: enterprise-cloud-adoption
ms.custom: governance
ms.date: 02/11/2019
description: 大型企业 – 大型企业的多层治理
author: BrianBlanchard
ms.openlocfilehash: 42f4159ca0701c6a798f239359509a3e3b246c38
ms.sourcegitcommit: 273e690c0cfabbc3822089c7d8bc743ef41d2b6e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/08/2019
ms.locfileid: "55900591"
---
# <a name="multiple-layers-of-governance-in-large-enterprises"></a>大型企业的多层治理

当大型企业需要进行多层治理时，必须在治理 MVP 和以后的治理演变中考虑到更高级别的复杂性。

此类复杂性的几个常见示例包括：

- 分布式治理功能。
- 企业 IT 支持业务部门 IT 组织。
- 企业 IT 支持按地理位置分布的 IT 组织。

本文探讨了应对此类复杂性的一些方法。

## <a name="large-enterprise-governance-is-a-team-sport"></a>大型企业治理是一项团队运动

大型成熟企业通常拥有专门的团队和员工，专注于整个治理过程中所涉及的规则。 此过程演示了使治理成为一项团队运动的方法。

在许多大型企业中，云治理规则可能会阻碍云的采用。 在整个企业内开发标识、安全性、操作、部署和配置方面的云专业技能需要时间。 全面实现 IT 治理策略和 IT 安全可能会使创新速度减缓数月甚至数年。 平衡业务创新需求和保护现有资源的治理需求是很微妙的。

云的固有功能可以消除创新障碍，但也会增加风险。 在此治理过程中，我们展示了示例公司如何建立防范措施来降低风险。 在其他团队生成必要的云成熟度时，云治理团队采用基于风险的方法来治理可部署的内容，而不是处理保护环境所需的每项规则。 最重要的是，当每个团队达到云成熟度时，治理团队将整体应用其解决方案。 随着每个团队逐渐成熟并添加到整个解决方案，云治理团队可以打开阶段关卡，以便大力推进更多的创新和采用。

该模型演示了云治理团队和现有企业团队（安全、IT 治理、网络、标识和其他）之间合作关系的发展。 这一过程从治理 MVP 开始，并通过治理演变发展到整体最终状态。

## <a name="requirements-to-supporting-such-a-team-sport"></a>支持此类团队运动的要求

多层治理模型的第一个要求是了解治理层次结构。 回答以下问题将帮助你了解常规治理层次结构：

- 如何跨业务部门分配云核算（云服务计费）？
- 如何跨企业 IT 和每个业务部门分配治理职责？
- 每个 IT 部门都管理哪些类型的环境？

## <a name="central-governance-of-a-distributed-governance-hierarchy"></a>分布式治理层次结构的中心治理

借助管理组等工具，企业 IT 可以创建与治理层次结构匹配的层次结构。 诸如 Azure 蓝图这样的工具可以将资产应用到该层次结构的不同层。 可以对 Azure 蓝图进行版本控制，将各种版本应用于管理组、订阅或资源组。 其中的每个概念将在治理 MVP 中做出详细描述。

其中每个工具的重要方面是能够对一个层次结构应用多个蓝图。 因此，治理可以是一个分层过程。 下面是此分层治理应用程序的一个示例：

- 企业 IT：企业 IT 创建一组适用于所有云采用的标准和策略。 这是在“基线”蓝图中具体实现的。 然后，企业 IT 拥有管理组层次结构，确保基线的一个版本应用于层次结构中的所有订阅。
- 地区或业务部门 IT：各种 IT 团队可以通过创建自己的蓝图来应用额外的治理层。 这些蓝图将创建附加策略和标准。 开发完成后，企业 IT 就可以将这些蓝图应用到管理组层次结构中的适用节点。
- 云采用团队：关于应用程序或工作负载的详细决策和实现可以由云采用团队在治理要求的上下文中完成。 有时团队还可以请求额外的 Azure 资源一致性模板来加速采用进程。

关于每个级别的治理实现的详细信息需要每个团队之间的协调。 在此过程中概述的治理 MVP 和治理演变可以帮助调整这一协调。