---
title: PowerShell を使用してデータ アクセスのための RBAC ロールを割り当てる
titleSuffix: Azure Storage
description: PowerShell を使用して、ロールベースのアクセス制御 (RBAC) により Azure Active Directory セキュリティ プリンシパルにアクセス許可を割り当てる方法について説明します。 Azure Storage では、Azure AD を使用した認証用の組み込みとカスタムの RBAC ロールがサポートされています。
services: storage
author: tamram
ms.service: storage
ms.topic: how-to
ms.date: 12/04/2019
ms.author: tamram
ms.reviewer: cbrooks
ms.subservice: common
ms.openlocfilehash: 57d30803f20d17ee31c3d42d9a26e04c1b0832b6
ms.sourcegitcommit: 8bd85510aee664d40614655d0ff714f61e6cd328
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "74892019"
---
# <a name="use-powershell-to-assign-an-rbac-role-for-access-to-blob-and-queue-data"></a>PowerShell を使用して、BLOB およびキュー データへのアクセスのための RBAC ロールを割り当てる

Azure Active Directory (Azure AD) では、[ロールベースのアクセス制御 (RBAC)](../../role-based-access-control/overview.md) を通じて、セキュリティで保護されたリソースへのアクセス権が承認されます。 コンテナーまたはキューへのアクセスに使用される一般的なアクセス許可セットを含む一連の組み込み RBAC ロールは、Azure Storage によって定義されます。

RBAC ロールが Azure AD セキュリティ プリンシパルに割り当てられると、Azure によりそのセキュリティ プリンシパルのリソースへのアクセス権が付与されます。 アクセスのスコープは、サブスクリプション、リソース グループ、ストレージ アカウント、あるいは個別のコンテナーまたはキューのレベルで指定できます。 Azure AD セキュリティ プリンシパルは、Azure リソースのユーザー、グループ、アプリケーション サービス プリンシパル、または[マネージド ID](../../active-directory/managed-identities-azure-resources/overview.md) の場合があります。

この記事では、Azure PowerShell を使用して、組み込みの RBAC ロールの一覧を表示し、ロールをユーザーに割り当てる方法について説明します。 Azure PowerShell の詳細については、「[Azure PowerShell の概要](https://docs.microsoft.com/powershell/azure/overview)」を参照してください。

[!INCLUDE [updated-for-az](../../../includes/updated-for-az.md)]

## <a name="rbac-roles-for-blobs-and-queues"></a>BLOB とキューの RBAC ロール

[!INCLUDE [storage-auth-rbac-roles-include](../../../includes/storage-auth-rbac-roles-include.md)]

## <a name="determine-resource-scope"></a>リソースのスコープを決定する

[!INCLUDE [storage-auth-resource-scope-include](../../../includes/storage-auth-resource-scope-include.md)]

## <a name="list-available-rbac-roles"></a>利用可能な RBAC ロールの一覧を表示する

Azure PowerShell を使用して利用可能な組み込み RBAC ロールの一覧を表示するには、[Get-AzRoleDefinition](/powershell/module/az.resources/get-azroledefinition) コマンドを使用します。

```powershell
Get-AzRoleDefinition | FT Name, Description
```

組み込みの Azure Storage データ ロールが、Azure のその他の組み込みロールとともに表示されます。

```Example
Storage Blob Data Contributor             Allows for read, write and delete access to Azure Storage blob containers and data
Storage Blob Data Owner                   Allows for full access to Azure Storage blob containers and data, including assigning POSIX access control.
Storage Blob Data Reader                  Allows for read access to Azure Storage blob containers and data
Storage Queue Data Contributor            Allows for read, write, and delete access to Azure Storage queues and queue messages
Storage Queue Data Message Processor      Allows for peek, receive, and delete access to Azure Storage queue messages
Storage Queue Data Message Sender         Allows for sending of Azure Storage queue messages
Storage Queue Data Reader                 Allows for read access to Azure Storage queues and queue messages
```

## <a name="assign-an-rbac-role-to-a-security-principal"></a>セキュリティ プリンシパルへの RBAC ロールの割り当て

RBAC ロールをセキュリティ プリンシパルに割り当てるには、[New-AzRoleAssignment](/powershell/module/az.resources/new-azroleassignment) コマンドを使用します。 コマンドの形式は、割り当てのスコープによって異なります。 次の例は、さまざまなスコープでユーザーにロールを割り当てる方法を示していますが、同じコマンドを使用して、任意のセキュリティ プリンシパルにロールを割り当てることができます。

### <a name="container-scope"></a>コンテナー スコープ

コンテナーに対してスコープが指定されたロールを割り当てるには、コンテナーのスコープを含む文字列を `--scope` パラメーターに指定します。 コンテナーのスコープのフォームは次のとおりです。

```
/subscriptions/<subscription>/resourceGroups/<resource-group>/providers/Microsoft.Storage/storageAccounts/<storage-account>/blobServices/default/containers/<container-name>
```

次の例では、*sample-container* という名前のコンテナーにスコープが指定された**ストレージ BLOB データ共同作成者**ロールをユーザーに割り当てます。 サンプルの値とブラケット内のプレースホルダーの値は、実際の値に置き換えてください。 

```powershell
New-AzRoleAssignment -SignInName <email> `
    -RoleDefinitionName "Storage Blob Data Contributor" `
    -Scope  "/subscriptions/<subscription>/resourceGroups/sample-resource-group/providers/Microsoft.Storage/storageAccounts/<storage-account>/blobServices/default/containers/sample-container"
```

### <a name="queue-scope"></a>キュー スコープ

キューに対してスコープが指定されたロールを割り当てるには、キューのスコープを含む文字列を `--scope` パラメーターに指定します。 キューのスコープのフォームは次のとおりです。

```
/subscriptions/<subscription>/resourceGroups/<resource-group>/providers/Microsoft.Storage/storageAccounts/<storage-account>/queueServices/default/queues/<queue-name>
```

次の例では、*sample-queue* という名前のキューに対してスコープが指定された**ストレージ キュー データ共同作成者**ロールをユーザーに割り当てます。 サンプルの値とブラケット内のプレースホルダーの値は、実際の値に置き換えてください。 

```powershell
New-AzRoleAssignment -SignInName <email> `
    -RoleDefinitionName "Storage Queue Data Contributor" `
    -Scope  "/subscriptions/<subscription>/resourceGroups/sample-resource-group/providers/Microsoft.Storage/storageAccounts/<storage-account>/queueServices/default/queues/sample-queue"
```

### <a name="storage-account-scope"></a>ストレージ アカウント スコープ

ストレージ アカウントにスコープが指定されたロールを割り当てるには、ストレージ アカウント リソースのスコープを `--scope` パラメーターに指定します。 ストレージ アカウントのスコープのフォームは次のとおりです。

```
/subscriptions/<subscription>/resourceGroups/<resource-group>/providers/Microsoft.Storage/storageAccounts/<storage-account>
```

次の例は、ストレージ アカウントのレベルでユーザーに対して**ストレージ BLOB データ閲覧者**ロールのスコープを指定する方法を示しています。 サンプルの値は必ず実際の値に置き換えてください。 

```powershell
New-AzRoleAssignment -SignInName <email> `
    -RoleDefinitionName "Storage Blob Data Reader" `
    -Scope  "/subscriptions/<subscription>/resourceGroups/sample-resource-group/providers/Microsoft.Storage/storageAccounts/<storage-account>"
```

### <a name="resource-group-scope"></a>リソース グループ スコープ

リソース グループにスコープが指定されたロールを割り当てるには、リソース グループの名前または ID を `--resource-group` パラメーターに指定します。 次の例は、リソース グループのレベルで**ストレージ キュー データ閲覧者**ロールをユーザーに割り当てています。 サンプルの値とブラケット内のプレースホルダーの値は、実際の値に置き換えてください。 

```powershell
New-AzRoleAssignment -SignInName <email> `
    -RoleDefinitionName "Storage Queue Data Reader" `
    -ResourceGroupName "sample-resource-group"
```

### <a name="subscription-scope"></a>サブスクリプション スコープ

サブスクリプションにスコープが指定されたロールを割り当てるには、サブスクリプションのスコープを `--scope` パラメーターに指定します。 サブスクリプションのスコープのフォームは次のとおりです。

```
/subscriptions/<subscription>
```

次の例は、ストレージ アカウントのレベルで**ストレージ BLOB データ閲覧者**ロールをユーザーに割り当てる方法を示しています。 サンプルの値は必ず実際の値に置き換えてください。 

```powershell
New-AzRoleAssignment -SignInName <email> `
    -RoleDefinitionName "Storage Blob Data Reader" `
    -Scope  "/subscriptions/<subscription>"
```

## <a name="next-steps"></a>次の手順

- [RBAC と Azure PowerShell を使用して Azure リソースへのアクセス権をユーザーに付与する](../../role-based-access-control/role-assignments-powershell.md)
- [RBAC と Azure CLI を使用して Azure BLOB とキューのデータへのアクセスを付与する](storage-auth-aad-rbac-cli.md)
- [Azure portal で RBAC を使用して Azure BLOB とキューのデータへのアクセスを付与する](storage-auth-aad-rbac-portal.md)
