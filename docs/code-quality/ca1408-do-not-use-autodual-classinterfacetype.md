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
ms.openlocfilehash: c811c7e2b6ba06c716179469c8b038fd26b3b38a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546039"
---
# <a name="ca1408-do-not-use-autodual-classinterfacetype"></a>CA1408: AutoDual ClassInterFaceType kullanmayın

|||
|-|-|
|TypeName|DoNotUseAutoDualClassInterfaceType|
|CheckId|CA1408|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bileşen Nesne Modeli (COM) görünen bir tür ile işaretlenmiş <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliğini `AutoDual` değerini <xref:System.Runtime.InteropServices.ClassInterfaceType>.

## <a name="rule-description"></a>Kural açıklaması
 Çift arabirim kullanan türler, belirli bir arabirim düzenine bağlanmak için istemcileri etkinleştirir. Gelecek sürümdeki değişiklikler, türün düzeni veya bazı temel türler, arayüze bağlanan COM istemcilerini kesintiye uğratır. Varsayılan olarak, <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliği belirtilmezse, yalnızca gönderme arabirimi kullanılır.

 Tersi durumda işaretlenmiş sürece tüm genel türlere COM görünür; Tüm özel ve genel türler COM'a görünmez

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için değerini değiştirmek <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliğini `None` değerini <xref:System.Runtime.InteropServices.ClassInterfaceType> ve arabirimini açıkça tanımlar.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu düzen türü kendi taban türleri ve gelecekte yayımlanacak bir sürümde değişmez belirli olmadığı sürece bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kural ve açık bir arabirim kullanmak için sınıfı yeniden bildirimi ihlal eden bir sınıfı gösterir.

 [!code-csharp[FxCop.Interoperability.AutoDual#1](../code-quality/codesnippet/CSharp/ca1408-do-not-use-autodual-classinterfacetype_1.cs)]
 [!code-vb[FxCop.Interoperability.AutoDual#1](../code-quality/codesnippet/VisualBasic/ca1408-do-not-use-autodual-classinterfacetype_1.vb)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1403: Otomatik Yerleşim türleri COM görünebilir olmamalıdır](../code-quality/ca1403-auto-layout-types-should-not-be-com-visible.md)

 [CA1412: ComSource arabirimlerini IDispatch olarak işaretleyin](../code-quality/ca1412-mark-comsource-interfaces-as-idispatch.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Birlikte Çalışma için .NET Türlerini Niteleme](/dotnet/framework/interop/qualifying-net-types-for-interoperation)
- [Yönetilmeyen Kod ile Birlikte Çalışma](/dotnet/framework/interop/index)