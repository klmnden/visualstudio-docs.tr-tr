---
title: Yönetilen nesnelerin özel görünümlerini oluşturma | Microsoft Docs
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
- data types [C#], custom
- custom data types
- managed code, custom data types
- autoexp.dat file
- mcee_cs.dat file
- debugger, expanding data types
- mcee_mc.dat file
ms.assetid: 9969e9b2-9008-4729-8a14-0d6deaa61576
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- dotnet
ms.openlocfilehash: 9a7ff5d534cd343f18d0cf0a841801df434c75e7
ms.sourcegitcommit: 59c48e1e42b48ad25a4e198af670faa4d8dae370
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/10/2019
ms.locfileid: "54204235"
---
# <a name="create-custom-views-of-objects-c-visual-basic-c"></a>Nesnelerin özel görünümlerini oluşturma (C#, Visual Basic, C++)
Visual Studio hata ayıklayıcı değişken pencerelerinde veri türleri görüntüleme biçimini özelleştirebilirsiniz.  
  
## <a name="attributes"></a>Öznitelikler

C# ve Visual Basic kullanarak özel verileri için genişletmeleri ekleyebilirsiniz <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, <xref:System.Diagnostics.DebuggerDisplayAttribute>, ve <xref:System.Diagnostics.DebuggerBrowsableAttribute>.  
  
İçinde [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)] kod, Visual Basic DebuggerBrowsable özniteliği desteklemiyor. Bu sınırlama, .NET Framework'ün daha yeni sürümlerde kaldırılmıştır.    

## <a name="native-code"></a>Yerel kod

C++ kodu için Natvis çerçevesini kullanarak özel veri türü genişletmeleri açıklandığı ekleyebilirsiniz [hata ayıklayıcıda yerel nesnesinin özel görünümlerini oluşturma](/visualstudio/debugger/create-custom-views-of-native-objects). Veya özel veri kullanma genişletmeleri de ekleyebilirsiniz <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, <xref:System.Diagnostics.DebuggerDisplayAttribute>, ve <xref:System.Diagnostics.DebuggerBrowsableAttribute>.

## <a name="visualizers"></a>Görselleştiriciler

Herhangi bir yönetilen veri türü görüntülenecek Görselleştirici yazabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Görselleştirici yazma](/visualstudio/debugger/create-custom-visualizers-of-data).
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [DebuggerTypeProxy özniteliğini kullanma](../debugger/using-debuggertypeproxy-attribute.md)   
 [DebuggerDisplay özniteliğini kullanma](../debugger/using-the-debuggerdisplay-attribute.md)   
 [İzleme ve QuickWatch Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Hata Ayıklayıcı Görüntü Öznitelikleriyle Hata Ayıklamayı Geliştirme](/dotnet/framework/debug-trace-profile/enhancing-debugging-with-the-debugger-display-attributes)