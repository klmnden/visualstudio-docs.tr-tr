---
title: 'CA2302: BinaryFormatter.Deserialize çağırmadan önce BinaryFormatter.Binder öğesinin ayarlandığından emin olun'
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
- CA2302
- EnsureBinaryFormatterBinderIsSetBeforeCallingBinaryFormatterDeserialize
ms.openlocfilehash: 1d7c87921a226b8918bfaa79fda6de85d710baa4
ms.sourcegitcommit: 673b9364fc9a96b027662dcb4cf5d61cab60ef11
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2019
ms.locfileid: "69891197"
---
# <a name="ca2302-ensure-binaryformatterbinder-is-set-before-calling-binaryformatterdeserialize"></a>CA2302: BinaryFormatter.Deserialize çağırmadan önce BinaryFormatter.Binder öğesinin ayarlandığından emin olun

|||
|-|-|
|TypeName|EnsureBinaryFormatterBinderIsSetBeforeCallingBinaryFormatterDeserialize|
|CheckId|CA2302|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Seri kaldırma yöntemi çağrıldı veya başvuruluyor <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> ve özellik null olabilir. <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType>

## <a name="rule-description"></a>Kural açıklaması

[!INCLUDE[insecure-deserializers-description](includes/insecure-deserializers-description-md.md)]

Bu kural, <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType> <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> null olabileceği zaman seri kaldırma yöntemi çağrılarını veya başvurularını bulur. <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> Özelliği <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter> ne olursa olsun, serisini kaldırmak istiyorsanız, bu kuralı ve [CA2301](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md)' ı devre dışı bırakın ve [CA2300](ca2300-do-not-use-insecure-deserializer-binaryformatter.md)kuralını etkinleştirin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

- Mümkünse, bunun yerine güvenli bir serileştirici kullanın ve **bir saldırganın seri durumdan çıkarmak için rastgele bir tür belirtmesini sağlayın**. Bazı güvenli serileştiriciler şunları içerir:
  - <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=nameWithType>
  - <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=nameWithType>
  - <xref:System.Web.Script.Serialization.JavaScriptSerializer?displayProperty=nameWithType>-Hiçbir şekilde <xref:System.Web.Script.Serialization.SimpleTypeResolver?displayProperty=nameWithType>kullanmayın. Bir tür Çözümleyicisi kullanmanız gerekiyorsa, serisi kaldırılan türleri beklenen bir listeyle kısıtlayın.
  - <xref:System.Xml.Serialization.XmlSerializer?displayProperty=nameWithType>
  - Newtonsoft Json.NET-TypeNameHandling. None kullanın. TypeNameHandling için başka bir değer kullanmanız gerekiyorsa, serisi kaldırılan türleri özel bir ISerializationBinder ile beklenen bir listeyle kısıtlayın.
  - Protokol arabellekleri
- Seri hale getirilen verileri prova yapın. Serileştirmeden sonra, serileştirilmiş verileri şifreli olarak imzalayın. Seri durumdan önce, şifreleme imzasını doğrulayın. Şifreleme anahtarını, önemli döndürmeler için açıklanmasını ve tasarıma karşı koruyun.
- Seri durumdan çıkarılan türleri kısıtla. Özel <xref:System.Runtime.Serialization.SerializationBinder?displayProperty=nameWithType>bir uygulama uygulayın. İle <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter>seri durumdan kaldırmadan önce, <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özelliği özel <xref:System.Runtime.Serialization.SerializationBinder>bir örneğine ayarlayın. Geçersiz kılınan <xref:System.Runtime.Serialization.SerializationBinder.BindToType%2A> yöntemde, tür beklenmiyorsa, serisini durdurmak için bir özel durum oluşturur.
  - Tüm kod yollarının <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Binder> özellik kümesine sahip olduğundan emin olun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

[!INCLUDE[insecure-deserializers-common-safe-to-suppress](includes/insecure-deserializers-common-safe-to-suppress-md.md)]

## <a name="pseudo-code-examples"></a>Sözde kod örnekleri

### <a name="violation"></a>Edildiği

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

## <a name="related-rules"></a>İlgili kurallar

[CA2300: Güvenli olmayan seri hale getirici BinaryFormatter kullanma](ca2300-do-not-use-insecure-deserializer-binaryformatter.md)

[CA2301: İlk önce BinaryFormatter. Ciltçi ayarını yapmadan BinaryFormatter. serisini çağırma](ca2301-do-not-call-binaryformatter-deserialize-without-first-setting-binaryformatter-binder.md)
