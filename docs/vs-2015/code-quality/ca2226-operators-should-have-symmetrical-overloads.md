---
title: 'CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- OperatorsShouldHaveSymmetricalOverloads
- CA2226
helpviewer_keywords:
- OperatorsShouldHaveSymmetricalOverloads
- CA2226
ms.assetid: d202401a-ea14-4559-b15e-0ea4f5b68789
caps.latest.revision: 16
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a2500fef2de955e4065016eba4709e427bc62225
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53929610"
---
# <a name="ca2226-operators-should-have-symmetrical-overloads"></a>CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|OperatorsShouldHaveSymmetricalOverloads|
|CheckId|CA2226|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir tür, eşitlik ya da eşitsizlik operatörünü uygular ve ters işleci uygulamaz.

## <a name="rule-description"></a>Kural Tanımı
 Burada da eşitlik ve eşitsizlik tür örnekleri için geçerlidir ve ters işleci tanımsızdır hiçbir koşullar vardır. Türleri eşitlik işlecini çevrilerek değeri döndürerek eşitsizlik işleci genellikle uygulayın.

 C# Derleyici, bu kural ihlalleri için bir hata verir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için eşitlik ve eşitsizlik işleçleri uygulayın veya var olanı kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Türünüz ile tutarlı bir şekilde çalışmaz [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)].

## <a name="related-rules"></a>İlgili kuralları
 [CA1046: Başvuru türlerinde eşittir işleçlerini aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)

 [CA2225: İşleç aşırı yüklemeleri adlandırılmış Alternatiflere sahiptir](../code-quality/ca2225-operator-overloads-have-named-alternates.md)

 [CA2224: Eşittir işlecini aşırı yüklemesi üzerinde geçersiz kılma değerine eşittir](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)

 [CA2218: Gethashcode'u eşittir geçersiz kılmada geçersiz kıl](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)

 [CA2231: Eşittir işlecini ValueType.equals'ı geçersiz kılarak üzerinde](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)
