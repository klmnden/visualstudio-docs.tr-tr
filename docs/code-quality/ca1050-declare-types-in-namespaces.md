---
title: 'CA1050: Ad alanlarında türleri bildirin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1050
- DeclareTypesInNamespaces
helpviewer_keywords:
- DeclareTypesInNamespaces
- CA1050
ms.assetid: 1002748d-ac8d-404f-85dd-7a12d1ad3e05
author: gewarren
ms.author: gewarren
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 5cb2000249e7e809f4570d93703c0c15093ec2cb
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53845239"
---
# <a name="ca1050-declare-types-in-namespaces"></a>CA1050: Ad alanlarında türleri bildirin

|||
|-|-|
|TypeName|DeclareTypesInNamespaces|
|CheckId|CA1050|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Ortak veya korumalı tür, adlandırılmış bir ad alanı kapsamı dışında tanımlanır.

## <a name="rule-description"></a>Kural açıklaması
 Türleri ad çakışmalarını önlemek için ad alanları ve ilgili türü bir nesne hiyerarşisine düzenlemek için bir yol olarak bildirilir. Herhangi bir adlandırılmış ad alanı dışında olan kod içinde başvurulan bir genel ad alanında türleridir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için bir ad alanında tür yerleştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan bir uyarıyı bastırmak hiçbir zaman sahip, ancak derleme hiçbir zaman diğer Derlemelerle birlikte kullanılması durumunda bunu yapmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, hatalı bir ad alanı dışında bildirilen bir türe sahip bir kitaplık ve bir ad alanında bildirilen aynı ada sahip bir tür gösterir.

 [!code-csharp[FxCop.Design.TypesLiveInNamespaces#1](../code-quality/codesnippet/CSharp/ca1050-declare-types-in-namespaces_1.cs)]
 [!code-vb[FxCop.Design.TypesLiveInNamespaces#1](../code-quality/codesnippet/VisualBasic/ca1050-declare-types-in-namespaces_1.vb)]

## <a name="example"></a>Örnek
 Aşağıdaki uygulama önceden tanımlanmış kitaplığını kullanır. Bir ad dışında bildirilen tür ne zaman oluşturulduğunu unutmayın adı `Test` bir ad ile nitelenmiyor. Ayrıca erişmeye unutmayın `Test` yazın `Goodspace`, ad alanı adı gereklidir.

 [!code-csharp[FxCop.Design.TestTypesLive#1](../code-quality/codesnippet/CSharp/ca1050-declare-types-in-namespaces_2.cs)]
 [!code-vb[FxCop.Design.TestTypesLive#1](../code-quality/codesnippet/VisualBasic/ca1050-declare-types-in-namespaces_2.vb)]