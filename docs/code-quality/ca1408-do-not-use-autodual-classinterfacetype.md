---
title: 'CA1408: AutoDual ClassInterFaceType kullanmayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotUseAutoDualClassInterfaceType
- CA1408
helpviewer_keywords:
- CA1408
- DoNotUseAutoDualClassInterfaceType
ms.assetid: 60ca5e02-3c51-42dd-942b-4f950eecfa0f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: b26d92ca63a94cac7e293a688b1c7b3331586877
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234787"
---
# <a name="ca1408-do-not-use-autodual-classinterfacetype"></a>CA1408: AutoDual ClassInterFaceType kullanmayın

|||
|-|-|
|TypeName|DoNotUseAutoDualClassInterfaceType|
|CheckId|CA1408|
|Kategori|Microsoft. çalışabilirliği|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bileşen nesne modeli (com) görünür türü <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliği `AutoDual` değeri <xref:System.Runtime.InteropServices.ClassInterfaceType>olarak ayarlanan özniteliğiyle işaretlenir.

## <a name="rule-description"></a>Kural açıklaması
Çift arabirim kullanan türler, belirli bir arabirim düzenine bağlanmak için istemcileri etkinleştirir. Gelecek sürümdeki değişiklikler, türün düzeni veya bazı temel türler, arayüze bağlanan COM istemcilerini kesintiye uğratır. Varsayılan olarak, <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> öznitelik belirtilmemişse, yalnızca bir dağıtım arabirimi kullanılır.

Aksi belirtilmedikçe genel olmayan genel türler COM 'a görünür; Tüm ortak ve genel türler COM 'da görünmez.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliğinin `None` değerini değerini <xref:System.Runtime.InteropServices.ClassInterfaceType> değiştirin ve arabirimi açık olarak tanımlayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Türün düzeninin ve temel türlerinin sonraki bir sürümde değişmemesini gerekmedikçe, bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bir açık arabirim kullanmak için kuralı ve bir yeniden bildirimini ihlal eden bir sınıfı gösterir.

[!code-csharp[FxCop.Interoperability.AutoDual#1](../code-quality/codesnippet/CSharp/ca1408-do-not-use-autodual-classinterfacetype_1.cs)]
[!code-vb[FxCop.Interoperability.AutoDual#1](../code-quality/codesnippet/VisualBasic/ca1408-do-not-use-autodual-classinterfacetype_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA1403 Otomatik Düzen türleri COM görünebilir olmamalıdır](../code-quality/ca1403-auto-layout-types-should-not-be-com-visible.md)

[CA1412 ComSource Arabirimlerini IDispatch olarak işaretle](../code-quality/ca1412-mark-comsource-interfaces-as-idispatch.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Birlikte Çalışma için .NET Türlerini Niteleme](/dotnet/framework/interop/qualifying-net-types-for-interoperation)
- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)