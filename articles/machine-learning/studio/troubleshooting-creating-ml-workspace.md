---
title: ワークスペースのトラブルシューティング
titleSuffix: ML Studio (classic) - Azure
description: このガイドでは、クラシック バージョンの Azure Machine Learning Studio ワークスペースの設定に伴い、よく生じることのある問題の解決策を説明します。
services: machine-learning
ms.service: machine-learning
ms.subservice: studio
ms.topic: conceptual
author: xiaoharper
ms.author: amlstudiodocs
ms.custom: previous-author=heatherbshapiro, previous-ms.author=hshapiro
ms.date: 03/20/2017
ms.openlocfilehash: 88f4e1edae84892892d1a8a9e76499d71d551abf
ms.sourcegitcommit: 35715a7df8e476286e3fee954818ae1278cef1fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "73838034"
---
# <a name="troubleshooting-guide-create-and-connect-to-an-azure-machine-learning-studio-classic-workspace"></a>トラブルシューティング ガイド:Azure Machine Learning Studio (クラシック) ワークスペースの作成と接続
このガイドでは、Azure Machine Learning Studio (クラシック) ワークスペースの設定に伴い、よく生じることのある問題の解決策を説明します。



## <a name="workspace-owner"></a>ワークスペースの所有者
Machine Learning Studio (クラシック) でワークスペースを開くには、ワークスペースを作成する際に使用した Microsoft アカウントにサインインするか、所有者からワークスペースへの参加の招待を受け取る必要があります。 ワークスペースの管理は Azure Portal で実行できます。アクセス許可もポータルで構成できます。

ワークスペースの管理方法の詳細については、「[Azure Machine Learning Studio (クラシック) ワークスペースの管理]」をご覧ください。

[Azure Machine Learning Studio (クラシック) ワークスペースの管理]: manage-workspace.md

## <a name="allowed-regions"></a>許可されたリージョン
現在、Machine Learning は一部のリージョンでのみ利用できます。 サブスクリプションに対象のリージョンが含まれていない場合は、"許可されたリージョンにサブスクリプションがありません" というエラー メッセージが表示されることがあります。

サブスクリプションへのリージョンの追加を要求するには、Azure Portal で Microsoft サポート要求を新規作成し、問題の種類として **[課金]** を選択して、プロンプトに従って要求を送信します。

## <a name="storage-account"></a>ストレージ アカウント
Machine Learning サービスでは、データを格納するためのストレージ アカウントが必要です。 既存のストレージ アカウントを使用するか、新しい Machine Learning Studio (クラシック) ワークスペースの作成時に新しいストレージ アカウントを作成することができます (新しいストレージ アカウントを作成するためのクォータがある場合)。

新しい Machine Learning Studio (クラシック) ワークスペースの作成後は、ワークスペースの作成に使用した Microsoft アカウントで Machine Learning Studio (クラシック) にサインインできます。 エラー メッセージ「ワークスペースが見つかりません」(次のスクリーン ショットに類似) が発生する場合は、次の手順に従ってブラウザーの Cookie を削除します。

![Workspace not found](media/troubleshooting-creating-ml-workspace/screen3.png)

**ブラウザーの Cookie を削除するには**

1. Internet Explorer を使用している場合は、右上隅の **[ツール]** をクリックして、 **[インターネット オプション]** を選択します。  

   ![[インターネット オプション]](media/troubleshooting-creating-ml-workspace/screen4.png)

2. **[全般]** タブで、 **[削除]** をクリックします。

   ![[全般] タブ](media/troubleshooting-creating-ml-workspace/screen5.png)

3. **[閲覧の履歴の削除]** ダイアログ ボックスで、 **[クッキーと Web サイト データ]** が選択されていることを確認し、 **[削除]** をクリックします。

   ![Cookie の削除](media/troubleshooting-creating-ml-workspace/screen6.png)

Cookie が削除されたら、ブラウザーを再起動し、[Microsoft Azure Machine Learning Studio (クラシック)](https://studio.azureml.net) ページに移動します。 ユーザー名とパスワードの入力が求められたら、ワークスペースの作成時に使用したアカウントと同じ Microsoft アカウントを入力します。

## <a name="comments"></a>説明

目的は、可能な限り円滑でシームレスに Machine Learning を体験していただくことです。 お客様の操作の円滑化をお手伝いできるよう、コメントや問題がありましたら、 [Azure Machine Learning フォーラム](https://social.msdn.microsoft.com/Forums/windowsazure/home?forum=MachineLearning) に投稿してください。
