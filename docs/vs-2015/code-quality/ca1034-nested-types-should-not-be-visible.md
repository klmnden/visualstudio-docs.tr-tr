---
title: 'CA1034: İç içe türler görünebilir olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- NestedTypesShouldNotBeVisible
- CA1034
helpviewer_keywords:
- NestedTypesShouldNotBeVisible
- CA1034
ms.assetid: e9789a2c-2540-42a1-8705-ae7104011194
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 915b5807f7b14269acf4b7509ffceaecfb13af47
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62536405"
---
# <a name="ca1034-nested-types-should-not-be-visible"></a>CA1034: İç içe türler görünür olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|NestedTypesShouldNotBeVisible|
|CheckId|CA1034|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen tür dışarıdan görünen tür bildirimi içerir. İç içe geçmiş sabit listeleri ve korumalı türler, bu kuralın dışındadır.

## <a name="rule-description"></a>Kural Tanımı
 İç içe türü başka bir tür kapsamı içinde bildirilen bir türdür. İç içe geçmiş türler, içeren türde özel uygulama ayrıntılarını kapsüllemek için kullanışlıdır. Bu amaçla kullanılan, iç içe türün dışarıdan görünür olmaması gerekir.

 Dışarıdan görünen bir iç içe geçmiş türler, mantıksal gruplandırma veya ad çakışmalarını önlemek için kullanmayın; Bunun yerine, ad alanları kullanın.

 İç içe türler bazı programcılar açıkça anlaşılmıyor üye erişilebilirliği, kavramını içerir.

 Korumalı türler, alt sınıfların ve iç içe geçmiş türler Gelişmiş özelleştirme senaryolarda kullanılabilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 İç içe türün dışarıdan görünür olmasını düşünmüyorsanız, türün erişilebilirliği değiştirin. Aksi takdirde, iç içe türün üst öğesinden kaldırın. İç içe amacı, iç içe türün kategorilere ayırmak için ise, bunun yerine bir hiyerarşi oluşturmak için bir ad kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kuralını ihlal eden bir tür gösterir.

 [!code-cpp[FxCop.Design.NestedTypes#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.NestedTypes/cpp/FxCop.Design.NestedTypes.cpp#1)]
 [!code-csharp[FxCop.Design.NestedTypes#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.NestedTypes/cs/FxCop.Design.NestedTypes.cs#1)]
 [!code-vb[FxCop.Design.NestedTypes#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.NestedTypes/vb/FxCop.Design.NestedTypes.vb#1)]
