---
title: Seçenekler iletişim kutusu, projeler ve çözümler, derleme ve çalıştırma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Projects.Build_and_Run
- VS.ToolsOptionsPag.Projects.Build_and_Run
helpviewer_keywords:
- builds [Visual Studio], setting up
- run actions
- debugger, run options
ms.assetid: c884976e-c0df-4c6d-8e3a-856ea2bd547c
caps.latest.revision: 24
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 0aa325aa016b95a0dac0047f4b6fe9ae67f52ecc
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54800868"
---
# <a name="options-dialog-box--projects-and-solutions-build-and-run"></a>Seçenekler iletişim kutusu, projeler ve çözümler, derleme ve çalıştırma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

  
Bu iletişim kutusunda, aynı anda oluşturabilirsiniz Visual C++ ya da Visual C# projeleri sayısı belirtebilirsiniz, bazı varsayılan davranışlar oluşturun ve bazı günlük ayarlarını oluşturun. Açmak için **seçenekleri** iletişim kutusunda **Araçları**, **seçenekleri** menü çubuğundaki. Bu seçenek kümesi erişmek için genişletme **projeler ve çözümler**ve ardından **derleme ve çalıştırma**.  
  
## <a name="uielement-list"></a>UIElement Listesi  
 **derleme en fazla paralel proje sayısı**  
 Aynı anda oluşturabilirsiniz Visual C++ ve Visual C# projeleri maksimum sayısını belirtir. Derleme işlemi iyileştirmek için en fazla paralel proje yapılandırma sayısını bilgisayarınızın CPU sayısını otomatik olarak ayarlanır. En fazla 32'dir.  
  
 **Başlangıç projelerini ve bağımlılıkları sadece çalıştırıldığında Derle**  
 F5 tuşuna basın, bu onay kutusu seçili değilse, yalnızca başlangıç projesi ve bağımlılıklarını yerleşiktir; seçin **hata ayıklama**, **Başlat** menüsünde seçin ya da çubuk; **derleme**, **derleme** menü çubuğunda. F5 tuşuna basın, bu onay kutusu işaretli değilse, tüm projeler, bağımlılıklar ve çözüm dosyaları yerleşiktir; seçin **hata ayıklama**, **Başlat** menüsünde seçin ya da çubuk; **derleme**, **derleme** menü çubuğunda. Varsayılan olarak, bu seçenek işaretli değildir.  
  
 **Çalıştırmada, projelerin güncel olduğunda**  
 > [!NOTE]
>  Bu liste uygulandığı [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)] yalnızca projeleri.  
  
 Bir proje yapılandırması F5 tuşuna basın veya seçin, güncel değil ise, varsayılan olarak, bir ileti görünür **hata ayıklama**, **Başlat** menü çubuğundaki. Projeyi yine de oluşturmak ve iletinin görüntülenip belirtebilirsiniz. İletinin görüntülenip görüntülenmeyeceğini belirtir ve yapı davranışını ileti görünmüyorsa ne olması gerektiğini belirtmek için bu seçeneği kullanın.  
  
 **Her zaman Derle**  
 İleti kutusu görünmez ve projenin güncel yapılandırmanın rağmen oluşturulmuştur. Bu seçeneği seçtiğinizde ayarlanır **bu iletişim kutusunu bir daha gösterme** iletisinde kutusuna ve ardından **Evet** düğmesi.  
  
 **Asla derleme**  
 İleti kutusu görünmez ve proje oluşturulan değil. Bu seçeneği seçtiğinizde ayarlanır **bu iletişim kutusunu bir daha gösterme** iletisinde kutusuna ve ardından **Hayır** düğmesi.  
  
 **Derlerken uyar**  
 Bir proje yapılandırması güncel değil her zaman ileti kutusu görüntüler.  
  
 **Alıştırmada, ne zaman derleme veya dağıtım hataları oluşuyor**  
 Derlemeden başlattığınızda yapı hataları oluşursa **derleme** menüsünde, bir ileti görüntülenir. Uygulama ve her zaman, yapı hataları iletinin görüntülenip ortaya başlatarak devam edilip edilmeyeceğini belirtebilirsiniz. İletinin görüntülenip görüntülenmeyeceğini belirtir ve ileti görünmüyorsa davranışı neler olması gerektiğini belirtmek için bu seçeneği kullanın.  
  
> [!NOTE]
>  Bu seçenek uygulanır [!INCLUDE[vcprvc](../../includes/vcprvc-md.md)] yalnızca projeleri.  
  
 **Başlatırken uyar**  
 Her bir ileti kutusunda görüntüler, derleme hataları oluşur.  
  
 **Başlatma**  
 İleti kutusu görünmez ve uygulama çalışmaya değil. Bu seçeneği seçtiğinizde ayarlanır **bu iletişim kutusunu bir daha gösterme** ileti kutusunda onay kutusunu işaretleyin ve ardından **Hayır** düğmesi.  
  
 **Eski sürümü Başlat**  
 İleti kutusu görünmez ve yeni oluşturulmuş bir uygulama sürümüne çalışmaya değil. Bu seçeneği seçtiğinizde ayarlanır **bu iletişim kutusunu bir daha gösterme** ileti kutusunda onay kutusunu işaretleyin ve ardından **Evet** düğmesi.  
  
 **Yeni çözümleri şu anda seçili projeyi başlangıç projesi olarak kullanın.**  
 Bu onay kutusu seçili değilse, yeni çözümleri şu anda seçili projeyi başlangıç projesi olarak kullanın.  
  
 **MSBuild proje oluşturması çıkış ayrıntısı**  
 Ne kadar bilgi görünür belirler **çıkış** derleme için penceresi.  
  
 **MSBuild proje derleme günlük dosyası ayrıntısı**  
 > [!NOTE]
>  Bu seçenek yalnızca Visual C++ projeleri için geçerlidir.  
  
 Şu konumdadır derleme günlüğü dosyası için ne kadar bilgi yazılacağını belirler \\... \\ *ProjectName*\Debug\\*ProjectName*. günlük.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Derleme ve Oluşturma](../../ide/compiling-and-building-in-visual-studio.md)
