---
title: 'CA2000: Kapsamı kaybetmeden önce nesneleri bırakın'
ms.date: 05/14/2019
ms.topic: reference
f1_keywords:
- CA2000
- Dispose objects before losing scope
- DisposeObjectsBeforeLosingScope
helpviewer_keywords:
- CA2000
- DisposeObjectsBeforeLosingScope
ms.assetid: 0c3d7d8d-b94d-46e8-aa4c-38df632c1463
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 732b3d683802c50042ee40fee1549a9d247e2470
ms.sourcegitcommit: 283f2dbce044a18e9f6ac6398f6fc78e074ec1ed
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "65804972"
---
# <a name="ca2000-dispose-objects-before-losing-scope"></a>CA2000: Kapsamı kaybetmeden önce nesneleri bırakın

|||
|-|-|
|TypeName|DisposeObjectsBeforeLosingScope|
|CheckId|CA2000|
|Kategori|Microsoft.Reliability|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Yerel bir nesne bir <xref:System.IDisposable> türü oluşturulur, ancak nesne tüm başvuruları kapsam dışına çıkmadan önce nesne atılmaz.

## <a name="rule-description"></a>Kural açıklaması

Tüm başvuruları kapsam dışı olmadan önce atılabilir bir nesne açıkça elden değil, nesnenin çöp toplayıcı nesnenin Sonlandırıcısı çalıştığında belirsiz bir zamanda silinip. Olağanüstü bir olay ortaya çıkabilecek çünkü Sonlandırıcı engelleyecek çalışmasını nesne, nesne açıkça elden çıkarılmalıdır.

### <a name="special-cases"></a>Özel durumlar

Nesne değil kaldırıldıktan bile kural CA2000 aşağıdaki türleri için yerel nesnelerin başlatılmıyor:

- <xref:System.IO.Stream?displayProperty=nameWithType>
- <xref:System.IO.TextReader?displayProperty=nameWithType>
- <xref:System.IO.TextWriter?displayProperty=nameWithType>
- <xref:System.Resources.IResourceReader?displayProperty=nameWithType>

Şu türlerden birinde bir nesne için bir oluşturucu geçirerek ve bir alan atayarak gösteren bir *sahipliğinin aktarılmasını dispose* yeni oluşturulan tür için. Diğer bir deyişle, yeni oluşturulan tür artık nesnesinin elden için sorumludur. Kodunuz şu türlerden birinde bir nesne için bir oluşturucu geçirir, hiçbir nesne tüm başvuruları önce bırakılmıyor bile CA2000 gerçekleşir kural ihlalini kapsam dışına demektir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için çağrı <xref:System.IDisposable.Dispose%2A> tüm başvuruları kapsam dışı olmadan önce nesne üzerinde.

Kullanabileceğiniz [ `using` deyimi](/dotnet/csharp/language-reference/keywords/using-statement) ([ `Using` ](/dotnet/visual-basic/language-reference/statements/using-statement) Visual Basic'te) uygulayan nesneler sarmalamak için <xref:System.IDisposable>. Bu şekilde sarmalanmış nesneler otomatik olarak sonunda atıldı `using` blok. Ancak, aşağıdaki durumlarda kullanılmamalıdır veya ile işlenemez bir `using` deyimi:

- Atılabilir bir nesne döndürülecek nesne gerekir oluşturulmuş içinde bir `try/finally` bloğu dışında bir `using` blok.

- Oluşturucusunun içinde tek kullanımlık bir nesnenin üyelerine başlatmayın bir `using` deyimi.

- Ne zaman yalnızca bir özel durum işleyicisi tarafından korunan oluşturuculara iç içe içinde [edinme parçası bir `using` deyimi](/dotnet/csharp/language-reference/language-specification/statements#the-using-statement), dış oluşturucu içinde bir hata hiçbir zaman iç içe geçmiş Oluşturucu tarafından oluşturulan nesne neden olabilir kapatıldığından kuşkulanılıyor. Aşağıdaki örnekte, bir hata <xref:System.IO.StreamReader> Oluşturucusu sonuçlanabilir <xref:System.IO.FileStream> nesne hiçbir zaman kapatıldığından kuşkulanılıyor. Bu durumda, CA2000 kural ihlalini işaretler.

   ```csharp
   using (StreamReader sr = new StreamReader(new FileStream("C:\myfile.txt", FileMode.Create)))
   { ... }
   ```

- Dinamik nesneler dispose desenini uygulamak için bir gölge nesnesi kullanmalıdır <xref:System.IDisposable> nesneleri.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Sürece bu kuraldan bir uyarıyı bastırmayın:

- Bir yöntemi çağıran nesneniz üzerinde çağırdıktan `Dispose`, gibi <xref:System.IO.Stream.Close%2A>
- Uyarı verir başlatan yöntem bir <xref:System.IDisposable> nesnenizi sarmalayan bir nesne
- Dispose sahipliği ayırma metoduna sahip değil; diğer bir deyişle, nesneyi silmek için sorumluluk başka bir nesne veya yöntem içinde oluşturulan ve çağırana döndürülen sarmalayıcı aktarılır

## <a name="related-rules"></a>İlgili kuralları

- [CA2213: Atılabilen alanlar atılmalıdır](../code-quality/ca2213-disposable-fields-should-be-disposed.md)
- [CA2202: Nesneleri birden çok kez atmayın](../code-quality/ca2202-do-not-dispose-objects-multiple-times.md)

## <a name="example"></a>Örnek

Atılabilir bir nesne döndüren bir yöntem uyguluyorsanız, nesneyi elden emin olmak için bir try/finally bloğu bir catch bloğu olmadan kullanın. Bir try/finally bloğu kullanarak hataya noktada oluşturulması ve bu nesneyi elden emin olmak özel durumlara izin.

OpenPort1 yönteminde ISerializable nesneyi çevirmek için SerialPort açmak için bir çağrı veya SomeMethod çağrısı başarısız olabilir. Bu uygulama üzerinde CA2000 uyarısı oluşturulur.

OpenPort2 yönteminde bildirilmiş ve ayarlanmış null iki çevirmek için SerialPort nesneleri şunlardır:

- `tempPort`, yöntemi işlemleri başarılı olduğunu test etmek için kullanılır.

- `port`, yöntemin dönüş değeri için kullanılır.

`tempPort` Oluşturulur ve açılır bir `try` blok ve diğer gerekli iş aynı gerçekleştirilir `try` blok. Sonunda `try` blok, açılan bağlantı noktası atanır `port` döndürülecek nesne ve `tempPort` nesne ayarlandığında `null`.

`finally` Blok değerini denetler `tempPort`. Null değilse, yöntem bir işlem başarısız oldu, ve `tempPort` tüm kaynakları serbest bırakıldığından emin olmak için kapatılır. Döndürülen bağlantı nesnesi yöntemi işlemleri başarılı ya da bir işlem başarısız olursa null olacaktır açılmış çevirmek için SerialPort nesne içerir.

```csharp
public SerialPort OpenPort1(string portName)
{
   SerialPort port = new SerialPort(portName);
   port.Open();  //CA2000 fires because this might throw
   SomeMethod(); //Other method operations can fail
   return port;
}

public SerialPort OpenPort2(string portName)
{
   SerialPort tempPort = null;
   SerialPort port = null;
   try
   {
      tempPort = new SerialPort(portName);
      tempPort.Open();
      SomeMethod();
      //Add any other methods above this line
      port = tempPort;
      tempPort = null;

   }
   finally
   {
      if (tempPort != null)
      {
         tempPort.Close();
      }
   }
   return port;
}
```

```vb
Public Function OpenPort1(ByVal PortName As String) As SerialPort

   Dim port As New SerialPort(PortName)
   port.Open()    'CA2000 fires because this might throw
   SomeMethod()   'Other method operations can fail
   Return port

End Function

Public Function OpenPort2(ByVal PortName As String) As SerialPort

   Dim tempPort As SerialPort = Nothing
   Dim port As SerialPort = Nothing

   Try
      tempPort = New SerialPort(PortName)
      tempPort.Open()
      SomeMethod()
      'Add any other methods above this line
      port = tempPort
      tempPort = Nothing

   Finally
      If Not tempPort Is Nothing Then
         tempPort.Close()
      End If

   End Try

   Return port

End Function
```

## <a name="example"></a>Örnek

Varsayılan olarak, Visual Basic Derleyicisi için taşmayı denetle tüm aritmetik işleçlere sahiptir. Bu nedenle, herhangi bir Visual Basic aritmetik işlem fırlatabilir bir <xref:System.OverflowException>. Bu kurallar CA2000 gibi beklenmeyen ihlallerini neden olabilir. Örneğin, Visual Basic Derleyicisi, yönerge değil çıkarılması StreamReader neden olan bir özel durum oluşturabilir eklenmesi için denetimi taşma yayma çünkü aşağıdaki CreateReader1 işlevi bir CA2000 ihlaline neden olur.

Bunu düzeltmek için projenizdeki Visual Basic derleyici tarafından taşma denetimleri yaymayı devre dışı bırakabilir veya kodunuz aşağıdaki CreateReader2 işlevi olduğu gibi değiştirebilirsiniz.

Taşma denetimleri yaymayı devre dışı bırakmak için Çözüm Gezgini'nde proje adına sağ tıklayın ve ardından **özellikleri**. Tıklayın **derleme**, tıklayın **Gelişmiş derleme seçenekleri**, iade edin **tamsayı taşması denetimlerini Kaldır**.

[!code-vb[FxCop.Reliability.CA2000.DisposeObjectsBeforeLosingScope#1](../code-quality/codesnippet/VisualBasic/ca2000-dispose-objects-before-losing-scope-vboverflow_1.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IDisposable>
- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)