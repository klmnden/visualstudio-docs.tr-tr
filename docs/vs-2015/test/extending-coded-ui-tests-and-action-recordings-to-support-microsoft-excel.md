---
title: Genişletme kodlanmış UI testlerini ve Eylem kayıtlarını Microsoft Excel'i desteklemek için | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-test
ms.topic: conceptual
ms.assetid: 6b0f72a4-70ca-4e55-b236-2ea1034fd8a7
caps.latest.revision: 32
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 4852dc5b65f00f7d298f5f1a15d39ff041022578
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54791998"
---
# <a name="extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel"></a>Kodlanmış Kullanıcı Arabirimi Testlerini ve Eylem Kayıtlarını Microsoft Excel'i Desteklemek için Genişletme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kodlanmış UI testleri ve eylem kayıtları için test çerçevesi, her olası kullanıcı arabirimi desteklemiyor. Test etmek istediğiniz belirli bir kullanıcı Arabirimi desteklemiyor olabilir. Örneğin, hemen ya da kodlanmış UI testi için bir eylem kaydı oluşturamazsınız bir [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)] elektronik tablo. Ancak, belirli kullanıcı Arabirimi, kodlanmış UI testi framework'ün genişletilebilirlik avantajlarından yararlanarak destekleyecek kodlanmış kullanıcı Arabirimi testi çerçevesini kendi uzantınızı oluşturun. Kodlanmış UI testleri ve eylem kayıtları için oluşturulmasını desteklemek için çerçevesinin nasıl genişletileceğine örneği aşağıdaki konuda verir [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)]. Desteklenen platformlar hakkında daha fazla bilgi için bkz. [kodlanmış UI testleri ve eylem kayıtları için desteklenen yapılandırmalar ve platformlar](../test/supported-configurations-and-platforms-for-coded-ui-tests-and-action-recordings.md).  
  
 **Gereksinimler**  
  
- Visual Studio Enterprise  
  
  Bu bölümde, kaydedebilir ve Excel çalışma sayfalarında testleri kayıttan yürütme kodlanmış bir UI testi uzantısı gösterir. Her bir parçasının uzantısı yalnızca böyle bir uzantı oluşturmak isteyen geliştiriciler için bu bölümdeki ve kod yorumlarında açıklanmıştır.  
  
  ![UI Test mimarisi](../test/media/ui-testarch.png "UI_TestArch")  
  Mimariye Genel Bakış  
  
## <a name="download-the-sample"></a>Örneği indirme  
 Dört projelerinde örnek oluşan `CodedUIExtensibilitySample.sln` çözümü:  
  
- CodedUIExtensibilitySample  
  
- ExcelCodedUIAddinHelper  
  
- ExcelUICommunicationHelper  
  
- SampleTestProject  
  
  Bu örnek edinin [blog gönderisi](http://go.microsoft.com/fwlink/?LinkID=185592).  
  
> [!NOTE]
>  Örnek Microsoft Excel 2010 ile kullanıma yöneliktir. Örnek Microsoft Excel diğer sürümleri de çalışabilir fakat şu anda desteklenmiyor.  
  
## <a name="details-about-the-sample"></a>Örnek hakkındaki ayrıntıları  
 Aşağıdaki bölümlerde, örnek ve yapısı hakkında bilgi sağlar.  
  
### <a name="microsoft-excel-add-in-excelcodeduiaddinhelper"></a>Microsoft Excel Eklentisi: ExcelCodedUIAddinHelper  
 Bu proje, Excel işlemde çalışan bir eklenti içerir. Bkz: [kodlanmış UI testi için örnek Excel eklentisi](../test/sample-excel-add-in-for-coded-ui-testing.md) Eklenti projesinin kısa bir genel bakış.  
  
 Daha fazla bilgi için [izlenecek yol: Excel için ilk VSTO eklentinizi oluşturma](http://msdn.microsoft.com/library/a855e2be-3ecf-4112-a7f5-ec0f7fad3b5f).  
  
### <a name="excel-ui-communication-exceluicommunicationhelper"></a>Excel kullanıcı Arabirimi iletişim: ExcelUIcommunicationHelper  
 Bu proje içerir `IExcelUICommunication` arabirimi ve kodlanmış UI test çerçevesi ve Excel arasında veri iletmek için kullanılan bilgileri içerir. Daha fazla bilgi için [Excel Communicator arabirimi örnekleme](../test/sample-excel-communicator-interface.md).  
  
### <a name="coded-ui-test-extension-codeduiexentsibilitysample"></a>Kodlanmış UI testi uzantısı: CodedUIExentsibilitySample  
 Bu proje bir Excel çalışma sayfasına testlerinde kullanılan özel sınıflar içerir. Bu sınıfların her birini okunarak kodudur. Ancak, her özel bir sınıf kısa bir açıklamasını sağlar. Daha fazla bilgi için [örnek kodlanmış UI testi uzantısı için Excel](../test/sample-coded-ui-test-extension-for-excel.md).  
  
### <a name="deploying-your-add-in-and-extension"></a>Eklenti ve uzantısını dağıtma  
 Tüm projeler ve nesneleri oluşturduktan sonra sağlanan çalıştırma `CopyDrop.bat` dosyasını yönetici olarak. Bu dosyayı kopyalar `ExcelCodedUIAddinHelper` DLL ve PDB dosyaları:  
  
 "`%CommonProgramFiles(x86)%\Microsoft Shared\VSTT\<version number>\UITestExtensionPackages\*.*`", sürüm numarası, 11.0 olabilir. Burada, Visual Studio sürümü 12.0 vb. temel.  
  
 `ExcelUICommunicationHelper` DLL ve PDB dosyaları kopyalanır `"%ProgramFiles(x86)%\Microsoft Visual Studio <version number>\Common7\IDE\PrivateAssemblies”`.  
  
 Tam kopya yollarını ayarlamanız gerekebilir, ancak hiçbir ek yükleme gereklidir. Bir 64-bit makinede 32-bit Visual Studio Enterprise komut isteminde çalıştırmak için kullanın. `CopyDrop.bat` dosya.  
  
### <a name="testing-excel-with-the-sampletestproject"></a>SampleTestProject ile test etme  
 Sağlanan test projesinde Excel değil, ya da kendi test projesi oluşturun ve olabilirsiniz kendi testi, belirli bir sürümünü kullanan bir test çalıştırabilirsiniz. Daha fazla bilgi için [kodlanmış UI testleri](../test/use-ui-automation-to-test-your-code.md#VerifyingCodeUsingCUITCreate).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>   
 <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITechnologyElement>   
 <xref:Microsoft.VisualStudio.TestTools.UITest.Common.UITestActionFilter>   
 <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.UITestExtensionPackage>   
 [Kodunuzu test etmek için UI otomasyonunu kullanma](../test/use-ui-automation-to-test-your-code.md)   
 [Kodlanmış UI testleri için en iyi uygulamalar](../test/best-practices-for-coded-ui-tests.md)   
 [Kodlanmış UI Testleri ve Eylem Kayıtları için Desteklenen Yapılandırmalar ve Platformlar](../test/supported-configurations-and-platforms-for-coded-ui-tests-and-action-recordings.md)
