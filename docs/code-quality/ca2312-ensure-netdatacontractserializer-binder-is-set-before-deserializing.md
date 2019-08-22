---
title: 'CA2312: Seri durumdan çıkarmadan önce NetDataContractSerializer.Binder öğesinin ayarlandığından emin olun'
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
- CA2312
- EnsureNetDataContractSerializerBinderIsSetBeforeDeserializing
ms.openlocfilehash: 38495a3c8d5a2efb5e5e96785cecbd6d50e9cd00
ms.sourcegitcommit: 673b9364fc9a96b027662dcb4cf5d61cab60ef11
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2019
ms.locfileid: "69891116"
---
# <a name="ca2312-ensure-netdatacontractserializerbinder-is-set-before-deserializing"></a>CA2312: Seri durumdan çıkarmadan önce NetDataContractSerializer.Binder öğesinin ayarlandığından emin olun

|||
|-|-|
|TypeName|EnsureNetDataContractSerializerBinderIsSetBeforeDeserializing|
|CheckId|CA2312|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Seri kaldırma yöntemi çağrıldı veya başvuruluyor <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> ve özellik null olabilir. <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType>

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural, <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType> <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> null olabileceği zaman seri kaldırma yöntemi çağrılarını veya başvurularını bulur. <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> Özelliği <xref:System.Runtime.Serialization.NetDataContractSerializer> ne olursa olsun, serisini kaldırmak istiyorsanız, bu kuralı ve [CA2311](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md)' ı devre dışı bırakın ve [CA2310](ca2310-do-not-use-insecure-deserializer-netdatacontractserializer.md)kuralını etkinleştirin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

- Mümkünse, bunun yerine güvenli bir serileştirici kullanın ve **bir saldırganın seri durumdan çıkarmak için rastgele bir tür belirtmesini sağlayın**. Bazı güvenli serileştiriciler şunları içerir:
  - <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>
  - <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>
  - <xref:System.Web.Script.Serialization.JavaScriptSerializer?displayProperty=nameWithType>-Hiçbir şekilde <xref:System.Web.Script.Serialization.SimpleTypeResolver?displayProperty=nameWithType>kullanmayın. Bir tür Çözümleyicisi kullanmanız gerekiyorsa, serisi kaldırılan türleri beklenen bir listeyle kısıtlayın.
  - <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>
  - Newtonsoft Json.NET-TypeNameHandling. None kullanın. TypeNameHandling için başka bir değer kullanmanız gerekiyorsa, serisi kaldırılan türleri özel bir ISerializationBinder ile beklenen bir listeyle kısıtlayın.
  - Protokol arabellekleri
- Seri hale getirilen verileri prova yapın. Serileştirmeden sonra, serileştirilmiş verileri şifreli olarak imzalayın. Seri durumdan önce, şifreleme imzasını doğrulayın. Şifreleme anahtarını, önemli döndürmeler için açıklanmasını ve tasarıma karşı koruyun.
- Seri durumdan çıkarılan türleri kısıtla. Özel <xref:System.Runtime.Serialization.SerializationBinder?displayProperty=nameWithType>bir uygulama uygulayın. İle <xref:System.Runtime.Serialization.NetDataContractSerializer>seri durumdan kaldırmadan önce, <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özelliği özel <xref:System.Runtime.Serialization.SerializationBinder>bir örneğine ayarlayın. Geçersiz kılınan <xref:System.Runtime.Serialization.SerializationBinder.BindToType%2A> yöntemde, tür beklenmiyorsa, serisini durdurmak için bir özel durum oluşturur.
  - Tüm kod yollarının <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özellik kümesine sahip olduğundan emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>Edildiği

```csharp
using System;
using System.IO;
using System.Runtime.Serialization;

[DataContract]
public class BookRecord
{
    [DataMember]
    public string Title { get; set; }

    [DataMember]
    public string Author { get; set; }

    [DataMember]
    public int PageCount { get; set; }

    [DataMember]
    public AisleLocation Location { get; set; }
}

[DataContract]
public class AisleLocation
{
    [DataMember]
    public char Aisle { get; set; }

    [DataMember]
    public byte Shelf { get; set; }
}

public class ExampleClass
{
    public NetDataContractSerializer Serializer { get; set; }

    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        using (MemoryStream ms = new MemoryStream(bytes))
        {
            return (BookRecord) this.Serializer.Deserialize(ms);
        }
    }
}
```

```vb
Imports System
Imports System.IO
Imports System.Runtime.Serialization

<DataContract()>
Public Class BookRecord
    <DataMember()>
    Public Property Title As String

    <DataMember()>
    Public Property Author As String

    <DataMember()>
    Public Property Location As AisleLocation
End Class

<DataContract()>
Public Class AisleLocation
    <DataMember()>
    Public Property Aisle As Char

    <DataMember()>
    Public Property Shelf As Byte
End Class

Public Class ExampleClass
    Public Property Serializer As NetDataContractSerializer

    Public Function DeserializeBookRecord(bytes As Byte()) As BookRecord
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(Me.Serializer.Deserialize(ms), BookRecord)
        End Using
    End Function
End Class
```

### <a name="solution"></a>Çözüm

```csharp
using System;
using System.IO;
using System.Runtime.Serialization;

public class BookRecordSerializationBinder : SerializationBinder
{
    public override Type BindToType(string assemblyName, string typeName)
    {
        // One way to discover expected types is through testing deserialization
        // of **valid** data and logging the types used.

        ////Console.WriteLine($"BindToType('{assemblyName}', '{typeName}')");

        if (typeName == "BookRecord" || typeName == "AisleLocation")
        {
            return null;
        }
        else
        {
            throw new ArgumentException("Unexpected type", nameof(typeName));
        }
    }
}

[DataContract]
public class BookRecord
{
    [DataMember]
    public string Title { get; set; }

    [DataMember]
    public string Author { get; set; }

    [DataMember]
    public int PageCount { get; set; }

    [DataMember]
    public AisleLocation Location { get; set; }
}

[DataContract]
public class AisleLocation
{
    [DataMember]
    public char Aisle { get; set; }

    [DataMember]
    public byte Shelf { get; set; }
}

public class ExampleClass
{
    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        NetDataContractSerializer serializer = new NetDataContractSerializer();
        serializer.Binder = new BookRecordSerializationBinder();
        using (MemoryStream ms = new MemoryStream(bytes))
        {
            return (BookRecord) serializer.Deserialize(ms);
        }
    }
}
```

```vb
Imports System
Imports System.IO
Imports System.Runtime.Serialization

Public Class BookRecordSerializationBinder
    Inherits SerializationBinder

    Public Overrides Function BindToType(assemblyName As String, typeName As String) As Type
        ' One way to discover expected types is through testing deserialization
        ' of **valid** data and logging the types used.

        'Console.WriteLine($"BindToType('{assemblyName}', '{typeName}')")

        If typeName = "BinaryFormatterVB.BookRecord" Or typeName = "BinaryFormatterVB.AisleLocation" Then
            Return Nothing
        Else
            Throw New ArgumentException("Unexpected type", NameOf(typeName))
        End If
    End Function
End Class

<DataContract()>
Public Class BookRecord
    <DataMember()>
    Public Property Title As String

    <DataMember()>
    Public Property Author As String

    <DataMember()>
    Public Property Location As AisleLocation
End Class

<DataContract()>
Public Class AisleLocation
    <DataMember()>
    Public Property Aisle As Char

    <DataMember()>
    Public Property Shelf As Byte
End Class

Public Class ExampleClass
    Public Function DeserializeBookRecord(bytes As Byte()) As BookRecord
        Dim serializer As NetDataContractSerializer = New NetDataContractSerializer()
        serializer.Binder = New BookRecordSerializationBinder()
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(serializer.Deserialize(ms), BookRecord)
        End Using
    End Function
End Class
```

## <a name="related-rules"></a>İlgili kurallar

[CA2310: Güvenli olmayan seri hale getirici kullanmayan NetDataContractSerializer kullanma](ca2310-do-not-use-insecure-deserializer-netdatacontractserializer.md)

[CA2311: Önce NetDataContractSerializer. Ciltçi Ayarlamasız seri durumdan çıkarma](ca2311-do-not-deserialize-without-first-setting-netdatacontractserializer-binder.md)
