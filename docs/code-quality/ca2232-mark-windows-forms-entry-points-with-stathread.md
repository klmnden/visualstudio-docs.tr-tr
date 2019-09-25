---
title: 'CA2232: Windows Forms giriş noktalarını STAThread ile işaretleyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MarkWindowsFormsEntryPointsWithStaThread
- CA2232
helpviewer_keywords:
- CA2232
- MarkWindowsFormsEntryPointsWithStaThread
ms.assetid: a3c95130-8e7f-4419-9fcd-b67d077e8efb
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 06772f8dd91c27834b329293d06cfbc2a7dcfcef
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71230766"
---
# <a name="ca2232-mark-windows-forms-entry-points-with-stathread"></a>CA2232: Windows Forms giriş noktalarını STAThread ile işaretleyin

|||
|-|-|
|TypeName|MarkWindowsFormsEntryPointsWithStaThread|
|CheckId|CA2232|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir bütünleştirilmiş kod <xref:System.Windows.Forms> ad alanına başvurur ve giriş noktası <xref:System.STAThreadAttribute?displayProperty=fullName> özniteliğiyle işaretlenmez.

## <a name="rule-description"></a>Kural açıklaması
 <xref:System.STAThreadAttribute>uygulama için COM iş parçacığı modelinin tek iş parçacıklı apartman olduğunu gösterir. Bu öznitelik Windows Forms kullanan herhangi bir uygulamanın girişinde sunulur; atlanırsa, Windows bileşenleri doğru çalışmayabilir. Özniteliği yoksa, uygulama Windows Forms için desteklenmeyen çok iş parçacıklı grup modelini kullanır.

> [!NOTE]
> [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]Uygulama çerçevesini kullanan projeler, STAThread ile **Main** metodunu işaretlemek zorunda değildir. [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] Derleyici bunu otomatik olarak yapar.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, giriş noktasına <xref:System.STAThreadAttribute> özniteliğini ekleyin. <xref:System.MTAThreadAttribute?displayProperty=fullName> Öznitelik varsa kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
<xref:System.STAThreadAttribute> Özniteliğin gereksiz ve desteklenmeyen .NET Compact Framework için geliştirme yapıyorsanız, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="example"></a>Örnek
Aşağıdaki örneklerde doğru kullanımı <xref:System.STAThreadAttribute>gösterilmektedir:

[!code-csharp[FxCop.Usage.StaThread#1](../code-quality/codesnippet/CSharp/ca2232-mark-windows-forms-entry-points-with-stathread_1.cs)]
[!code-vb[FxCop.Usage.StaThread#1](../code-quality/codesnippet/VisualBasic/ca2232-mark-windows-forms-entry-points-with-stathread_1.vb)]