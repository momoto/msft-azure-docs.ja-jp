---
title: 動的ディクショナリ - Translator Text API
titleSuffix: Azure Cognitive Services
description: この記事では、Azure Cognitive Services Translator Text API の動的ディクショナリ機能の使用方法について説明します。
services: cognitive-services
author: swmachan
manager: nitinme
ms.service: cognitive-services
ms.subservice: translator-text
ms.topic: conceptual
ms.date: 06/04/2019
ms.author: swmachan
ms.openlocfilehash: 5f007660b98a22ff9ffad072991a39cf59518b6a
ms.sourcegitcommit: 35715a7df8e476286e3fee954818ae1278cef1fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "73837354"
---
# <a name="how-to-use-a-dynamic-dictionary"></a>動的ディクショナリを使用する方法

単語や語句に適用する翻訳があらかじめわかっている場合は、それを要求内でマークアップとして指定することができます。 動的ディクショナリは、固有名詞や製品名のような複合名詞に対してのみ安全に使用できます。

**構文:**

<mstrans:dictionary translation="translation of phrase">phrase</mstrans:dictionary>

**要件:**

* `From` と `To` の言語は異なっている必要があります。 
* 自動検出機能を使用する代わりに、API translation 要求に `From` パラメーターを含める必要があります。 

**例: en-de:**

ソース入力:The word <mstrans:dictionary translation=\"wordomatic\">word or phrase</mstrans:dictionary> is a dictionary entry.

ターゲット出力:Das Wort "wordomatic" ist ein Wörterbucheintrag.

この機能は、HTML を使用する場合と使用しない場合で同じように動作します。

この機能は慎重に使用する必要があります。 翻訳をカスタマイズするには、Custom Translator を使用するのが適切で望ましい方法です。 Custom Translator では、コンテキストおよび統計的確率を最大限に活用します。 コンテキスト内の単語または語句を表示するトレーニング データがある場合、またはそれを作成できる場合、はるかに良い結果が得られます。 Custom Translator の詳細については、[https://aka.ms/CustomTranslator](https://aka.ms/CustomTranslator) で確認できます。
