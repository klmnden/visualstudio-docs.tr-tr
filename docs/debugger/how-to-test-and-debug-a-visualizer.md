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
ms.openlocfilehash: f0353234e5a266ca1a344ce7bc304f27d8c3af95
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62906290"
---
# <a name="how-to-test-and-debug-a-visualizer"></a>Nasıl yapılır: Test ve hata ayıklama Görselleştirici
Görselleştirici, hata ayıklama ve test için ihtiyaç duyduğunuz bir kez yazdığınız.

Görselleştiriciyi sınamak için bir Visual Studio yükleyerek ve bir hata ayıklayıcı penceresinde çağırma yoludur. (Bkz [nasıl yapılır: Görselleştiriciyi yükleme](../debugger/how-to-install-a-visualizer.md).) Bunu yaparsanız, ekleyin ve hata ayıklayıcı ilk örneğinde çalışan görselleştiricisi hata ayıklamak için Visual Studio'nun ikinci bir örneğini kullanmanız gerekir.

Görselleştiriciyi hata ayıklamak için daha kolay bir yolu, bir test sürücüsünden görselleştiricisi çalıştırmaktır. Görselleştirici API'leri adı verilen bu tür bir sürücüsü oluşturmak kolaylaştırır *Görselleştirici geliştirme konak*.

### <a name="to-create-a-visualizer-development-host"></a>Görselleştirici geliştirme ana bilgisayar oluşturmak için

1. Hata ayıklayıcı tarafı sınıfınızda oluşturan bir statik yöntem dahil bir <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerDevelopmentHost> nesne ve onun show yöntemi çağırır:

    ```csharp
    public static void TestShowVisualizer(object objectToVisualize)
    {
        VisualizerDevelopmentHost myHost = new VisualizerDevelopmentHost(objectToVisualize, typeof(DebuggerSide));
        myHost.ShowVisualizer();
    }
    ```

    Ana bilgisayar oluşturmak için kullanılan görselleştiricisi içinde gösterilecek veri nesnesi parametreleridir (`objectToVisualize`) ve hata ayıklayıcı tarafı sınıf türü.

2. Çağırmak için aşağıdaki deyimi ekleyin `TestShowVisualizer`. Bir sınıf kitaplığında, görselleştiricisi oluşturduysanız, sınıf kitaplığı çağırın ve bu bildirimi, yürütülebilir dosya yerleştirmek için yürütülebilir bir dosya oluşturmak gerekir:

    ```csharp
    DebuggerSide.TestShowVisualizer(myString);
    ```

    Daha eksiksiz bir örnek için bkz: [izlenecek yol: Görselleştirici yazma C# ](../debugger/walkthrough-writing-a-visualizer-in-csharp.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [İzlenecek yol: C# Dilinde Görselleştirici Yazma](../debugger/walkthrough-writing-a-visualizer-in-csharp.md)
- [Nasıl yapılır: Görselleştiriciyi Yükleme](../debugger/how-to-install-a-visualizer.md)
- [Özel Görselleştirici Oluşturma](../debugger/create-custom-visualizers-of-data.md)
