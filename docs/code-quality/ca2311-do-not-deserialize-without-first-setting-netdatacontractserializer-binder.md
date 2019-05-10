---
title: 'CA2311: İlk ayarlamadan NetDataContractSerializer.Binder seri durumdan değil'
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
- CA2311
- DoNotDeserializeWithoutFirstSettingNetDataContractSerializerBinder
ms.openlocfilehash: aec95d4bbd2d9bc498f9688c5601591d480d7f3b
ms.sourcegitcommit: db30651dc0ce4d0b274479b23a6bd102a5559098
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65135562"
---
# <a name="ca2311-do-not-deserialize-without-first-setting-netdatacontractserializerbinder"></a>CA2311: İlk ayarlamadan NetDataContractSerializer.Binder seri durumdan değil

|||
|-|-|
|TypeName|DoNotDeserializeWithoutFirstSettingNetDataContractSerializerBinder|
|CheckId|CA2311|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

A <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType> seri durumundan çıkarma yöntemi çağrılan veya başvurulan olmadan <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özellik kümesi.

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural bulur <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=nameWithType> yöntem çağrıları veya başvuruları seri durumdan çıkarma olduğunda <xref:System.Runtime.Serialization.NetDataContractSerializer> yok, <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> ayarlayın. İle herhangi bir seri durumundan çıkarma engellemek istiyorsanız <xref:System.Runtime.Serialization.NetDataContractSerializer> bakılmaksızın <xref:System.Runtime.Serialization.NetDataContractSerializer.Binder> özelliği, bu kuralı devre dışı bırak ve [CA2312](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md)ve kuralı etkinleştirmek [CA2310](ca2310-do-not-use-insecure-deserializer-netdatacontractserializer.md).

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

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

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
    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        NetDataContractSerializer serializer = new NetDataContractSerializer();
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
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(serializer.Deserialize(ms), BookRecord)
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

## <a name="related-rules"></a>İlgili kuralları

[CA2310: Güvenli olmayan seri durumdan çıkarıcının NetDataContractSerializer kullanmayın](ca2310-do-not-use-insecure-deserializer-netdatacontractserializer.md)

[CA2312: Seri durumdan çıkarılırken önce NetDataContractSerializer.Binder ayarlandığından emin olun](ca2312-ensure-netdatacontractserializer-binder-is-set-before-deserializing.md)