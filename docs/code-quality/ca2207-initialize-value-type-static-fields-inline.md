---
title: 'CA2207: Değer türü statik alanları satır içi başlatın'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- InitializeValueTypeStaticFieldsInline
- CA2207
helpviewer_keywords:
- CA2207
- InitializeValueTypeStaticFieldsInline
ms.assetid: d1ea9d8b-ecc2-46ca-86e2-c41dd0e76658
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fb75c6d06502c9d2fac437a8924af4d51ddd6d0a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55036166"
---
# <a name="ca2207-initialize-value-type-static-fields-inline"></a>CA2207: Değer türü statik alanları satır içi başlatın

|||
|-|-|
|TypeName|InitializeValueTypeStaticFieldsInline|
|CheckId|CA2207|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir değer türü açık bir statik Oluşturucu bildirir.

## <a name="rule-description"></a>Kural açıklaması
 Bir değer türü bildirildiğinde, burada tüm değer tür alanları sıfıra ayarlanır ve tüm başvuru türü alanlarını ayarlamak bir varsayılan başlatma uğradığında `null` (`Nothing` Visual Basic'te). Açık bir statik Oluşturucu yalnızca bir örnek oluşturucusu önce çalıştırması garantili olan veya türün statik üyesi çağrılır. Türün örnek oluşturucusu çağırmaya gerek kalmadan oluşturulursa, bu nedenle, statik Oluşturucusu çalıştırmak için garanti edilmez.

 Tüm statik verileri başlatılmış satır içi olduğundan ve hiçbir açık bir statik Oluşturucu bildirimi, C# ve Visual Basic derleyicileri ekleyin `beforefieldinit` MSIL sınıf tanımına bayrağı. Derleyiciler, ayrıca statik başlatma kodu içeren özel bir statik oluşturucu ekleyin. Bu özel bir statik Oluşturucu tüm türü statik alanları erişebilmek için önce çalıştırılacak garanti edilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Düzeltmek için bu kural ihlalini başlatmak tüm statik verileri bildirilir ve statik oluşturucuyu kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="related-rules"></a>İlgili kuralları
 [CA1810: Başvuru türü statik alanları satır içi başlatın](../code-quality/ca1810-initialize-reference-type-static-fields-inline.md)