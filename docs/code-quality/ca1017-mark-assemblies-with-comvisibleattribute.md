---
title: 'CA1017: Derlemeleri ComVisibleAttribute ile işaretleyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 85c3abdce2845cc46e92ae6b0c4c9d565562bcad
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54959284"
---
# <a name="ca1017-mark-assemblies-with-comvisibleattribute"></a>CA1017: Derlemeleri ComVisibleAttribute ile işaretleyin

|||
|-|-|
|TypeName|MarkAssembliesWithComVisible|
|CheckId|CA1017|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir derleme olmayan <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> özniteliğinin.

## <a name="rule-description"></a>Kural açıklaması
 <xref:System.Runtime.InteropServices.ComVisibleAttribute> Özniteliği COM istemcilerinin yönetilen kod nasıl eriştiğini belirler. İyi tasarım derlemelerin açıkça COM görünürlüğünde gösterildiğini belirler. COM görünürlüğü tüm bir derleme için ayarlanabilir ve sonra bireysel tür ve tür üyeleri için geçersiz kılındı. Öznitelik yoksa derleme içeriği COM istemcilerine görülebilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için özniteliği derlemeye ekleyin. Derlemenin COM istemcilerine görünür olmasını istemiyorsanız özniteliğini uygulayın ve değerini ayarlamak `false`.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Derleme görünür olmasını istiyorsanız, özniteliğini uygulayın ve değerini ayarlamak `true`.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir derlemeye gösterir <xref:System.Runtime.InteropServices.ComVisibleAttribute> COM istemcilerine görünür olmasını engellemek için uygulanan bir öznitelik.

 [!code-cpp[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/CPP/ca1017-mark-assemblies-with-comvisibleattribute_1.cpp)]
 [!code-vb[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/VisualBasic/ca1017-mark-assemblies-with-comvisibleattribute_1.vb)]
 [!code-csharp[FxCop.Design.AssembliesCom#1](../code-quality/codesnippet/CSharp/ca1017-mark-assemblies-with-comvisibleattribute_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)
- [Birlikte Çalışma için .NET Türlerini Niteleme](/dotnet/framework/interop/qualifying-net-types-for-interoperation)