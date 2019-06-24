---
title: Dil Hizmetleri ve çekirdek Düzenleyicisi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- editors [Visual Studio SDK], legacy - language services
ms.assetid: e03199a6-ad5f-4075-bfba-8d36865112b7
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a27fc9ec55b301dc3355e03e2e86e968752fbbd0
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309529"
---
# <a name="language-services-and-the-core-editor"></a>Dil Hizmetleri ve çekirdek Düzenleyicisi
Visual Studio düzenleyicilerinde sık dil hizmeti ile ilişkilendirilmiştir. Diğerlerinin yanı sıra bir dil hizmeti söz dizimi renklendirme, deyim tamamlama, IntelliSense ve metin biçimlendirme sağlar.

## <a name="core-editors-and-document-data-objects"></a>Çekirdek düzenleyici ve belge veri nesneleri
 Çekirdek Düzenleyici eriştiğinizde, belge verileri ve belge görünümü nesneleri oluşturma. IDE oluşturur ve bu iki nesne denetler ve Üreteç uygulaması Düzenleyicisi'nde uygun çağrıları yaparak bunları tanıtıcıları alırsınız.

 Daha fazla bilgi için [belirlemek hangi Düzenleyicisi, bir projede bir dosya açar](../extensibility/internals/determining-which-editor-opens-a-file-in-a-project.md).

## <a name="language-services-and-the-core-editor"></a>Dil Hizmetleri ve çekirdek Düzenleyicisi
 Dil hizmeti kullanarak, belge görünümü'nde verilerin nasıl görüntüleneceğini denetleyebilirsiniz. Dil hizmeti bilgileri ve Visual C++ gibi belirli bir dile özgü davranış sağlar. Bir metin arabelleği açmakta belgenin dosya adı uzantısı belirlemek, bir kayıt defteri anahtarından bu dosya adı uzantısıyla ilişkili dil hizmeti metin arabelleğini belirler **HKEY_LOCAL_MACHINE\SOFTWARE\ Microsoft\Editors\\{YourLanguageService GUID} \Extensions**. Yordam sonra yükleme standart VSPackage'ı, VSPackage'ı yükler ve, dil hizmetinin bir örneği oluşturulur.

 Temel dil hizmeti aşağıdaki çizimde gösterilmektedir.

 ![Dil hizmetinin Modeli grafiği](../extensibility/media/vslanguageservicemodel.gif "vsLanguageServiceModel") çekirdek düzenleyici ve dil hizmeti nesneleri

 İçin çekirdek Düzenleyici belge veri nesnesi bir metin arabelleği olarak adlandırılır ve tarafından temsil edilen <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextBuffer> nesne. Belge görünüm nesnesi bir metin görünümü olarak adlandırılır ve tarafından temsil edilen <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow> nesne. Bu iki nesne, çekirdek Düzenleyici birleşik bir görünümünü sağlamak için dil hizmeti ile birlikte çalışır. Metin arabelleği ve belge penceresinde metin görünümünü görüntüler bilgilerinden bir kod penceresinde çağrılır. Kod penceresi belgenin bir kod penceresinde Yöneticisi tarafından yönetilir.

## <a name="see-also"></a>Ayrıca bkz.
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsLanguageInfo>
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsColorizer>
- <xref:Microsoft.VisualStudio.TextManager.Interop.VsTextView>
- <xref:Microsoft.VisualStudio.TextManager.Interop.IVsCodeWindowManager>
- <xref:Microsoft.VisualStudio.TextManager.Interop.VsCodeWindow>
- [Eski API'yi kullanarak bir dil Hizmet bağlamı sağlar.](../extensibility/providing-a-language-service-context-by-using-the-legacy-api.md)
- [IntelliSense barındırma](../extensibility/intellisense-hosting.md)
- [Kapsanan dilleri](../extensibility/contained-languages.md)
- [Eski dil hizmeti geliştirme](../extensibility/internals/developing-a-legacy-language-service.md)