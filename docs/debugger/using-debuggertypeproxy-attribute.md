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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cfe19bea0b62b7d137ac806208a9c505469cd214
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/26/2019
ms.locfileid: "55069596"
---
# <a name="using-debuggertypeproxy-attribute-c-visual-basic-ccli"></a>DebuggerTypeProxy özniteliğini kullanma (C#, Visual Basic, C + +/ CLI)

<xref:System.Diagnostics.DebuggerTypeProxyAttribute> bir proxy ya da bir tür ve tür şeklini hata ayıklayıcı pencerelerinde görüntülenen değişiklikler için stand-in belirtir. Bir proxy sahip bir değişken görüntülediğinizde, proxy özgün türü için anlamına gelir **görüntüleme**. Proxy türü yalnızca genel üyeleri hata ayıklayıcı değişken penceresinde görüntüler. Özel üyeler görüntülenmez.

Bu öznitelik için uygulanabilir:

- Yapılar
- Sınıflar
- Derlemeleri

> [!NOTE]
> Yerel kod için bu öznitelik yalnızca C + desteklenir +/ CLI kodu.

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
