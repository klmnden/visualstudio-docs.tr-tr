---
title: 'CA1017: Derlemeleri ComVisibleAttribute ile işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1017
- MarkAssembliesWithComVisible
helpviewer_keywords:
- MarkAssembliesWithComVisible
- CA1017
ms.assetid: 4842cb49-8dd8-4e5d-a2d6-ceeaf6c6cf8e
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: e6bc88d3932baa5bbb4a723d7a16509831d58146
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923081"
---
# <a name="ca1017-mark-assemblies-with-comvisibleattribute"></a>CA1017: Derlemeleri ComVisibleAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkAssembliesWithComVisible|
|CheckId|CA1017|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir bütünleştirilmiş koda <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> uygulanmış özniteliği yok.

## <a name="rule-description"></a>Kural açıklaması
Özniteliği <xref:System.Runtime.InteropServices.ComVisibleAttribute> , com istemcilerinin yönetilen koda nasıl erişebileceğini belirler. İyi tasarım derlemelerin açıkça COM görünürlüğünde gösterildiğini belirler. Tüm derleme için COM görünürlüğü ayarlanabilir ve sonra bağımsız türler ve tür üyeleri için geçersiz kılınabilir. Özniteliği yoksa, derlemenin içerikleri COM istemcileri tarafından görülebilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, derlemeye özniteliğini ekleyin. Derlemenin COM istemcilerine görünür olmasını istemiyorsanız, özniteliğini uygulayın ve değerini olarak `false`ayarlayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın. Derlemenin görünür olmasını istiyorsanız, özniteliğini uygulayın ve değerini olarak `true`ayarlayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, com istemcilerine görünür olmasını engellemek için <xref:System.Runtime.InteropServices.ComVisibleAttribute> özniteliği uygulanmış bir derlemeyi gösterir.

[!code-cpp[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/CPP/ca1017-mark-assemblies-with-comvisibleattribute_1.cpp)]
[!code-vb[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/VisualBasic/ca1017-mark-assemblies-with-comvisibleattribute_1.vb)]
[!code-csharp[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/CSharp/ca1017-mark-assemblies-with-comvisibleattribute_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)
- [Birlikte Çalışma için .NET Türlerini Niteleme](/dotnet/framework/interop/qualifying-net-types-for-interoperation)