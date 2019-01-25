---
title: 'CA1600: Boş işlem önceliğini kullanmayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotUseIdleProcessPriority
- CA1600
helpviewer_keywords:
- CA1600
- DoNotUseIdleProcessPriority
ms.assetid: 9b0d073b-78b6-41be-8ef3-14692a735283
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 4002e17e3988ca3b449e141394ce762f95ffc78b
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54833749"
---
# <a name="ca1600-do-not-use-idle-process-priority"></a>CA1600: Boş işlem önceliğini kullanmayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotUseIdleProcessPriority|
|CheckId|CA1600|
|Kategori|Microsoft.Mobility|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bu kural işlemleri ayarlandığından oluşur `ProcessPriorityClass.Idle`.

## <a name="rule-description"></a>Kural Tanımı
 İşlem önceliğini Boşta olarak ayarlamayın. Sahip işlemler `System.Diagnostics.ProcessPriorityClass.Idle` Aksi durumda boş olacak ve bu nedenle beklemeyi engeller, CPU dolduracaktır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Ayarlama işlemleri `ProcessPriorityClass.BelowNormal`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kural yalnızca boş işlem önceliğini gereklidir ve mobility konuları güvenle görmezden gelinebilir atlanması.
