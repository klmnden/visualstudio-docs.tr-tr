---
title: 'CA2001: Sorunlu metotları çağırmaktan kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2001
- AvoidCallingProblematicMethods
helpviewer_keywords:
- CA2001
- AvoidCallingProblematicMethods
ms.assetid: 19db8edb-31ce-441c-b0de-a0f2746155b7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 95209067f3821b6446b64dc7990e189720d20cea
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233187"
---
# <a name="ca2001-avoid-calling-problematic-methods"></a>CA2001: Sorunlu metotları çağırmaktan kaçının

|||
|-|-|
|TypeName|AvoidCallingProblematicMethods|
|CheckId|CA2001|
|Kategori|Microsoft. güvenilirliği|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir üye olası tehlikeli ya da sorunlu yöntemi çağırır.

## <a name="rule-description"></a>Kural açıklaması

Gereksiz ve potansiyel olarak tehlikeli Yöntem çağrıları yapmaktan kaçının. Bu kuralın ihlali, bir üye aşağıdaki yöntemlerden birini çağırdığında oluşur:

|Yöntem|Açıklama|
|------------|-----------------|
|<xref:System.GC.Collect%2A?displayProperty=fullName>|GC çağrılıyor. Toplama, uygulama performansını önemli ölçüde etkileyebilir ve nadiren gereklidir. Daha fazla bilgi için, MSDN 'de bkz. [Riko Marianı 'Nin performans ve](http://go.microsoft.com/fwlink/?LinkId=169256) blog girişi.|
|<xref:System.Threading.Thread.Resume%2A?displayProperty=fullName><br /><br /> <xref:System.Threading.Thread.Suspend%2A?displayProperty=fullName>|Thread. Suspend ve Thread. özgeçmişi öngörülemeyen davranışları nedeniyle kullanım dışı bırakıldı.  İş parçacıklarını ve kaynakları korumak <xref:System.Threading> için,, ve <xref:System.Threading.Monitor> <xref:System.Threading.Semaphore>gibi <xref:System.Threading.Mutex>ad alanındaki diğer sınıfları kullanın.|
|<xref:System.Runtime.InteropServices.SafeHandle.DangerousGetHandle%2A?displayProperty=fullName>|DangerousGetHandle çağrısını yöntemi, geçerli olmayan bir tanıtıcı döndürebildiğinden bir güvenlik riski taşıyor. DangerousGetHandle çağrısını yönteminin nasıl güvenli <xref:System.Runtime.InteropServices.SafeHandle.DangerousRelease%2A> bir şekilde kullanılacağı hakkında daha fazla bilgi için bkz. veyöntemleri.<xref:System.Runtime.InteropServices.SafeHandle.DangerousAddRef%2A>|
|<xref:System.Reflection.Assembly.LoadFrom%2A?displayProperty=fullName><br /><br /> <xref:System.Reflection.Assembly.LoadFile%2A?displayProperty=fullName><br /><br /> <xref:System.Reflection.Assembly.LoadWithPartialName%2A?displayProperty=fullName>|Bu yöntemler, beklenmeyen konumlardan derleme yükleyebilir. Örneğin, bkz. Suzanne Cook 'ın .NET CLR notları blog gönderileri [LoadFile vs. LoadFrom](http://go.microsoft.com/fwlink/?LinkId=164450) ve derlemeleri yükleyen yöntemler hakkında bilgi için [bir bağlama bağlamı seçme](http://go.microsoft.com/fwlink/?LinkId=164451) .|
|[Cosetproxypaket](http://go.microsoft.com/fwlink/?LinkID=169250) Ole32<br /><br /> [CoInitializeSecurity](http://go.microsoft.com/fwlink/?LinkId=169255) Ole32|Yönetilen bir işlemde kullanıcı kodunun yürütülmeye başladığı zaman, Cosetproxypaket güvenilir bir şekilde çağrılamaz. Ortak dil çalışma zamanı (CLR), kullanıcıların P/Invoke işleminin başarılı olmasını engelleyebilen başlatma eylemleri alır.<br /><br /> Yönetilen bir uygulama için Cosetproxyıncall çağrısı yapmanız gerekiyorsa, yerel kod (C++) yürütülebilir dosyası kullanarak işlemi başlatmanız, yerel kodda Cosetproxyıncall çağrısı yapmanız ve sonra yönetilen kod uygulamanızı işlem içinde başlatmanız önerilir. (Bir çalışma zamanı sürüm numarası belirttiğinizden emin olun.)|

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için, tehlikeli veya sorunlu yönteme çağrıyı kaldırın veya değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Yalnızca sorunlu yöntemin herhangi bir alternatifi kullanılabilir olmadığında bu kuraldan iletileri bastırmalısınız.

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenilirlik Uyarıları](../code-quality/reliability-warnings.md)