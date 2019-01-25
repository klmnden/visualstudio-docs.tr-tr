---
title: SharePoint çözüm paketleri oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packages
- packages [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 059bf8068ad3a14d01f0a8167900563eebdff215
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867994"
---
# <a name="create-sharepoint-solution-packages"></a>SharePoint çözüm paketleri oluşturma
  Paket Tasarımcısı'nı kullanarak oluşturun ve dağıtım paketleri özelleştirin. Örneğin, SharePoint Proje öğeleri ve özellikleri, IIS sunucusu sıfırlandığında, özellik etkinleştirme kapsamı ayarla ve özellik bağımlılıkları tanımlayın ekleyebilirsiniz. Tasarımcı, ayrıca her paket açıklayan bir XML dosyasını bir bildirim oluşturur.  
  
## <a name="packaging-tools"></a>Paketleme araçları
 Kullanabileceğiniz **paket Tasarımcısı** paketleme ve bildirimi oluşturun. SharePoint Proje öğeleri eklemek, Web sunucusu sıfırlama ve dağıtım sunucusu türü olup olmadığını yapılandırın. Daha fazla bilgi için [nasıl yapılır: Ekleme ve paket Tasarımcısını kullanarak, özellikler ve öğeler pakete kaldırma](../sharepoint/how-to-add-and-remove-features-and-items-to-a-package-by-using-the-package-designer.md).  
  
 Alternatif olarak, **paketleme Gezgini** paket dosyanızdaki öğeleri ve özellikleri değiştirmek için (*.wsp*). Daha fazla bilgi için [nasıl yapılır: Ekleme ve paketleme Gezgini'ni kullanarak, özellikler ve öğeler pakete kaldırma](../sharepoint/how-to-add-and-remove-features-and-items-to-a-package-by-using-the-packaging-explorer.md).  
  
 Paket oluşturmak için Visual Studio ve MSBuild kullanabilirsiniz (*.wsp*) SharePoint çözümünüzü dağıtmak için dosyalar. Bu işlem SharePoint dağıtım için gerekli dosyaları oluşturur. Daha fazla bilgi için [nasıl yapılır: MSBuild görevleri kullanarak bir SharePoint çözüm paketini oluşturma](../sharepoint/how-to-create-a-sharepoint-solution-package-by-using-msbuild-tasks.md).  
  
## <a name="package-designer-options"></a>Paket Tasarımcısı seçenekleri
 Aşağıdaki tablo ile SharePoint paketlerdeki özelleştirebilirsiniz özelliklerini gösterir. **paket Tasarımcısı**.  
  
|Paket Tasarımcısı özelliği|Varsayılan ayar açıklaması|  
|-------------------------------|------------------------------------|  
|Ad|Gerekli. Paketin varsayılan adı kümesine *ProjectName*.|  
|Web sunucusunu sıfırlama|İsteğe bağlı. Web sunucusu sonra yeniden başlatmak istiyorsanız belirleyin *.wsp* dosyanın SharePoint sunucusunda yüklü.|  
|Dağıtım sunucusu türü|Gerekli. Varsayılan olarak, kapsamı ApplicationServer için ayarlanır.<br /><br /> ApplicationServer: Hizmetleri barındıran bir sunucu açıklar.<br /><br /> WebFrontEnd: Web sitelerini barındıran bir sunucu açıklar.|  
|Çözümdeki öğeler|Tüm SharePoint Proje öğeleri ve pakete eklenen özellikler.|  
|Paket öğeleri|İsteğe bağlı. Tüm SharePoint öğeleri ve paketinizdeki dağıtmak istediğiniz özellikler.|  
  
## <a name="configure-the-packaging-process"></a>Paketleme işlemi yapılandırma
 Visual Studio'da SharePoint çözümleri geliştirme sonra nasıl projeleri paketlenmiş özelleştirebilirsiniz.  
  
 Aşağıdaki tablo, özelleştirmek için kullanabileceğiniz iki MSBuild hedefleri gösterir nasıl *.wsp* dosyası oluşturulur.  
  
|Hedef|Açıklama|  
|------------|-----------------|  
|BeforeLayout|Dosyalar için bir ara dizin hemen kopyalanır önce görevleri gerçekleştiren hedefi. Bir paket dosyası oluşturmadan önce dosyaları değiştirebilirsiniz (*.wsp*).|  
|AfterLayout|Dosyalar için bir ara dizin hemen kopyalandıktan sonra görevleri gerçekleştiren hedefi.|  
  
 Daha fazla bilgi için [nasıl yapılır: MSBuild hedeflerini kullanarak SharePoint çözüm paketini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-solution-package-by-using-msbuild-targets.md).  
  
## <a name="packaging-architecture"></a>Paketleme mimarisi
 Bir SharePoint paketi oluşturduğunuzda, aşağıdaki adımlar oluşur (*.wsp*) Visual Studio'da.  
  
1.  Paketler ve özellikleri, paket fiziksel ve anlamsal yapısının doğru olduğundan emin olmak için doğrulanır.  
  
2.  Özellikler, proje öğeleri ve paket dosyaları paketteki numaralandırılır. Paketler ve özellikler için bildirim dosyalarını, dağıtım ve etkinleştirme için gerekli tüm bilgileri içerecek şekilde dönüştürülür. Belirteçleri tam değeriyle değiştirilir.  
  
3.  Özelleştirilebilir BeforeLayout MSBuild hedefi gerçekleştirilir. Paketten önce herhangi bir özel değişiklik yapmak için bu adımı oluşturabilirsiniz *.wsp* dosyası oluşturulur.  
  
4.  Numaralandırılmış dosyaları ara bir dizine kopyalanır.  
  
5.  Özelleştirilebilir AfterLayout MSBuild hedefi gerçekleştirilir. Paketten önce herhangi bir özel değişiklik yapmak için bu adımı oluşturabilirsiniz *.wsp* dosyası oluşturulur.  
  
6.  Ara dizindeki dosyaları eklenir *.wsp* dosya.  
  
## <a name="package-folder-structure"></a>Paket klasör yapısı
 SharePoint projenizi paketi sıralanırken bir *.wsp* dosyası içinde sizin için oluşturulur *SolutionFolder\bin\\\<BuildConfiguration >* klasör. Örneğin, çözümünüz içinde ise *C:\Visual Studio 2013\Projects\ListDefinition1* ve yapı yapılandırmanızı sürüm için ayarlanmış *.wsp* dosyası *C:\Visual Studio 2013\ Projects\ListDefinition1\bin\Release*.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Bir SharePoint çözüm paketini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-solution-package.md)  
 [Nasıl yapılır: Ekleme ve özellikler ve öğeler bir paketi paket Tasarımcısını kullanarak kaldırma](../sharepoint/how-to-add-and-remove-features-and-items-to-a-package-by-using-the-package-designer.md)   
 [Nasıl yapılır: MSBuild görevleri kullanarak bir SharePoint çözüm paketini oluşturma](../sharepoint/how-to-create-a-sharepoint-solution-package-by-using-msbuild-tasks.md)   
 [Nasıl yapılır: MSBuild görevleri kullanarak bir SharePoint çözüm paketini oluşturma](../sharepoint/how-to-create-a-sharepoint-solution-package-by-using-msbuild-tasks.md)   
 [Nasıl yapılır: MSBuild hedeflerini kullanarak SharePoint çözüm paketini özelleştirme](../sharepoint/how-to-customize-a-sharepoint-solution-package-by-using-msbuild-targets.md)  
