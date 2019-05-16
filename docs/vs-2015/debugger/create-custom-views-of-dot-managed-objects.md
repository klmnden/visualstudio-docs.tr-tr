---
title: Yönetilen nesnelerin özel görünümlerini oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.data.elements
dev_langs:
- FSharp
- VB
- CSharp
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
caps.latest.revision: 37
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cb5b56404c7ddc99b7999b47cf3c2a899f915efd
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65702414"
---
# <a name="create-custom-views-of-managed-objects"></a>Yönetilen nesnelerin özel görünümlerini oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio hata ayıklayıcı değişken pencerelerinde veri türleri görüntüleme biçimini özelleştirebilirsiniz.  
  
## <a name="attributes"></a>Öznitelikler  
 C# ve Visual Basic kullanarak özel verileri için genişletmeleri ekleyebilirsiniz <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, <xref:System.Diagnostics.DebuggerDisplayAttribute>, ve <xref:System.Diagnostics.DebuggerBrowsableAttribute>.  
  
 İçinde [!INCLUDE[dnprdnlong](../includes/dnprdnlong-md.md)] kod, Visual Basic DebuggerBrowsable özniteliği desteklemiyor. Bu sınırlama, .NET Framework'ün daha yeni sürümlerde kaldırılmıştır.  
  
## <a name="visualizers"></a>Görselleştiriciler  
 Herhangi bir yönetilen veri türü görüntülenecek Görselleştirici yazabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Görselleştirici yazma](../debugger/how-to-write-a-visualizer.md).  
  
## <a name="native-code"></a>Yerel kod  
 Yerel kod için özel veri türü genişletmeleri, Program Files\Microsoft Visual Studio 11.0\Common7\Packages\Debugger dizininde bulunan dosya autoexp.dat ekleyebilirsiniz. Yazma yönergeler `autoexp` kuralları dosyasında bulunur.  
  
> [!CAUTION]
> Bu dosya yapısını ve söz dizimi autoexp kurallarının bir Visual Studio sürümünden sonraki değişebilir.  
  
 Yerel tür görünümleri, bir ifade değerlendirici eklenti yazarak da özelleştirilebilir. Daha fazla bilgi için [EEAddIn örnek: Hata ayıklama ifade değerlendirici eklenti](https://msdn.microsoft.com/d4f6b068-c812-45bc-9ec0-7e0363c4bb9e).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [DebuggerTypeProxy özniteliğini kullanma](../debugger/using-debuggertypeproxy-attribute.md)   
 [DebuggerDisplay özniteliğini kullanma](../debugger/using-the-debuggerdisplay-attribute.md)   
 [İzleme ve QuickWatch Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Hata Ayıklayıcı Görüntü Öznitelikleriyle Hata Ayıklamayı Geliştirme](https://msdn.microsoft.com/library/72bb7aa9-459b-42c4-9163-9312fab4c410)
