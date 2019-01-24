---
title: "CA1415: P-Invoke'ları doğru bildirin | Microsoft Docs"
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1415
- DeclarePInvokesCorrectly
helpviewer_keywords:
- CA1415
- DeclarePInvokesCorrectly
ms.assetid: 42a90796-0264-4460-bf97-2fb4a093dfdc
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 5fa1473d96d8b74b07497ef72a0a92bcf80e1fe3
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54770588"
---
# <a name="ca1415-declare-pinvokes-correctly"></a>CA1415: P/Invoke'ları doğru bildirin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DeclarePInvokesCorrectly|
|CheckId|CA1415|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|P/Invoke, parametre bildirirse bölünemez - derlemenin dışından görülemez. P/Invoke parametresi bildiren derlemesi dışında görülebilir, - kesiliyor.|

## <a name="cause"></a>Sebep
 Bir platform çağırma yöntemi hatalı bildirilmiş.

## <a name="rule-description"></a>Kural Tanımı
 Bir platform yöntemi erişimleri yönetilmeyen kod çağırmak ve tarafından tanımlanan `Declare` anahtar sözcüğünü [!INCLUDE[vbprvb](../includes/vbprvb-md.md)] veya <xref:System.Runtime.InteropServices.DllImportAttribute?displayProperty=fullName>. Bu kural için platform çağırma işaretçiniz bir ÇAKIŞAN yapı parametresine Win32 işlevlerini hedef yöntem bildirimleri ve yönetilen bir işaretçi değil. şu anda görünür bir <xref:System.Threading.NativeOverlapped?displayProperty=fullName> yapısı.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için doğru platform bildirin yöntemi çağır.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte gösterildiği platform çağırma kuralı ihlal ediyor ve kural karşılamak yöntemler.

 [!code-csharp[FxCop.Interoperability.DeclarePInvokes#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.DeclarePInvokes/cs/FxCop.Interoperability.DeclarePInvokes.cs#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 [Yönetilmeyen Kod ile Birlikte Çalışma](http://msdn.microsoft.com/library/ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258)
