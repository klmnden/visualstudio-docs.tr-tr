---
title: 'Nasıl yapılır: Yüksek performanslı kümede hata ayıklama | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- cluster debugging
- high-performance debugging
ms.assetid: a2f0eb07-840e-4f95-a1b1-9509217e5b8f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8eedc9c469e4ceb4ac4b5be018f2ebdd227ffcf2
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56681796"
---
# <a name="how-to-debug-on-a-high-performance-cluster-c-visual-basic-c"></a>Nasıl yapılır: Yüksek performanslı kümede hata ayıklama (C#, Visual Basic, C++)

Yüksek performanslı kümede çoklu işlem program hata ayıklama uzak bilgisayardaki sıradan bir programın hata ayıklama gibi değildir. Ancak, bazı ek hususlar vardır. Genel Uzaktan Kurulum gereksinimleri için bkz [uzaktan hata ayıklama](../debugger/remote-debugging.md).

 Yüksek performanslı kümede hata ayıklaması yaparken, tüm kullanabilirsiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] windows ve uzaktan hata ayıklama için kullanılabilir olan teknikleri hata ayıklama. Ancak, uzaktan hata ayıklaması yaptığınızdan, harici konsol penceresi kullanılabilir değil.

 **İş parçacıkları** penceresi ve **işlemleri** penceresi özellikle paralel uygulamalarda hata ayıklama için yararlıdır. Bu windows kullanma hakkında daha fazla ipucu için bkz. [nasıl yapılır: İşlemler penceresini kullanma](/previous-versions/visualstudio/visual-studio-2010/7h8h5sdw(v=vs.100)) ve [izlenecek yol: İş parçacıkları penceresini kullanarak hata ayıklama](../debugger/how-to-use-the-threads-window.md).

 Aşağıdaki yordamlar, yüksek performanslı kümede hata ayıklama için özellikle yararlı olan bazı teknikleri gösterir.

 Paralel uygulamada hata ayıklaması yaparken, belirli bir iş parçacığı, işlem veya bilgisayarda bir kesme noktası ayarlamak isteyebilirsiniz. Bu, normal bir kesme noktası oluşturarak ve sonra bir kesme noktası filtresi ekleyerek yapabilirsiniz.

### <a name="to-open-the-breakpoint-filter-dialog-box"></a>Kesme noktası filtresi iletişim kutusunu açmak için

1.  Bir kaynak penceresinde kesme noktası glifine sağ **ayrıştırılmış kodu** penceresinde **çağrı yığını** penceresinde veya **kesme noktaları** penceresi.

2.  Kısayol menüsünde **filtre**. Bu seçenek üst düzey veya alt menüsü altında görünebilir **kesme noktaları**.

### <a name="to-set-a-breakpoint-on-a-specific-computer"></a>Belirli bir bilgisayarda bir kesme noktası ayarlamak için

1.  Bilgisayar adını alın **işlemleri** penceresi.

2.  Bir kesme noktası seçin ve açın **kesme noktası filtresi** önceki yordamda açıklanan iletişim kutusu.

3.  İçinde **kesme noktası filtresi** iletişim kutusunda:

     MachineName =*yourmachinename*

     Daha karmaşık bir filtre oluşturmak için kullanarak ifadeleri birleştirebilirsiniz `&`, AND işleci `||`, OR işleci `!`, NOT işleci ve parantezler.

4.  **Tamam**'ı tıklatın.

### <a name="to-set-a-breakpoint-on-a-specific-process"></a>Belirli bir işlemde bir kesme noktası ayarlamak için

1.  İşlem adı alma veya işlem kimlik numarasını **işlemleri** penceresi.

2.  Bir kesme noktası seçin ve açın **kesme noktası filtresi** ve ilk yordamdaki gibi iletişim kutusu.

3.  İçinde **kesme noktası filtresi** iletişim kutusunda:

     `ProcessName =`  *yourprocessname*

     —veya—

     `ProcessID =` *yourprocessIDnumber*

     Daha karmaşık bir filtre oluşturmak için kullanarak ifadeleri birleştirebilirsiniz `&`, AND işleci `||`, OR işleci `!`, NOT işleci ve parantezler.

4.  **Tamam**'ı tıklatın.

### <a name="to-set-a-breakpoint-on-a-specific-thread"></a>Belirli bir iş parçacığında bir kesme noktası ayarlamak için

1.  İş parçacığı adı veya iş parçacığı kimlik numarasını **iş parçacıkları** penceresi.

2.  Bir kesme noktası seçin ve açın **kesme noktası filtresi** bölümündeki ilk yordamda açıklandığı gibi iletişim kutusu.

3.  İçinde **kesme noktası filtresi** iletişim kutusunda:

     `ThreadName =` *yourthreadname*

     —veya—

     `ThreadID =` *yourthreadIDnumber*

     Daha karmaşık bir filtre oluşturmak için kullanarak ifadeleri birleştirebilirsiniz `&`, AND işleci `||`, OR işleci `!`, NOT işleci ve parantezler.

4.  **Tamam**'ı tıklatın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, adlı bir bilgisayarda bir kesme noktası için bir filtre oluşturma işlemi gösterilmektedir `marvin` ve adlı bir iş parçacığı `fourier1`.

`(MachineName = marvin) & (ThreadName = fourier1)`


## <a name="see-also"></a>Ayrıca Bkz.
- [Çok İş Parçacıklı Uygulamaların Hatalarını Ayıklama](../debugger/debug-multithreaded-applications-in-visual-studio.md)
- [Uzaktan Hata Ayıklama](../debugger/remote-debugging.md)
- [Nasıl yapılır: İşlemler penceresini kullanma](/previous-versions/visualstudio/visual-studio-2010/7h8h5sdw(v=vs.100))
- [Hata ayıklama çok iş parçacıklı uygulamaları kullanmaya başlayın](../debugger/get-started-debugging-multithreaded-apps.md)
- [İş parçacıklarında ve işlemlerde](/previous-versions/visualstudio/visual-studio-2010/ms164740(v=vs.100))
- [Kesme Noktalarını Kullanma](../debugger/using-breakpoints.md)