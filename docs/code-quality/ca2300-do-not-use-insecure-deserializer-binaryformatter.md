---
title: 'CA2300: Güvenli olmayan seri durumdan çıkarıcı BinaryFormatter kullanmayın'
ms.date: 04/05/2019
ms.topic: reference
author: dotpaul
ms.author: paulming
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
f1_keywords:
- CA2300
- DoNotUseInsecureDeserializerBinaryFormatter
ms.openlocfilehash: 13b50e9eba49ff3457aff41d59448f1a0dfc2ea7
ms.sourcegitcommit: db30651dc0ce4d0b274479b23a6bd102a5559098
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65083880"
---
# <a name="ca2300-do-not-use-insecure-deserializer-binaryformatter"></a>CA2300: Güvenli olmayan seri durumdan çıkarıcı BinaryFormatter kullanmayın

|||
|-|-|
|TypeName|DoNotUseInsecureDeserializerBinaryFormatter|
|CheckId|CA2300|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

A <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> seri durumundan çıkarma yöntemi çağrılan veya başvurulan.

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural bulur <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> yöntem çağrıları veya başvurular seri durumdan çıkarma. Yalnızca zaman seri durumdan istiyorsanız <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> türlerini kısıtlamak, bu kuralı devre dışı bırak ve kurallarını etkinleştirmek için özelliği ayarlanmış [CA2301](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md) ve [CA2302](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md) yerine.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

- Mümkünse, bunun yerine, güvenli bir serileştirici kullanın ve **serisini kaldırmak için rastgele bir tür belirtmek bir saldırgan izin verme**. Bazı güvenli seri hale getiricileri genişletme şunlardır:
  - <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>
  - <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>
  - <xref:System.Web.Script.Serialization.JavaScriptSerializer?displayProperty=nameWithType> -Hiçbir zaman kullanmayın <xref:System.Web.Script.Serialization.SimpleTypeResolver?displayProperty=nameWithType>. Tür çözümleyici kullanmanız gerekirse, seri durumdan çıkarılmış türü beklenen bir listeye kısıtlayın.
  - <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>
  - Newtonsoft Json.NET - TypeNameHandling.None kullanın. Başka bir değer için TypeNameHandling kullanmanız gerekirse, seri durumdan çıkarılmış türü özel ISerializationBinder beklenen bir listesiyle kısıtlayın.
  - Protokol arabellekleri
- Seri hale getirilmiş veri artıklığının olun. Serileştirme sonra serileştirilmiş veriler şifreli olarak oturum açın. Seri durumundan çıkarma önce şifreleme imzası doğrulayın. İfşa gelen şifreleme anahtarını ve anahtar devirlerini için tasarım koruyun.
- Seri durumdan çıkarılmış türlerini kısıtlayın. Özel bir uygulama <xref:System.Runtime.Serialization.SerializationBinder?displayProperty=nameWithType>. İle seri durumdan çıkarılırken önce <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter>ayarlayın <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özelliği özel örneğine <xref:System.Runtime.Serialization.SerializationBinder>. Geçersiz kılınan içinde <xref:System.Runtime.Serialization.SerializationBinder.BindToType%2A> türü beklenmedik bir durumsa yöntemi bir özel durum oluşturur.
- Seri durumdan çıkarılmış türlerini kısıtlamak, bu kural devre dışı bırakabilir ve kurallarını etkinleştirmek isteyebilirsiniz [CA2301](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md) ve [CA2302](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md). Kuralları [CA2301](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md) ve [CA2302](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md) emin olmak için Yardım <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özelliği, seri durumdan çıkarılırken önce her zaman ayarlanır.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System.IO;
using System.Runtime.Serialization.Formatters.Binary;

public class ExampleClass
{
    public object MyDeserialize(byte[] bytes)
    {
        BinaryFormatter formatter = new BinaryFormatter();
        return formatter.Deserialize(new MemoryStream(bytes));
    }
}
```

```vb
Imports System.IO
Imports System.Runtime.Serialization.Formatters.Binary

Public Class ExampleClass
    Public Function MyDeserialize(bytes As Byte()) As Object
        Dim formatter As BinaryFormatter = New BinaryFormatter()
        Return formatter.Deserialize(New MemoryStream(bytes))
    End Function
End Class
```

## <a name="related-rules"></a>İlgili kuralları

[CA2301: İlk ayarlamadan BinaryFormatter.Binder BinaryFormatter.Deserialize çağırmayın](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md)

[CA2302: BinaryFormatter.Binder BinaryFormatter.Deserialize çağırmadan önce ayarlandığından emin olun](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md)