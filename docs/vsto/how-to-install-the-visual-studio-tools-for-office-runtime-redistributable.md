---
title: "Nasıl yapılır: Office çalışma zamanı yeniden dağıtılabilir için Visual Studio Araçları 'i yükler"
titleSuffix: ''
ms.custom: seodec18
ms.date: 08/14/2019
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office runtime [Office development in Visual Studio]
- installing Office development tools in Visual Studio
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5d9bb53fbdc3d6766dab47c654f0a43ad902b2f3
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551829"
---
# <a name="how-to-install-the-visual-studio-tools-for-office-runtime-redistributable"></a>Nasıl yapılır: Office çalışma zamanı yeniden dağıtılabilir için Visual Studio Araçları 'i yükler
  Office çalışma zamanı için Visual Studio 2010 araçları, ' de [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]Microsoft Office geliştirici araçları kullanılarak oluşturulan çözümler çalıştıran her bilgisayara yüklenmelidir. Çalışma zamanı, yüklediğinizde [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]ve Microsoft Office otomatik olarak yüklenir. Daha fazla bilgi için bkz. [Office çalışma zamanı yükleme senaryoları için Visual Studio Araçları](../vsto/visual-studio-tools-for-office-runtime-installation-scenarios.md).

[!include[Add-ins note](includes/addinsnote.md)]

 Aşağıdaki durumlarda el ile yükleme yönergelerini izlemeniz gerekebilir:

- [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] ' Nı bir sunucusuna yüklemeniz gerekir. Örneğin, bir sunucudaki belge düzeyi çözümlerini yönetmek <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> için sınıfını kullanmak istiyorsunuz.

- Çalışma zamanını, Office çözümlerinin tüm diğer önkoşullarının zaten yüklü olduğu bir bilgisayara yüklemeniz gerekir.

    > [!NOTE]
    > .NET Framework ve ' [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]ü yüklemek için geliştirme bilgisayarında bir yönetici olmanız gerekir.

## <a name="to-install-the-visual-studio-tools-for-office-runtime"></a>Office çalışma zamanı Visual Studio Araçları yüklemek için

1. [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Veya sonraki sürümünü yükler.

    - İndirmek [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)]için, bkz. [Microsoft .NET Framework 4 (Web Yükleyicisi)](http://go.microsoft.com/fwlink/?LinkId=178957).

    - İndirmek [!INCLUDE[net_client_v40_long](../vsto/includes/net-client-v40-long-md.md)]için, bkz. [Microsoft .NET Framework 4 istemci profili (Web Yükleyicisi)](http://go.microsoft.com/fwlink/?LinkId=178958).

    - İndirmek [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]için, bkz. [Microsoft .NET Framework 4,5](http://www.microsoft.com/download/details.aspx?id=30653).

2. Yüklemek[!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]için *vstor_redist. exe dosyasını* çalıştırın.

     Bu kurulum dosyalarını, [Office çalışma zamanı Için Visual Studio 2010 araçlarından](http://go.microsoft.com/fwlink/?LinkId=140384)indirebilirsiniz. İçin önkoşulları, .NET Framework [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] önkoşulları ile eşleşir.

     , [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] Dil paketlerini içerir. Windows yüklemeniz Ingilizce dışında bir dile ayarlandıysa, çalışma zamanı iletilerini Windows için kullandığınız dilde görüntüleyebilirsiniz. Benzer şekilde, son kullanıcılar ürününü yüklerse [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] ve sonra, İngilizce dışındaki bir dile ayarlanmış Windows yüklemelerinde çözümlerinizi çalıştırırsanız, çalışma zamanı iletileri Windows ile aynı dilde görünür. Bazı durumlarda, ek dil paketlerine ihtiyacınız bulunabilir. Örneğin, Windows kopyanız birden fazla dil ayarı kullanıyorsa veya daha önce [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)]yükledikten sonra başka bir dile geçiş yaparsanız, ek dil paketlerine ihtiyaç duyabilirsiniz. Dil paketlerini [Microsoft Office sistemi (sürüm 4,0 çalışma zamanı) dil paketi için Microsoft Visual Studio 2010 araçlarında](http://go.microsoft.com/fwlink/?LinkId=140386)bulabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio &#40;'da Office geliştirme ile çalışmaya başlama&#41;](../vsto/getting-started-office-development-in-visual-studio.md)
- [Office çözümleri geliştirmek için bir bilgisayarı yapılandırma](../vsto/configuring-a-computer-to-develop-office-solutions.md)
- [Nasıl yapılır: Office çözümleri geliştirmek için bir bilgisayarı yapılandırma](../vsto/how-to-configure-a-computer-to-develop-office-solutions.md)
- [Nasıl yapılır: Office birincil birlikte çalışma derlemelerini yükler](../vsto/how-to-install-office-primary-interop-assemblies.md)
- [ServerDocument sınıfını kullanarak bir sunucudaki belgeleri yönetme](../vsto/managing-documents-on-a-server-by-using-the-serverdocument-class.md)
- [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)
