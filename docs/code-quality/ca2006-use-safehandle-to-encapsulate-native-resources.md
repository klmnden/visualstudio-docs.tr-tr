---
title: 'CA2006: Yerel kaynakları kapsamak için SafeHandle kullanın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2006
- UseSafeHandleToEncapsulateNativeResources
helpviewer_keywords:
- UseSafeHandleToEncapsulateNativeResources
- CA2006
ms.assetid: a71950bd-bcc1-463d-b1f2-5233bc451456
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- cplusplus
ms.openlocfilehash: 0e671deab060346bb998932495e5590f19945eaa
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233098"
---
# <a name="ca2006-use-safehandle-to-encapsulate-native-resources"></a>CA2006: Yerel kaynakları kapsamak için SafeHandle kullanın

|||
|-|-|
|TypeName|UseSafeHandleToEncapsulateNativeResources|
|CheckId|CA2006|
|Kategori|Microsoft. güvenilirliği|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Yönetilen kod, <xref:System.IntPtr> yerel kaynaklara erişmek için kullanır.

## <a name="rule-description"></a>Kural açıklaması

`IntPtr` Yönetilen kodda kullanımı olası bir güvenlik ve güvenilirlik sorununa işaret edebilir. ' Nin `IntPtr` tüm kullanımları, onun yerine bir ya da benzer bir <xref:System.Runtime.InteropServices.SafeHandle> teknolojinin kullanılması gerekip gerekmediğini belirleyebilmek için incelenmelidir. Yönetilen kodun sahip olarak kabul `IntPtr` edildiği bellek, dosya tanıtıcısı veya bir yuva gibi bir yerel kaynağı temsil ediyorsa sorunlar meydana gelir. Yönetilen kod kaynağın sahibi ise, bunun bir hata olması durumunda kaynak sızıntısı oluşmasına neden olacağından, onunla ilişkili yerel kaynakları da serbest bırakmalıdır.

Bu tür senaryolarda, `IntPtr` `IntPtr` çok iş parçacıklı erişime izin veriliyorsa ve tarafından temsil edilen kaynağı serbest bırakma yoluyla güvenlik veya güvenilirlik sorunları da vardır. Bu sorunlar, kaynağın eşzamanlı kullanımı `IntPtr` başka bir iş parçacığında yapıldığında kaynak sürümündeki değerin geri dönüşümünü içerir. Bu, bir iş parçacığının yanlış kaynakla ilişkili verileri okuyabildiği veya yazabileceği yarış koşullarına neden olabilir. Örneğin, türünüz bir işletim sistemi tanıtıcısını bir `IntPtr` olarak depoluyorsa ve kullanıcıların her zaman ve bu tanıtıcıyı kullanan başka bir yöntemi aynı anda ve bir tür eşitleme olmadan çağırmasını sağlar.

Bu tanıtıcı geri dönüştürme sorunu, verilerin bozulmasına ve sıklıkla bir güvenlik açığına neden olabilir. `SafeHandle`ve eşdüzey sınıfı <xref:System.Runtime.InteropServices.CriticalHandle> , bu tür iş parçacığı sorunlarından kaçınılması için bir kaynağa yerel tanıtıcıyı kapsüllemek için bir mekanizma sağlar. Ek olarak, diğer iş `SafeHandle` parçacığı sorunları için ve `CriticalHandle` alt sınıfını kullanarak, yerel metotların çağrıları üzerinde yerel tanıtıcının bir kopyasını içeren yönetilen nesnelerin ömrünü dikkatlice kontrol edebilirsiniz. Bu durumda, genellikle çağrılarını `GC.KeepAlive`kaldırabilirsiniz. `SafeHandle` Ve kullanırken, daha az bir `CriticalHandle`dereceye kadar yaptığınız performans yükü, dikkatli bir tasarım aracılığıyla azalabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Yerel `IntPtr` kaynaklara erişimi `SafeHandle` güvenle yönetmek için kullanımı öğesine dönüştürün. Örnekler için <xref:System.Runtime.InteropServices.SafeHandle> başvuru makalesine bakın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu uyarıyı bastırmayın.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IDisposable>