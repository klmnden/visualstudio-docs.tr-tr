---
title: 'CA1050: Ad alanlarında türleri bildirin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1050
- DeclareTypesInNamespaces
helpviewer_keywords:
- DeclareTypesInNamespaces
- CA1050
ms.assetid: 1002748d-ac8d-404f-85dd-7a12d1ad3e05
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: f13684df70db7026e874bc8edb6282faca2cf98d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68200538"
---
# <a name="ca1050-declare-types-in-namespaces"></a>CA1050: Ad alanlarında türler bildirin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DeclareTypesInNamespaces|
|CheckId|CA1050|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı tür, adlandırılmış bir ad alanı kapsamı dışında tanımlanır.

## <a name="rule-description"></a>Kural Tanımı
 Türleri ad çakışmalarını önlemek için ad alanları ve ilgili türü bir nesne hiyerarşisine düzenlemek için bir yol olarak bildirilir. Herhangi bir adlandırılmış ad alanı dışında olan kod içinde başvurulan bir genel ad alanında türleridir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için bir ad alanında tür yerleştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak hiçbir zaman sahip, ancak derleme hiçbir zaman diğer Derlemelerle birlikte kullanılması durumunda bunu yapmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, hatalı bir ad alanı dışında bildirilen bir türe sahip bir kitaplık ve bir ad alanında bildirilen aynı ada sahip bir tür gösterir.

 [!code-csharp[FxCop.Design.TypesLiveInNamespaces#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.TypesLiveInNamespaces/cs/FxCop.Design.TypesLiveInNamespaces.cs#1)]
 [!code-vb[FxCop.Design.TypesLiveInNamespaces#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.TypesLiveInNamespaces/vb/FxCop.Design.TypesLiveInNamespaces.vb#1)]

## <a name="example"></a>Örnek
 Aşağıdaki uygulama önceden tanımlanmış kitaplığını kullanır. Bir ad dışında bildirilen tür ne zaman oluşturulduğunu unutmayın adı `Test` bir ad ile nitelenmiyor. Ayrıca erişmeye unutmayın `Test` yazın `Goodspace`, ad alanı adı gereklidir.

 [!code-csharp[FxCop.Design.TestTypesLive#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.TestTypesLive/cs/FxCop.Design.TestTypesLive.cs#1)]
 [!code-vb[FxCop.Design.TestTypesLive#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.TestTypesLive/vb/FxCop.Design.TestTypesLive.vb#1)]
