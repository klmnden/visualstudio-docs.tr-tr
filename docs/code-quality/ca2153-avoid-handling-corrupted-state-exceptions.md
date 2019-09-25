---
title: Bozuk durum özel durumları için kod analizi kuralı CA2153
ms.date: 02/19/2019
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 36442ad0792ef712acd322d17688d8ceb21444cb
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231887"
---
# <a name="ca2153-avoid-handling-corrupted-state-exceptions"></a>CA2153: Bozuk durum özel durumlarını işlemeyi önleyin

|||
|-|-|
|TypeName|AvoidHandlingCorruptedStateExceptions|
|CheckId|CA2153|
|Kategori|Microsoft.Security|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

[Bozulmuş durum özel durumları (CSEs)](https://msdn.microsoft.com/magazine/dd419661.aspx) , işlem sırasında bellek bozulmasının bulunduğunu gösterir. Bir saldırgan bozuk bellek bölgesine bir yararlanma işlemi gerçekleştirilebileceği takdirde, işlemin çökmesine izin vermek yerine bunları yakalama güvenlik açıklarına yol açabilir.

## <a name="rule-description"></a>Kural açıklaması

CSE, bir işlemin durumunun bozuk olduğunu ve sistem tarafından yakalanmadığını gösterir. Bozuk durum senaryosunda, bir genel işleyici yalnızca yöntemi <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute?displayProperty=fullName> özniteliğiyle işaretlediğinizde özel durumu yakalar. Varsayılan olarak, [ortak dil çalışma zamanı (CLR)](/dotnet/standard/clr) CSEs için catch işleyicilerini çağırmaz.

En güvenli seçenek, işlemin bu tür özel durumları yakalanmadan kilitlenmesine izin vermaktır. Günlüğe kaydetme kodu bile saldırganların bellek bozulması hatalarından yararlanmaya çalışmasına izin verebilir.

Bu uyarı, `catch (System.Exception e)` örneğin veya `catch` özel durum parametresi olmadan, tüm özel durumları yakalayan genel bir işleyici ile CSEs yakalama sırasında tetiklenir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu uyarıyı çözmek için aşağıdakilerden birini yapın:

- <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> Özniteliği kaldırın. Bu, CSEs 'nin catch işleyicilerine geçirilmediği varsayılan çalışma zamanı davranışına geri döner.

- Özel özel durum türlerini yakalayacak işleyicilerin tercih halinde genel catch işleyicisini kaldırın. Bu, işleyici kodunun güvenli bir şekilde işleyebileceğini (nadir) varsayarak, CSEs içerebilir.

- Özel durumu çağırana geçiren ve çalışan işlemi sonlandırmaya neden olması gereken catch işleyicisinde CSE 'yi yeniden oluşturun.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="pseudo-code-example"></a>Sözde kod örneği

### <a name="violation"></a>Edildiği

Aşağıdaki sözde kod, bu kural tarafından algılanan kalıbı gösterir.

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

### <a name="solution-1---remove-the-attribute"></a>Çözüm 1-özniteliği kaldırma

Özniteliğini kaldırmak <xref:System.Runtime.ExceptionServices.HandleProcessCorruptedStateExceptionsAttribute> , bozuk durum özel durumlarının yönteminiz tarafından işlenmemesini sağlar.

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

### <a name="solution-2---catch-specific-exceptions"></a>Çözüm 2-belirli özel durumları yakala

Genel catch işleyicisini kaldırın ve yalnızca belirli özel durum türlerini yakalayın.

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

### <a name="solution-3---rethrow"></a>Çözüm 3-Rethrow

Özel durumu yeniden oluşturun.

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