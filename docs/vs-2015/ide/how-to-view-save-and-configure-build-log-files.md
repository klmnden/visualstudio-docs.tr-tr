---
title: 'Nasıl yapılır: Görüntüleme, kaydetme ve derleme günlüğü dosyalarını yapılandırma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
ms.assetid: 75d38b76-26d6-4f43-bbe7-cbacd7cc81e7
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 7bd8bae0213755b11c145c4bef9c312fe3990c4d
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432323"
---
# <a name="how-to-view-save-and-configure-build-log-files"></a>Nasıl yapılır: Derleme Günlüğü Dosyalarını Görüntüleme, Kaydetme ve Yapılandırma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio IDE içinde bir projeyi derledikten sonra bu yapı hakkındaki bilgileri görüntüleyebilirsiniz **çıkış** penceresi. Bu bilgileri kullanarak, örneğin, bir derleme hatası giderme olabilir. C++ projeleri için oluşturulan ve otomatik olarak kaydedilmiş bir .txt dosyasına aynı bilgileri de görüntüleyebilirsiniz. Yönetilen kod projeleri için kopyalayın ve yapıştırın bilgilerinden **çıkış** penceresine bir .txt dosyasına ve dosyayı kaydedin. IDE, hangi tür bilgileri, her yapı hakkındaki görüntülemek istediğinizi belirtmek için de kullanabilirsiniz.  
  
 Proje herhangi bir türden Msbuild'i kullanarak derleme yaparsanız, yapı hakkındaki bilgileri kaydetmek için bir .txt dosyasına oluşturabilirsiniz. Daha fazla bilgi için [derleme günlükleri alma](../msbuild/obtaining-build-logs-with-msbuild.md).  
  
### <a name="to-view-the-build-log-file-for-a-c-project"></a>Bir C++ projesi için derleme günlük dosyasını görüntülemek için  
  
1. İçinde **Windows Explorer** veya **dosya Gezgini**, aşağıdaki dosyayı açın: \\...\Visual Studio *sürüm*\Projects\\  *ProjectName*\\*ProjectName*\Debug\\*ProjectName*.txt  
  
### <a name="to-create-a-build-log-file-for-a-managed-code-project"></a>Yönetilen kod projesi için derleme günlük dosyası oluşturmak için  
  
1. Menü çubuğunda, **derleme**, **Çözümü Derle**.  
  
2. İçinde **çıkış** penceresinde derleme bilgileri vurgulayın ve ardından panoya kopyalayın.  
  
3. Not Defteri gibi bir metin düzenleyicisinde açın, bilgileri dosyasına yapıştırın ve kaydedin.  
  
### <a name="to-change-the-amount-of-information-included-in-the-build-log"></a>Yapı günlüğünde dahil bilgi miktarını değiştirmek için  
  
1. Menü çubuğunda, **Araçları**, **seçenekleri**.  
  
2. Üzerinde **projeler ve çözümler** sayfasında **derleme ve çalıştırma** sayfası.  
  
3. İçinde **MSBuild proje oluşturması çıkış ayrıntısı** listesinde, aşağıdaki değerlerden birini seçin ve ardından **Tamam** düğmesi.  
  
    |Ayrıntı düzeyi|Açıklama|  
    |---------------------|-----------------|  
    |Quiet|Yalnızca yapı özetini görüntüler.|  
    |En az|Derleme ve hatalarını, uyarılarını ve ayrılır iletileri bir özeti, son derece önemli olarak görüntüler.|  
    |Normal|Yapı özetini görüntüler. hataları, uyarıları ve son derece önemli olarak sınıflandırılmış iletileri; ve yapı ana adımlar. Bu ayrıntı düzeyini en sık kullanacaksınız.|  
    |Ayrıntılı|Yapı özetini görüntüler. hataları, uyarıları ve son derece önemli olarak sınıflandırılmış iletileri; Tüm; derleme adımları ve itibaren normal önem kategorilere iletileri.|  
    |Tanılama|Derleme için kullanılabilir olan tüm verileri görüntüler. Özel derleme betikleri ile ve diğer yapı sorunlarını hata ayıklama yardımcı olmak için bu düzeyde ayrıntı kullanabilirsiniz.|  
  
     Daha fazla bilgi için [Seçenekler iletişim kutusu, projeler ve çözümler, derleme ve çalıştırma](../ide/reference/options-dialog-box-projects-and-solutions-build-and-run.md) ve <xref:Microsoft.Build.Framework.LoggerVerbosity>.  
  
    > [!IMPORTANT]
    > Proje etkili olması yaptığınız değişiklikleri için yeniden oluşturmanız gerekir **çıkış** penceresi (tüm projeler) ve *ProjectName*.txt dosyasına (yalnızca C++ projeleri için).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Derleme günlükleri alma](../msbuild/obtaining-build-logs-with-msbuild.md)   
 [Projeleri ve Visual Studio çözümleri oluşturma ve temizleme](../ide/building-and-cleaning-projects-and-solutions-in-visual-studio.md)   
 [Derleme ve Oluşturma](../ide/compiling-and-building-in-visual-studio.md)
