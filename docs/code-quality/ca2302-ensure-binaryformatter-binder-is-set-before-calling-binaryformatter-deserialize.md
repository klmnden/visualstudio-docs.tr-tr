---
title: 'CA2302: BinaryFormatter.Binder BinaryFormatter.Deserialize çağırmadan önce ayarlandığından emin olun'
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
ms.openlocfilehash: fb997d8184ea9459b46eee95bfe2863e8c1c6ed0
ms.sourcegitcommit: 0e22ead8234b2c4467bcd0dc047b4ac5fb39b977
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59367362"
---
# <a name="ca2302-ensure-binaryformatterbinder-is-set-before-calling-binaryformatterdeserialize"></a>CA2302: BinaryFormatter.Binder BinaryFormatter.Deserialize çağırmadan önce ayarlandığından emin olun

|||
|-|-|
|TypeName|EnsureBinaryFormatterBinderIsSetBeforeCallingBinaryFormatterDeserialize|
|CheckId|CA2302|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

A <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> seri durumundan çıkarma yöntemi çağrılan veya başvurulan ve <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özelliği null.

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural bulur <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> yöntem çağrıları veya başvuruları seri durumdan çıkarma sırasında <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> olduğunda kendi <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> null olabilir. İle herhangi bir seri durumundan çıkarma engellemek istiyorsanız <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> bakılmaksızın <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özelliği, bu kuralı devre dışı bırak ve [CA2301](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md)ve kuralı etkinleştirmek [CA2300](ca2300-do-not-use-insecure-deserializer-binaryformatter.md).

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

- Mümkünse, bunun yerine, güvenli bir serileştirici kullanın ve **serisini kaldırmak için rastgele bir tür belirtmek bir saldırgan izin verme**. Bazı güvenli seri hale getiricileri genişletme şunlardır:
  - <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>
  - <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>
  - <xref:System.Web.Script.Serialization.JavaScriptSerializer?displayProperty=nameWithType> -Hiçbir zaman kullanmayın <xref:System.Web.Script.Serialization.SimpleTypeResolver?displayProperty=nameWithType>. Tür çözümleyici kullanmanız gerekirse, seri durumdan çıkarılmış türü beklenen bir listesine erişimi kısıtlamanız gerekir.
  - <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>
  - NewtonSoft Json.NET - TypeNameHandling.None kullanın. Başka bir değer için TypeNameHandling kullanmanız gerekirse, beklenen bir listesi için seri durumdan çıkarılmış türü kısıtlamanız gerekir.
  - Protokol arabellekleri
- Kavram değiştirmesine serileştirilmiş veriler olun. Serileştirme sonra serileştirilmiş veriler şifreli olarak oturum açın. Seri durumdan çıkarılırken önce şifreleme imzası doğrulayın. Şifreleme anahtarının ifşa korumanız gerekir ve anahtar devirlerini için tasarlamanız gerekir.
- Seri durumdan çıkarılmış türlerini kısıtlayın. Özel bir uygulama <xref:System.Runtime.Serialization.SerializationBinder?displayProperty=nameWithType>. İle seri durumdan çıkarılırken önce <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter>ayarlayın <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özelliği özel örneğine <xref:System.Runtime.Serialization.SerializationBinder>. Geçersiz kılınan içinde <xref:System.Runtime.Serialization.SerializationBinder.BindToType%2A> türü beklenmeyen ise yöntemi daha sonra bir özel durum oluşturur.
  - Tüm kod yolları sağlamak <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özellik kümesi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

- Giriş güvenilir olduğunu biliyorsanız, bu kuraldan bir uyarıyı bastırmak güvenlidir. Güven sınırı ve veri akışları, uygulamanızın zaman içinde değişebilir göz önünde bulundurun.
- Yukarıdaki önlemler zamandaki varsa, bu uyarının gösterilmemesi güvenlidir.

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
    public BinaryFormatter Formatter { get; set; }

    public BookRecord DeserializeBookRecord(byte[] bytes)
    {
        using (MemoryStream ms = new MemoryStream(bytes))
        {
            return (BookRecord) this.Formatter.Deserialize(ms);
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
    Public Property Formatter As BinaryFormatter

    Public Function DeserializeBookRecord(bytes As Byte()) As BookRecord
        Using ms As MemoryStream = New MemoryStream(bytes)
            Return CType(Me.Formatter.Deserialize(ms), BookRecord)
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
            throw new ArgumentException("Unexpected type", "typeName");
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
            Throw New ArgumentException("Unexpected type", "typeName")
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

[CA2301: İlk ayarlamadan BinaryFormatter.Binder BinaryFormatter.Deserialize çağırmayın](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md)
