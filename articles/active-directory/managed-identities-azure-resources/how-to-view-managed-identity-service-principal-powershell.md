---
title: PowerShell を使用してマネージド ID のサービス プリンシパルを表示する - Azure AD
description: PowerShell を使用してマネージド ID のサービス プリンシパルを表示するための段階的手順。
services: active-directory
documentationcenter: ''
author: MarkusVi
manager: daveba
editor: ''
ms.service: active-directory
ms.subservice: msi
ms.devlang: na
ms.topic: conceptual
ms.tgt_pltfrm: na
ms.workload: identity
ms.date: 11/29/2018
ms.author: markvi
ms.collection: M365-identity-device-management
ms.openlocfilehash: 9ac2d1d4fc5e669f63bff49a7948db74ec1baa62
ms.sourcegitcommit: dbde4aed5a3188d6b4244ff7220f2f75fce65ada
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/19/2019
ms.locfileid: "74184121"
---
# <a name="view-the-service-principal-of-a-managed-identity-using-powershell"></a>PowerShell を使用してマネージド ID のサービス プリンシパルを表示する

Azure リソースのマネージド ID は、Azure Active Directory で自動的に管理される ID を Azure サービスに提供します。 この ID を使用して、コードに資格情報が含まれていなくても、Azure AD の認証をサポートする任意のサービスに認証することができます。 

この記事では、PowerShell を使用してマネージド ID のサービス プリンシパルを表示する方法について説明します。

[!INCLUDE [az-powershell-update](../../../includes/updated-for-az.md)]

## <a name="prerequisites"></a>前提条件

- Azure リソースのマネージド ID の基本点な事柄については、[概要](overview.md)に関するセクションを参照してください。
- まだ Azure アカウントを持っていない場合は、[無料アカウントを新規登録](https://azure.microsoft.com/free/)してください。
- [仮想マシン](/azure/active-directory/managed-identities-azure-resources/qs-configure-portal-windows-vm#system-assigned-managed-identity)または[アプリケーション](/azure/app-service/overview-managed-identity#adding-a-system-assigned-identity)でシステム割り当ての ID を有効にします。
- 最新バージョンの [Azure PowerShell](/powershell/azure/install-az-ps) をインストールします

## <a name="view-the-service-principal"></a>サービス プリンシパルを表示する

次のコマンドは、システム割り当ての ID を有効にして VM またはアプリケーションのサービス プリンシパルを表示する方法を示しています。 `<VM or application name>` を独自の値に置き換えます。

```powershell
Get-AzADServicePrincipal -DisplayName <VM or application name>
```

## <a name="next-steps"></a>次の手順

PowerShell を使用して Azure AD サービス プリンシパルを表示する方法の詳細については、[Get-AzADServicePrincipal](/powershell/module/az.resources/get-azadserviceprincipal) に関するページを参照してください。


