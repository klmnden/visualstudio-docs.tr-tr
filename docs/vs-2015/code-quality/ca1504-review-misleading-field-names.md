---
title: 'CA1504: Yanıltıcı alan adlarını gözden geçirin | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- ReviewMisleadingFieldNames
- CA1504
helpviewer_keywords:
- CA1504
- ReviewMisleadingFieldNames
ms.assetid: 94136ff1-4aaf-4dc2-9170-48c171ab7499
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 3c877580b60209d1f21dac96717dd9ae94183859
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53933375"
---
# <a name="ca1504-review-misleading-field-names"></a>CA1504: Yanıltıcı alan adlarını gözden geçirin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|ReviewMisleadingFieldNames|
|CheckId|CA1504|
|Kategori|Microsoft.Maintainability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Örnek alan adı "kendisinin" ya da adı ile başlatılır bir `static` (`Shared` içinde [!INCLUDE[vbprvb](../includes/vbprvb-md.md)]) alanı "m_" ile başlar.

## <a name="rule-description"></a>Kural Tanımı
 "Kendisinin" ile başlayan alan adları ile statik verileri birden çok kullanıcı tarafından ilişkilendirilir. Benzer şekilde, "m_" ile başlayan alan adlarını, örneği (üye) verileri ile ilişkilidir. Daha kolay tutulan kodunu adları genel olarak kullanılan kuralları izlemelidir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için uygun önekle kullanarak alanı'nı yeniden adlandırın. Alternatif olarak, geçerli son eki ile ekleyerek veya kaldırarak kabul alan olun `static` değiştiricisi.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.
