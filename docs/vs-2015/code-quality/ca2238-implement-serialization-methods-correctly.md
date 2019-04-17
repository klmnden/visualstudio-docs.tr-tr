---
title: 'CA2238: Serileştirme yöntemlerini doğru uygulama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- ImplementSerializationMethodsCorrectly
- CA2238
helpviewer_keywords:
- ImplementSerializationMethodsCorrectly
- CA2238
ms.assetid: 00882cf9-e10d-4d40-9126-3e6753e3c934
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: cff617adf2b31ef773de3bc41db7245346795bee
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59657135"
---
# <a name="ca2238-implement-serialization-methods-correctly"></a>CA2238: Serileştirme metotlarını doğru uygulayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [CA2238: Serileştirme yöntemlerini doğru uygulama](https://docs.microsoft.com/visualstudio/code-quality/ca2238-implement-serialization-methods-correctly).  
  
|||  
|-|-|  
|TypeName|ImplementSerializationMethodsCorrectly|  
|CheckId|CA2238|  
|Kategori|Microsoft.Usage|  
|Yeni Değişiklik|Derlemenin dışında görünür bir yöntem ise - kesiliyor.<br /><br /> Bölünemez - yöntemi derlemenin dışında görünür değilse.|  
  
## <a name="cause"></a>Sebep  
 Seri hale getirme olayı tanıtan yöntem türü, doğru imzaya, dönüş türüne veya görünürlüğe sahip değil.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Bir yöntem, aşağıdaki serileştirme olay özniteliklerden birini uygulayarak bir seri hale getirme olayı işleyicisi atanır:  
  
- <xref:System.Runtime.Serialization.OnSerializingAttribute?displayProperty=fullName>  
  
- <xref:System.Runtime.Serialization.OnSerializedAttribute?displayProperty=fullName>  
  
- <xref:System.Runtime.Serialization.OnDeserializingAttribute?displayProperty=fullName>  
  
- <xref:System.Runtime.Serialization.OnDeserializedAttribute?displayProperty=fullName>  
  
  Serileştirme olay işleyicileri ele türünde tek bir parametre <xref:System.Runtime.Serialization.StreamingContext?displayProperty=fullName>, dönüş `void`ve `private` görünürlük.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Bu kural ihlalini düzeltmek için imza, dönüş türü veya seri hale getirme olay işleyicisi görünürlüğünü düzeltin.  
  
## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında  
 Bu kuraldan uyarıyı bastırmayın.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, olay işleyicileri doğru olarak bildirilen bir seri hale getirme gösterir.  
  
 [!code-csharp[FxCop.Usage.SerializationEventHandlers#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Usage.SerializationEventHandlers/cs/FxCop.Usage.SerializationEventHandlers.cs#1)]
 [!code-vb[FxCop.Usage.SerializationEventHandlers#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Usage.SerializationEventHandlers/vb/FxCop.Usage.SerializationEventHandlers.vb#1)]  
  
## <a name="related-rules"></a>İlgili kuralları  
 [CA2236: ISerializable türler üzerinde taban sınıf yöntemlerini çağırın](../code-quality/ca2236-call-base-class-methods-on-iserializable-types.md)  
  
 [CA2240: ISerializable'ı doğru uygulayın](../code-quality/ca2240-implement-iserializable-correctly.md)  
  
 [CA2229: Serileştirme oluşturucularını uygulayın](../code-quality/ca2229-implement-serialization-constructors.md)  
  
 [CA2235: Tüm serileştirilebilir olmayan alanları işaretleyin](../code-quality/ca2235-mark-all-non-serializable-fields.md)  
  
 [CA2237: İşareti ISerializable türleri SerializableAttribute ile işaretleyin](../code-quality/ca2237-mark-iserializable-types-with-serializableattribute.md)  
  
 [CA2239: İsteğe bağlı alanlar için seri halden çıkarma yöntemleri sağlar.](../code-quality/ca2239-provide-deserialization-methods-for-optional-fields.md)  
  
 [CA2120: Serileştirme oluşturucularının güvenliğini sağlayın](../code-quality/ca2120-secure-serialization-constructors.md)
