---
title: 'CA1408: AutoDual ClassInterfaceType kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotUseAutoDualClassInterfaceType
- CA1408
helpviewer_keywords:
- CA1408
- DoNotUseAutoDualClassInterfaceType
ms.assetid: 60ca5e02-3c51-42dd-942b-4f950eecfa0f
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 88d23ee703b482813ad0a5401e9dea7adf9a063c
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65705703"
---
# <a name="ca1408-do-not-use-autodual-classinterfacetype"></a>CA1408: AutoDual ClassInterFaceType kullanmayın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotUseAutoDualClassInterfaceType|
|CheckId|CA1408|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bileşen Nesne Modeli (COM) görünen bir tür ile işaretlenmiş <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliğini `AutoDual` değerini <xref:System.Runtime.InteropServices.ClassInterfaceType>.

## <a name="rule-description"></a>Kural Tanımı
 Çift arabirim kullanan türler, belirli bir arabirim düzenine bağlanmak için istemcileri etkinleştirir. Gelecek sürümdeki değişiklikler, türün düzeni veya bazı temel türler, arayüze bağlanan COM istemcilerini kesintiye uğratır. Varsayılan olarak, <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliği belirtilmezse, yalnızca gönderme arabirimi kullanılır.

 Tersi durumda işaretlenmiş sürece tüm genel türlere COM görünür; Tüm özel ve genel türler COM'a görünmez

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için değerini değiştirmek <xref:System.Runtime.InteropServices.ClassInterfaceAttribute> özniteliğini `None` değerini <xref:System.Runtime.InteropServices.ClassInterfaceType> ve arabirimini açıkça tanımlar.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu düzen türü kendi taban türleri ve gelecekte yayımlanacak bir sürümde değişmez belirli olmadığı sürece bu kuraldan bir uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kural ve açık bir arabirim kullanmak için sınıfı yeniden bildirimi ihlal eden bir sınıfı gösterir.

 [!code-csharp[FxCop.Interoperability.AutoDual#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.AutoDual/cs/FxCop.Interoperability.AutoDual.cs#1)]
 [!code-vb[FxCop.Interoperability.AutoDual#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Interoperability.AutoDual/vb/FxCop.Interoperability.AutoDual.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1403: Otomatik Yerleşim türleri COM görünebilir olmamalıdır](../code-quality/ca1403-auto-layout-types-should-not-be-com-visible.md)

 [CA1412: ComSource arabirimlerini IDispatch olarak işaretleyin](../code-quality/ca1412-mark-comsource-interfaces-as-idispatch.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Sınıf arabirimine giriş](https://msdn.microsoft.com/733c0dd2-12e5-46e6-8de1-39d5b25df024) [birlikte çalışma için .NET türlerini niteleme](https://msdn.microsoft.com/library/4b8afb52-fb8d-4e65-b47c-fd82956a3cdd) [yönetilmeyen kod ile birlikte](https://msdn.microsoft.com/library/ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258)
