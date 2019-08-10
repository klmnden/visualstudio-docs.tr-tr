---
title: 'CA2124: Savunmasız sonunda yan tümcelerini dış deneme içine sarmalayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2124
- WrapVulnerableFinallyClausesInOuterTry
helpviewer_keywords:
- CA2124
- WrapVulnerableFinallyClausesInOuterTry
ms.assetid: 82efd224-9e60-4b88-a0f5-dfabcc49a254
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c75c7c240f694b18caacefc0f9b1ee07f54faf36
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920794"
---
# <a name="ca2124-wrap-vulnerable-finally-clauses-in-outer-try"></a>CA2124: Savunmasız sonunda yan tümcelerini dış deneme içine sarmalayın

|||
|-|-|
|TypeName|WrapVulnerableFinallyClausesInOuterTry|
|CheckId|CA2124|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
.NET Framework 1,0 ve 1,1 sürümlerinde, genel veya korumalı bir `try` Yöntem bir / `catch` / `finally` blok içerir. Blok güvenlik durumunu sıfırlayıp bir `finally` blok içine alınmaz. `finally`

## <a name="rule-description"></a>Kural açıklaması
Bu kural, `try` çağrı yığınında mevcut olan kötü amaçlı özel durum filtrelerinde savunmasız olabilecek .NET Framework 1,0 ve 1,1 sürümlerini hedefleyen koddaki blokları bulur / `finally` . Kimliğe bürünme gibi hassas işlemler try bloğunda gerçekleşirse ve bir özel durum oluşturulursa, filtre `finally` bloğundan önce yürütülür. Kimliğe bürünme örneği için bu, filtrenin kimliğine bürünülen kullanıcı olarak yürütüleceği anlamına gelir. Filtreler Şu anda yalnızca Visual Basic ' de uygulardır.

> [!NOTE]
> .NET Framework 2,0 sürümlerinde ve sonrasında, sıfırlama doğrudan yöntem içinde gerçekleşirse, çalışma zamanı `try` kötü amaçlı durum filtrelerinden bir /  / `catch` `finally` bloğu otomatik olarak korur. özel durum bloğunu içerir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Sarmalanmamış `try` / bir dıştrybloğunayerleştirin.`finally` Aşağıdaki ikinci örneğe bakın. Bu, `finally` kodu filtre kodundan önce yürütmeye zorlar.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="pseudo-code-example"></a>Sözde kod örneği

### <a name="description"></a>Açıklama

Aşağıdaki sözde kod, bu kural tarafından algılanan kalıbı gösterir.

```csharp
try {
   // Do some work.
   Impersonator imp = new Impersonator("John Doe");
   imp.AddToCreditCardBalance(100);
}
finally {
   // Reset security state.
   imp.Revert();
}
```

Aşağıdaki sözde kod, kodunuzu korumak ve bu kuralı karşılamak için kullanabileceğiniz bir model gösterir.

```csharp
try {
     try {
        // Do some work.
     }
     finally {
        // Reset security state.
     }
}
catch()
{
    throw;
}
```