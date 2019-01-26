---
title: 'Nasıl yapılır: Görselleştiriciyi hata ayıklama ve test | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- visualizers, testing
- visualizers, debugging
- debugging [Visual Studio], visualizers
ms.assetid: 5cc12ce8-c819-48e4-b487-98d403001b28
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 89a7cd7648b7e04e82e5e490f4958ad5a97f6521
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54936543"
---
# <a name="how-to-test-and-debug-a-visualizer"></a>Nasıl yapılır: Test ve hata ayıklama Görselleştirici
Görselleştirici, hata ayıklama ve test için ihtiyaç duyduğunuz bir kez yazdığınız.  
  
 Görselleştiriciyi sınamak için bir Visual Studio yükleyerek ve bir hata ayıklayıcı penceresinde çağırma yoludur. (Bkz [nasıl yapılır: Görselleştiriciyi yükleme](../debugger/how-to-install-a-visualizer.md).) Bunu yaparsanız, ekleyin ve hata ayıklayıcı ilk örneğinde çalışan görselleştiricisi hata ayıklamak için Visual Studio'nun ikinci bir örneğini kullanmanız gerekir.  
  
 Görselleştiriciyi hata ayıklamak için daha kolay bir yolu, bir test sürücüsünden görselleştiricisi çalıştırmaktır. Görselleştirici API'leri adı verilen bu tür bir sürücüsü oluşturmak kolaylaştırır *Görselleştirici geliştirme konak*.  
  
### <a name="to-create-a-visualizer-development-host"></a>Görselleştirici geliştirme ana bilgisayar oluşturmak için  
  
1.  Hata ayıklayıcı tarafı sınıfınızda oluşturan bir statik yöntem dahil bir <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerDevelopmentHost> nesne ve onun show yöntemi çağırır:  
  
    ```csharp
    public static void TestShowVisualizer(object objectToVisualize)  
    {  
       VisualizerDevelopmentHost myHost = new VisualizerDevelopmentHost(objectToVisualize, typeof(DebuggerSide));  
       myHost.ShowVisualizer();  
    }  
    ```  
  
     Ana bilgisayar oluşturmak için kullanılan görselleştiricisi içinde gösterilecek veri nesnesi parametreleridir (`objectToVisualize`) ve hata ayıklayıcı tarafı sınıf türü.  
  
2.  Çağırmak için aşağıdaki deyimi ekleyin `TestShowVisualizer`. Bir sınıf kitaplığında, görselleştiricisi oluşturduysanız, sınıf kitaplığı çağırın ve bu bildirimi, yürütülebilir dosya yerleştirmek için yürütülebilir bir dosya oluşturmak gerekir:  
  
    ```csharp
    DebuggerSide.TestShowVisualizer(myString);  
    ```  
  
     Daha eksiksiz bir örnek için bkz: [izlenecek yol: Görselleştirici yazma C# ](../debugger/walkthrough-writing-a-visualizer-in-csharp.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İzlenecek yol: C# ile Görselleştirici yazma](../debugger/walkthrough-writing-a-visualizer-in-csharp.md)   
 [Nasıl yapılır: Görselleştiriciyi yükleme](../debugger/how-to-install-a-visualizer.md)   
 [Özel Görselleştirici Oluşturma](../debugger/create-custom-visualizers-of-data.md)
