---
title: "CA1415: P-Invoke'ları doğru bildirin | Microsoft Docs"
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
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
ms.openlocfilehash: b1edb0d85d4f00696f03dce0d8bfb6152d6a5042
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49251088"
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



