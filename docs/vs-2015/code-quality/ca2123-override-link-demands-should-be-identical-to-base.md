---
title: 'CA2123: Geçersiz kılma bağlantı talepleri taban ile özdeş | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2123
- OverrideLinkDemandsShouldBeIdenticalToBase
helpviewer_keywords:
- OverrideLinkDemandsShouldBeIdenticalToBase
- CA2123
ms.assetid: 4538ecd5-fc6f-4480-ab00-90b2ce4730db
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 338d61db9c24972b7fef656498abd43f8ea0b976
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65687218"
---
# <a name="ca2123-override-link-demands-should-be-identical-to-base"></a>CA2123: Geçersiz kılan bağlantı talepleri taban ile özdeş olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|OverrideLinkDemandsShouldBeIdenticalToBase|
|CheckId|CA2123|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak türde ortak veya korumalı bir yöntem bir yöntemini geçersiz kılan veya bir arabirim uygular ve aynı yok [bağlantı talepleri](https://msdn.microsoft.com/library/a33fd5f9-2de9-4653-a4f0-d9df25082c4d) arabirimi veya sanal bir yöntem.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, arabirim ya da başka bir türdeki sanal yöntem olan temel yöntem ile başka bir yöntemi eşleştirir ve sonra her bir bağlantı talebini inceler. Bir ihlali, yöntemi veya taban yöntemi bağlantı talebi ve diğer yok bildirilir.

 Bu kural ihlal edilirse kötü niyetli arayan yalnızca güvenli olmayan bir yöntem çağırarak bağlantı talebi atlayabilirsiniz.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için aynı bağlantı talebi geçersiz kılma yöntemi veya uygulama için geçerlidir. Bu mümkün değilse tam talep yöntemi işaretlemek veya öznitelik tamamen kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, çeşitli bu kural ihlalleri gösterir.

 [!code-csharp[FxCop.Security.OverridesAndSecurity#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.OverridesAndSecurity/cs/FxCop.Security.OverridesAndSecurity.cs#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 [Güvenli kodlama yönergeleri](https://msdn.microsoft.com/library/4f882d94-262b-4494-b0a6-ba9ba1f5f177) [bağlantı talepleri](https://msdn.microsoft.com/library/a33fd5f9-2de9-4653-a4f0-d9df25082c4d)
