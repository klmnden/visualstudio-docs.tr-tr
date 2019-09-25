---
title: 'CA2310: Güvenli olmayan seri kaldırıcı NetDataContractSerializer kullanmayın'
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
ms.openlocfilehash: 5335e72307ea201ad77d6e59b267572d4d9aae56
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237714"
---
# <a name="ca2310-do-not-use-insecure-deserializer-netdatacontractserializer"></a>CA2310: Güvenli olmayan seri kaldırıcı NetDataContractSerializer kullanmayın

|||
|-|-|
|TypeName|DoNotUseInsecureDeserializerNetDataContractSerializer|
|CheckId|CA2310|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

<xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType> Seri kaldırma yöntemi çağrıldı veya başvuruluyor.

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural, <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType> seri kaldırma yöntemi çağrılarını veya başvurularını bulur. Yalnızca <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> Özellik türleri kısıtla olarak ayarlandığında serisini kaldırmak istiyorsanız, bu kuralı devre dışı bırakın ve bunun yerine [CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md) ve [CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md) kurallarını etkinleştirin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

- Mümkünse, bunun yerine güvenli bir serileştirici kullanın ve **bir saldırganın seri durumdan çıkarmak için rastgele bir tür belirtmesini sağlayın**. Bazı güvenli serileştiriciler şunları içerir:
  - <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>
  - <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>
  - <xref:System.Web.Script.Serialization.JavaScriptSerializer?displayProperty=nameWithType>-Hiçbir şekilde <xref:System.Web.Script.Serialization.SimpleTypeResolver?displayProperty=nameWithType>kullanmayın. Bir tür Çözümleyicisi kullanmanız gerekiyorsa, serisi kaldırılan türleri beklenen bir listeyle kısıtlayın.
  - <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>
  - Newtonsoft Json.NET-TypeNameHandling. None kullanın. TypeNameHandling için başka bir değer kullanmanız gerekiyorsa, serisi kaldırılan türleri özel bir ISerializationBinder ile beklenen bir listeyle kısıtlayın.
  - Protokol Arabellekleri
- Seri hale getirilen verileri prova yapın. Serileştirmeden sonra, serileştirilmiş verileri şifreli olarak imzalayın. Seri durumdan önce, şifreleme imzasını doğrulayın. Şifreleme anahtarını, önemli döndürmeler için açıklanmasını ve tasarıma karşı koruyun.
- Seri durumdan çıkarılan türleri kısıtla. Özel <xref:System.Runtime.Serialization.SerializationBinder?displayProperty=nameWithType>bir uygulama uygulayın. İle <xref:System.Runtime.Serialization.NetDataContractSerializer>seri durumdan kaldırmadan önce, <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özelliği özel <xref:System.Runtime.Serialization.SerializationBinder>bir örneğine ayarlayın. Geçersiz kılınan <xref:System.Runtime.Serialization.SerializationBinder.BindToType%2A> yöntemde, tür beklenmiyorsa, serisini durdurmak için bir özel durum oluşturur.
  - Seri durumdan çıkarılan türleri kısıtladığınızda, bu kuralı devre dışı bırakmak ve [CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md) ve [CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md)kurallarını etkinleştirmek isteyebilirsiniz. [CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md) ve [CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md) kuralları, <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özelliğin seri durumdan çıkarılamadı önce her zaman ayarlandığından emin olmaya yardımcı olur.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>Edildiği

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

## <a name="related-rules"></a>İlgili kurallar

[CA2311: Önce NetDataContractSerializer. Ciltçi Ayarlamasız seri durumdan çıkarma](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md)

[CA2312: NetDataContractSerializer. Ciltçi serisini kaldırmada önce ayarlandığından emin olun](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md)
