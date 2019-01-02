---
title: Genişletme ve aracı Windows özelleştirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- user interfaces, essentials
- tool windows, standard
ms.assetid: 46b2892e-7b2b-4b3f-83a7-b884f1e114ee
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 4c942076f10aa39994c2a809f994b9725831d67b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53949842"
---
# <a name="extend-and-customize-tool-windows"></a>Genişletme ve özelleştirme araç pencereleri
Visual Studio, windows, örneğin araç pencereleri, belge pencereleri ve iletişim windows birkaç farklı türde sağlar. Gibi diğer windows **özellikleri** penceresinde **çıkış** penceresinde ve **görev listesi** penceresinde araç pencereleri türleridir.  
  
## <a name="tool-windows"></a>Araç pencereleri  
 Visual Studio araç pencereleri, dosya tabanlı olmayan salt okunur genellikle dizisidir. Bu konuda, dosyaları okuma-yazma modunda görüntüleme belge windows, farklı. **Araç kutusu**, **Çözüm Gezgini**, **özellikleri** penceresinde ve **Web tarayıcısı** araç pencereleri örnekleridir.  
  
 Basit bir araç penceresi oluşturma konusunda bilgi edinmek için bkz: [araç penceresi ekleme](../extensibility/adding-a-tool-window.md).  
  
 Araç penceresi ile Visual Studio'yu kayıt ettirmek için bkz: [araç penceresi kaydetme](../extensibility/registering-a-tool-window.md).  
  
 Aracı windows Tek Örnekli varsayılan olarak, araç penceresi yalnızca bir örneğini anlamına gelir açık bir anda olabilir. Tek Örnekli araç penceresi açıldıktan sonra IDE kapatılana kadar açık kalır. Tek Örnekli araç penceresini kapattığınızda, yalnızca görünürlüğü değiştirir. Pencerenin birden çok örneği aynı anda açık olacak şekilde çok örnekli araç pencerelerini de oluşturabilirsiniz. Bkz: [çok örnekli araç penceresi oluşturma](../extensibility/creating-a-multi-instance-tool-window.md) daha fazla bilgi için.  
  
 Araç pencereleri olabilir *dinamik*, ilgili kullanıcı Arabirimi bağlamları geçerli olduğunda görünür olmalarını anlamına gelir. IDE'de pencereleri gösterip otomatik görünürlük kullanımını azaltabilirsiniz. Daha fazla bilgi için [dinamik araç penceresini açma](../extensibility/opening-a-dynamic-tool-window.md).  
  
 Araç pencereleri, yerleşik, kayan ve sekmeli belge çerçevede olabilir. Araç pencere çerçevesi IDE tarafından sağlanır ve boyut, konum, yerleştirme durumu ve kalıcı diğer özellikleri denetlemek için kullanılır. Araç penceresi bölmesi içeriğini görüntüler. Varsayılan boyut ve konum yalnızca araç penceresi ilk açıldığında uygulanır. Bundan sonra araç penceresi durumu kalıcı hale getirilir.  
  
 Araç pencere bölmeleri, WPF kullanıcı denetimleri barındırmak ve araç çubukları destekler. Geçersiz kılabilirsiniz <xref:Microsoft.VisualStudio.Shell.WindowPane.Window%2A> özelliği denetimden tanıtıcısını döndürür.  
  
 Araç pencereleri için birçok farklı özelliği ekleyebilirsiniz. Örneğin, bir araç çubuğu ekleyebilirsiniz: [Araç penceresine araç çubuğu eklemek](../extensibility/adding-a-toolbar-to-a-tool-window.md) veya bir kısayol menüsü: [Araç penceresine kısayol menüsü ekleme](../extensibility/adding-a-shortcut-menu-in-a-tool-window.md). Araç penceresi içinde öğeleri aramasına izin veren bir arama denetimi ekleyebilirsiniz: [Araç penceresine arama ekleme](../extensibility/adding-search-to-a-tool-window.md).  
  
 Araç penceresi olaylarına abone olabilirsiniz: [Bir olaya abone](../extensibility/subscribing-to-an-event.md).  
  
## <a name="extend-existing-tool-windows"></a>Mevcut araç pencerelerini genişletme  
 Bilgi, araç penceresi hakkında yeni bir ekleyebileceğiniz **seçenekleri** sayfası ve yeni bir ayar **özellikleri** sayfasında, yazma **görev listesi** ve **çıkış**  windows. Daha fazla bilgi için [özellikleri, görev listesi, çıktı ve Seçenekler pencerelerini genişletme](../extensibility/extending-the-properties-task-list-output-and-options-windows.md) ve [özellikleri, görev listesi, çıktı ve Seçenekler pencerelerini genişletme](../extensibility/extending-the-properties-task-list-output-and-options-windows.md).  
  
## <a name="modal-dialog-boxes"></a>Kalıcı iletişim kutuları  
 Visual Studio Uzantısı'nda bunları türetilerek kalıcı iletişim kutuları oluşturmalısınız <xref:Microsoft.VisualStudio.PlatformUI.DialogWindow?displayProperty=fullName>, bunları ve diğer UI kontrol sağlar. Daha fazla bilgi için [oluşturma ve yönetme kalıcı iletişim kutuları](../extensibility/creating-and-managing-modal-dialog-boxes.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Araç penceresi içeren bir uzantı oluşturma](../extensibility/creating-an-extension-with-a-tool-window.md)