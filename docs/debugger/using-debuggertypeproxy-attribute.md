---
title: DebuggerTypeProxy özniteliğini kullanma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- attributes [C#], debugger
- DebuggerTypeProxyAttribute class
- DebuggerTypeProxy attribute
ms.assetid: 943f3bb1-993e-4800-a47e-0af78b063014
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a7a2ca6cbeba30f836a4878db569db14ff2af10d
ms.sourcegitcommit: 59c48e1e42b48ad25a4e198af670faa4d8dae370
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/10/2019
ms.locfileid: "54204260"
---
# <a name="using-debuggertypeproxy-attribute-c-visual-basic"></a>DebuggerTypeProxy özniteliğini kullanma (C#, Visual Basic)

<xref:System.Diagnostics.DebuggerTypeProxyAttribute> bir proxy ya da bir tür ve tür şeklini hata ayıklayıcı pencerelerinde görüntülenen değişiklikler için stand-in belirtir. Bir proxy sahip bir değişken görüntülediğinizde, proxy özgün türü için anlamına gelir **görüntüleme**. Proxy türü yalnızca genel üyeleri hata ayıklayıcı değişken penceresinde görüntüler. Özel üyeler görüntülenmez.

Bu öznitelik için uygulanabilir:

- Yapılar
- Sınıflar
- Derlemeleri

Proxy yerini alacak türünde bir bağımsız değişken alan bir oluşturucu türü proxy sınıfı olmalıdır. Hedef türünde bir değişken görüntülemek ihtiyaç duyduğu her seferinde hata ayıklayıcı türü proxy sınıfının yeni bir örneğini oluşturur. Bu performans etkileri olabilir. Sonuç olarak, tüm kıyasla daha fazla oluşturucuda kesin olarak gerekmedikçe yapmamanız gerekir.

Türü kullanıcı tıklayarak genişletilir sürece performans cezaları en aza indirmek için ifade değerlendirici türündeki görüntü proxy özniteliklerinde incelemez + simgesi hata ayıklayıcı penceresinde veya kullanımını <xref:System.Diagnostics.DebuggerBrowsableAttribute>. Bu nedenle, öznitelikler görünen türün kendisine girmemelisiniz. Öznitelikleri olabilir ve görünen yöntemin gövdesinde kullanılmalıdır.

Özel bir iç içe geçmiş sınıf sınıf içinde olacak şekilde proxy türü için iyi bir fikir olduğunu, öznitelik hedefleri. Bu durum iç üyeleri bir kolayca erişmenizi sağlar.

<xref:System.Diagnostics.DebuggerTypeProxyAttribute> proxy türü üzerinde bir temel sınıf belirtilmişse bu türetilmiş sınıfların kendi proxy türü belirtmediğiniz sürece, türetilmiş bir sınıfa uygulanır, devralınabilir.

Varsa <xref:System.Diagnostics.DebuggerTypeProxyAttribute> derleme düzeyinde kullanılan `Target` parametresi proxy değiştirilecek olan türünü belirtir.

Bu öznitelik ile birlikte kullanma örneği için <xref:System.Diagnostics.DebuggerDisplayAttribute> ve <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, bkz:[DebuggerDisplay özniteliğini kullanma](../debugger/using-the-debuggerdisplay-attribute.md).

## <a name="using-generics-with-debuggertypeproxy"></a>DebuggerTypeProxy ile Genellemeleri kullanma

Genel türler için destek sınırlıdır. C# ' ta, `DebuggerTypeProxy` yalnızca açık türlerini destekler. Unconstructed bir tür olarak da bilinir, açık bir tür bağımsız değişkenleri için tür parametrelerinden biri ile oluşturulmadı genel bir türdür. Oluşturulan türler olarak da bilinir, kapalı türleri desteklenmez.

Açık bir tür için söz dizimi şu şekilde görünür:

`Namespace.TypeName<,>`

Bir hedef olarak bir genel tür kullanıyorsanız `DebuggerTypeProxy`, bu sözdizimini kullanmanız gerekir. `DebuggerTypeProxy` Mekanizması, tür parametreleri algılar.

C# açık ve kapalı türleri hakkında daha fazla bilgi için bkz. [C# dil belirtimi](/dotnet/csharp/language-reference/language-specification), 20.5.2 bölümünü açın ve türleri.

Visual Basic açık tür sözdizimi olmadığından, Visual Basic'te de aynı bunu yapamazsınız. Bunun yerine açık tür adı bir dize gösterimini kullanmanız gerekir.

`"Namespace.TypeName'2"`

## <a name="see-also"></a>Ayrıca Bkz.

- [DebuggerDisplay Özniteliğini Kullanma](../debugger/using-the-debuggerdisplay-attribute.md)
- [.Managed nesnelerin özel görünümlerini oluşturma](../debugger/create-custom-views-of-dot-managed-objects.md)
- [Hata Ayıklayıcı Görüntü Öznitelikleriyle Hata Ayıklamayı Geliştirme](/dotnet/framework/debug-trace-profile/enhancing-debugging-with-the-debugger-display-attributes)
