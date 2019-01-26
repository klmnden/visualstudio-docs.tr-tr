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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e1ecd5fc5163bfcb5a0f217e21b5aab353a074a7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54972946"
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