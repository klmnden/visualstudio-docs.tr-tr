---
title: Yayımlama Sihirbazı (Visual Studio'da Office Geliştirme)
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.ProjectProperties.PublishWizard
- VST.PublishWizard.Publish.2007System
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ClickOnce deployment [Office development in Visual Studio], Publish Wizard
- deploying applications [Office development in Visual Studio], Publish Wizard
- Office applications [Office development in Visual Studio], Publish Wizard
- Publish Wizard, Office solutions
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 7879ad7cf18c3d09fddbab3923296e0896688af9
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63447061"
---
# <a name="publish-wizard-office-development-in-visual-studio"></a>Yayımlama Sihirbazı (Visual Studio'da Office Geliştirme)
  Kullanım **Yayımlama Sihirbazı** çözüm dosyaları belirtilen bir konuma kopyalamak için bildirim dosyalarını oluşturmak ve bir Kurulum programı oluşturma.

 Bu Sihirbazı'na erişmek için **derleme** menüsünde seçin **Yayımla** *SolutionName*. Ayrıca erişebileceğiniz **Yayımlama Sihirbazı** gelen **Çözüm Gezgini**. Proje düğümü için kısayol menüsünü açın ve ardından **Yayımla**.

 Aşağıdaki bölümde her bir sayfasında açıklar.

## <a name="where-do-you-want-to-publish-the-application"></a>Burada uygulamayı yayımlamak istiyor musunuz?
 **Bu uygulamayı yayımlamak için konumu belirtin** gerekli. Yayımlama konumunun dizinidir burada **Yayımlama Sihirbazı** derlemeden bildirimleri, derlemeleri, geçici sertifika ve diğer dosyalar gibi çözüm dosyalarını kopyalar. Bu dizine yazma erişimi olmalıdır.

 Bir disk yolu, dosya paylaşımı, FTP sitesi veya web sitesi URL'si bir konum yazın ya da tıklayın **Gözat** konumu için Gözat düğmesini. Yol, aşağıdaki biçimlerde olabilir:

- Göreli veya mutlak bir yol standart Windows, aşağıdakiler gibi biçimlendirme *C:\Deploy\MyApplication* veya *\MyApplication*.

- Bir Evrensel Adlandırma Kuralı (UNC) yolu gibi  *\\\ServerName\MyApplication\\* .

- Gibi bir URL bir web sitesi http://www.microsoft.com/MyApplication.

  Varsayılan olarak, yayımlama konumdur *http://localhost/projectname/* IIS yüklü veya bunu yaparsanız yayınla\ dizini IIS yüklü.

> [!NOTE]
> Hedef bilgisayarın Windows Vista çalıştırıyorsa, daha fazla ilgili önemli noktalar vardır. Yerel yayımlama seçeneğini kullanmak için Windows Vista bilgisayarda yönetici olması gerekir. Ayrıca, her zaman varsayılan konumu: *yayımlama\\*  IIS yüklü olup olmadığından bağımsız olarak dizin.

## <a name="what-is-the-default-installation-path-on-end-user-computers"></a>Son kullanıcı bilgisayarlarında varsayılan yükleme yolu nedir?
 Yükleme yolu isteğe bağlıdır. İsterseniz, yükleme yolu daha sonra ayarlayabilirsiniz. Ayrıntılar için bkz [nasıl yapılır: Office çözümünü yükleme yolunu değiştirmek](https://msdn.microsoft.com/d0eaa07b-2d72-4902-899f-2f9fb165b8fd).

 Yükleme yolu, son kullanıcının özelleştirme yükleyecek dizindir. Ayrıca çözüm güncelleştirmeleri denetlemek için kullanacağı yoludur. **Yayımlama Sihirbazı** çözüm yolu, girdiğiniz aynı olmadığı sürece bu konuma dağıtmaz **bu uygulamayı yayımlamak için konumu belirtin** önceki sayfada kutusu.

 **Bir Web sitesinden** , son kullanıcıların çözümü yüklemek için izleyeceği URL'sini belirtin.

 **Bir UNC yolu veya dosya paylaşımından** , son kullanıcıların çözümü yüklemek için izleyeceği UNC yolunu belirtin.

 **Bir CD-ROM veya DVD-ROM** bu seçenek, bir yükleme yolu gerektirmez.

 Visual Studio, CD veya DVD yazma değil. Çıktı bir CD veya DVD elle kopyalamanız gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [ClickOnce kullanarak Office çözümü dağıtma](../vsto/deploying-an-office-solution-by-using-clickonce.md)
- [Yayımlama Sayfası, Proje Tasarımcısı &#40;Visual Studio'da Office geliştirme&#41;](../vsto/publish-page-project-designer-office-development-in-visual-studio.md)
- [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)
