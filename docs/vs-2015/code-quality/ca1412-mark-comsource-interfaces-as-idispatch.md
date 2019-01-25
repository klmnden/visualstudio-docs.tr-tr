---
title: 'CA1412: ComSource arabirimlerini IDispatch olarak işaretleyin | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- MarkComSourceInterfacesAsIDispatch
- CA1412
helpviewer_keywords:
- CA1412
- MarkComSourceInterfacesAsIDispatch
ms.assetid: 131a7563-0410-443c-a8f5-52104250cfb4
caps.latest.revision: 18
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 59fec1fddb16296f1238deb5c2f9bbf0c350cdd2
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54794935"
---
# <a name="ca1412-mark-comsource-interfaces-as-idispatch"></a>CA1412: ComSource arabirimlerini IDispatch olarak işaretleyin
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|MarkComSourceInterfacesAsIDispatch|
|CheckId|CA1412|
|Kategori|Microsoft.Interoperability|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir türü ile işaretlenmiş <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> özniteliği ve en az bir belirtilen arabirim işaretlenmemiş ile <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> özniteliğini `InterfaceIsDispatch` değeri.

## <a name="rule-description"></a>Kural Tanımı
 <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> Bileşen Nesne Modeli (COM) istemcilere bir sınıfı gösterir olay arabirimi tanımlamak için kullanılır. Bu arabirimleri olarak sunulmalıdır `InterfaceIsIDispatch` olay bildirimlerini almak üzere Visual Basic 6 COM istemcileri etkinleştirmek için. Varsayılan bir arabirim ile işaretlenmemiş olması <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> öznitelik, bir çift arabirim sunulur.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için ekleme veya değiştirme <xref:System.Runtime.InteropServices.InterfaceTypeAttribute> değeri ile belirtilen tüm arabirimlerin InterfaceIsIDispatch için ayarlanır böylece öznitelik <xref:System.Runtime.InteropServices.ComSourceInterfacesAttribute> özniteliği.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, burada bu arabirimlerinden birini kuralını ihlal eden bir sınıfı gösterir.

 [!code-csharp[FxCop.Interoperability.MarkIDispatch#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Interoperability.MarkIDispatch/cs/FxCop.Interoperability.MarkIDispatch.cs#1)]
 [!code-vb[FxCop.Interoperability.MarkIDispatch#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Interoperability.MarkIDispatch/vb/FxCop.Interoperability.MarkIDispatch.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1408: AutoDual ClassInterfaceType kullanma](../code-quality/ca1408-do-not-use-autodual-classinterfacetype.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Nasıl yapılır: Bir COM havuzu tarafından işlenen olay](http://msdn.microsoft.com/7c9944b2-e951-4c3e-a0a1-59b2ae37d7fd) [yönetilmeyen kod ile birlikte](http://msdn.microsoft.com/library/ccb68ce7-b0e9-4ffb-839d-03b1cd2c1258)
