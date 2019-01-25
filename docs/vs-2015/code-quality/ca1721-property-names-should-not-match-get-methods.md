---
title: 'CA1721: Özellik adları get yöntemleri değil eşleşmelidir | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
helpviewer_keywords:
- CA1721
- PropertyNamesShouldNotMatchGetMethods
ms.assetid: 45a0e853-1f06-4688-af1b-cc634409e295
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: c9a3dcf6566267cebdfeecb91f57bf139be46de2
ms.sourcegitcommit: c496a77add807ba4a29ee6a424b44a5de89025ea
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54834895"
---
# <a name="ca1721-property-names-should-not-match-get-methods"></a>CA1721: Özellik adları get metotları ile eşleşmemelidir
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|PropertyNamesShouldNotMatchGetMethods|
|CheckId|CA1721|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı bir üyenin adını 'Get' ile başlar ve aksi durumda ortak veya korumalı özellik adıyla eşleşen. Örneğin, 'GetColor' ve 'Color' adlı bir özellik adında bir yöntemi içeren bir tür, bu kuralı ihlal ediyor.

## <a name="rule-description"></a>Kural Tanımı
 Get yöntemleri ve özellikleri, açıkça işlevlerinden ayırt edilebilen adları olması gerekir.

 Adlandırma kuralları, ortak dil çalışma zamanını hedefleyen kitaplıkları için genel bir bakış sağlar. Bu, yeni bir yazılım kitaplığı öğrenmek için gereklidir ve kitaplık geliştirme yönetilen kodda uzmanlığına sahip olan kişi tarafından geliştirilmiştir müşterilerinizin size olan güvenini artırır süreyi azaltır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 'Get' önekli bir metot adı eşleşmiyor adı değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

> [!NOTE]
>  Bu uyarı, Iextenderprovider arabirimi uygulayarak alma yöntemini neden oluyorsa atlanabilir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir yöntem ve bu kuralı ihlal ediyor özelliği içerir.

 [!code-csharp[FxCop.Naming.GetMethod#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Naming.GetMethod/cs/FxCop.Naming.GetMethod.cs#1)]
 [!code-vb[FxCop.Naming.GetMethod#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Naming.GetMethod/vb/FxCop.Naming.GetMethod.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1024: Uygun yerlerde özellikler kullan](../code-quality/ca1024-use-properties-where-appropriate.md)
