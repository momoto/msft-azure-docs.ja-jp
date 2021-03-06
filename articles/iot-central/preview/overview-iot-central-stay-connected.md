---
title: Azure IoT Central のデバイス接続機能 | Microsoft Docs
description: この記事では、Azure IoT Central がデバイスの接続と正常性を維持するのにどのように役立つかの概要を説明します。
author: aaronbjork
ms.author: abjork
ms.date: 10/21/2019
ms.topic: conceptual
ms.service: iot-central
services: iot-central
manager: ''
ms.openlocfilehash: 20001247c608a52ffd18920c0b6b1f1aabd28313
ms.sourcegitcommit: cf36df8406d94c7b7b78a3aabc8c0b163226e1bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/09/2019
ms.locfileid: "73894391"
---
# <a name="stay-connected-with-azure-iot-central-preview-features"></a>Azure IoT Central との接続を維持する (プレビュー機能)

[!INCLUDE [iot-central-pnp-original](../../../includes/iot-central-pnp-original-note.md)]

この記事では、Azure IoT Central がデバイスの接続と正常性を維持するのにどのように役立つかの概要を説明します。

大規模な運用のために設計された IoT ソリューションであれば、デバイス管理に対するアプローチが適切に構造化されていることが重要です。 デバイスをクラウドに "接続" させるだけでは十分ではありません。ソリューションの進化、拡大、および経年に応じてデバイスの接続と正常性を維持するためのアプローチが必要です。 Azure IoT Central には、IoT ソリューションのデバイスに、アプリケーションのライフサイクル全体にわたって適切に注意が払われるようにするために必要な機能が用意されています。

## <a name="dashboards"></a>ダッシュボード 
組み込みの[ダッシュボード](howto-manage-devices.md#import-devices)は、デバイスの正常性とテレメトリを監視するための、カスタマイズ可能な領域を備えています。 [アプリケーション テンプレート](howto-use-app-templates.md)の事前構築済みダッシュボードを利用して開始するか、アプリケーションのニーズに合わせた独自のダッシュボードを作成します。 ダッシュボードは、アプリケーション内のすべてのユーザーと共有することも、非公開に保つこともできます。

## <a name="rules-and-actions"></a>ルールとアクション 
デバイスの状態とテレメトリに基づいて[カスタム規則](tutorial-create-telemetry-rules.md)を作成することで、注意を要するデバイスを迅速に特定します。 適切なユーザーに通知するアクションを構成し、適切なタイミングで是正措置が行われるようにします。

## <a name="jobs"></a>[ジョブ] 
[ジョブ](../core/howto-run-a-job.md?toc=/azure/iot-central/preview/toc.json&bc=/azure/iot-central/preview/breadcrumb/toc.json)を使用すると、デバイスのプロパティ、設定、およびコマンドの一括更新を実行できます。 

## <a name="user-roles-and-permissions"></a>ユーザーのロールとアクセス許可
[ロールとアクセス許可](howto-manage-users-roles.md)によって、各ユーザーのエクスペリエンスを調整する機能が提供されています。 UI を通してロールを直接作成し、簡単に適切なアクセス許可を割り当てます。 




