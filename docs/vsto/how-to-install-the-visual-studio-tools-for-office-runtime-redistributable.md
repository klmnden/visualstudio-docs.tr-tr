---
title: 'Nasıl Yapılır: Office çalışma zamanı yeniden dağıtılabilir için Visual Studio Araçları yükleme'
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office runtime [Office development in Visual Studio]
- installing Office development tools in Visual Studio
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: f9267e340d62def2660f807670dc9804dd531c8f
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53988773"
---
# <a name="how-to-install-the-visual-studio-tools-for-office-runtime-redistributable"></a>Nasıl Yapılır: Office çalışma zamanı yeniden dağıtılabilir için Visual Studio Araçları yükleme
  Office çalışma zamanı için Visual Studio 2010 Araçları, Microsoft Office geliştirici araçları kullanarak oluşturulan çözümleri çalıştıran her bilgisayara yüklenmelidir [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. Yükleme sırasında çalışma zamanı otomatik olarak yüklenen [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]ve Microsoft Office. Daha fazla bilgi için [Office çalışma zamanı yükleme senaryoları için Visual Studio Araçları](../vsto/visual-studio-tools-for-office-runtime-installation-scenarios.md).  
  
 Aşağıdaki durumlarda aşağıdaki el ile yükleme yönergeleri takip etmeniz gerekebilir:  
  
-   Yüklemeniz gereken [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] bir sunucuda. Örneğin, kullanmak istediğiniz <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> bir sunucuda belge düzeyi çözümlerde yönetmek için sınıf.  
  
-   Çalışma zamanı yüklü Office çözümleri için diğer tüm Önkoşullar zaten olan bir bilgisayara yüklemeniz gerekir.  
  
    > [!NOTE]  
    >  .NET Framework'ü yüklemek için yönetici geliştirme bilgisayarında olmalıdır ve [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)].  
  
## <a name="to-install-the-visual-studio-tools-for-office-runtime"></a>Office çalışma zamanı için Visual Studio Araçları'nı yüklemek için  
  
1.  Yükleme [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya üzeri.  
  
    -   İndirmek için [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)], bkz: [Microsoft .NET Framework 4 (Web Yükleyicisi)](http://go.microsoft.com/fwlink/?LinkId=178957).  
  
    -   İndirmek için [!INCLUDE[net_client_v40_long](../vsto/includes/net-client-v40-long-md.md)], bkz: [Microsoft .NET Framework 4 istemci profili (Web Yükleyicisi)](http://go.microsoft.com/fwlink/?LinkId=178958).  
  
    -   İndirmek için [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)], bkz: [Microsoft .NET Framework 4.5](http://www.microsoft.com/download/details.aspx?id=30653).  
  
2.  Çalıştırma *vstor_redist.exe* yüklemek için [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)].  
  
     Bu kurulum dosyalarından indirebileceğiniz [Office çalışma zamanı için Visual Studio 2010 Araçları](http://go.microsoft.com/fwlink/?LinkId=140384). Önkoşulları [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] .NET Framework için önkoşulları eşleşmesi.  
  
     [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]Dil paketlerini içerir. Windows yüklemesini İngilizce dışında bir dile ayarlanırsa, Windows için kullandığınız aynı dilde çalışma zamanı iletilerini görüntüleyebilirsiniz. Benzer şekilde, son kullanıcılar [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] ve çözümlerinizi aynı dilde Windows çalışma zamanı mesajlarını görünür ayarlanan İngilizce dışında bir dil için Windows yüklemeleri üzerinde çalıştırın. Bazı durumlarda, ek dil paketlerini gerekebilir. Örneğin, birden fazla dil ayarı Windows kopyanızı kullanıyorsa ya da devre dışı zaten yükledikten sonra başka bir dile geçiş yapmak ek dil paketlerini gerekebilir [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]. Dil paketlerinin bulabilirsiniz [Microsoft Visual Studio 2010 Araçları için Microsoft Office sistemi (sürüm 4.0 çalışma zamanı) dil paketi](http://go.microsoft.com/fwlink/?LinkId=140386).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Başlama &#40;Visual Studio'da Office geliştirme&#41;](../vsto/getting-started-office-development-in-visual-studio.md)   
 [Office çözümleri geliştirmek için bilgisayarı yapılandırma](../vsto/configuring-a-computer-to-develop-office-solutions.md)   
 [Nasıl yapılır: Office çözümleri geliştirmek için bilgisayarı yapılandırma](../vsto/how-to-configure-a-computer-to-develop-office-solutions.md)   
 [Nasıl yapılır: Office birincil birlikte çalışma derlemelerini yükleme](../vsto/how-to-install-office-primary-interop-assemblies.md)   
 [ServerDocument sınıfını kullanarak bir sunucu üzerinde belgeleri yönetme](../vsto/managing-documents-on-a-server-by-using-the-serverdocument-class.md)   
 [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)  
