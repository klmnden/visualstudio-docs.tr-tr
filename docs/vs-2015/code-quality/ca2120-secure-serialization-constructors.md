---
title: 'CA2120: Serileştirme oluşturucularının güvenliğini sağlayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2120
- SecureSerializationConstructors
helpviewer_keywords:
- SecureSerializationConstructors
- CA2120
ms.assetid: e9989da1-55a0-43f8-9aa9-da86afae3b41
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: ea70b7f9462e3195a78b915691a5069ebd6fe6aa
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68154352"
---
# <a name="ca2120-secure-serialization-constructors"></a>CA2120: Serileştirme oluşturucularının güvenliğini sağlayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|SecureSerializationConstructors|
|CheckId|CA2120|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Türün uyguladığı <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirim, temsilci veya arabirimi değil ve kısmen güvenilen arayanlara izin veren bir derlemede bildirilmiş. Alan bir oluşturucu türüne sahip bir <xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName> nesnesi ve bir <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName> nesnesi (seri hale getirme oluşturucusunu imzası). Bu oluşturucu güvenlik denetimi tarafından güvenli değildir, ancak bir veya daha fazla türü normal Oluşturucu güvenlidir.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, özel serileştirme destekleyen türler için geçerlidir. Bunu uygulayan bir tür özel serileştirme destekler <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName> arabirimi. Seri hale getirme oluşturucusunu gereklidir ve seri durumdan çıkarılamıyor veya kullanılarak serileştirilmiş nesneler yeniden oluşturmak için kullanılan <xref:System.Runtime.Serialization.ISerializable.GetObjectData%2A?displayProperty=fullName> yöntemi. Seri hale getirme oluşturucusunu ayırır ve bu nesneleri başlatır olduğundan, normal oluşturucu üzerinde mevcut olan güvenlik denetimleri de serileştirme Oluşturucu mevcut olması gerekir. Bu kuralı ihlal ediyor, yalnızca bir örneği oluşturulamadı, bunu yapmak için seri hale getirme oluşturucusunu kullanabilirsiniz.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için bu diğer oluşturucular koruma aynı güvenlik taleplerini seri hale getirme Oluşturucu koruyun.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kural ihlalini bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kuralını ihlal eden bir tür gösterir.

 [!code-csharp[FxCop.Security.SerialCtors#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Security.SerialCtors/cs/FxCop.Security.SerialCtors.cs#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)

 [CA2237: İşareti ISerializable türleri SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.Runtime.Serialization.ISerializable?displayProperty=fullName><xref:System.Runtime.Serialization.SerializationInfo?displayProperty=fullName>
 <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName>
