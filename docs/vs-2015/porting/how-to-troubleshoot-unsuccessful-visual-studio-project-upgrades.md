---
title: 'Nasıl yapılır: Başarısız bir proje yükseltmelerinde sorun giderme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: troubleshooting
f1_keywords:
- VisualStudio.SourceControl.CannotOpenFromSourceControlDSW
- vs.UpgradeProjectSolution.8.0
helpviewer_keywords:
- upgrading applications, Visual Studio
- upgrading projects [Visual Studio]
- projects [Visual Studio], upgrading
- Visual Studio Conversion Wizard
- Conversion wizard
ms.assetid: 842fe448-c044-4343-8eae-d81711cf48ba
caps.latest.revision: 31
author: kraigb
ms.author: kraigb
manager: jillfra
ms.openlocfilehash: 194dae93e3a013da366d454582b531a2cc4ff8b6
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60096341"
---
# <a name="how-to-troubleshoot-unsuccessful-visual-studio-project-upgrades"></a>Nasıl yapılır: Başarısız Visual Studio Proje yükseltmelerinde sorun giderme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bazı durumlarda Visual Studio tam olarak bir proje önceki bir sürümünü dönüştürülemiyor [!INCLUDE[vsprvs](../includes/vsprvs-md.md)]. Aşağıdaki bölümlerde ipuçları belirli sorununuzu çözmezse, daha ayrıntılı bilgi TechNet'te olanağınız olabilir [Wiki: Geliştirme portalı](http://go.microsoft.com/fwlink/?LinkId=254808).

## <a name="the-project-does-not-run-because-files-are-not-found"></a>Proje dosyaları bulunamadı çünkü çalışmaz
 Sabit kodlu dosya yollarının bir proje dosyasını içeren, [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] F5 tuşuna bastığınızda, projeyi çalıştırmak için kullanır. Bu yolları konumunu devenv.exe ve diğer gerekli dosyaları içerebilir. Yükseltilmiş sürümünü de [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], bu dosyaların yollarını değişmiş olabilir.

#### <a name="to-resolve-incorrect-file-paths"></a>Hatalı dosya yollarını çözmek için

1. Proje dosyanız, bir metin düzenleyicisinde açın.

2. Hatalı dosya yolları için özellikle içeren tarama bir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] sürüm numarası.

3. Hatalı dosya yolları yeni hedefe işaret edecek şekilde değiştirin.

## <a name="the-project-does-not-build-because-references-are-not-valid"></a>Proje başvuruları geçerli olmadığından oluşturmuyor
 Yükseltme yaptığınızda [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], ayrıca yükseltme [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] sürümü. Projenize yeni üretilmeyen başvurular içeriyorsa [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] sürümü, bunlar değil çözebilir doğru. Örneğin, sürüm numaralarını içeren başvuruları için özellikle büyük olasılıkla budur `Microsoft.VisualStudio.Shell.Interop.8.0`.

 Kodunuzu birçok geçersiz başvurular varsa, multi-targeting'e özelliğini kullanmak için kolay bir çözüm olabilir [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] önceki bir sürümünü hedefleyecek şekilde [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)].

#### <a name="to-resolve-incorrect-references"></a>Yanlış başvurularını çözümlemek için

1. Proje dosyanız, bir metin düzenleyicisinde açın.

2. Proje özelliklerini açın.

3. Doğru seçin **hedef Framework'ü** değeri. Alternatif olarak, değerini değiştirebilirsiniz `<TargetFrameworkVersion>` doğrudan proje dosyasında öğesi.

   Yükseltilen çalıştırmak üzere projenizi isteyip istemediğinizi [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] sürümü, proje başvurularını güncelleştirme ve ayrıca güncelleştirin `Imports` veya `Using` çağrısı deyimleri. Projenizi IDE'de yüklerse kullanarak başvurular güncelleştirebilirsiniz **Çözüm Gezgini** veya **başvuru Yöneticisi** iletişim kutusu.

## <a name="see-also"></a>Ayrıca Bkz.
 [/ Yükseltme (devenv.exe)](../ide/reference/upgrade-devenv-exe.md) [ASP.NET 4 için dönüştürme](http://msdn.microsoft.com/library/790147c6-36c1-41b5-a52d-30b9ccd2bd10)
