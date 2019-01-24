---
title: 'CA1017: Derlemeleri ComVisibleAttribute ile işaretleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1017
- MarkAssembliesWithComVisible
helpviewer_keywords:
- MarkAssembliesWithComVisible
- CA1017
ms.assetid: 4842cb49-8dd8-4e5d-a2d6-ceeaf6c6cf8e
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1a5adc7e9fcb0ee78a7dd93f05209ea331d3c768
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54783211"
---
# <a name="ca1017-mark-assemblies-with-comvisibleattribute"></a>CA1017: Derlemeleri ComVisibleAttribute ile işaretleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MarkAssembliesWithComVisible|
|CheckId|CA1017|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Bir derleme olmayan <xref:System.Runtime.InteropServices.ComVisibleAttribute?displayProperty=fullName> özniteliğinin.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.Runtime.InteropServices.ComVisibleAttribute> Özniteliği COM istemcilerinin yönetilen kod nasıl eriştiğini belirler. İyi tasarım derlemelerin açıkça COM görünürlüğünde gösterildiğini belirler. COM görünürlüğü tüm bir derleme için ayarlanabilir ve sonra bireysel tür ve tür üyeleri için geçersiz kılındı. Öznitelik yoksa derleme içeriği COM istemcilerine görülebilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için özniteliği derlemeye ekleyin. Derlemenin COM istemcilerine görünür olmasını istemiyorsanız özniteliğini uygulayın ve değerini ayarlamak `false`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Derleme görünür olmasını istiyorsanız, özniteliğini uygulayın ve değerini ayarlamak `true`.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir derlemeye gösterir <xref:System.Runtime.InteropServices.ComVisibleAttribute> COM istemcilerine görünür olmasını engellemek için uygulanan bir öznitelik.

 [!code-cpp[FxCop.Design.AssembliesCom#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesCom/cpp/FxCop.Design.AssembliesCom.cpp#1)]
 [!code-csharp[FxCop.Design.AssembliesCom#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesCom/cs/FxCop.Design.AssembliesCom.cs#1)]
 [!code-vb[FxCop.Design.AssembliesCom#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.AssembliesCom/vb/FxCop.Design.AssembliesCom.vb#1)]

## <a name="see-also"></a>Ayrıca Bkz.
 [Yönetilmeyen kod ile birlikte](http://msdn.microsoft.com/library/ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258) [birlikte çalışma için .NET türlerini niteleme](http://msdn.microsoft.com/library/4b8afb52-fb8d-4e65-b47c-fd82956a3cdd)
