---
title: Yazı tipi ve metin renklendirmesi için renk bilgisi alma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- text, coloring
- font and color control [Visual Studio SDK], coloring
ms.assetid: d1f985bd-743e-40b7-9458-d9af53647c91
caps.latest.revision: 23
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 8724c31accb26e478c2726dfe791256994fc95ca
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65696853"
---
# <a name="getting-font-and-color-information-for-text-colorization"></a>Yazı tipi ve metin renklendirmesi için renk bilgilerini alma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

İşler veya kullanıcı arabirimi (UI) öğeleri renklendirildi metni görüntüler işlem, proje, teknoloji ve geliştirici tercihleri türüne bağlıdır. **Yazı tipleri ve renkler** özellik sayfası ayarları depolar.  
  
 Renklendirilmiş metnini uygulamalarının çoğu gereksinim `T:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults` ve arabirimleri sunma, almaya ve metin depolama ayarlarını görüntülemek için ilişkili.  
  
> [!NOTE]
> Çekirdek Düzenleyici özelleştirirken (destekleyen **metin EditorCategory**), renklendirme teknoloji dil hizmeti kullanmanız önemle tavsiye edilir. Daha fazla bilgi için [yazı tipi ve renk genel bakış](../extensibility/font-and-color-overview.md).  
  
## <a name="getting-default-font-and-color-information"></a>Varsayılan yazı tipi ve renk bilgilerini alma  
 Tüm **yazı tipleri ve renkler** metin görüntüleme herhangi bir pencerenin ayarları belirtilmelidir **görünen öğeler** birinin **kategori**. Daha fazla bilgi için [yazı tipleri ve renkler, ortam, Seçenekler iletişim kutusu](../ide/reference/fonts-and-colors-environment-options-dialog-box.md).  
  
 VSPackage renklendirmeye geçerli edinmeniz gerekir **yazı tipleri ve renkler** ayarları. VSPackage, kendi ihtiyaçlarına bağlı olarak aşağıdaki yollarla bu görevleri gerçekleştirebilirsiniz:  
  
- Yazı tipi ve renk Kalıcılık mekanizması depolanmış veya geçerli durumunu almak için kullanın. Daha fazla bilgi için [erişme depolanan yazı tipi ve renk ayarlarını](../extensibility/accessing-stored-font-and-color-settings.md).  
  
- Kullanım <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider> örneğini almak için yazı tipi ve renk verileri sağlayan bir hizmet arabiriminin <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults>, VSPackage'ı da yazı tipini ve rengini sağlayıcısı değil.  
  
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorEvents> arabirimini gerçekleştirin.  
  
  Emin olmak için yoklama işlemi tarafından elde edilen sonucu güncel olan, kullanılacak yararlı olabilir <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorCacheManager> alma yöntemleri çağrılmadan önce bir güncelleştirme gerekip gerekmediğini belirlemek için arabirimi <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorStorage> arabirimi.  
  
  Sonra yazı tipi ve renk bilgilerini aldıysanız, renklendirme gerektiren öğeleri tanımlamak için görüntülenecek metni ayrıştırılamadı ve ardından metni uygun yazı tipleri ve renkler kullanarak pencereyi görüntülemek.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaultsProvider>   
 <xref:Microsoft.VisualStudio.Shell.Interop.IVsFontAndColorDefaults>   
 [Yazı tipleri ve metin kullanma](https://msdn.microsoft.com/library/d43640f3-da94-4df2-a29d-a9d021a1c069)   
 [Renklerle çalışma](https://msdn.microsoft.com/library/d34ff96f-241d-494f-abdd-13811ada8cd3)   
 [GDI (grafik cihaz arabirimi)](https://msdn.microsoft.com/7e1d4540-bb2e-4257-8eee-eee376acba83)
