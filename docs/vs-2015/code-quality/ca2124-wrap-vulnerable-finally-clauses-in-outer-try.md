---
title: 'CA2124: Savunmasız sonunda yan tümcelerini dış sarmalayın | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology: vs-devops-test
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- CA2124
- WrapVulnerableFinallyClausesInOuterTry
helpviewer_keywords:
- CA2124
- WrapVulnerableFinallyClausesInOuterTry
ms.assetid: 82efd224-9e60-4b88-a0f5-dfabcc49a254
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 6ec643e28d35884513f92a6bb5e90cd9065d7b08
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53967689"
---
# <a name="ca2124-wrap-vulnerable-finally-clauses-in-outer-try"></a>CA2124: Savunmasız sonunda yan tümcelerini dış sarmalayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|WrapVulnerableFinallyClausesInOuterTry|
|CheckId|CA2124|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 1.0 ve 1.1 sürümlerinde [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)], bir ortak veya korumalı yöntem içerir bir `try` / `catch` / `finally` blok. `finally` Blok güvenlik durumunu sıfırlamak için görünür ve sınırlanan değil bir `finally` blok.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural bulur `try` / `finally` 1.0 ve 1.1 sürümlerini hedefleyen kodda engeller [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] olabilecek kötü amaçlı bir özel durum filtreleri çağrı yığınında mevcut açıktır. Kimliğe bürünme gibi hassas işlemler try bloğunda oluşur ve bir özel durum, filtre önce yürütebilir `finally` blok. Kimliğe bürünme örneği için bu filtrenin bürünülen kullanıcıyla yürütmesine anlamına gelir. Şu anda yalnızca Visual Basic'te implementable filtrelerdir.

> [!WARNING]
>  **Not** 2.0 ve sonraki sürümlerinde [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)], çalışma zamanı otomatik olarak koruyan bir `try` / `catch` /  `finally` sıfırlama oluşursa kötü amaçlı bir özel durum filtrelerden engelle doğrudan yöntem içinde özel durum bloğu içerir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Sarmalanmış halden yerleştirin `try` / `finally` bir dış try bloğu içinde. Aşağıdaki ikinci örneğe bakın. Bu zorlar `finally` filtre kodundan önce yürütülecek.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="pseudo-code-example"></a>Sözde kod örneği

### <a name="description"></a>Açıklama
 Bu kural tarafından algılanan düzeni aşağıdaki sözde kod göstermektedir.

### <a name="code"></a>Kod

```
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

## <a name="example"></a>Örnek
 Aşağıdaki sözde kod kodunuzu koruyun ve bu kural karşılamak için kullanabileceğiniz desenini gösterir.

```
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
