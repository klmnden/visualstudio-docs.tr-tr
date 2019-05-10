---
title: 'CA2310: Güvenli olmayan seri durumdan çıkarıcının NetDataContractSerializer kullanmayın'
ms.date: 05/01/2019
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
- CA2310
- DoNotUseInsecureDeserializerNetDataContractSerializer
ms.openlocfilehash: e4af6bbfbd7e14b99f39ffa0adb5d1117c200d9a
ms.sourcegitcommit: db30651dc0ce4d0b274479b23a6bd102a5559098
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65135559"
---
# <a name="ca2310-do-not-use-insecure-deserializer-netdatacontractserializer"></a>CA2310: Güvenli olmayan seri durumdan çıkarıcının NetDataContractSerializer kullanmayın

|||
|-|-|
|TypeName|DoNotUseInsecureDeserializerNetDataContractSerializer|
|CheckId|CA2310|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

A <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType> seri durumundan çıkarma yöntemi çağrılan veya başvurulan.

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural bulur <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType> yöntem çağrıları veya başvurular seri durumdan çıkarma. Yalnızca zaman seri durumdan istiyorsanız <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> türlerini kısıtlamak, bu kuralı devre dışı bırak ve kurallarını etkinleştirmek için özelliği ayarlanmış [CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md) ve [CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md) yerine.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

- Mümkünse, bunun yerine, güvenli bir serileştirici kullanın ve **serisini kaldırmak için rastgele bir tür belirtmek bir saldırgan izin verme**. Bazı güvenli seri hale getiricileri genişletme şunlardır:
  - <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>
  - <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>
  - <xref:System.Web.Script.Serialization.JavaScriptSerializer?displayProperty=nameWithType> -Hiçbir zaman kullanmayın <xref:System.Web.Script.Serialization.SimpleTypeResolver?displayProperty=nameWithType>. Tür çözümleyici kullanmanız gerekirse, seri durumdan çıkarılmış türü beklenen bir listeye kısıtlayın.
  - <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>
  - Newtonsoft Json.NET - TypeNameHandling.None kullanın. Başka bir değer için TypeNameHandling kullanmanız gerekirse, seri durumdan çıkarılmış türü özel ISerializationBinder beklenen bir listesiyle kısıtlayın.
  - Protokol arabellekleri
- Seri hale getirilmiş veri artıklığının olun. Serileştirme sonra serileştirilmiş veriler şifreli olarak oturum açın. Seri durumundan çıkarma önce şifreleme imzası doğrulayın. İfşa gelen şifreleme anahtarını ve anahtar devirlerini için tasarım koruyun.
- Seri durumdan çıkarılmış türlerini kısıtlayın. Özel bir uygulama <xref:System.Runtime.Serialization.SerializationBinder?displayProperty=nameWithType>. İle seri durumdan çıkarılırken önce <xref:System.Runtime.Serialization.NetDataContractSerializer>ayarlayın <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özelliği özel örneğine <xref:System.Runtime.Serialization.SerializationBinder>. Geçersiz kılınan içinde <xref:System.Runtime.Serialization.SerializationBinder.BindToType%2A> türü beklenmedik bir durumsa yöntemi bir özel durum oluşturur.
- Seri durumdan çıkarılmış türlerini kısıtlamak, bu kural devre dışı bırakabilir ve kurallarını etkinleştirmek isteyebilirsiniz [CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md) ve [CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md). Kuralları [CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md) ve [CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md) emin olmak için Yardım <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özelliği, seri durumdan çıkarılırken önce her zaman ayarlanır.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System.IO;
using System.Runtime.Serialization;

public class ExampleClass
{
    public object MyDeserialize(byte[] bytes)
    {
        NetDataContractSerializer serializer = new NetDataContractSerializer();
        return serializer.Deserialize(new MemoryStream(bytes));
    }
}
```

```vb
Imports System.IO
Imports System.Runtime.Serialization

Public Class ExampleClass
    Public Function MyDeserialize(bytes As Byte()) As Object
        Dim serializer As NetDataContractSerializer = New NetDataContractSerializer()
        Return serializer.Deserialize(New MemoryStream(bytes))
    End Function
End Class
```

## <a name="related-rules"></a>İlgili kuralları

[CA2311: İlk ayarlamadan NetDataContractSerializer.Binder seri durumdan değil](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md)

[CA2312: Seri durumdan çıkarılırken önce NetDataContractSerializer.Binder ayarlandığından emin olun](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md)
