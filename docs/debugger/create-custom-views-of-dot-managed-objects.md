---
title: Nesnelerin özel görünümlerini oluşturma | Microsoft Docs
ms.date: 01/08/2019
ms.topic: conceptual
f1_keywords:
- vs.debug.data.elements
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- data types, custom
- custom data types
- managed code, custom data types
- autoexp.dat file
- mcee_cs.dat file
- debugger, expanding data types
- mcee_mc.dat file
ms.assetid: 9969e9b2-9008-4729-8a14-0d6deaa61576
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- dotnet
ms.openlocfilehash: 911f0423184f22919be016691b9333b2f62d1b61
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66744795"
---
# <a name="create-custom-views-of-objects-c-visual-basic-c"></a>Nesnelerin özel görünümlerini oluşturma (C#, Visual Basic, C++)
Visual Studio hata ayıklayıcı değişken pencerelerinde veri türleri görüntüleme biçimini özelleştirebilirsiniz.

## <a name="native-code"></a>Yerel kod

İçin C++ kodu ekleyebileceğiniz Natvis çerçevesini kullanarak özel veri türü genişletmeleri açıklandığı [özel görünümlerini oluşturma C++ hata ayıklayıcısı nesnelerini](/visualstudio/debugger/create-custom-views-of-native-objects). İçin C++/CLI kodunu ayrıca kullanabileceğiniz burada bu makalede açıklanan öznitelikleri.

## <a name="attributes"></a>Öznitelikler

İçinde C#, Visual Basic ve C++ (C++/CLI kodu), özel veri kullanma genişletmeleri ekleyebilirsiniz <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, <xref:System.Diagnostics.DebuggerDisplayAttribute>, ve <xref:System.Diagnostics.DebuggerBrowsableAttribute>.

.NET Framework 2.0 kodda, Visual Basic DebuggerBrowsable özniteliğini desteklemiyor. Bu sınırlama, .NET Framework'ün daha yeni sürümlerde kaldırılmıştır.

## <a name="visualizers"></a>Görselleştiriciler

Herhangi bir yönetilen veri türü görüntülenecek Görselleştirici yazabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Görselleştirici yazma](/visualstudio/debugger/create-custom-visualizers-of-data).

## <a name="see-also"></a>Ayrıca Bkz.

- [DebuggerDisplay özniteliğini kullanma göstermek hangi hata ayıklayıcının işlemi durdurmasını](../debugger/using-the-debuggerdisplay-attribute.md)
- [Debugger DebuggerTypeProxy özniteliğini kullanma göstermek için ne tür söyleyin](../debugger/using-debuggertypeproxy-attribute.md)
- [İzleme ve Hızlı İzleme Pencereleri](../debugger/watch-and-quickwatch-windows.md)
- [Hata Ayıklayıcı Görüntü Öznitelikleriyle Hata Ayıklamayı Geliştirme](/dotnet/framework/debug-trace-profile/enhancing-debugging-with-the-debugger-display-attributes)