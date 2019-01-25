---
title: Komut yönlendirme algoritması | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- commands, routing
- command routing
ms.assetid: 998b616b-bd08-45cb-845f-808efb8c33bc
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 3cfd90bf3cefd941c28e20eccdafb44d4a4d1b36
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54769884"
---
# <a name="command-routing-algorithm"></a>Komut Yönlendirme Algoritması
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Visual Studio'da komutlar çeşitli farklı bileşenler tarafından işlenir. Komutlar, en dıştaki (genel olarak da bilinir) bağlamına geçerli seçime göre en içteki bağlamından yönlendirilir. Daha fazla bilgi için [kullanılabilirlik](../../extensibility/internals/command-availability.md).  
  
## <a name="order-of-command-resolution"></a>Komut çözüm sırası  
 Komutları komut içeriğini aşağıdaki düzeylerde geçirilir:  
  
1.  Eklentiler: Ortamı, tüm mevcut eklenti komutu ilk sunar.  
  
2.  Öncelik komutlar: Bu komutlar kullanılarak kaydedilen <xref:Microsoft.VisualStudio.Shell.Interop.IVsRegisterPriorityCommandTarget>. Bunlar, Visual Studio'da her komut için çağrılır ve kayıtlı olan sırayla çağrılır.  
  
3.  Bağlam menüsü komutları: Bağlam menüsünde bulunan bir komut, tipik yönlendirme için bağlam menüsünü ve sonra sağlanan komut hedefi için ilk olarak sunulur.  
  
4.  Araç çubuğu komut hedefleri ayarlayın: Bu komut hedefleri çağırdığınızda kayıtlı <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIShell4.SetupToolbar2%2A>. `pCmdTarget` Parametresi `null`. Değilse `null`, bu komut hedefi ayarladığınız araç çubuğunda bulunan herhangi bir komut güncelleştirmek için kullanılır. Shell araç ayarlıyor sonra pencere çerçevesi olarak geçirir `pCmdTarget` böylece komutları araç akışınız pencere çerçevesi aracılığıyla yapılan tüm güncelleştirmeler bile olmadığı odakta.  
  
5.  Araç penceresi: Aracı genellikle uygulayan windows <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane> arabirimi, aynı zamanda uygulamalıdır <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> araç penceresi etkin pencere olduğunda, Visual Studio komut hedefi alabilmesi arabirim. Ancak, araç penceresi, odak ise **proje** penceresini, sonra komutu yönlendirileceğini <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> seçilen öğelerin ortak üst arabirimi. Bu seçim birden çok projeleri yayılmış durumdaysa komutu yönlendirilir <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolution> hiyerarşisi. <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> Arabirimi içeren <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.ExecCommand%2A> ilgili komutları için benzer yöntemler <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> arabirimi.  
  
6.  Belge penceresi: Komutu, .vsct dosyası içinde ayarlanmış RouteToDocs bayrağı varsa, Visual Studio bir komut hedefi üzerinde ya da belge view nesnesinin bir örneğini arar bir <xref:Microsoft.VisualStudio.Shell.Interop.IVsWindowPane> arabirimi ya da bir belge nesnesi örneğini (genellikle bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextLines> arabirimi veya bir <xref:Microsoft.VisualStudio.TextManager.Interop.IVsTextBuffer> arabirimi). Belge view nesnesinin komutu desteklemiyorsa, Visual Studio komutu yönlendiren <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> döndürülen arabirimi. (İsteğe bağlı bir arabirim belge veri nesneleri için budur.)  
  
7.  Geçerli hiyerarşi: Etkin belge penceresini veya Seçili hiyerarşiyi sahip projenin geçerli hiyerarşi olabilir **Çözüm Gezgini**. Visual Studio arar <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> geçerli ya da etkin hiyerarşisini uygulanan arabirimi. Hiyerarşi, proje öğesinin bir belge penceresi odağa sahip olsa bile hiyerarşi etkin olduğunda, geçerli olan komutlar desteklemelidir. Ancak, yalnızca geçerli komutları **Çözüm Gezgini** sahip odak kullanarak desteklenmelidir <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy> arabirimi ve kendi <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand%2A> ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.ExecCommand%2A>yöntemleri.  
  
     **Kes**, **kopyalama**, **Yapıştır**, **Sil**, **Yeniden Adlandır**, **girin**ve **DoubleClick** komutları özel işleme gerektirir. Nasıl yönetileceği hakkında bilgi için **Sil** ve **Kaldır** hiyerarşileri komutlarında bkz <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchyDeleteHandler> arabirimi.  
  
8.  Genel: Bir komut tarafından daha önce bahsedilen bağlamları işlenen değil, uygulayan bir komut sahibi VSPackage yönlendirmek Visual Studio denemesi <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget> arabirimi. VSPackage'ı zaten yüklü değil, Visual Studio çağırdığında yüklenmez <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A> yöntemi. VSPackage'ı yalnızca yüklenen <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec%2A> yöntemi çağrılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Komut Tasarımı](../../extensibility/internals/command-design.md)
