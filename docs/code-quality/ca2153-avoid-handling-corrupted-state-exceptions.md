---
title: Bozuk durum özel durumlar için kod çözümleme kural CA2153
ms.date: 02/19/2019
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4b75e45b8a199265eaefe3a2b3c37ed62039e0eb
ms.sourcegitcommit: 845442e2b515c3ca1e4e47b46cc1cef4df4f08d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/20/2019
ms.locfileid: "56450275"
---
# <a name="ca2153-avoid-handling-corrupted-state-exceptions"></a>CA2153: Bozuk durum özel durumlarını işlemekten kaçının

|||
|-|-|
|TypeName|AvoidHandlingCorruptedStateExceptions|
|CheckId|CA2153|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

[Bozuk durum özel durumlar (CSE'ler)](https://msdn.microsoft.com/magazine/dd419661.aspx) belirtmek, Bellek Bozulması işleminizde mevcut. Bir saldırgan bozuk bir bellek bölgesini bir yararlanma yerleştirebilirsiniz, kilitlenme işlemine izin vermek yerine bu yakalama güvenlik açıklarına neden olabilir.

## <a name="rule-description"></a>Kural açıklaması

CSE, bir işlemin durumunu olduğundan bozuk ve sistem tarafından yakalandı, gösterir. Bozuk durumda senaryosunda, yönteminiz ile işaretlerseniz genel bir işleyici yalnızca özel durumu yakalar. <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?displayProperty=fullName> özniteliği. Varsayılan olarak, [ortak dil çalışma zamanı (CLR)](/dotnet/standard/clr) catch işleyicileri için CSE çağrılmaz.

Güvenli seçenek, bu tür özel durumları yakalama olmadan işleminin kilitlenmesine izin vermektir. Kod bile oturum Bellek Bozulması hataları yararlanmaya saldırganlar izin verebilirsiniz.

Örneğin, tüm özel durumları yakalayan bir genel işleyici CSE'ler yakalama bu uyarıyı tetikler `catch (System.Exception e)` veya `catch` ile özel durum parametresi yok.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu uyarıyı çözmek için şunlardan birini yapın:

- Kaldırma <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> özniteliği. Bu, burada CSE'ler catch işleyicileri geçirilen değil varsayılan çalışma zamanı davranışı geri döner.

- Belirli bir özel durum türleri catch işleyicileri in preference of genel catch işleyicisi kaldırın. Bu işleyici kodu bunları güvenli bir şekilde işleyebilir (nadir) varsayılarak CSE'ler, içerebilir.

- CSE, çağırana özel durum geçirir ve çalışan işlemi sonlandırarak içinde sonuçlanmalıdır catch işleyicisi rethrow.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="pseudo-code-example"></a>Sözde kod örneği

### <a name="violation"></a>İhlali

Bu kural tarafından algılanan düzeni aşağıdaki sözde kod göstermektedir.

```csharp
[HandleProcessCorruptedStateExceptions]
// Method that handles CSE exceptions.
void TestMethod1()
{
    try
    {
        FileStream fileStream = new FileStream("name", FileMode.Create);
    }
    catch (Exception e)
    {
        // Handle exception.
    }
}
```

### <a name="solution-1---remove-the-attribute"></a>1 - çözüm özniteliği Kaldır

Kaldırma <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> öznitelik sağlar bozuk durum özel durumlar, yöntemi tarafından işlenmez.

```csharp
void TestMethod1()
{
    try
    {
        FileStream fileStream = new FileStream("name", FileMode.Create);
    }
    catch (Exception e)
    {
        // Handle exception.
    }
}
```

### <a name="solution-2---catch-specific-exceptions"></a>Çözüm 2 - catch özel durum

Genel bir catch işleyicisi kaldırın ve yalnızca belirli bir özel durum türleri yakalayın.

```csharp
void TestMethod1()
{
    try
    {
        FileStream fileStream = new FileStream("name", FileMode.Create);
    }
    catch (IOException e)
    {
        // Handle IOException.
    }
    catch (UnauthorizedAccessException e)
    {
        // Handle UnauthorizedAccessException.
    }
}
```

### <a name="solution-3---rethrow"></a>3 - çözüm yeniden fırlatma

Özel durumu yeniden.

```csharp
[HandleProcessCorruptedStateExceptions]
void TestMethod1()
{
    try
    {
        FileStream fileStream = new FileStream("name", FileMode.Create);
    }
    catch (Exception e)
    {
        // Rethrow the exception.
        throw;
    }
}
```