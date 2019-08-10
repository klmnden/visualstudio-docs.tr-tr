---
title: 'CA2144: Saydam kod derlemeleri bayt dizilerinden yüklememelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2144
ms.assetid: 777b1310-6e16-4413-b4ee-5f3136304f82
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9ff77d02ef9778112f5229e8104e9a1c1a1cde87
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68920432"
---
# <a name="ca2144-transparent-code-should-not-load-assemblies-from-byte-arrays"></a>CA2144: Saydam kod derlemeleri bayt dizilerinden yüklememelidir

|||
|-|-|
|TypeName|TransparentMethodsShouldNotLoadAssembliesFromByteArrays|
|CheckId|CA2144|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Saydam bir yöntem, aşağıdaki yöntemlerden birini kullanarak bir bayt dizisinden bir derlemeyi yükler:

- <xref:System.Reflection.Assembly.Load%2A>

- <xref:System.Reflection.Assembly.Load%2A>

- <xref:System.Reflection.Assembly.Load%2A>

## <a name="rule-description"></a>Kural açıklaması
Saydam kod için güvenlik incelemesi kritik kod için güvenlik incelemesi kadar kapsamlı değildir, çünkü saydam kod güvenlik duyarlı eylemleri gerçekleştiremez. Bir bayt dizisinden yüklenen derlemeler saydam kodda fark edilmeyebilir ve o bayt dizisi denetlenmesi gereken kritik ya da daha da önemlisi güvenli kritik kod içerebilir. Bu nedenle, saydam kodun bir bayt dizisinden derlemeleri yüklemesi gerekmez.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, <xref:System.Security.SecurityCriticalAttribute> <xref:System.Security.SecuritySafeCriticalAttribute> veya özniteliğiyle derlemeyi yükleyen yöntemi işaretleyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Saydam bir yöntem bir bayt dizisinden bir derlemeyi yüklediği için kural aşağıdaki kodda ateşlenir.

[!code-csharp[FxCop.Security.CA2144.TransparentMethodsShouldNotLoadAssembliesFromByteArrays#1](../code-quality/codesnippet/CSharp/ca2144-transparent-code-should-not-load-assemblies-from-byte-arrays_1.cs)]