---
title: 言語サポート - 音声サービス
titleSuffix: Azure Cognitive Services
description: 音声サービスでは、音声翻訳に加え、音声からテキストへの変換とテキストから音声への変換のためのさまざまな言語がサポートされます。 この記事では、サービス機能によってサポートされている言語の包括的な一覧を示します。
services: cognitive-services
author: erhopf
manager: nitinme
ms.service: cognitive-services
ms.subservice: speech-service
ms.topic: conceptual
ms.date: 11/21/2019
ms.author: erhopf
ms.custom: seodec18
ms.openlocfilehash: 8db70ccbabfc165dbe3f7b9a61dbe5023a87f708
ms.sourcegitcommit: 6c01e4f82e19f9e423c3aaeaf801a29a517e97a0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "74815388"
---
# <a name="language-and-region-support-for-the-speech-service"></a>音声サービスの言語とリージョンのサポート

言語サポートは、音声サービスの機能によって異なります。 次の表は、[音声テキスト変換](#speech-to-text)、[テキスト読み上げ](#text-to-speech)、および [音声翻訳](#speech-translation)サービスの言語サポートをまとめたものです。

## <a name="speech-to-text"></a>音声テキスト変換

Microsoft Speech SDK と REST API は、どちらも以下の言語 (ロケール) をサポートしています。 精度を高めるために、"オーディオ + 人間" というラベルが付いたトランスクリプトまたは関連テキスト (文) をアップロードすることにより、言語のサブセットに対してカスタマイズが提供されます。  現在、発音のカスタマイズは `en-US` および `de-DE` でのみ使用できます。 カスタマイズの詳細については、[こちら](how-to-custom-speech.md)を参照してください。

 Locale | 言語 | サポートされています | カスタマイズ可能
------|------------|-----------|-------------
`ar-EG` | アラビア語 (エジプト)、現代標準 | はい | はい
`ar-SA` | アラビア語 (サウジアラビア) | はい | はい
`ar-AE` | アラビア語 (UAE) | はい | はい
`ar-KW` | アラビア語 (クウェート) | はい | はい
`ar-QA` | アラビア語 (カタール) | はい | はい
`ca-ES` | カタルニア語 | はい | いいえ
`da-DK` | デンマーク語 (デンマーク) | はい | いいえ
`de-DE` | ドイツ語 (ドイツ) | はい | はい
`en-AU` | 英語 (オーストラリア) | はい | はい
`en-CA` | 英語 (カナダ) | はい | はい
`en-GB` | 英語 (イギリス) | はい | はい
`en-IN` | 英語 (インド) | はい | はい
`en-NZ` | 英語 (ニュージーランド) | はい | はい
`en-US` | 英語 (米国) | はい | はい
`es-ES` | スペイン語 (スペイン) | はい | はい
`es-MX` | スペイン語 (メキシコ) | はい | はい
`fi-FI` | フィンランド語 (フィンランド) | はい | いいえ
`fr-CA` | フランス語 (カナダ) | はい | はい
`fr-FR` | フランス語 (フランス) | はい | はい
`gu-IN` | グジャラート語 (インド) | はい | はい
`hi-IN` | ヒンディー語 (インド) | はい | はい
`it-IT` | イタリア語 (イタリア) | はい | はい
`ja-JP` | 日本語 (日本) | はい | はい
`ko-KR` | 韓国語 (韓国) | はい | はい
`mr-IN` | マラーティー語 (インド) | はい | はい
`nb-NO` | ノルウェー語 (ブークモール) (ノルウェー) | はい | いいえ
`nl-NL` | オランダ語 (オランダ) | はい | はい
`pl-PL` | ポーランド語 (ポーランド) | はい | いいえ
`pt-BR` | ポルトガル語 (ブラジル) | はい | はい
`pt-PT` | ポルトガル語 (ポルトガル) | はい | はい
`ru-RU` | ロシア語 (ロシア) | はい | はい
`sv-SE` | スウェーデン語 (スウェーデン) | はい | いいえ
`ta-IN` | タミール語 (インド) | はい | はい
`te-IN` | テルグ語 (インド) | はい | はい
`zh-CN` | 中国語 (標準、簡体字) | はい | はい
`zh-HK` | 広東語 (繁体字) | はい | はい
`zh-TW` | 中国語 (台湾標準中国語) | はい | はい
`th-TH` | タイ語 (タイ) | はい | いいえ
`tr-TR` | トルコ | はい | はい

## <a name="text-to-speech"></a>テキスト読み上げ

Microsoft Speech SDK と REST API のどちらでもこれらの音声がサポートされ、そのいずれでもロケールで識別される特定の言語と方言がサポートされています。

> [!IMPORTANT]
> 価格は、標準音声、カスタム音声、ニューラル音声ごとに異なります。 詳細については、[価格](https://azure.microsoft.com/pricing/details/cognitive-services/speech-services/)のページを参照してください。

### <a name="neural-voices"></a>ニューラル音声

ニューラル テキスト読み上げは、ディープ ニューラル ネットワークを利用した新しい種類の音声合成です。 ニューラル音声を使用した場合、合成音声は人間の録音とほとんど区別がつきません。

ニューラル音声を使用すると、チャットボットや音声アシスタントとの対話をより自然で魅力的なものにできます。また、電子書籍などのデジタル テキストをオーディオブックに変換したり、カーナビゲーション システムを強化したりすることもできます。 ニューラル音声では、人間のような自然な韻律と明瞭な発音により、ユーザーが AI システムと対話する際のリスニング疲労が大幅に軽減されます。

ニューラル音声の完全な一覧とリージョン別の提供状況については、[リージョン](regions.md#standard-and-neural-voices)に関するページを参照してください。

Locale | 言語 | 性別 | 完全なサービス名のマッピング | 短い音声名
--------|----------|--------|---------|------------
`de-DE` | ドイツ語 (ドイツ) | 女性 | "Microsoft Server Speech Text to Speech Voice (de-DE, KatjaNeural)" | "de-DE-KatjaNeural"
`en-US` | 英語 (米国) | 男性 | "Microsoft Server Speech Text to Speech Voice (en-US, GuyNeural)" | "en-US-GuyNeural"
`en-US` | 英語 (米国) | 女性 | "Microsoft Server Speech Text to Speech Voice (en-US, JessaNeural)" | "en-US-JessaNeural"
`it-IT` | イタリア語 (イタリア) | 女性 |"Microsoft Server Speech Text to Speech Voice (it-IT, ElsaNeural)" | "it-IT-ElsaNeural"
`zh-CN` | 中国語 (大陸) | 女性 | "Microsoft Server Speech Text to Speech Voice (zh-CN, XiaoxiaoNeural)" | "zh-CN-XiaoxiaoNeural"

> [!NOTE]
> 音声合成要求には、完全なサービス名のマッピングまたは短い音声名のいずれかを使用できます。

### <a name="standard-voices"></a>標準音声

テキストから合成音声への変換用に、45 を超える言語とロケールで 75 を超える標準的な音声が用意されています。 リージョン別の提供状況の詳細については、[リージョン](regions.md#standard-and-neural-voices)に関するページを参照してください。

Locale | 言語 | 性別 | 完全なサービス名のマッピング | 短い名前
-------|----------|---------|----------|----------
<sup>&dagger;</sup>`ar-EG` | アラビア語 (エジプト) | 女性 | "Microsoft Server Speech Text to Speech Voice (ar-EG, Hoda)" | "ar-EG-Hoda"
`ar-SA` | アラビア語 (サウジアラビア) | 男性 | "Microsoft Server Speech Text to Speech Voice (ar-SA, Naayf)" | "ar-SA-Naayf"
`bg-BG` | ブルガリア語 | 男性 | "Microsoft Server Speech Text to Speech Voice (bg-BG, Ivan)" | "bg-BG-Ivan"
`ca-ES` | カタルニア語 (スペイン) | 女性 | "Microsoft Server Speech Text to Speech Voice (ca-ES, HerenaRUS)" | "ca-ES-HerenaRUS"
`cs-CZ` | チェコ語 | 男性 | "Microsoft Server Speech Text to Speech Voice (cs-CZ, Jakub)" | "cs-CZ-Jakub"
`da-DK` | デンマーク語 | 女性 | "Microsoft Server Speech Text to Speech Voice (da-DK, HelleRUS)" | "da-DK-HelleRUS"
`de-AT` | ドイツ語 (オーストリア) | 男性 | "Microsoft Server Speech Text to Speech Voice (de-AT, Michael)" | "de-AT-Michael"
`de-CH` | ドイツ語 (スイス) | 男性 | "Microsoft Server Speech Text to Speech Voice (de-CH, Karsten)" | "de-CH-Karsten"
`de-DE` | ドイツ語 (ドイツ) | 女性 | "Microsoft Server Speech Text to Speech Voice (de-DE, Hedda)" | "de-DE-Hedda"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (de-DE, HeddaRUS)" | "de-DE-HeddaRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (de-DE, Stefan, Apollo)" | "de-DE-Stefan-Apollo"
`el-GR` | ギリシャ語 | 男性 | "Microsoft Server Speech Text to Speech Voice (el-GR, Stefanos)" | "el-GR-Stefanos"
`en-AU` | 英語 (オーストラリア) | 女性 | "Microsoft Server Speech Text to Speech Voice (en-AU, Catherine)" | "en-AU-Catherine"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (en-AU, HayleyRUS)" | "en-AU-HayleyRUS"
`en-CA` | 英語 (カナダ) | 女性 | "Microsoft Server Speech Text to Speech Voice (en-CA, Linda)" | "en-CA-Linda"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (en-CA, HeatherRUS)" | "en-CA-HeatherRUS"
`en-GB` | 英語 (英国) | 女性 | "Microsoft Server Speech Text to Speech Voice (en-GB, Susan, Apollo)" | "en-GB-Susan-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (en-GB, HazelRUS)" | "en-GB-HazelRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (en-GB, George, Apollo)" | "en-GB-George-Apollo"
`en-IE` | 英語 (アイルランド) | 男性 | "Microsoft Server Speech Text to Speech Voice (en-IE, Sean)" | "en-IE-Sean"
`en-IN` | 英語 (インド) | 女性 | "Microsoft Server Speech Text to Speech Voice (en-IN, Heera, Apollo)" | "en-IN-Heera-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (en-IN, PriyaRUS)" | "en-IN-PriyaRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (en-IN, Ravi, Apollo)" | "en-IN-Ravi-Apollo"
`en-US` | 英語 (米国) | 女性 | "Microsoft Server Speech Text to Speech Voice (en-US, ZiraRUS)" | "en-US-ZiraRUS"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (en-US, JessaRUS)" | "en-US-JessaRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (en-US, BenjaminRUS)" | "en-US-BenjaminRUS"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (en-US, Jessa24kRUS)" | "en-US-Jessa24kRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (en-US, Guy24kRUS)" | "en-US-Guy24kRUS"
`es-ES` | スペイン語 (スペイン) |女性 | "Microsoft Server Speech Text to Speech Voice (es-ES, Laura, Apollo)" | "es-ES-Laura-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (es-ES, HelenaRUS)" | "es-ES-HelenaRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (es-ES, Pablo, Apollo)" | "es-ES-Pablo-Apollo"
`es-MX` | スペイン語 (メキシコ) | 女性 | "Microsoft Server Speech Text to Speech Voice (es-MX, HildaRUS)" | "es-MX-HildaRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (es-MX, Raul, Apollo)" | "es-MX-Raul-Apollo"
`fi-FI` | フィンランド語 | 女性 | "Microsoft Server Speech Text to Speech Voice (fi-FI, HeidiRUS)" | "fi-FI-HeidiRUS"
`fr-CA` | フランス語 (カナダ) |女性 | "Microsoft Server Speech Text to Speech Voice (fr-CA, Caroline)" | "fr-CA-Caroline"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (fr-CA, HarmonieRUS)" | "fr-CA-HarmonieRUS"
`fr-CH` | フランス語 (スイス)| 男性 | "Microsoft Server Speech Text to Speech Voice (fr-CH, Guillaume)" | "fr-CH-Guillaume"
`fr-FR` | フランス語 (フランス)| 女性 | "Microsoft Server Speech Text to Speech Voice (fr-FR, Julie, Apollo)" | "fr-FR-Julie-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (fr-FR, HortenseRUS)" | "fr-FR-HortenseRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (fr-FR, Paul, Apollo)" | "fr-FR-Paul-Apollo"
`he-IL` | ヘブライ語 (イスラエル) | 男性| "Microsoft Server Speech Text to Speech Voice (he-IL, Asaf)" | "he-IL-Asaf"
`hi-IN` | ヒンディー語 (インド) | 女性 | "Microsoft Server Speech Text to Speech Voice (hi-IN, Kalpana, Apollo)" | "hi-IN-Kalpana-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (hi-IN, Kalpana)" | "hi-IN-Kalpana"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (hi-IN, Hemant)" | "hi-IN-Hemant"
`hr-HR` | クロアチア語 | 男性 | "Microsoft Server Speech Text to Speech Voice (hr-HR, Matej)" | "hr-HR-Matej"
`hu-HU` | ハンガリー語 | 男性 | "Microsoft Server Speech Text to Speech Voice (hu-HU, Szabolcs)" | "hu-HU-Szabolcs"
`id-ID` | インドネシア語| 男性 | "Microsoft Server Speech Text to Speech Voice (id-ID, Andika)" | "id-ID-Andika"
`it-IT` | イタリア語 | 男性 | "Microsoft Server Speech Text to Speech Voice (it-IT, Cosimo, Apollo)" | "it-IT-Cosimo-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (it-IT, LuciaRUS)" | "it-IT-LuciaRUS"
`ja-JP` | 日本語 | 女性 | "Microsoft Server Speech Text to Speech Voice (ja-JP, Ayumi, Apollo)" | "ja-JP-Ayumi-Apollo"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (ja-JP, Ichiro, Apollo)" | "ja-JP-Ichiro-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (ja-JP, HarukaRUS)" | "ja-JP-HarukaRUS"
`ko-KR` | 韓国語 | 女性 | "Microsoft Server Speech Text to Speech Voice (ko-KR, HeamiRUS)" | "ko-KR-HeamiRUS"
`ms-MY` | マレー語 | 男性 | "Microsoft Server Speech Text to Speech Voice (ms-MY, Rizwan)" | "ms-MY-Rizwan"
`nb-NO` | ノルウェー語 | 女性 | "Microsoft Server Speech Text to Speech Voice (nb-NO, HuldaRUS)" | "nb-NO-HuldaRUS"
`nl-NL` | オランダ語 | 女性 | "Microsoft Server Speech Text to Speech Voice (nl-NL, HannaRUS)" | "nl-NL-HannaRUS"
`pl-PL` | ポーランド語 | 女性 | "Microsoft Server Speech Text to Speech Voice (pl-PL, PaulinaRUS)" | "pl-PL-PaulinaRUS"
`pt-BR` | ポルトガル語 (ブラジル) | 女性 | "Microsoft Server Speech Text to Speech Voice (pt-BR, HeloisaRUS)" | "pt-BR-HeloisaRUS"
| | | 男性 |"Microsoft Server Speech Text to Speech Voice (pt-BR, Daniel, Apollo)" | "pt-BR-Daniel-Apollo"
`pt-PT` | ポルトガル語 (ポルトガル) | 女性 | "Microsoft Server Speech Text to Speech Voice (pt-PT, HeliaRUS)" | "pt-PT-HeliaRUS"
`ro-RO` | ルーマニア語 | 男性 | "Microsoft Server Speech Text to Speech Voice (ro-RO, Andrei)" | "ro-RO-Andrei"
`ru-RU` |ロシア語| 女性 | "Microsoft Server Speech Text to Speech Voice (ru-RU, Irina, Apollo)" | "ru-RU-Irina-Apollo"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (ru-RU, Pavel, Apollo)" | "ru-RU-Pavel-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (ru-RU, EkaterinaRUS)" | ru-RU-EkaterinaRUS
`sk-SK` | スロバキア語 | 男性 | "Microsoft Server Speech Text to Speech Voice (sk-SK, Filip)" | "sk-SK-Filip"
`sl-SI` | スロベニア語 | 男性 | "Microsoft Server Speech Text to Speech Voice (sl-SI, Lado)" | "sl-SI-Lado"
`sv-SE` | スウェーデン語 | 女性 | "Microsoft Server Speech Text to Speech Voice (sv-SE, HedvigRUS)" | "sv-SE-HedvigRUS"
`ta-IN` | タミール語 (インド) | 男性 | "Microsoft Server Speech Text to Speech Voice (ta-IN, Valluvar)" | "ta-IN-Valluvar"
`te-IN` | テルグ語 (インド) | 女性 | "Microsoft Server Speech Text to Speech Voice (te-IN, Chitra)" | "te-IN-Chitra"
`th-TH` | タイ語 | 男性 | "Microsoft Server Speech Text to Speech Voice (th-TH, Pattara)" | "th-TH-Pattara"
`tr-TR` | トルコ語 | 女性 | "Microsoft Server Speech Text to Speech Voice (tr-TR, SedaRUS)" | "tr-TR-SedaRUS"
`vi-VN` | ベトナム語 | 男性 | "Microsoft Server Speech Text to Speech Voice (vi-VN, An)" | "vi-VN-An"
`zh-CN` | 中国語 (大陸) | 女性 | "Microsoft Server Speech Text to Speech Voice (zh-CN, HuihuiRUS)" | "zh-CN-HuihuiRUS"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (zh-CN, Yaoyao, Apollo)" | "zh-CN-Yaoyao-Apollo"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (zh-CN, Kangkang, Apollo)" | "zh-CN-Kangkang-Apollo"
`zh-HK` | 中国語 (香港) | 女性 | "Microsoft Server Speech Text to Speech Voice (zh-HK, Tracy, Apollo)" | "zh-HK-Tracy-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (zh-HK, TracyRUS)" | "zh-HK-TracyRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (zh-HK, Danny, Apollo)" | "zh-HK-Danny-Apollo"
`zh-TW` | 中国語 (台湾) | 女性 | "Microsoft Server Speech Text to Speech Voice (zh-TW, Yating, Apollo)" | "zh-TW-Yating-Apollo"
| | | 女性 | "Microsoft Server Speech Text to Speech Voice (zh-TW, HanHanRUS)" | "zh-TW-HanHanRUS"
| | | 男性 | "Microsoft Server Speech Text to Speech Voice (zh-TW, Zhiwei, Apollo)" | "zh-TW-Zhiwei-Apollo"

&dagger; *ar-EG では現代標準アラビア語 (MSA) をサポートしています。*

> [!NOTE]
> 音声合成要求には、完全なサービス名のマッピングまたは短い音声名のいずれかを使用できます。

### <a name="customization"></a>カスタマイズ

音声のカスタマイズは、`de-DE`、`en-GB`、`en-IN`、`en-US`、`es-MX`、`fr-FR`、`it-IT`、`pt-BR`、および `zh-CN` に使用できます。 カスタム音声モデルをトレーニングする必要があるトレーニング データと一致する適切なロケールを選択します。 たとえば、持っている録音データが英国アクセントの英語で話されている場合は、`en-GB` を選択します。

> [!NOTE]
> カスタム音声では、中国語と英語のバイリンガルを除き、バイリンガル モデル トレーニングはサポートされていません。 英語も話すことができる中国人の音声をトレーニングする場合は、[Chinese-English bilingual]\(中国語 - 英語のバイリンガル\) を選択します。 すべてのロケールの音声トレーニングは、任意のサイズのトレーニング データから始めることができる `en-US` と `zh-CN` を除き、2,000 以上の発話のデータ セットから始まります。

## <a name="speech-translation"></a>音声翻訳

**Speech Translation** API では、音声を音声に翻訳し、音声をテキストに翻訳するために、さまざまな言語をサポートしています。 ソース言語は、音声テキスト変換言語の表に常に含まれている必要があります。 使用可能なターゲット言語は、何に翻訳するか (音声かテキストか) によって決まります。 受信した音声は [60 言語](https://www.microsoft.com/translator/business/languages/)以上に翻訳できます。 一部の言語は[音声合成](language-support.md#text-languages)に利用できます。

### <a name="text-languages"></a>テキスト言語

| テキスト言語    | 言語コード |
|:----------- |:-------------:|
| アフリカーンス語      | `af`          |
| アラビア語       | `ar`          |
| ベンガル語      | `bn`          |
| ボスニア語 (ラテン)      | `bs`          |
| ブルガリア語      | `bg`          |
| 広東語 (繁体字)      | `yue`          |
| カタルニア語      | `ca`          |
| 中国語 (簡体字)      | `zh-Hans`          |
| 中国語 (繁体字)      | `zh-Hant`          |
| クロアチア語      | `hr`          |
| チェコ語      | `cs`          |
| デンマーク語      | `da`          |
| オランダ語      | `nl`          |
| 英語      | `en`          |
| エストニア語      | `et`          |
| フィジー語      | `fj`          |
| フィリピン語      | `fil`          |
| フィンランド語      | `fi`          |
| フランス語      | `fr`          |
| ドイツ語      | `de`          |
| ギリシャ語      | `el`          |
| ハイチ・クレオール語      | `ht`          |
| ヘブライ語      | `he`          |
| ヒンディー語      | `hi`          |
| ミャオ語      | `mww`          |
| ハンガリー語      | `hu`          |
| インドネシア語      | `id`          |
| イタリア語      | `it`          |
| 日本語      | `ja`          |
| スワヒリ語      | `sw`          |
| クリンゴン語      | `tlh`          |
| クリンゴン語 (plqaD)      | `tlh-Qaak`          |
| 韓国語      | `ko`          |
| ラトビア語      | `lv`          |
| リトアニア語      | `lt`          |
| マダガスカル語      | `mg`          |
| マレー語      | `ms`          |
| マルタ語      | `mt`          |
| ノルウェー語      | `nb`          |
| ペルシャ語      | `fa`          |
| ポーランド語      | `pl`          |
| ポルトガル語      | `pt`          |
| オトミ語      | `otq`          |
| ルーマニア語      | `ro`          |
| ロシア語      | `ru`          |
| サモア語      | `sm`          |
| セルビア語 (キリル文字)      | `sr-Cyrl`          |
| セルビア語 (ラテン)      | `sr-Latn`          |
| スロバキア語     | `sk`          |
| スロベニア語      | `sl`          |
| スペイン語      | `es`          |
| スウェーデン語      | `sv`          |
| タヒチ語      | `ty`          |
| タミル語      | `ta`          |
| テルグ語      | `te`          |
| タイ語      | `th`          |
| トンガ語      | `to`          |
| トルコ語      | `tr`          |
| ウクライナ語      | `uk`          |
| ウルドゥー語      | `ur`          |
| ベトナム語      | `vi`          |
| ウェールズ語      | `cy`          |
| ユカテコ語      | `yua`          |


## <a name="next-steps"></a>次の手順

* [音声サービス試用版サブスクリプションを取得する](https://azure.microsoft.com/try/cognitive-services/)
* [C# で音声を認識する方法を確認する](~/articles/cognitive-services/Speech-Service/quickstarts/speech-to-text-from-microphone.md?pivots=programming-language-chsarp)
