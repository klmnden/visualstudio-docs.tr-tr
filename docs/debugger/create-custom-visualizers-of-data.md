---
title: Verilerin özel Görselleştiricilerini oluşturma | Microsoft Docs
ms.custom: ''
ms.date: 06/19/2017
ms.technology: vs-ide-debug
ms.topic: conceptual
f1_keywords:
- vs.debug.visualizer.troubleshoot
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
helpviewer_keywords:
- debugger, visualizers
- visualizers
ms.assetid: c24c006f-f2ac-429f-89db-677fc0c6e1ea
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 859bf6493a06663a8977898ffa07d600b826d458
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49854318"
---
# <a name="create-custom-visualizers-of-data"></a>Verilerin özel Görselleştiricilerini oluşturma
 Görselleştiriciler bileşenlerinin [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] hata ayıklayıcı kullanıcı arabirimi. A *Görselleştirici* bir iletişim kutusu veya bir değişkeni veya nesneyi, veri türüne uygun bir şekilde görüntülemek için başka bir arabirim oluşturur. Örneğin, bir HTML Görselleştirici bir HTML dizesi olarak yorumlar ve sonucu bir tarayıcı penceresinde görüneceği şekilde görüntüler; bit eşlem Görselleştirici bir bit eşlem yapısı yorumlar ve onu gösteren grafiği görüntüler. Bazı görselleştiriciler yanı sıra değişiklik verilerini görüntülemek etkinleştirin.

 [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] Hata ayıklayıcı altı standart görselleştiriciler içerir. Bunlar, metin, HTML, XML ve JSON görselleştiriciler, her biri dize nesneler üzerinde çalışmak, bir WPF nesne görsel ağacı özelliklerini görüntülemek için WPF ağacı görselleştiricisini, ve veri kümesi, DataView ve DataTable nesneleri için çalışan bir veri kümesi görselleştiricisi. Ek görselleştiriciler, gelecekte Microsoft Corporation'ın indirilebilir olabilir ve üçüncü taraflar ve topluluktan kullanılabilir. Ayrıca, kendi görselleştiriciler yazabilir ve bunları yüklemek [!INCLUDE[vs_current_short](../code-quality/includes/vs_current_short_md.md)] hata ayıklayıcı.

 > [!NOTE]
 > Yerel kod için özel Görselleştirici oluşturmak için bkz [SQLite yerel hata ayıklama görselleştiricisi](https://github.com/Microsoft/VSSDK-Extensibility-Samples/tree/master/SqliteVisualizer) örnek. Özel görselleştiriciler, UWP ve Windows 8.x uygulamalarında desteklenmiyor.

 Hata ayıklayıcıda, görselleştiriciler Büyüteç simgesi ile temsil edilen ![VisualizerIcon](../debugger/media/dbg-tips-visualizer-icon.png "Görselleştirici simgesi"). Büyüteç simgesini gördüğünüzde bir **DataTip**, gibi hata ayıklayıcı penceresindeki **Watch** penceresinde veya **QuickWatch** iletişim kutusu için Büyüteç tıklayabilirsiniz karşılık gelen nesne veri türü için uygun Görselleştirici'ı seçin.

## <a name="overview-of-custom-visualizers"></a>Özel görselleştiriciler genel bakış

Dışında herhangi bir yönetilen sınıfın bir nesnesi için özel Görselleştirici yazabileceğiniz <xref:System.Object> veya <xref:System.Array>.  
  
 Hata ayıklama görselleştiricisi mimarisini iki bölümden oluşur:  
  
- *Hata ayıklayıcı, yan* Visual Studio hata ayıklayıcısı içinde çalıştırır. Hata ayıklayıcı tarafı kodunu oluşturup, görselleştiricisi için kullanıcı arabirimini görüntüler.  
  
- *Hata ayıklanan yan* Visual Studio hata ayıklama işlemi içinde çalıştırılan ( *hata ayıklanan*).  
  
  (Bir dize nesnesi, örneğin gibi) görselleştirmek istediğiniz veri nesnesi içinde hata ayıklanan işlem var. Bu nedenle, bu veri nesnesi daha sonra oluşturduğunuz bir kullanıcı arabirimi kullanarak görüntüleyebilirsiniz hata ayıklayıcı tarafa göndermek hata ayıklanan yan vardır.  
  
  Hata ayıklayıcı yan gelen görünür için bu veri nesnesi alan bir *nesne sağlayıcı* uygulayan <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider> arabirimi. Hata ayıklanan yan üzerinden veri nesnesine gönderir *nesne kaynağı*, türetilen <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource>. Nesne sağlayıcısı ayrıca veri görüntüler yanı sıra düzenler Görselleştirici yazma sağlar, nesne kaynak için verileri geri gönderebilirsiniz. İfade değerlendirici ve, bu nedenle, nesne kaynağı konuşmak için nesne sağlayıcı geçersiz kılınabilir  
  
  Hata ayıklanan yan ve hata ayıklayıcı yan başka iletişim kurmak <xref:System.IO.Stream>. Yöntemler, bir veri nesnesine serileştirmek için sağlanan bir <xref:System.IO.Stream> ve seri durumdan <xref:System.IO.Stream> yeniden içine bir veri nesnesi.  
  
  Hata ayıklanan tarafı kod DebuggerVisualizer özniteliğini kullanarak belirtilen (<xref:System.Diagnostics.DebuggerVisualizerAttribute>).  
  
  Hata ayıklayıcı tarafında görselleştiricisi kullanıcı arabirimi oluşturmak için devralınan bir sınıf oluşturmanız gerekir <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer> ve geçersiz kılma <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer.Show%2A?displayProperty=fullName> arabirim görüntülemesi için yöntemi.  
  
  Kullanabileceğiniz <xref:Microsoft.VisualStudio.DebuggerVisualizers.IDialogVisualizerService> Windows forms iletişim kutuları ve, Görselleştirici denetimlerini görüntülemek için.  
  
  Genel türler için destek sınırlıdır. Yalnızca genel tür açık bir tür ise, genel türde bir hedef için Görselleştirici yazabilirsiniz. Bu kısıtlama aynı kısıtlama olarak kullanıldığında `DebuggerTypeProxy` özniteliği. Ayrıntılar için bkz [DebuggerTypeProxy özniteliğini kullanma](../debugger/using-debuggertypeproxy-attribute.md).  
  
  Özel görselleştiriciler, güvenlik konuları olabilir. Bkz: [Görselleştirici güvenlik konuları](../debugger/visualizer-security-considerations.md).  
  
  Aşağıdaki yordamlar Görselleştirici oluşturmak için yapmanız gerekenleri gösteren üst düzey bir görünüm sağlar. Daha ayrıntılı bir açıklaması için bkz. [izlenecek yol: C# ile Görselleştirici yazma](../debugger/walkthrough-writing-a-visualizer-in-csharp.md).  
  
### <a name="to-create-the-debugger-side"></a>Hata ayıklayıcı yan oluşturmak için  
  
1.  Kullanım <xref:Microsoft.VisualStudio.DebuggerVisualizers.IVisualizerObjectProvider> görselleştirilen nesne hata ayıklayıcı tarafta almak için yöntemleri.  
  
2.  Devralınan bir sınıf oluşturmanız <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer>.  
  
3.  Geçersiz kılma <xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer.Show%2A?displayProperty=fullName> Arabiriminizin görüntülemek için yöntemi. Kullanım <xref:Microsoft.VisualStudio.DebuggerVisualizers.IDialogVisualizerService> Windows forms iletişim kutuları ve denetimleri, arabiriminin bir parçası görüntülenecek yöntemleri.  
  
4.  Uygulama <xref:System.Diagnostics.DebuggerVisualizerAttribute>, Görselleştirici veren (<xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer>).  
  
### <a name="to-create-the-debuggee-side"></a>Hata ayıklanan yan oluşturmak için  
  
1.  Uygulama <xref:System.Diagnostics.DebuggerVisualizerAttribute>, Görselleştirici veren (<xref:Microsoft.VisualStudio.DebuggerVisualizers.DialogDebuggerVisualizer>) ve bir nesne kaynağı (<xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource>). Varsayılan nesne kaynak nesne kaynağı atarsanız, kullanılacak  
  
2.  Veri nesneleri düzenleyebilmek için Görselleştirici, isterseniz de bunları olarak geçersiz kılmak ihtiyacınız olacak `TransferData` veya `CreateReplacementObject` yöntemlerinden <xref:Microsoft.VisualStudio.DebuggerVisualizers.VisualizerObjectSource>.   
  
## <a name="in-this-section"></a>Bu Bölümde
  
 [İzlenecek Yol: C# ile Görselleştirici Yazma](../debugger/walkthrough-writing-a-visualizer-in-csharp.md)  

 [İzlenecek Yol: Visual Basic'de Görselleştirici Yazma](../debugger/walkthrough-writing-a-visualizer-in-visual-basic.md)  
  
 [Nasıl Yapılır: Görselleştirici Yükleme](../debugger/how-to-install-a-visualizer.md)  
  
 [Nasıl Yapılır: Görselleştiriciyi Test Etme ve Hata Ayıklama](../debugger/how-to-test-and-debug-a-visualizer.md)  
  
 [Görselleştirici API Başvurusu](../debugger/visualizer-api-reference.md)  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [Hata ayıklayıcı görünümü verileri](../debugger/viewing-data-in-the-debugger.md)