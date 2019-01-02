---
title: Yönetilen nesnelerin özel görünümlerini oluşturma | Microsoft Docs
ms.date: 11/04/2016
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
ms.openlocfilehash: 389deb0b6504ca5c7a3716399429f176e5dc7870
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53861442"
---
# <a name="create-custom-views-of-managed-objects"></a>Yönetilen nesnelerin özel görünümlerini oluşturma
Visual Studio hata ayıklayıcı değişken pencerelerinde veri türleri görüntüleme biçimini özelleştirebilirsiniz.  
  
## <a name="attributes"></a>Öznitelikler  
 C# ve Visual Basic kullanarak özel verileri için genişletmeleri ekleyebilirsiniz <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, <xref:System.Diagnostics.DebuggerDisplayAttribute>, ve <xref:System.Diagnostics.DebuggerBrowsableAttribute>.  
  
 İçinde [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)] kod, Visual Basic DebuggerBrowsable özniteliği desteklemiyor. Bu sınırlama, .NET Framework'ün daha yeni sürümlerde kaldırılmıştır.  
  
## <a name="visualizers"></a>Görselleştiriciler  
 Herhangi bir yönetilen veri türü görüntülenecek Görselleştirici yazabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Görselleştirici yazma](/visualstudio/debugger/create-custom-visualizers-of-data).  
  
## <a name="native-code"></a>Yerel kod  
 Yerel kod için özel veri türü genişletmeleri, Program Files\Microsoft Visual Studio 11.0\Common7\Packages\Debugger dizininde bulunan dosya autoexp.dat ekleyebilirsiniz. Yazma yönergeler `autoexp` kuralları dosyasında bulunur.  
  
> [!CAUTION]
>  Bu dosya yapısını ve söz dizimi autoexp kurallarının bir Visual Studio sürümünden sonraki değişebilir.  
  
 Yerel tür görünümleri, bir ifade değerlendirici eklenti yazarak da özelleştirilebilir. Daha fazla bilgi için [EEAddIn örnek: Hata ayıklama ifade değerlendirici eklenti](https://msdn.microsoft.com/library/d4f6b068-c812-45bc-9ec0-7e0363c4bb9e).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [DebuggerTypeProxy özniteliğini kullanma](../debugger/using-debuggertypeproxy-attribute.md)   
 [DebuggerDisplay özniteliğini kullanma](../debugger/using-the-debuggerdisplay-attribute.md)   
 [İzleme ve QuickWatch Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Hata Ayıklayıcı Görüntü Öznitelikleriyle Hata Ayıklamayı Geliştirme](/dotnet/framework/debug-trace-profile/enhancing-debugging-with-the-debugger-display-attributes)