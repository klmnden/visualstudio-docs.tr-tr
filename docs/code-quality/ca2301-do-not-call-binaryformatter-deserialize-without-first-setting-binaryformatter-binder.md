---
title: 'CA2301: İlk olarak BinaryFormatter.Binder öğesini ayarlamadan önce BinaryFormatter.Deserialize çağırmayın'
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
- CA2301
- DoNotCallBinaryFormatterDeserializeWithoutFirstSettingBinaryFormatterBinder
ms.openlocfilehash: d9ac57ae00631088dacd9a23c502ba7693d5a903
ms.sourcegitcommit: db30651dc0ce4d0b274479b23a6bd102a5559098
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65083910"
---
# <a name="ca2301-do-not-call-binaryformatterdeserialize-without-first-setting-binaryformatterbinder"></a>CA2301: İlk olarak BinaryFormatter.Binder öğesini ayarlamadan önce BinaryFormatter.Deserialize çağırmayın

|||
|-|-|
|TypeName|DoNotCallBinaryFormatterDeserializeWithoutFirstSettingBinaryFormatterBinder|
|CheckId|CA2301|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

A <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> seri durumundan çıkarma yöntemi çağrılan veya başvurulan olmadan <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özellik kümesi.

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural bulur <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> yöntem çağrıları veya başvuruları seri durumdan çıkarma olduğunda <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> yok, <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> ayarlayın. İle herhangi bir seri durumundan çıkarma engellemek istiyorsanız <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> bakılmaksızın <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özelliği, bu kuralı devre dışı bırak ve [CA2302](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md)ve kuralı etkinleştirmek [CA2300](ca2300-do-not-use-insecure-deserializer-binaryformatter.md).

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

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>İhlali

```csharp
using System;
using System.IO;
using System.Runtime.Serialization.Formatters.Binary;

[Serializable]
public class BookRecord
{
    public string Title { get; set; }
    public string Author { get; set; }
    public int PageCount { get; set; }
    public AisleLocation Location { get; set; }
}

[Serializable]
public class AisleLocation
{
    public char Aisle { get; set; }
    public byte Shelf { get; set; }
}

public class ExampleClass
{
    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        BinaryFormatter formatter = new BinaryFormatter();
        using (MemoryStream ms = new MemoryStream(bytes))
        {
            return (BookRecord) formatter.Deserialize(ms);
        }
    }
}
```

```vb
Imports System
Imports System.IO
Imports System.Runtime.Serialization.Formatters.Binary

<Serializable()>
Public Class BookRecord
    Public Property Title As String
    Public Property Author As String
    Public Property Location As AisleLocation
End Class

<Serializable()>
Public Class AisleLocation
    Public Property Aisle As Char
    Public Property Shelf As Byte
End Class

Public Class ExampleClass
    Public Function DeserializeBookRecord(bytes As Byte()) As BookRecord
        Dim formatter As BinaryFormatter = New BinaryFormatter()
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(formatter.Deserialize(ms), BookRecord)
        End Using
    End Function
End Class
```

### <a name="solution"></a>Çözüm

```csharp
using System;
using System.IO;
using System.Runtime.Serialization;
using System.Runtime.Serialization.Formatters.Binary;

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

[Serializable]
public class BookRecord
{
    public string Title { get; set; }
    public string Author { get; set; }
    public int PageCount { get; set; }
    public AisleLocation Location { get; set; }
}

[Serializable]
public class AisleLocation
{
    public char Aisle { get; set; }
    public byte Shelf { get; set; }
}

public class ExampleClass
{
    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        BinaryFormatter formatter = new BinaryFormatter();
        formatter.Binder = new BookRecordSerializationBinder();
        using (MemoryStream ms = new MemoryStream(bytes))
        {
            return (BookRecord) formatter.Deserialize(ms);
        }
    }
}
```

```vb
Imports System
Imports System.IO
Imports System.Runtime.Serialization
Imports System.Runtime.Serialization.Formatters.Binary

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

<Serializable()>
Public Class BookRecord
    Public Property Title As String
    Public Property Author As String
    Public Property Location As AisleLocation
End Class

<Serializable()>
Public Class AisleLocation
    Public Property Aisle As Char
    Public Property Shelf As Byte
End Class

Public Class ExampleClass
    Public Function DeserializeBookRecord(bytes As Byte()) As BookRecord
        Dim formatter As BinaryFormatter = New BinaryFormatter()
        formatter.Binder = New BookRecordSerializationBinder()
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(formatter.Deserialize(ms), BookRecord)
        End Using
    End Function
End Class
```

## <a name="related-rules"></a>İlgili kuralları

[CA2300: Güvenli olmayan seri durumdan çıkarıcının BinaryFormatter kullanmayın](ca2300-do-not-use-insecure-deserializer-binaryformatter.md)

[CA2302: BinaryFormatter.Binder BinaryFormatter.Deserialize çağırmadan önce ayarlandığından emin olun](ca2302-ensure-binaryformatter-binder-is-set-before-calling-binaryformatter-deserialize.md)