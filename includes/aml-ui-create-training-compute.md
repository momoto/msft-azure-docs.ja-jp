---
title: インクルード ファイル
description: インクルード ファイル
services: machine-learning
author: peterclu
ms.service: machine-learning
ms.author: peterlu
manager: cgronlund
ms.custom: include file
ms.topic: include
ms.date: 10/09/2019
ms.openlocfilehash: 1ee90e0c99234497b072bbee0b92d76129baea48
ms.sourcegitcommit: a10074461cf112a00fec7e14ba700435173cd3ef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2019
ms.locfileid: "73929650"
---
パイプラインは、ワークスペースにアタッチされたコンピューティング リソースであるコンピューティング先で実行されます。 コンピューティング先を作成した後、それを将来の実行のために再利用できます。

1. キャンバス上部の **[実行]** を選択してパイプラインを実行します。

1. **[設定]** ウィンドウが表示されたら、 **[コンピューティング先を選択]** を選択します。

    使用できるコンピューティング先が既にある場合は、それを選択してこのパイプラインを実行できます。

    > [!NOTE]
    > デザイナーは、Azure Machine Learning コンピューティング先でのみ実験を実行できます。 その他のコンピューティング先は表示されません。

1. コンピューティング リソースの名前を入力します。

1. **[保存]** を選択します。

    ![コンピューティング先を設定する](./media/aml-ui-create-training-compute/set-compute.png)

1. **[実行]** を選択します。

1. **[パイプライン実行のセットアップ]** ダイアログ ボックスで、 **[実験]** の **[+ 新しい実験]** を選択します。

    > [!NOTE]
    > 実験グループの同様のパイプラインは同時に実行されます。 パイプラインを複数回実行する場合は、一連の実行に対して同じ実験を選択できます。

    1. **[実験名]** にわかりやすい名前を入力します。

    1. **[実行]** を選択します。
    
    実行の状態と詳細は、キャンバスの右上で確認できます。

    > [!NOTE]
    > コンピューティング リソースを作成するには約 5 分かかります。 リソースの作成後は、それを再利用できるため、今後の実行では、この待機時間をスキップできます。
    >
    > コンピューティング リソースは、コストを節約するために、アイドル状態のときは 0 ノードに自動スケーリングされます。 しばらくしてからそれを再度使用すると、スケールアップして元に戻すときに約 5 分の待機時間が発生することがあります。
