---
title: Dil Hizmetleri ve çekirdek Düzenleyicisi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - language services
ms.assetid: e03199a6-ad5f-4075-bfba-8d36865112b7
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 1e708ffe796bfc9342bc20c3e7f20d5cf0d05058
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68180299"
---
# <a name="language-services-and-the-core-editor"></a>Dil Hizmetleri ve Temel Düzenleyici
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio düzenleyicilerinde sık dil hizmeti ile ilişkilendirilmiştir. Diğerlerinin yanı sıra bir dil hizmeti söz dizimi renklendirme, deyim tamamlama, IntelliSense ve metin biçimlendirme sağlar.  
  
## <a name="core-editors-and-document-data-objects"></a>Çekirdek düzenleyici ve belge veri nesneleri  
 Çekirdek Düzenleyici eriştiğinizde, belge verileri ve belge görünümü nesneleri oluşturma. IDE oluşturur ve bu iki nesne denetler ve Üreteç uygulaması Düzenleyicisi'nde uygun çağrıları yaparak bunları tanıtıcıları alırsınız.  
  
 Daha fazla bilgi için [hangi Düzenleyicisi belirleme, bir projede bir dosya açılır](../extensibility/internals/determining-which-editor-opens-a-file-in-a-project.md).  
  
## <a name="language-services-and-the-core-editor"></a>Dil Hizmetleri ve Temel Düzenleyici  
 Dil hizmeti kullanarak, belge görünümü'nde verilerin nasıl görüntüleneceğini denetleyebilirsiniz. Dil hizmeti bilgileri ve Visual C++ gibi belirli bir dile özgü davranış sağlar. Bir metin arabelleği açmakta olduğunuz belgenin dosya adı uzantısı belirlemek, bir kayıt defteri anahtarından HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Editors bu dosya adı uzantısıyla ilişkili dil hizmeti metin arabelleğini belirler. \\{YourLanguageService GUID} \Extensions. Yordam sonra yükleme standart VSPackage'ı, VSPackage'ı yükler ve, dil hizmetinin bir örneği oluşturulur.  
  
 Temel dil hizmeti aşağıdaki çizimde gösterilmektedir.  
  
 ![Dil hizmetinin Modeli grafiği](../extensibility/media/vslanguageservicemodel.gif "vsLanguageServiceModel")  
Çekirdek düzenleyici ve dil hizmeti nesneleri  
  
 İçin çekirdek Düzenleyici belge veri nesnesi bir metin arabelleği olarak adlandırılır ve tarafından temsil edilen <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> nesne. Belge görünüm nesnesi bir metin görünümü olarak adlandırılır ve tarafından temsil edilen <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow> nesne. Bu iki nesne, çekirdek Düzenleyici birleşik bir görünümünü sağlamak için dil hizmeti ile birlikte çalışır. Metin arabelleği ve belge penceresinde metin görünümünü görüntüler bilgilerinden bir kod penceresinde çağrılır. Kod penceresi belgenin bir kod penceresinde Yöneticisi tarafından yönetilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager>   
 <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow>   
 [Eski API'yi kullanarak bir dil hizmetinin bağlamına sağlama](../extensibility/providing-a-language-service-context-by-using-the-legacy-api.md)   
 [IntelliSense barındırma](../extensibility/intellisense-hosting.md)   
 [Kapsanan dilleri](../extensibility/contained-languages.md)   
 [Eski Dil Hizmeti Geliştirme](../extensibility/internals/developing-a-legacy-language-service.md)
