---
title: 'CA1716: Tanımlayıcılar anahtar sözcükler ile eşleşmemelidir'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
helpviewer_keywords:
- IdentifiersShouldNotMatchKeywords
- CA1716
ms.assetid: 900cc8a1-1089-4069-a4ce-10b109ac4fab
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: d27fdd455d019532b47bc531f9f7377bacd6572e
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53828634"
---
# <a name="ca1716-identifiers-should-not-match-keywords"></a>CA1716: Tanımlayıcılar anahtar sözcükler ile eşleşmemelidir

|||
|-|-|
|TypeName|IdentifiersShouldNotMatchKeywords|
|CheckId|CA1716|
|Kategori|Microsoft.Naming|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir ad alanı, bir tür veya viritual veya arabirim üye adı ayrılmış bir anahtar sözcük bir programlama dili ile eşleşir.

## <a name="rule-description"></a>Kural açıklaması

Tanımlayıcı ad alanları, türler, için ve sanal ve arabirim üyeleri olmayan ortak dil çalışma zamanını hedefleyen diller tarafından tanımlanan anahtar sözcükleri eşleşmelidir. Kullanılan dil ve anahtar sözcüğü bağlı olarak, derleyici hataları ve belirsizlikler kitaplığı kullanmak zorlaştırabilir.

Bu kural, anahtar sözcükleri şu dillerde karşı denetler:

- Visual Basic

- C#

- C++/CLI

Büyük küçük harf duyarsız bir karşılaştırma için kullanılan [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] anahtar sözcükleri ve büyük küçük harfe duyarlı karşılaştırma diğer diller için kullanılır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Anahtar sözcükler listesinde görünmeyen bir adı seçin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Tanımlayıcı kullanıcılara API'nin karıştırır değil ve kitaplık .NET Framework içindeki kullanılabilir tüm dillerde kullanılabilir ikna varsa bu kuraldan bir uyarıyı gösterilmemesini sağlayabilirsiniz.